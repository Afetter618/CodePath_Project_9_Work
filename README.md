# Honeypot Implementation

**Time spent:** **23** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?

I deployed the MHN-Admin website through GCP and opened the website using its IP address on my host browser.

![CodePath_Week_9_Lab_SS_1_MHN_Admin_Configuration](https://user-images.githubusercontent.com/111651054/201005079-44797e2f-8211-4cbd-bfc5-938e65b4673a.gif)

### Dionaea Honeypot Deployment

**Summary:** Briefly in your own words, what does dionaea do?

Dionaea is a honeypot records attacks and malware and makes a copy of that malware in order to help the host of the real website understand how an attacker would go about hacking it and what vulnerabilities there are in the wbsite itself.

![CodePath_Week_9_Lab_SS_2_Honeypot_Configuration](https://user-images.githubusercontent.com/111651054/201005101-3bfbaa5a-857e-4cd2-9740-b089c8d6511e.gif)

### Database Backup

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?

The RDBMS that MHN-Admin uses is MongoDB. The information that the JSON file records is the information about the attackers. Not only does it store the IP addresses, but also the protocols used, timestamps of when the attacks occurred, and honeypot the attacks were performed on.

**Json file in branch**

## Notes

When doing this project, I had a lot of challenges. I first tried creating the mhn-admin VM through the GCP Cloud Shell. However, it was not working at first so I began manually creating each of the VMs. Although everything worked well and the MHM-Admin page was successfully created along with the honeypot VM, none of the attacks were showing up after using nmap on my Kali Linux VM. This problem resulted in me recreating the VMs over 5 times and completely starting over 3 times. However, after the third restart, I realized that I had been following the guildine's timezome and region when I shouldn't have. Since I am in Eastern Standard Time, I should have been using "us-east1" as the region and "us-east1-b" as the zone. After realizing this problem, I eventually got the attacks to work and successfully implement the honeypot.
