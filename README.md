# Project 3: Amazon RDS Backup &amp; Restore Using AWS Backup

## What I learned from this project;

- Creating an On-Demand Backup for an Amazon RDS Database
- Setting Up Automatic Backups for Amazon RDS Stuff with AWS Backup
- How to add resources to an existing backup plan using tags
- Bringing Back Data from a Backup


------------------------------------------------------------------
Creating the DB instance;
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/7ea8de6e-1dac-49b8-a86a-b3ada8d7e70e)

I opted for the easy create option because I don't want to spend time configuring it manually, especially since this is only for testing purposes.
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/dc49f759-593f-49ba-a639-eef88e4038cb)
Dev/Test
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/7bdd9fe4-3fcf-4226-9bff-1fa366ac4d50)
Creating...
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/514512c8-1a5e-4c96-beee-8a34becef41d)
Our DB is now available;
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/618c67a7-5192-41e7-8b74-03341f6295f6)
Now, let's create our backup plan
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/2144f868-a713-4b2e-b0e6-7947d2a4cab9)
Click settings > configure resources || In the Configure Resources section, utilize the toggle switches to activate or deactivate the services associated with AWS Backup. Select Confirm once your services are configured.
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/f11eb8d8-ac30-4213-bfa1-dc68d8514f96)
Proceed to create on-demand backup;
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/ede64b7e-3eae-4ab2-90dc-76b84dfac7c4)
After choosing RDS and making sure I'm in N. Virginia region, I don't know why I'm not seeing my database, so I'll go through the DB again to check if I need to grant it one permission 
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/f33f9689-d0a3-4f46-9791-739b97bdf84a)
