# CST8912 – Cloud Solution Architecture

## Cloud Development and Operations
### CST8912_013 Cloud Solution Architecture  
### Lab 3_Week 4

---

**Prepared By:**  
Daniyal Shahid (041110791)  

**Submitted to:**  
Prof. Ragini Madaan  

---

## Graded Lab Activity #3

### Purpose of this Lab

Compose the appropriate networking, compute, storage, and database services to meet the operational requirements of various application scenarios. 

•	Design cloud architecture layers and their function to maximize reliability and resiliency of application services.

•	Outline core architectural components to meet the operational requirements of various application scenarios.

•	Describe cloud service models (IaaS, PaaS, SaaS) and implement highly available and elastically scalable solutions.

•	Identify the core features of cloud computing and their interactions with each service layer.


### STEPS

In this lab, you will explore the Azure storage account, and generate shared access signatures for Azure Cloud, how to change rules and conditions to manage lifecycle of cloud storage

**1.**	Create a storage account “labtest8912” understudent subscription and resource group “CST8912-demo” for region Canada central and select geo redundant storage (geo redundant storage GRS), keep networking and data protection options default.

### Resource Group CST8912-demo


![Step 1 - Storage Account Creation](./images/1.png "Resource Group CST8912-demo")


### Storage Account labtest8912

![Step 1 - Storage Account Creation](./images/2.png "Storage Account labtest8912")


**2.**	Go to your storage account resource blade, in data management section, go to redundancy tab and change redundancy to “local redundant storage” from dropdown, and under settings choose configuration and set blob access tier to cool and save the change /2

### Changing Redundancy to Local Redundant Storage

![Step 2 - Storage Account Creation](./images/3.png "Changing Redundancy to Local Redundant Storage")

### Setting blob access tier configuration to cool

![Step 2 - Storage Account Creation](./images/4.png " Setting blob access tier configuration to cool")

**3.**	under data storage in left, click containers and add new container named “labtestcontainer8912” and select upload a blob and change the advance settings and change the access tier to “hot” and upload to folder named “sampletest8912”, browse the files from the sample files links shared in this lab (check with your instructor if you cannot find the sample file link) /6

### New Container labtestcontainer8912


![Step 2 - Storage Account Creation](./images/5.png " New Container labtestcontainer8912")


### labtestcontainer8912

![Step 2 - Storage Account Creation](./images/6.png " labtestcontainer8912")

### Uploading the file to folder named “sampletest8912”,

![Step 2 - Storage Account Creation](./images/7.png " Uploading the file to folder named “sampletest8912")


**4.**	click the file uploaded in the container to see the configuration options and copy the blob url and open a new private window from the browser to paste the copied url 
note : The url should not work since the containers public access is set to private, resource was not found.  /2 

### URL not working since the containers public access is set to private, resource was not found


![Step 2 - Storage Account Creation](./images/8.png " URL not working since the containers public access is set to private, resource was not found")


**5.**	On the file blade, click generate SAS and copy the SAS token generated and paste the blob SAS URL on the private window of the browser, you must be able to see the file /3


### SAS Token Creation

![Step 2 - Storage Account Creation](./images/9.png " SAS Token Creation")


### File is visible after using SAS

![Step 2 - Storage Account Creation](./images/10.png " File is visible after using SAS")

**6.**	On the container blade under data management tab go to “Lifecycle Management” and create a new rule name “myrule8912”, rule scope should be “limit blobs with filters” and blob type and blob subtype should be default, add condition if base blobs were last modified more than “ 15 days” ago then “move to cool storage” /4


### New Rule myrule8912


![Step 2 - Storage Account Creation](./images/11.png " New Rule myrule8912")


### Overview

![Step 2 - Storage Account Creation](./images/12.png " Overview")

### Changing Base blobs settings to last modified more than “ 15 days” ago then “move to cool storage

![Step 2 - Storage Account Creation](./images/13.png " Changing Base blobs settings to last modified more than “ 15 days” ago then “move to cool storage")


**7.**	After demo delete all the resources created during lab and create a lab report documenting all the steps with screenshots                                                             

![Step 2 - Storage Account Creation](./images/14.png " After demo delete all the resources created during lab and create a lab report documenting all the steps with screenshots")

### YouTube videos for reference for azure:

https://www.youtube.com/watch?v=sI2ahWX8RH8
##### Azure SAS token: https://www.youtube.com/watch?v=0PX1eW1sCGg
##### YouTube videos for reference for AWS:
https://www.youtube.com/watch?v=xFzJw6wJ8eY
##### YouTube videos for reference for GCP:
https://www.youtube.com/watch?v=DviqTrRZJ44
##### Grading criteria for this lab: 

For grading prepare a lab report with your findings, analysis and screenshots and share that report in an Assignments tab in Brightspace.

##### Optional (not graded) – If you would like to change the access policy for the blob storage at the blob or container level, one can grant public read access to blobs so one can view the content of the blob/container, there is an option to change the access policy : https://www.youtube.com/watch?v=FSZXH9i07jg
