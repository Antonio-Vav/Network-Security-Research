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

## 6. Change sally's password
![Changing password for sally](images/images/psswdChang.png)

---

## 7. Why not stay logged in as root?
Every command runs with full system privileges. A simple typo could destroy the whole system

---

## 8. Show user ID
![Showing user ID](images/images/id.png)

---

# Group Tasks

## 9. Give sally sudo access and use that access to create new user earl
![Sally with sudo](images/images/specialSal.png)
![Sally with sudo creating new user](images/images/earlHiAgain.png)

---

## 10. Create cybersec group, add sally to cybersec and check sally's groups
![Creating cybersec group](images/images/groupCyber+sal.png)

---

# Permissions and ACL Tasks

## 11. Create lab1 directory
![lab1 directory permissions](images/images/mkdir.png)
Owner = vavallea    
Group owner = vavallea  
The owner and group have read and write and execute perms  
Other has read and execute perms but no write

---

## 12. Create helloWorld script, make it executable and run helloWorld script
![helloWorld bash script created](images/images/nano.png)
![helloWorld bash script executed](images/images/helloWorl.png)

---

## 13. Check and modify helloWorld permissions and view ACL of helloWorld
![helloWorld permissions updated](images/images/removeAdd.png)
The permissions for this file are as follows:   
owner: read, write and execute    
group: read, write and execute    
other: read and execute

---

## 14. Give sally read & write access using setfacl then check with getfacl
![Setting ACL for sally on helloWorld](images/images/setfacl.png)


