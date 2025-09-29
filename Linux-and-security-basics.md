# Crucial Commands in Linux

---

## 4. Change the current user to root
```bash
sudo su root
```
**Prompt after switching:**  
```
root@hostname:~#
```
![Prompt after switching to root](images/root_prompt.png)

---

## 5. Create new users
```bash
sudo useradd bobby
sudo adduser sally
```
**Difference:**  
- `useradd` → low-level command; adds the user but doesn’t set password or home directory by default.  
- `adduser` → interactive, higher-level utility; sets up password, home directory, shell, etc.  

![User creation outputs](images/user_creation.png)

---

## 6. Switch to user sally
```bash
su - sally
```
**Prompt looks like:**  
```
sally@hostname:~$
```
![Prompt after switching to sally](images/sally_prompt.png)

---

## 7. Try creating a user as sally
```bash
sudo useradd earl   # (fails without sudo access)
```
**Result:** Permission denied, because normal users cannot add new system users.  

![Permission denied when sally creates a user](images/sally_useradd_fail.png)

---

## 8. Exit to ubuntu and delete earl
```bash
exit
exit
sudo deluser earl
```
![Deleting user earl](images/delete_user_earl.png)

---

## 9. Change password of sally
```bash
sudo passwd sally
```
![Changing password for sally](images/passwd_sally.png)

---

## 10. Why not stay logged in as root?
It’s unsafe — mistakes (like deleting system files) can permanently damage the system. Best practice: use `sudo` only when needed.  

---

## 11. Show your user ID
```bash
id -u
```
![Showing user ID](images/user_id.png)

---

# Group Tasks

## 12. Groups ubuntu belongs to
```bash
groups ubuntu
```
![Groups ubuntu belongs to](images/ubuntu_groups.png)

---

## 13. Give sally sudo access
```bash
sudo usermod -aG sudo sally
```
Now switch to sally and try:
```bash
su - sally
sudo useradd newuser
```
![Sally with sudo creating new user](images/sally_sudo_useradd.png)

---

## 14. Create a new group
```bash
sudo groupadd cybersec
```
![Creating cybersec group](images/create_cybersec.png)

---

## 15. Add sally to cybersec
```bash
sudo usermod -aG cybersec sally
```
![Adding sally to cybersec group](images/add_sally_cybersec.png)

---

## 16. Check sally’s groups
```bash
groups sally
```
![Checking sally’s groups](images/sally_groups.png)

---

# Permissions and ACL Tasks

## 17. Create directory lab1 and check permissions
```bash
mkdir lab1
ls -ld lab1
```
![lab1 directory permissions](images/lab1_permissions.png)

---

## 18. Create helloWorld bash script
```bash
cd lab1
nano helloWorld
# Add:
# !/bin/bash
# echo "Hello World!"
chmod +x helloWorld
```
![helloWorld bash script created](images/helloWorld_script.png)

---

## 19. Check file permissions
```bash
ls -la helloWorld
```
**Modify group permissions:**
```bash
chmod g+wx helloWorld
```
![helloWorld permissions updated](images/helloWorld_permissions.png)

---

## 20. View ACL
```bash
getfacl helloWorld
```
![Viewing ACL of helloWorld](images/helloWorld_acl.png)

---

## 21. Give sally read & write access
```bash
setfacl -m u:sally:rw helloWorld
```
![Setting ACL for sally on helloWorld](images/sally_acl.png)

