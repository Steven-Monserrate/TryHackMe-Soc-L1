#Notes:

#Fast Flux – A DNS technique used by botnets to hide phishing, web proxying, malware delivery, and malware communication activities behind compromised hosts acting as proxies

#Domain Name – Mapping an IP address to a string of text

#Punycode – A way of converting words that cannot be written in ASCII, into a Unicode ASCII encoding

#URL Shortener – A tool that creates a short and unique URL that will redirect to the specific website specified during the initial step of setting up the URL Shortener link

#Lab

#Lab used the link attached ot open up a security vendor's report and answered the following questions:
  #Link - https://assets.tryhackme.com/additional/pyramidofpain/task5-report.pdf
  #Q 1 - A process named regidle.exe makes a POST request to an IP address based in the United States (US) on port 8080. What is the IP address?
    #96.126.101.6
  #Q2 - The actor drops a malicous executable (EXE). What is the name of this executable?
    #G_jugk.exe
  #Q3 - Look at this report by VirusTotal. How many vendors determine this host to be malicious?
    #https://assets.tryhackme.com/additional/pyramidofpain/vtotal2.png
    #9

#Lab 2

#Which network indicator helped us to identify the malware type (Emotet)?
  #User-Agent

#How many POST requests are in the screenshot from the PCAP file?
  #6

#Lab 3

#Use the Link to answer the questions: https://ssdeep-project.github.io/ssdeep/index.html

  #Q 1 - Provide the method used to determine similarity between the files
    #Fuzzy Hashing

  #Q 2 - Provide the alternative name for fuzzy hashes without the abbreviation
    #Context triggered piecewise hashes

#Lab 4

#Use the Link to answer the questions: https://attack.mitre.org/

  #Q 1 - Navigate to ATT&CK Matrix webpage. How many techniques fall under the Exfiltration category?
    #9

  #Q 2 - Chimera is a China-based hacking group that has been active since 2018. What is the name of the commercial, remote access tool they use for C2 beacons and data exfiltration?
    #Cobalt Strike

#Lab 5

![alt text](Photos/12)

![alt text](Photos/13)

![alt text](Photos/14)

#TTP - The attackers plans and objectives
#Tools - The attacker has utilized these to accomplish their objectives
#Network - These artifacts can present themselves as C2 traffic
#Domain Names - An attacker has purchased this and used it in a typo-squatting campaign
#IP Addresses - These addresses can be used to identify the infrastructure an attacker is using for their campaign
#Hash Values - These signatures can be used to attribute payloads and artifacts to an actor

