````md
# User Management (Linux)

This section covers **user and group management** in Linux. All commands are shown in a clean, consistent Markdown format with proper code blocks.

---

## Introduction to User Management in Linux

Linux is a multi-user operating system, meaning multiple users can operate on a system simultaneously. Proper user management ensures security, controlled access, and system integrity.

### Key files involved in user management

- `/etc/passwd` – Stores user account details  
- `/etc/shadow` – Stores encrypted user passwords  
- `/etc/group` – Stores group information  
- `/etc/gshadow` – Stores secure group details  

---

## Creating Users

### Create a user (basic)

```bash
useradd username
```

> Creates a user **without** a home directory (depends on distro defaults).

---

### Create a user with a home directory

```bash
useradd -m username
```

> `-m` ensures `/home/username` is created.

---

### Specify a default shell

```bash
useradd -s /bin/bash username
```

> Sets the login shell explicitly.

---

## adduser Command (Debian-Based Systems)

```bash
adduser username
```

This is an **interactive** command that:

- Creates a home directory  
- Prompts for a password  
- Asks for optional user details  

> `adduser` is a higher-level wrapper around `useradd`.

---

## Managing User Passwords

### Set or change a user’s password

```bash
passwd username
```

---

### Enforcing Password Policies

#### Set password expiration (for example, 90 days)

```bash
chage -M 90 username
```

---

### Lock a user account

```bash
passwd -l username
```

---

### Unlock a user account

```bash
passwd -u username
```

---

## Modifying Users

Modify existing users using `usermod`.

---

### Change the username

```bash
usermod -l new_username old_username
```

---

### Change the home directory and move files

```bash
usermod -d /new/home/directory -m username
```

> `-m` moves existing files to the new home directory.

---

### Change the default shell

```bash
usermod -s /bin/zsh username
```

---

## Deleting Users

### Delete a user without removing the home directory

```bash
userdel username
```

---

### Delete a user along with the home directory

```bash
userdel -r username
```

---

## Working with Groups

### Create a group

```bash
groupadd groupname
```

---

### Add a user to a group

```bash
usermod -aG groupname username
```

> `-a` = append, `-G` = supplementary group.

---

### View group membership

```bash
groups username
```

---

### Change the primary group

```bash
usermod -g new_primary_group username
```

---

## Sudo Access and Privilege Escalation

### Adding a user to the sudo group

#### Debian-based systems

```bash
usermod -aG sudo username
```

#### RHEL-based systems

```bash
usermod -aG wheel username
```

---

### Granting specific commands with sudo

Edit the sudoers file safely:

```bash
visudo
```

Add the following line:

```bash
username ALL=(ALL) NOPASSWD: /path/to/command
```

---
