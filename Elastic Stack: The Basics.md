#This lab review was from the TryHackMe room "Elastic Stack: The Basics."

#Lab:

15

#Open Firefox and type in the http://(IP Address)
  #Doing so will bring up the following screen. Log in and progress to the next step
  ![Alt Text](/Photos/15.png)
  
#Q1 - Select the index vpn_connections and filter from 31st December 2021 to 2nd Feb 2022. How many hits are returned?

#Filter the results in the top bar to only show hits between 12/31/2021 through 2/2/2022
  #Look at the number of hits displayed. That provides the answer to how many records are displayed
  #Answer 1 - 2861
 ![Alt Text](/Photos/16.png)
 
#Q2 - Which IP address has the maximum number of connections?
#Expand the screen and click on "Source_ip" in the left side of the query. This will bring up the filter and display the top 5 IP users
  #Answer 2 - 238.163.231.224
 ![Alt Text](/Photos/18.png)
 
#Q3 - Which user is responsible for the overall maximum traffic?
  #Click on Discover, and remove all the filters except for the December 31, 2021 - February 2, 2022 dates. Then, click on UserName
    #Answer 3 - James
 ![Alt Text](/Photos/19.png)
 
  #Q4 - Apply Filter on UserName "Emanda"; which SourceIP has max hits?
    #click on filter, type in "Emanda". Click on Source_Ip. Top result
      #Asnwer 4 - 107.14.1.247
 ![Alt Text](/Photos/20.png)
 
  #Q5 - On 11th Jan, which IP caused the spike observed in the time chart?
    #Clear filters. Click on Source_ip, then filter by date. Then, isolate 1/11
      #Answer 5 - 172.201.60.191

#Q6 - How many connections were observed from IP 238.163.231.224?
  #Clear filters, click on Soure_ip, and type in 238.163.231.224, and change states to exclude New York. Verify that filter is still between 12/31/2021 - 2/2/2022
    #Answer 6 - 48
 ![Alt Text](/Photos/21.png)
  ![Alt Text](/Photos/22.png)
  
#Q7 - Create a table with the fields IP, UserName, Source_Country and save.
  #Clear filters, click on "Source_IP", visualize, and then click and drag the values into the table.
    #NOTE - I turned my chart into a donut chart for easier comprehension, but think that a scatter map would potentially be a better choice
 ![Alt Text](/Photos/23.png)
 
#Q8 - Create a search query to filter the logs where Source_Country is the United States and show logs from User James or Albert. How many records were returned?
  #Source_Country: "United States" and UserName : "Albert" or UserName : "James"
    #Answer 8 - 161
 ![Alt Text](/Photos/24.png)
 
#Q9 - A user Johny Brown was terminated on the 1st of January, 2022. Create a search query to determine how many times a VPN connection was observed after his termination
  #UserName : "Johnny Brown" and Source_ip : * / Filtered dates 12/31/2021 through 2/2/2022
    #Answer 9 - 1

#Q10 - Create a filtered table to display all failed login attempts, listing both UserName and Source_ip as the table fields.
  #QA - Which user was observed with the greatest number of failed attempts?
    #A - Simon
  #QB - How many wrong VPN connection attempts were observed in January?
    #B - 274

#Q11 - Lessons Learned Notes
  #The final portion of this lab was to upload all of the previous tables and searches. However, I went afk and forgot to save my results. In future endeavors, I'll make sure to save all KQL searches as they pertain to making the table.
  #The photo under this Q will show 1 of the tables that should have been present. Others can be referenced in the Q's above this one
   ![Alt Text](/Photos/25.png)
