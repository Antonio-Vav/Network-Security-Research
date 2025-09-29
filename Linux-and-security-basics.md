# Crucial Commands in Linux

---
# User Tasks

## 1. Switch to root
![Prompt after switching to root](images/images/root.png)

---

## 2. Create users bobby and sally
![User creation outputs](images/images/sallyBob.png)
useradd = It just creates the user account with minimal defaults. It doesn't set up a password, home directory, or shell  
adduser = it asks for details like password, full name, and sets up the home directory automatically

---

## 3. Switch to sally
![Prompt after switching to sally](images/images/suSally.png)

---

## 4. Try creating a user as sally
![Permission denied when sally creates a user](images/images/sallyNo.png)
This is because sally does not have root access and is not root user

---

## 5. Create then Delete user earl
![Creating user earl](images/images/sudoEarl.png)
![Deleting user earl](images/images/byEarl.png)

---

## 6. Change sally’s password
![Changing password for sally](images/images/passwd_sally.png)

---

## 7. Why not stay logged in as root?
![Explanation about root practice](images/images/root_bad_practice.png)

---

## 8. Show user ID
![Showing user ID](images/images/user_id.png)

---

# Group Tasks

## 9. Groups ubuntu belongs to
![Groups ubuntu belongs to](images/images/ubuntu_groups.png)

---

## 10. Give sally sudo access
![Sally with sudo creating new user](images/images/sally_sudo_useradd.png)

---

## 11. Create cybersec group
![Creating cybersec group](images/images/create_cybersec.png)

---

## 12. Add sally to cybersec
![Adding sally to cybersec group](images/images/add_sally_cybersec.png)

---

## 13. Check sally’s groups
![Checking sally’s groups](images/images/sally_groups.png)

---

# Permissions and ACL Tasks

## 14. Create lab1 directory
![lab1 directory permissions](images/images/lab1_permissions.png)

---

## 15. Create helloWorld script
![helloWorld bash script created](images/images/helloWorld_script.png)

---

## 16. Check and modify helloWorld permissions
![helloWorld permissions updated](images/images/helloWorld_permissions.png)

---

## 17. View ACL of helloWorld
![Viewing ACL of helloWorld](images/images/helloWorld_acl.png)

---

## 18. Give sally read & write access
![Setting ACL for sally on helloWorld](images/images/sally_acl.png)


