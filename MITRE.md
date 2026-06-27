#This document contains lessons learned and a lab involving threat hunting through MITRE's ATT&CK repository. Lab identified APT and its methods commonly utilized in attacks.

#Notes:

#MITRE ATT&CK Framework - “a globally-accessible knowledge base of adversary tactics and techniques based on real-world observations. The ATT&CK knowledge base is used as a foundation for the development of specific threat models and methodologies
#in the private sector, in government, and in the cyber security product and service community.”
  #Originally developed in 2013 and updated constantly since

#Tactic – The goal that the attacker is seeking to achieve

#Technique – How the attacker attempts to achieve that goal

#Sub-technique – Specific methods attackers use, i.e. Scanning IP Blocks, Vulnerability Scanning, or Wordlist Scanning

#Cyber Analytics Repository (CAR) – A collection of ready-made detection analytics built around ATT&CK

#D3FEND – Detection, Denial, and Disruption Framework Empowering Network Defense) – a structured framework that maps out defensive techniques and establishes a common language for describing how security controls work
  #Is broken down into its own matrix consisting of seven tactics
    #Model
    #Harden
    #Detect
    #Isolate
    #Deceive
    #Evict
    #Restore

#Lab 1:

#Scenario: You are a security analyst in the aviation sector, and your organization is migrating its infrastructure to the cloud. Your task is to use ATT&CK to gather intelligence on APT groups known to target this sector, identify their tactics and
#techniques, and assess any potential gaps in your defensive coverage.

![alt text] (6.png)
