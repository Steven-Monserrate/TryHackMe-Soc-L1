#Phishing for Information – The attempt to trick targets into divulging information

#Sender Policy Framework (SPF) – Used to authenticate the sender of an email
  #Uses three categories:
    #Pass, Neutral, None – Accepted and allowed to process the email
    #SoftFail, PermError – Flagged (But still allowed to process)
    #Fail, TempError – Rejected (Immediately discards the email)

#Google Admin Toolbox Messageheader – Allows you to analyze delivery details using an email’s full header

#DomainKeys Identified Mail (DKIM) – Used for the authentication of an email that is being sent

#Domain-Based Message Authentication, Reporting, and Conformance (DMARC) – An open source standard, uses a concept called alignment to tie the result of two other open source standards – SPF and DKIM – to the content of an email

# p=reject – provides the greatest amount of protection by blocking emails that fail the DMARC check

#Secure/Multipurpose Internet Mail Extensions (S/MIME) - A standard protocol for sending digitally signed and encrypted messages

#Which S/MIME component ensures that only the intended recipient can read the contents of an email message?
  #Encryption

