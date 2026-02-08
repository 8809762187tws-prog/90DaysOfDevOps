Service: nginx

1. Command to print system info -> uname -a
   
   Result ->Linux ip-172-31-12-61 6.14.0-1018-aws #18~24.04.1-Ubuntu SMP Mon Nov 24 19:46:27 
   UTC 2025 x86_64 x86_64 x86_64 GNU/Linux

2. Command to print distribution-specific information.
   Command -> lsb_release -a
   Result -> No LSB modules are available.
                Distributor ID:	Ubuntu
                Description:	Ubuntu 24.04.3 LTS
                Release:	24.04
                Codename:	noble

3. Command to make a directory.
   Command -> mkdir dir_name
   mkdir commands
    ubuntu@ip-172-31-12-61:~/devops$ ls -l
    total 16
    drwxrwxr-x 2 ubuntu ubuntu 4096 Feb  8 01:41 commands
    -rw-rw-r-- 1 ubuntu docker   60 Jan 31 05:51 file1.txt
    -rw-rw-r-- 1 ubuntu ubuntu    0 Jan 31 05:53 file2.txt
    -r-------- 1 ubuntu ubuntu   19 Jan 31 05:59 file3.txt
    drwxr-xr-x 2 root   root   4096 Feb  7 06:35 shell_scripting
    ubuntu@ip-172-31-12-61:~/devops$ ls
    commands  file1.txt  file2.txt  file3.txt  shell_scripting

4. Command to see disk info.
   Command -> df -h
   Result -> Filesystem       Size  Used Avail Use% Mounted on
            /dev/root         19G  2.5G   16G  14% /
            tmpfs            458M     0  458M   0% /dev/shm
            tmpfs            183M  896K  182M   1% /run
            tmpfs            5.0M     0  5.0M   0% /run/lock
            efivarfs         128K  3.8K  120K   4% /sys/firmware/efi/efivars
            /dev/nvme0n1p16  881M   89M  730M  11% /boot
            /dev/nvme0n1p15  105M  6.2M   99M   6% /boot/efi
            tmpfs             92M   12K   92M   1% /run/user/1000

5. Command to check process level cpu & memory
   Command -> ps -C nginx -o pid,pcpu,pmem,comm
   Result -> PID %CPU %MEM COMMAND
             611  0.0  0.2 nginx
             618  0.0  0.4 nginx
             619  0.0  0.5 nginx

6. Command to check system memory.
   Command -> free 
   result ->               total        used        free      shared  buff/cache   available
            Mem:          936152      390824      129900        2788      579360      545328
            Swap:              0           0           0

7. Command to see Virtual Machine Statistics.
   Command -> vmstat 1 5
   result -> vmstat 1 5
procs -----------memory---------- ---swap-- -----io---- -system-- -------cpu-------
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st gu
 2  0      0 128192  24800 555536    0    0   174     9   93    0  0  0 100  0  0  0
 0  0      0 128192  24800 555576    0    0     0     0  284  173  0  0 100  0  0  0
 0  0      0 128192  24800 555576    0    0     0     0  303  154  0  0 100  0  0  0
 0  0      0 128192  24800 555576    0    0     0     0  224  113  0  0 100  0  0  0
 0  0      0 128192  24800 555576    0    0     0     0   70   65  0  0 100  0  0  0

8. Command to check service endpoint.
   Command -> url -I http://localhost/ping
   Result -> HTTP/1.1 404 Not Found
             Server: nginx/1.24.0 (Ubuntu)
             Date: Sun, 08 Feb 2026 01:54:45 GMT
             Content-Type: text/html
             Content-Length: 162
             Connection: keep-alive

9. Command to get system logs.
   Command -> journalctl
   Result -> -u nginx -n 50
              Jan 31 04:52:47 ip-172-31-12-61 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server.>
              Jan 31 04:52:47 ip-172-31-12-61 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
              Jan 31 04:59:29 ip-172-31-12-61 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server.>
              Jan 31 04:59:29 ip-172-31-12-61 systemd[1]: nginx.service: Deactivated successfully.
              Jan 31 04:59:29 ip-172-31-12-61 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
              Jan 31 05:00:46 ip-172-31-12-61 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server.>
              Jan 31 05:00:46 ip-172-31-12-61 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
              Jan 31 05:01:33 ip-172-31-12-61 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server.>
              Jan 31 05:01:33 ip-172-31-12-61 systemd[1]: nginx.service: Deactivated successfully.
              Jan 31 05:01:33 ip-172-31-12-61 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
              -- Boot 739aaeaa353c41b084870601e8cb6656 --
              Feb 01 03:31:17 ip-172-31-12-61 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server.>
              Feb 01 03:31:18 ip-172-31-12-61 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
              Feb 01 06:46:20 ip-172-31-12-61 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server.>
              Feb 01 06:46:20 ip-172-31-12-61 systemd[1]: nginx.service: Deactivated successfully.
              Feb 01 06:46:20 ip-172-31-12-61 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
              -- Boot d8056a8b3edb400e8945862a68d4e6e1 --
              Feb 07 03:42:39 ip-172-31-12-61 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server.>
              Feb 07 03:42:39 ip-172-31-12-61 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
              Feb 07 06:42:14 ip-172-31-12-61 systemd[1]: Stopping nginx.service - A high performance web server and a reverse proxy server.>
              Feb 07 06:42:14 ip-172-31-12-61 systemd[1]: nginx.service: Deactivated successfully.
              Feb 07 06:42:14 ip-172-31-12-61 systemd[1]: Stopped nginx.service - A high performance web server and a reverse proxy server.
              -- Boot 44f530ad6a2d4eb79a461c5aecc8803a --
              Feb 08 01:07:29 ip-172-31-12-61 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server.>
              Feb 08 01:07:29 ip-172-31-12-61 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.

10. No error logs.
