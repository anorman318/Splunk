# Splunk
Utilized Splunk skills in a simulated environment to design a monitoring solution to protect Vandalay from security attacks.

**Let's Go Splunking!**  
You have just been hired as an SOC analyst by Vandalay Industries, an importing and exporting company.  
* Vandalay Industries uses Splunk for their security monitoring and have been experiencing a variety of security issues against their online systems over the past few months.  
* You are tasked with developing searches, custom reports, and alerts to monitor Vandalay's security environment in order to protect them from future attacks.  

**Vandalay Industries Monitoring Activity Instructions**  
**Step 1: The Need for Speed**  
**Background:** As the worldwide leader of importing and exporting, Vandalay Industries has been the target of many adversaries attempting to disrupt their online business. Recently, Vandalay has been experiencing DDOS attacks against their web servers.  

Not only were Vandalay web servers taken offline by a DDOS attack, but upload and download speed were also significantly impacted after the outage. Your networking team provided results of a network speed run around the time of the latest DDOS attack.  

**Your Task:** Create a report to determine the impact of the DDOS attack on upload and download speed. Create an additional field to calculate the ratio of the upload speed to the download speed. To do so, complete the following steps:  

1. Upload the following file containing the system speeds around the time of the attack

2. Using the eval command, create a field called ratio that shows the ratio between the upload and download speeds.  

4. Create a report using Splunk's table command to display the following fields in a statistics report:  

    _time  
    IP_ADDRESS  
    DOWNLOAD_MEGABITS  
    UPLOAD_MEGABITS  
    ratio  
    
Questions:      
1. Based on the report you created, what is the approximate date and time of the attack?  
    Answer: The approximate date and time of the attack is 2-23-2020 at 14:30 as there is a significant drop in Download_megabits seen.  

2. How long did it take your systems to recover?   
    Answer: It took approximately 9 hours for the system to recover.  On 2-23-2020 at 23:30 you see downlad_megabits return to normal levels.  

  Provide a screenshot of your report:  
  <img width="914" alt="speed test report" src="https://user-images.githubusercontent.com/106919343/200918681-a8b7f60f-27ee-4719-a40f-2d7fb0831c0e.png">  

**Step 2: Are We Vulnerable?**  
**Background:** Due to the frequency of attacks, your manager needs to be sure that sensitive customer data on their servers is not vulnerable. Since Vandalay uses Nessus vulnerability scanners, you have pulled the last 24 hours of scans to see if there are any critical vulnerabilities.  

**Your Task:** Create a report determining how many critical vulnerabilities exist on the customer data server. Then, build an alert to notify your team if a critical vulnerability reappears on this server. To do so, complete the following steps:  

1. Upload the following file from the Nessus vulnerability scan  

2. Create a report that shows the count of critical vulnerabilities from the customer database server.  
  * The database server IP is 10.11.36.23.  
  * The field that identifies the level of vulnerabilities is severity.  
  
3. Build an alert that monitors every day to see if this server has any critical vulnerabilities. If a vulnerability exists, have an alert emailed to soc@vandalay.com.  

4. Provide a screenshot of your report:  
<img width="927" alt="nessus vulnerability table" src="https://user-images.githubusercontent.com/106919343/200919425-16c755f8-d26b-47b9-b713-f6b10b98c89b.png">  

5. Provide a screenshot showing that the alert has been created:  
  <img width="923" alt="nessus alert 1" src="https://user-images.githubusercontent.com/106919343/200920360-8f211d89-a9e8-47f2-a6be-a26a3146f4b8.png">  

**Step 3: Drawing the (Base)line**  
**Background:** A Vandaly server is also experiencing brute force attacks into their administrator account. Management would like you to set up monitoring to notify the SOC team if a brute force attack occurs again.  

**Your Task:** Analyze administrator logs that document a brute force attack. Then, create a baseline of the ordinary amount of administrator bad logins and determine a threshold to indicate if a brute force attack is occurring. To do so, complete the following steps:  

1. Upload the following administrator login logs  

2. Answer the following in the M19 Submission File:  
  (1) When did the brute force attack occur?  
      Answer: The brute force attack started at 9 am on Friday February 21, 2020 and lasted until 1 pm that day.  

   (2) Determine a baseline of normal activity and a threshold that would alert if a brute force attack is occurring:  
      Answer: Over the course of the 36 hours there were a total of 1,004 failed logins. Taking these numbers we can find the average number of failed logins per         hour and get 28. Using this information we could determine a baseline of any attempts exceeding 50 bad logins per hour would alert of a brute force attack           occurring.  

   (3) Provide a screenshot showing that the alert has been created:  
    <img width="925" alt="log validation alert" src="https://user-images.githubusercontent.com/106919343/200919617-da59b032-d630-48bf-a4d2-4a1bb595bd4f.png">  
