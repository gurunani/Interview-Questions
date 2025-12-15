````md
# Linux Interview Questions, Answers, Commands, and Explanations

Based on the video provided, here are the Linux interview questions, answers, commands, and explanations exactly as they appear in the presentation.

---

### 1. Q: How do you list hidden files in a directory?
**A:**
```bash
ls -la
````

---

### 2. Q: How do you check the size of a folder in Linux?

**A:**

```bash
du -sh <folder-path>
```

---

### 3. Q: How do you check if a port is open?

**A:**

```bash
netstat -intp
```

---

### 4. Q: Write a script to find files accessed in the last 30 days

**A:**

```bash
find /path -atime -30 -type f
```

---

### 5. Q: How do you check running logs?

**A:** By following the logs

```bash
tail -f /path/to/log
```

---

### 6. Q: How to check memory usage on a Linux server?

**A:** We can use multiple commands to check the RAM usage.

**Command 1:**

```bash
free -h
```

This command displays the total RAM, cached RAM, used, free RAM, etc.

**Command 2:**

```bash
top
```

`top` displays the dynamic memory usage by different system processes.

**Command 3 (Human Readable):**
If we can install the `htop` command, we can see memory usage in a human-readable format.

```bash
dnf install htop -y
htop
```

**Command 4:**
We can check memory info

```bash
cat /proc/meminfo
```

---

### 7. Q: How do you list the top 10 processes based on memory usage?

**A:**

```bash
ps aux --sort=-%mem | head -n 10
```

---

### 8. Q: What is Swap memory in Linux?

**A:** Swap memory is extra space on your computer’s hard drive or SSD that works like backup RAM. When physical RAM is full, the system moves less-used data to swap so the system doesn’t crash.

---

### 9. Q: How do you check the IP address of a Linux server?

**A:** By using the `ifconfig` command

```bash
ifconfig
```

---

### 10. Q: What is the purpose of the `chmod` command in Linux?

**A:** The `chmod` command is used to change file or directory permissions. We can set RWX permissions for the owner, group, and others.

---

### 11. Q: What do you do when disk space is full on the server?

**A:**
Check disk space usage:

```bash
df -ht
```

Check disk utilization:

```bash
du -sh *
```

Find top files occupying disk space:

```bash
du -ah / | sort -rh | head -n 20
```

**Steps to resolve:**

* Remove unnecessary files
* Remove files in the `/tmp` directory
* Move files to another disk if available:

```bash
mv /path/to/large/file /mnt/otherdisk/
```

* Add extra disk space

---

### 12. Q: How to troubleshoot high memory usage?

**A:**
Check memory usage:

```bash
htop
free -h
```

Check top memory-consuming processes:

```bash
ps aux --sort=-%mem | head -n 10
```

**Steps to resolve:**
Restart services that are not releasing memory, optimize applications, increase RAM if required, and monitor memory usage.

---

### 13. Q: What is the difference between a hard link and a soft link in Linux?

**A:**
A hard link points to the same inode as the original file.
A soft (symbolic) link points to the file name/path.
Hard links share data, while soft links act as shortcuts.

---

### 14. Q: Describe a scenario when you get a “filesystem is full” error but `df` shows free space.

**A:**
This happens when inodes are full. Each file consumes one inode, and once all inodes are used, no new files can be created.

**Example script causing this:**

```bash
for i in {1..1000000}; do touch file_$i; done
```

**Check inode usage:**

```bash
df -i
```

**Steps to resolve:**

* Delete unnecessary small files
* Compress files not frequently required

---

### 15. Q: Find all files accessed within the last 30 days

```bash
find /path/to/search -type f -atime -30
```

---

### 16. Q: How to reboot the server when the reboot command is not responding?

**A:** Use the shutdown/init command

```bash
sudo init 6
```

---

### 17. Q: How do you check CPU usage on a Linux server?

**A:**

```bash
top
mpstat
```

---

### 18. Q: How do you find the process ID (PID) of a running service?

**A:**

```bash
ps -ef | grep <process-name>
pidof <process-name>
```

---

### 19. Q: How do you kill a process in Linux?

**A:**

```bash
kill <PID>
kill -9 <PID>
```

---

### 20. Q: How do you check disk I/O performance?

**A:**

```bash
iostat
iotop
```

---

### 21. Q: How do you find large files on a system?

**A:**

```bash
find / -type f -size +1G
```

---

### 22. Q: How do you check open ports and listening services?

**A:**

```bash
ss -tulnp
netstat -tulnp
```

---

### 23. Q: What is the difference between `grep`, `egrep`, and `fgrep`?

**A:**

* `grep` → basic pattern matching
* `egrep` → extended regular expressions
* `fgrep` → fixed-string search (no regex)

---

### 24. Q: How do you schedule a task in Linux?

**A:** By using cron jobs

```bash
crontab -e
```

---

### 25. Q: How do you check cron job logs?

**A:**

```bash
cat /var/log/cron
cat /var/log/syslog | grep CRON
```

---

### 26. Q: How do you change ownership of a file or directory?

**A:**

```bash
chown user:group file_name
```

---

### 27. Q: What is the difference between `systemctl` and `service` commands?

**A:**
`systemctl` is used in systemd-based systems, while `service` is a legacy SysVinit command.

---

### 28. Q: How do you check OS version in Linux?

**A:**

```bash
cat /etc/os-release
uname -a
```

---

### 29. Q: How do you monitor logs in real time?

**A:**

```bash
tail -f /var/log/messages
journalctl -f
```

---

### 30. Q: How do you find which user is logged into the system?

**A:**

```bash
who
w
```

```
```
