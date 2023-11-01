# MAVEN TOOL 

# Learning Maven Basics:

# 1. Installation:

    Download and install Maven from the official Apache Maven website.

# 2. Project Structure:

    Maven follows a standard project structure, which includes source code, resources, and configuration in specific directories. A simple Maven project structure looks like this:
       my-project/
├── src/
│   ├── main/
│   │   ├── java/       # Java source code
│   │   └── resources/  # Resources like properties files
│   └── test/
│       ├── java/       # Test source code
│       └── resources/  # Test resources
├── pom.xml             # Project configuration file

# 3. POM (Project Object Model):

    Maven projects are defined by a pom.xml file, which specifies project information, dependencies, 
        and build configurations. You can create a pom.xml file manually or generate it using Maven archetypes.

# 4. Dependencies:

    Define project dependencies in the dependencies section of the pom.xml file. Maven will automatically 
         download and manage these dependencies from central repositories.

# 5. Plugins:

    Maven uses plugins to perform various build tasks. Common plugins include the maven-compiler-plugin for 
       compiling source code and the maven-surefire-plugin for running tests.

# 6. Goals:

    Maven has various build goals like clean, compile, test, package, and more. You can execute these goals using the mvn command.

# 7. Build Lifecycle:

    Maven follows a build lifecycle that includes phases like validate, compile, test, package, install, and deploy. Each phase is a sequence of goals.
