Directories. 
1. / (root) - This is the top directory of linux filesystem. 
    All the directories are in the root directory.
    cd / - this is the command to goto root directory.

2. /home - this directory contains personal directories of all the users.
3. /root - this is the home directory for thr root user.
4. /etc - this directory conatins system configuration files.
5. /var/log - this directory contains log files genetrated by system and services.
6. /tmp - It contains temporary files created by applications.
7. /bin - It contains essential system commands required for operations.
8. /usr/bin - this directory contains user level commands and installed applications.
9. /opt - It is used for third party software installations.



ubuntu@ip-172-31-12-61:~$ du -sh /var/log/* 2>/dev/null | sort -h | tail -5
188K	/var/log/kern.log.1
216K	/var/log/sysstat
568K	/var/log/cloud-init.log
616K	/var/log/syslog.1
66M	/var/log/journal


ubuntu@ip-172-31-12-61:~$ cat /etc/hostname
ip-172-31-12-61


ubuntu@ip-172-31-12-61:~$ ls -la
total 64
drwxr-x---  6 ubuntu ubuntu  4096 Feb  8 07:03 .
drwxr-xr-x 13 root   root    4096 Feb  8 05:05 ..
-rw-------  1 ubuntu ubuntu  6650 Feb  8 07:08 .bash_history
-rw-r--r--  1 ubuntu ubuntu   220 Mar 31  2024 .bash_logout
-rw-r--r--  1 ubuntu ubuntu  3771 Mar 31  2024 .bashrc
drwx------  2 ubuntu ubuntu  4096 Jan 31 04:48 .cache
drwx------  3 ubuntu ubuntu  4096 Feb  8 06:12 .config
-rw-------  1 ubuntu ubuntu    20 Feb  8 06:11 .lesshst
-rw-------  1 ubuntu ubuntu    24 Feb  7 05:37 .lvm_history
-rw-r--r--  1 ubuntu ubuntu   807 Mar 31  2024 .profile
drwx------  2 ubuntu ubuntu  4096 Jan 31 04:47 .ssh
-rw-r--r--  1 ubuntu ubuntu     0 Jan 31 04:52 .sudo_as_admin_successful
-rw-------  1 ubuntu docker 11297 Feb  8 07:03 .viminfo
drwxrwxr-x  5 ubuntu docker  4096 Feb  8 07:03 devops






    
