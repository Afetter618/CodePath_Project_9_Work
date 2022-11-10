# Honeypot Assignment

**Time spent:** **22** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?

I deployed the MHN-Admin website through GCP and opened the website using its IP address on my host browser.

![CodePath_Week_9_Lab_SS_1_MHN_Admin_Configuration](https://user-images.githubusercontent.com/111651054/201005079-44797e2f-8211-4cbd-bfc5-938e65b4673a.gif)

### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do?

Dionaea is a honeypot records attacks and malware and makes a copy of that malware in order to help the host of the real website understand how an attacker would go about hacking it and what vulnerabilities there are in the wbsite itself.

![CodePath_Week_9_Lab_SS_2_Honeypot_Configuration](https://user-images.githubusercontent.com/111651054/201005101-3bfbaa5a-857e-4cd2-9740-b089c8d6511e.gif)

### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?

The RDBMS that MHN-Admin uses is Pwnlandia. The information that the JSON file records is the information about the attackers. Not only does it store the IP addresses, but also the protocols used, timestamps of when the attacks occurred, and honeypot the attacks were performed on.

**Json file in branch**

### Deploying Additional Honeypot(s) (Optional)

#### X Honeypot

**Summary:** What does this honeypot simulate and do for a security researcher?

<img src="x-honeypot.gif">

### Malware Capture and Identification (Optional)

#### X Malware

**Summary:** How did you find it? Which honeypot captured it? What does each malware do?

MD5 Hash: *Run `md5sum` on the file and record the hash here.*

SHA1 Hash: *Run `sha1sum` on the file and record the hash here.*

<img src="x-malware.gif">

## Notes

Describe any challenges encountered while doing the assignment.
