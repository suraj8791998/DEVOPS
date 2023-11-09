
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
      
**7.Grant Sudo Privileges:**
   
   Adds a user to the sudo group, granting administrative privileges.
   
        usermod -aG sudo username
**8.View User Information:**
   
   Displays information about a user, including user and group IDs.
   
        id username
**9.Change User's Home Directory:**

   Moves a user's home directory.

        usermod -d /path/to/new/directory username
**10.Lock/Unlock User Account:**

   Locks a user account.

        passwd -l username  
   
   Unlocks a previously locked user account.
   
        passwd -u username
**11.Force User to Change Password:**

   Forces a user to change their password on next login.

        chage -d 0 username

**12.Set Password Expiry:**

   Sets the maximum number of days between password changes.
   
        chage -M days username
        
**13.Delete User and Home Directory:**

Removes a user along with their home directory.

        userdel -r username

