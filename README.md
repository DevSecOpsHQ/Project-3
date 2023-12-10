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

![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/2144f868-a713-4b2e-b0e6-7947d2a4cab9)
Click settings > configure resources || In the Configure Resources section, utilize the toggle switches to activate or deactivate the services associated with AWS Backup. Select Confirm once your services are configured.
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/f11eb8d8-ac30-4213-bfa1-dc68d8514f96)
Proceed to create on-demand backup;
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/ede64b7e-3eae-4ab2-90dc-76b84dfac7c4)
After choosing RDS and making sure I'm in N. Virginia region, I don't know why I'm not seeing my database, so I'll go through the DB again to check if I need to grant it one permission 
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/f33f9689-d0a3-4f46-9791-739b97bdf84a)
After some time, I discovered my mistake—it took me 4 hours, quite unusual! I unintentionally created a MySQL Aurora DB instead of an RDS MySQL. Now, I've set up a new DB. Let's see how it goes...
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/c5d5b43a-d606-4ea2-b954-0749b0a49083)
Boom, here we go
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/192f536b-42a9-478b-af38-0a7abe650843)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/61c73eec-5b8b-46bf-83c5-075cccd11d31)
Created an IAM role and clicked on create the on-demand-backup
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/b6b127bf-731e-4945-885f-c3a9cc066b30)
In progress
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/ddd361df-eb97-4fc6-8ef2-d15baca0f1c8)
Completed
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/a67b76af-780c-4f9d-bb78-b0bc713aeda1)
I have the option to select the Backup job ID for the chosen resource that was backed up to view the specifics of that particular job.

Now, let's create our backup plan;
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/a46e50d2-ac68-4f05-b82a-41f3e369db8c)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/fbf0a2d7-612a-4bd8-9971-1fb046c6b710)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/1bb07a4f-5194-4462-ba43-29414fa89bc7)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/cc84d9e2-64a5-479c-8a67-43e9fca6fdd4)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/7bf39a24-76ee-4478-8f6d-7eaa4d7d4050)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/b32c6bf2-ddb9-434a-a24a-e8ad5c3a6bd0)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/b6633c4e-3e6e-4a91-a0e6-4a808c450f51)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/22c375da-4d9f-4846-8609-75f8d38919df)
Let's navigate to the backup vault(default) that was selected in the backup plan and select the latest completed backup.
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/4f0d5295-a6ef-4387-b2bb-8bc0d3345c6f)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/077b1575-3e69-49c3-af65-247c6b0a7079)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/6a44e126-64c2-41da-8560-eba9bf149406)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/35278861-7a91-43d9-a992-3015fe795c29)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/b967c74f-c479-41d7-9f27-bce08fbcdd49)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/5cab4083-12b7-4d17-adac-d2baa003eaa9)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/d45f595e-da9c-4dfa-9605-5055bd229a42)
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/3106c4e9-ab9a-4e4d-bf83-41c97bd5a07b)
Let's check our RDS service;
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/577d003c-1386-45bf-8f18-72a482a9159e)
We can use the endpoint to connect to the database.
![image](https://github.com/DevSecOpsHQ/Project-3/assets/69714197/f6dd5a89-2c25-4255-87a9-48e4aa711e46)

### That's it for now. Remember to delete all the resources once you're done.
