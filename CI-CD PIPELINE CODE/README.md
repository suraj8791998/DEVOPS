
# CI-CD-PIPELINE-CODE
THIS IS ONLY FOR CODE TO STORE THE INFORMATION

pipeline {
    
    agent any 
    
    stages {
        
        stage ('checkout') {
            
            steps {
                
                git branch: 'main', url: 'https://github.com/Hemasuraj/fuck.git'
                
            }
        }
        
        stage ('build') {
            
            steps {
                
                sh 'mvn compile'
            }
        }
        
        stage('Static Code Analysis') {
          environment {
           SONAR_URL = "http://100.26.212.49:9000"
            }
           steps {
             withCredentials([string(credentialsId: 'sonarqube', variable: 'SONAR_AUTH_TOKEN')]) {
               sh 'mvn sonar:sonar -Dsonar.login=$SONAR_AUTH_TOKEN -Dsonar.host.url=${SONAR_URL}'
        }
      }

    }
    stage ('test') {
        
        steps {
            
            sh 'mvn test'
        }
    }
    
    stage ('integration test') {
        
        steps {
            
            sh 'mvn integration-test'
        }
    }
    stage ('artifact packing') {
        
        steps {
            
            script {
               def imageName = "myapp:${BUILD_NUMBER}"
                 sh "docker build -t ${imageName} ."
            }
        }
    }
    stage('Deployment to Staging Environment') {
      steps {
        sh 'ansible-playbook deploy-staging.yml'  
        }
   }
      stage('Notification and Reporting') {
    steps {
        script {
            emailext body: 'The CI/CD pipeline has completed successfully.',
                subject: 'CI/CD Pipeline Notification',
                to: 'mulaveesalav@gmail.com',
                from: 'sender@example.com'
         }
      }
   }

 }
}
