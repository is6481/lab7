Objectives
==========

-   Create a MySQL database using Amazon Web Services (AWS)
-   Connect to the newly created database and upload some data
-   Modify permissions for the database
-   Upload data to Domo for visualization

Instructions
============

To get started, [click
here](https://aws.amazon.com/getting-started/tutorials/create-mysql-db/)
and follow the instructions through step 3. (Feel free to go through
step 4 after the course is completed, but only if you really feel like
it.)

Once you have the MySQL workbench installed and connected to the
database, you’ll need to upload some data. To do this, go to Files/Data
Files in Canvas and download the northwind\_db\_mysql.sql file. Once the
file is open, click on the *Query* menu and select *Execute (All or
Selection)*. Note that it will take some time to create the database,
create the tables and load all the data.

By default, AWS will set up your database so it is accessible only to
the IP address of your computer at the time the database is created.
This means that if you create the database on campus, you will likely
not be able to connect to the database at home. Another consequence is
that the database will not be available to other cloud products (such as
Domo). Most cloud products will publish a list of IP addresses to
“whitelist”.

So, to complete this assignment and upload data to Domo, you’ll need to
adjust some settings. First, see the [list of IP addresses to whitelist
here](https://knowledge.domo.com/Connect/Connecting_to_Data_with_Connectors/General_Guide_to_Connecting_with_Connectors/Whitelisting_IP_Addresses_for_Connectors).
Then log in to your AWS account and do the following.

### Step 1

Once you have selected your database, click on the link to go to the
attached security group. ![Step
1](/Users/jeremymorris/utah_teaching/is6481/lab7/security_step01.png)

### Step 2

Click on the *Inbound* rules section and then click *Edit*. ![Step
2](/Users/jeremymorris/utah_teaching/is6481/lab7/security_step02.png)

### Step 3

This will bring up another menu (example below). You want to click *Add
Rule* for each of the IP addresses listed on Domo’s site. I believe
you’ll only need to do the ones listed in US East (AWS). Under *Type*
select *MySQL*. This will pre-populate the port correctly. Copy and
paste each IP address as shown on Domo’s site. ![Step
3](/Users/jeremymorris/utah_teaching/is6481/lab7/security_step03.png)

### Step 4

You will be finished after you click save. Be sure to add any additional
IP addresses you need to connect from before clicking save. Your current
IP address can be found by going to [this
website](https://www.whatismyip.com/).

To Turn In
==========

After you have everything configured, connect one of the tables from the
new database to Domo and create a card. To complete the assignment, copy
the url of the card as the submission of the lab.
