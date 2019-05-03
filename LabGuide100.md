
# Lab 100

## Introduction

This lab will show you how to setup the Autonomous Data Warehouse

## Objectives

- Get comfortable with Oracle's public cloud services

- ADW Provisioning

- ADW Connectivity


## Notional Architecture and Trial Account access

### **STEP 1**: Review Notional Architecture
![](./images/adw1.PNG)
![](./images/Notional_Architecure.PNG)

#### What is an Autonomous Data Warehouse?

Oracle Autonomous Data Warehouse is built around the market leading Oracle database and comes with fully automated data warehouse specific features that deliver outstanding query performance.  This environment is delivered as a fully managed cloud service running on optimized high-end Oracle hardware systems.  You don’t need to spend time thinking about how you should store your data, when or how to back it up or how to tune your queries.  

We take care of everything for you.

Click here to <a href="https://www.youtube.com/watch?v=tZMZODoi2xw" target="blank">watch our short video</a> that explains the key features in Oracle's Autonomous Data Warehouse.

Oracle’s Autonomous Data Warehouse is the perfect quick-start service for fast data loading and sophisticated data reporting and analysis.  Oracle manages everything for you so you can focus on your data.

Read on to begin your Getting Started journey with Oracle Autonomous Data Warehouse.


### **STEP 2**: Lab Prerequisites – Required Software
- Oracle Cloud Account
- Sql Developer

<a href="https://cloudcustomerconnect.oracle.com/resources/32a53f8587/summary" target="blank">**Cloud Customer Connect**</a> Forum for Autonomous Data Warehouse
If you have a question during this workshop then use the Autonomous Data Warehouse Forum to post questions, connect with experts, and share your thoughts and ideas about Oracle Autonomous Data Warehouse.

Are you are completely new to the <a href="https://cloudcustomerconnect.oracle.com/resources/32a53f8587/summary" target="blank">**Cloud Customer Connect**</a> forums? Visit our  <a href="https://cloudcustomerconnect.oracle.com/pages/1f00b02b84" target="blank">Getting Started forum page</a> to learn how to best leverage community resources.


### **STEP 3**: Access the Cloud

- Navigate to https://console.us-ashburn-1.oraclecloud.com
Note : You can Change region name in above URl

- Enter your tenancy name and click continue.

   ![](./images/adw2.png)

- Click Next to go in login page and then enter username/password

   ![](./images/adw3.png)


- Click top left menu to see all available service.

   ![](./images/cloud4.PNG)

## ADW Provisioning

### **STEP 4**: ADW Provisioning

- Login to cloud environment,Click on the Menu Icon to show the available services. In the list of available services, select Autonomous Data Warehouse.

- The console for Autonomous Data Warehouse displays. You can use the List Scope drop-down menu to select a compartment. Click Create Autonomous Data Warehouse.

  ![](./images/adw4.png)

