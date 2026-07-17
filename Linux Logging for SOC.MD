#Despite common belief, Linux isn't unhackable or immune to malware

#Linux-based systems are becoming increasingly targeted

#Lab

#Question 1
  #Which IP address failed to log in on multiple users via SSH?
    #cat /var/log.auth.log | grep -E 'Failed' = 10.14.94.82
  #Which user was created and added to the "sudo" group
    #cat /var/log/auth.log | grep -E '(useradd)' = xerxes

#Question 2:
  #According to the VM's package manager logs, which version of unzip was installed on the system?
    #cat /var/log/dpkg.log | grep unzip = 6.0-28ubuntu4.1
  #What is the flag you see in one of the users' bash history?
    #sudeo grep -i "THM{" /root/.bash_history = "THM{note to remember}"

#Question 3:
  #Which Linux system call is commonly used to execute a program?
    #execve
  #Can a typical program open a file or create a process bypassing system calls?
    #Nay

#Question 4:
  #When was the secret.thm file opened for the first time?
    #ausearch -i | grep "secret.thm" = 08/13/25 18:36:54
  #What is the original file name downloaded from GitHub via wget?
    #naabu_2.3.5_linux_amd64.zip
  #Which network range was scanned using the downloaded tool?
    #ausearch -i | grep naabu = 192.168.50.0/24

