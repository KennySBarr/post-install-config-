<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Configuration Steps</h2>

<h3>Step 1: Open osTicket and Log In

- Log in to osTicket using the credentials you made during the installation tutorial </h3>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/34adbb25-cbad-4129-9c91-714fb43099f2)

</p>
<p>



<h3>Step 2: Configure Roles </h3>

- Make sure you are in the Admin panel (check the top-right of the screen to see which panel you are in)
- Select the Agent tab > Roles > Add New Role
	- Name: Supreme Admin
	- Select Permissions tab and check every box under the "Tickets," "Tasks," and "Knowledgebase" sections
- Select Add Role

<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/a4637917-6b33-4005-a245-1da22191b536)


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/2c3add14-3a0f-450b-8253-7f6977eaf0fe)

</p>
<p>

<h3>Step 3: Configure Departments</h3>

- Ensure you are still in the Admin panel
- Select the Agent tab > Departments > Add New Department 
	- Name: System Administrators
- Select Create Department

<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/1e26f96f-20b9-4ea3-a33c-db2536afa208)

</p>

<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/2377ec77-cda2-4013-a3d3-d98c2407389b)

</p>

<h3>Step 4: Configure Teams
</h3>

- Select the Agent tab > Teams > Add New Team
	- Name: Level II Support 
- Go to the Members tab and select yourself in "Select Agent" dropdown menu
- Select Create Team


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/5a83accb-20fc-4088-8274-6e9d2ec0129b)

</p>

<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/9beae983-4103-47ed-b6a2-19e3e534c3ec)

</p>

<h3>Step 5: Allow Anyone to Create Tickets</h3>

- Select Settings > User Settings
	- Make sure the following box is unchecked: 
		- Registration Required: Require registration and login to create tickets


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/fd4cb0df-15f8-49ec-93f6-4959aa232464)

</p>

<h3>Step 6: Configure Agents</h3>

- Select the Agent tab > Add New Agents
	- Name: Jane Doe
	- Email : jane.doe(@)osticket.com
	- Username: jane.doe
	- Click Set Password and uncheck the box that says "Send the Agent a Password Reset Email"
		- Set your password to anything you like
		- Uncheck the box that says "Require Password Change at Next Login"
		- Select set


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/3cebc688-9785-4a20-a779-f5b17262a7d3)

</p>

<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/e05b9c64-d8ff-4afc-86dd-31351b3fc04e)

</p>


- Select the Access tab 
	- Under Primary Department: 
		- Select the Department dropdown menu > System Administrators
		- Select the Role dropdown menu > Supreme Admin
	- Extended Accesss 
		- Select Department > Support > Add > Supreme Admin
- Select Team tab
	- Select Team dropdown menu > Level II Support
	- Select Add
- Select Create	


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/657e1c69-9185-45d4-a2cd-35533c3c6435)

</p>

<p>

![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/0dfe36fd-2062-488d-91d5-8cb66cfe1601)

</p>

- Create another agent and replace Jane with John.
	- Follow the same steps as above, except make some changes to the Primary Department
		- Select the Department dropdown menu > Support
		- Select the Role dropdown menu > View Only
	- Extended Accesss 
		- Select Department > Support > Save Changes

<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/71e75d81-7d99-4024-89c4-dc9a534b7b17)

</p>

<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/aac9b0f1-fe88-4b6c-a895-d6bd41a8a40d)

</p>

<h3>Step 7: Configure Users
</h3>


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/29b37ae6-a54a-4c4c-bd5d-a0c0dafe13a6)

- Select the Users tab to create a user
	- Email Address: Karen(@)osticket.com
	- Full Name: Karen Karen
	- Select Add User

</p>


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/9f215245-2b8b-473e-8201-f980b44cfd7e)

</p>

 - Select the User tab again to create another user
	- Email Address: Ken(@)osticket.com
	- Full Name: Ken Ken
	- Select Add User


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/0faf36bd-9c3c-4a4c-ae6f-66cf8feda0b3)

</p>

<h3>Step 8:  Configure Service Level Agreements (SLA)
</h3>

- We will create three SLAs
- Select the Manage tab > SLA > Add New SLA Plan
	- Name: SEV-A 			
	- Grace Period: 1
	- Schedule dropdown menu: 24/7
	- Select Add Plan


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/d02aca6a-8d83-4131-8f24-fb897ac94d83)

</p>

<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/53078c6b-43ca-4cf9-ae88-8f4ba4b8856c)

</p>

- Name: SEV-B
	- Grace Period: 4
	- Schedule dropdown menu: 24/7
	- Select Add Plan


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/7ff6524a-f357-46eb-8e8f-49c6ad6e7cd8)

</p>

- Name: SEV-C 
	- Grace Period: 8
	- Schedule dropdown menu: Monday - Friday 8AM - 5PM with U.S. Holidays
	- Select Add Plan


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/c15e3be5-8c2a-4766-9a19-37951ccb5786)

</p>

<h3>Step 9:   Configure Help Topics
</h3>

- We will create four Help Topics
- Select the Manage tab > Help Topics > Add New Help Topic
	- Business Critical Outage
	- Personal Computer Issues
	- Equipment Request
	- Password Reset
- Select Add Topic for each topic


<p>
  
![image](https://github.com/JustinPeguero/post-install-config/assets/170198869/bf590b18-3ab5-4219-b5d2-f51912eeeaf0)





