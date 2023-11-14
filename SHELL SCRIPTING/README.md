# SHELL SCRIPTING 

# Shebang:

     Create a new file in your Linux system using the terminal: nano myscript.sh
  
      Add the shebang line: #!/bin/bash as the first line in the script.
    
        Save the file and exit.

# Comments:

    Within myscript.sh, you can add a comment to describe the script's purpose:

    # This script greets the user
echo "Hello, User!"

# Variables:

    You can create and use variables in your script like this:

    # Variable assignment
         my_var="Shell Scripting is fun!"

   Printing the variable's value -   echo $my_var
   
# Input and Output:

    Accepting user input and displaying output are crucial. You can use read to get input and echo to print output.

    #!/bin/bash

 Taking user input
   echo "Enter your name:"
  read user_name

    Displaying personalized greeting
    echo "Hello, $user_name! Welcome to the shell scripting world."

# Conditional Statements:

    Use if, else, and elif to make decisions in your script based on conditions.

    #!/bin/bash

        Checking if a number is even or odd
         echo "Enter a number:"
           read num
        if [ $((num % 2)) -eq 0 ]; then
          echo "$num is even."
       else
         echo "$num is odd."
      fi

# Loops:

    Loops, such as for and while, help in iterating through lists of items or until a condition is met

      #!/bin/bash

       Printing numbers from 1 to 5 using a for loop
           echo "Numbers from 1 to 5:"
            for i in {1..5}; do
               echo $i
           done

# Functions:

    Functions allow you to group code into reusable blocks.

      #!/bin/bash

       Function to calculate the square of a number
         calculate_square() {
           local num=$1
           echo $((num * num))
           }

   Using the function
     echo "Enter a number:"
         read input_num

      result=$(calculate_square $input_num)
      echo "The square of $input_num is: $result"



