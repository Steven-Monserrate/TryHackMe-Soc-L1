#Notes:

#File paths and names are like crime scene clues, revealing attacker behavior

#C:/ (System drive) - can be a common target for persistence mechanisms

#C:\Users\Public - profile can enable cross-user access of denoted adversary tools

#C:\Users\Public\Public Downloads - provides a high-traffic directory that would often evade strict monitoring

#Filenames can also be used to hide malware
  #Double extensions - invoice.pdf.exe - Uses Windows to hide file extensions
  #System binary impersonation - scvhost.exe - Abuses the user's familiarity with core system processes
  #High-entropy strings - jh8F21.exe - suggests automated packing or polymorphic generation, which is commonly used in a high-churn phishing operation
  #Masquerading - Filenames such as backup-2300.exe can blend with routine files, thus leveraging on reduced suspicion

#VirusTotal - A widely used threat intelligence service that aggregates scan results from dozens of antivirus vendors into a single report
  #Detection score: Represents a crowdsourced security verdict from various vendors displayed as a ratio. The higher the number, the higher the confidence threat
  #Threat labels and categories: These are vendor-specific classifications of threats that help confirm their attribution across vendors
  #Detection rules: These are the technical signatures used by AV engines to identify threats. Typical classifications are YARA rules, Heuristic patterns, and behavioral triggers
  #Properties: This is where the core metadata for the file is stored, including the file type, size, and compilation timestamp
  #Contained domains and IPs: This information covers the malware's network infrastructure
  #Contained files: This section details any files embedded or dropped during the malware's execution

#MalwareBazaar - An all-in-one database for malware collection and analysis. Supports the following features:
  #Malware Samples Upload: Security analysts can upload their malware samples for analysis and build the intelligence database. This can be done through the browser or an API
  #Malware Hunting: Hunting for malware samples is possible through various elements, such as:
    #Malware Family tagging: You will find files classified by their malware families. An example of this is a file with only 5/70 detections on VirusTotal but tagged as #IcedID in MalwareBazaar; it should be treated as malicious
    #YARA rule integration: Many submissions will include rules that detect related samples. As an analyst, you should take note of these rules to be added to the EDR/SIEM for future hunting
    #Campaign attribution: Tags such as #TA551, which belong to a threat actor group, help link observed incidents to known adversaries. This can help identify coordinated attacks against an environment
    #Sample Availability: Malware samples are available for download and analysis. Reanalyzing samples in a sandbox is best practice, which we shall cover in the next task

#Static properties such as hashes, strings, and sections tell you identity

#Security analysts will use sandboxes to do three things:
  #Confirm execution
  #Extract runtime IOCs
  #Map to ATT&CK


#Lab

#One of the files included the CTI Files folder on the Desktop shows one of the indicators mentioned. Can you identify the file and the indicators mentioned. Can you identify the file and the indicator?
  #payroll.pdf, Double extensions
![alt text](Photos/120.png)

#What is the SHA256 hash of the file bl0gger?
  #2672b6688d7b32a90f9153d2ff607d6801e6cbde61f509ed36d0450745998d58
![alt text](Photos/121.png)

#What is the threat classification label used to identify the malicious file?
  #trojan.graftor/flystudio
![alt text](Photos/122.png)

#When was the file first submitted for analysis? (Answer format: YYYY-MM-DD HH:MM:SS)
  #2025-05-15 12:03:49

#Which vendor classified the Morse-Code-Analyzer file as non-malicious?
  #CyberFortress
![alt text](Photos/123.png)

#What MITRE technique has been flagged for persistence and privilege escalation for the Morse-Code-Analyzer file?
  #DLL Side-Loading
![alt text](Photos/124.png)

#What tags are used to identify the bl0gger.exe malicious file on Hybrid Analysis?
  #BlackMoon, Discovery, windows-server-utility
![alt text](Photos/125.png)

#What was the stealth command line executed from the file?
  #regsvr32 %WINDIR%\Media\ActiveX.ocx /s
![alt text](Photos/126.png)