- In the Create Autonomous Data Warehouse dialog, enter the following information.
  * Display Name - Enter a name for the data warehouse for display   (eg. adwapexdemo).
  * Database Name - Use letters and numbers only, starting with a letter (eg. adwapexdemo). Maximum length is 14 characters. (Underscores not initially supported.)
  * CPU Core Count - Number of CPUs for your service.(Minimum to be 5)
  * Storage (TB) - Select your storage capacity in terabytes. It is the actual space available to your service instance, including system-related space allocations.(Minimum to be 1 TB)
  * Administrator Credentials - Password for ADMIN user of the service instance. The password must meet the following requirements:
  * The password must be between 12 and 30 characters long and must include at least one uppercase letter, one lowercase letter, and one numeric character.
      * The password cannot contain the username.
      * The password cannot contain the double quote (") character.
      * The password must be different from the last 4 passwords used.
      * The password must not be the same password that is set less than 24 hours ago.
  * License Type - Select whether you have existing licenses or if you want to subscribe to new database software licenses and the database cloud service.
  * Tags - (Optional) Tagging is a metadata system that allows you to organize and track resources within your tenancy. Tags are composed of keys and values which can be attached to resources.
  * Click Create Autonomous Data Warehouse.
  ![](./images/adw5.png)
  ![](./images/adw6.png)
  ![](./images/adw7.png)
- The Create Autonomous Data Warehouse dialog closes. On the console, the State field indicates that the data warehouse is Provisioning. Once creation is completed, the State field changes from Provisioning to Available.
 ![](./images/adw8.png)
 ![](./images/adw9.png)
- Download the Credentials Zip File. Once you have created the data warehouse, download the credentials zip file for client access to that data warehouse. Click newly created instance and then select DB Connection.
- The Database Connection dialog opens for downloading client credentials. Click Download.
- In the Download Wallet dialog, enter an encryption password (BEstrO0ng_#11) for the wallet, confirm the password, and then click Download.
 ![](./images/adwc8.png)
- Click Save File, and then click OK.
- Store the zip file and make note of the password. You will use the zip file in the next step to define a SQL Developer connection to your Autonomous Data Warehouse database.
-	Open SQL Developer on your local computer. In the Connections panel, right-click Connections and select New Connection.
 ![](./images/adwc9.png)
- The New/Select Database Connection dialog appears. Enter the following information.
  * Connection Name - Enter the name for this cloud connection.
  * Username - Enter the database username. Use the default administrator database account (admin) that is provided as part of the service.
  * Password - Enter the admin user's password that you or your Autonomous Data Warehouse administrator specified when creating the service instance.
  * Connection Type - Select Cloud Wallet.
  * Configuration File - Click Browse, and select the Client Credentials zip file, downloaded from the Autonomous Data Warehouse service console by you, or given to you by your Autonomous Data Warehouse administrator.
  * Service - In the drop-down menu, service selections are prepended with database names. Select the low, medium, high, or parallel menu item for your database. These service levels map to the LOW, MEDIUM, HIGH, and PARALLEL consumer groups, which provide different levels of priority for your session.
 Note: Earlier versions of SQL Developer may not support this feature.             
 ![](./images/adw10.png)
-	Click Test.
Status: Success displays at the left-most bottom of the New/Select Database Connection dialog.
- Click Connect to connect to your ADW instance . 

## ADW Scaling 

- To Scale Up or Scale Down your ADW instance, Go to your ADW instance in your console . 

- Click on Scale Up/Down tab . 

- ![](./images/adw17.png)

- Once you click on this tab, you will be able to see below screen . 

- ![](./images/adw17.png)

- Increase or decrease the count as per your requirement and Click on " Update" to update the count . 



## Data Loading

- To load data in your ADW instance, identify the file which you want to load . 
- In our case , we have "bigml_marketbasket" csv file in our local machine which we want to load in our ADW instance . 
- Go to your Sql Developer (which is already connected to your ADW instance) .
- On your right hand side , you will be able to "Tables" option . 
- Right click on "Tables" option and Select "Import" option . 
-  ![](./images/adw11.png)
- 
- Once you click on "Import" button , you will be able to see below window . 
-  ![](./images/adw12.png)
- 
- Click on Browse option and Browse the file from Local machine which you want to upload to ADW instance . 
- Give ";" in Line Terminator field and modify other fields as per your requirement . 
- Click on "Next" button . 
- Once you click on "Next" button, you will be able to see below screen . 
- ![](./images/adw13.png)
- 
- Give desired table name and click on "Next" button . 
- Select the columns which you want to import and click on "Next" button . 
- ![](./images/adw14.png)

- Click Next

- ![](./images/adw16.png)

- You will be able to see below screen. 

- ![](./images/adw15.png)

- Check the summary and click on "Finish" button to Finish the data load process .
- You will be able to see loaded data in your ADW instance now  . 

## Creation of ML User

- To create ML(Machine Learning User), go to your ADW instance and click on "Service Console"

 ![](./images/adw21.png)
 
- Click on "Administration" Tab 

  ![](./images/adw22.png)
  
- Click on "Manage Oracle ML User "
  
  ![](./images/adw23.png)
  
- Give username and password. 

NOTE : We will insert image here . Not able to upload due to console server issue . 

- Click on "Create" button to create ML user .






