ubuntu@ip-172-31-12-61:~/devops/commands$ touch notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line1: Task started day1" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line2: Task  day2" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line3: Task  day3" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line4: Task  day4" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line5: Task  day5" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line 6: Task day 6" > notes.txt | tee -a notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line 6: Task day 6"  notes.txt | tee -a notes.txt   
Line 6: Task day 6 notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line7: Task  day7" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line8: Task  day8" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ cat notes.txt
Line 6: Task day 6
Line 6: Task day 6 notes.txt
Line7: Task  day7
Line8: Task  day8
ubuntu@ip-172-31-12-61:~/devops/commands$ ls
notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ cat notes.txt
Line 6: Task day 6
Line 6: Task day 6 notes.txt
Line7: Task  day7
Line8: Task  day8
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line1: Task started day1" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ cat notes.txt
Line 6: Task day 6
Line 6: Task day 6 notes.txt
Line7: Task  day7
Line8: Task  day8
Line1: Task started day1
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line2: Task started day1" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line3: Task started day1" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line4: Task started day1" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ echo "Line5: Task started day1" >> notes.txt
ubuntu@ip-172-31-12-61:~/devops/commands$ cat notes.txt
Line 6: Task day 6
Line 6: Task day 6 notes.txt
Line7: Task  day7
Line8: Task  day8
Line1: Task started day1
Line2: Task started day1
Line3: Task started day1
Line4: Task started day1
Line5: Task started day1
ubuntu@ip-172-31-12-61:~/devops/commands$ head -n 3 notes.txt
Line 6: Task day 6
Line 6: Task day 6 notes.txt
Line7: Task  day7
ubuntu@ip-172-31-12-61:~/devops/commands$ tail -n 3 notes.txt
Line3: Task started day1
Line4: Task started day1
Line5: Task started day1

