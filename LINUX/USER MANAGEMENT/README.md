
# User Managemnt 

**1.Create User:**

   Use the useradd command to add a new user.
   
       useradd username
**2.Set Password:**
   
   Set a password for the new user with the passwd command.
       
       passwd username
**3.User Information:**

   Add additional user information with the usermod command.
       
       usermod -c "Full Name" username
**4.Assign Groups:**
   
   Add the user to specific groups using usermod.
      
      usermod -aG groupname username
**5.Delete User:**
   
   To remove a user, use the userdel command.
      
      userdel username
**6.Modify User Properties:**

   Adjust user properties with the usermod command.
      
      usermod -options username
  Remember to replace "username" and "groupname" with actual values.
