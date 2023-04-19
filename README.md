<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle</h1>
This tutorial outlines the lifecycle of a ticket in osTicket. 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- OsTicket

<h2>Operating Systems Used </h2>

- Windows 10</b> 

<h2>Prerequisetes</h2>
- Have completed part <a href="https://github.com/TimjMerida/osTicket-pt3-Post-instillation-setup/blob/main/README.md">Three</a> of the 4 part tutorial
- Be connected to the Windows VM via RDP  
- Logged into osTicket

<h2>Objectives</h2>
Our objective in the final part of this four part tuorial is to to see how a ticket will be made, triaged and closed by a agent and user. After this tutorial we will clean up our resources in Azure. 

<h2>Ticket Lifecycle</h2>


The first step in our ticket lifecycle will be to login as the admin of osTicket. We will use the admin to triage tickets for the employees and set teh SLA's for the tickets.
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232955063-07231646-344e-4564-bd1c-1a5f1eb83e1d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

</p>
<p>
To make a ticket as a user we will open a new tab and go to this link http://localhost/osTicket/. From here click open a new ticket. This would be a user either internal or a client creating a ticket for their issue.  
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232955126-ecb4be01-0183-4d6d-b0d9-22fbf125fa76.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
For the name and email put in one of the users from the last part. I will put in Gregs. For the Help topic put severe outage. For the issue summary i will put that the server is unresponsive.When done click create ticket at the bottom.  In the last part we made help topics to streamline their process. When we go back to admin we will set SLA's according to the sverity.   
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232955137-fe571b38-a9c6-4bba-81e7-474830e3b4de.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will then make another ticket as Greg again this time with the a connection issue. That issue being a different website is taking a long time to load. This will be a lower SLA as the website still works but is still impacted by a network issue.   
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232955150-c3b608d9-5712-4892-8bc6-9340c28f1437.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The last ticket we will make with Peles info. We will make this issue a low severity pasword reset. This is a common issue that is usualy not severe and will be handled by a level 1 team member.    
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232955167-63c64534-1917-453d-bac6-d94e3bd4c763.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Going back to the Admin account in osTicket. Under agent panel and tickets we should see the three newly created tickets. We will now triage them as a sys admin might in a real world senario. Click the server down ticket and we will change some settings.  
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232955183-672ed803-4117-477f-bb26-e06154727bf9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For this ticket we will change the priority to high and the SLA to SEV-A. Then we will change the department to System administrator. When you change this it will say access denied as the admin account is not the sys admin Jess that we created.  
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232955217-c620c9dd-a4c6-480a-8146-8d91d15db421.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After we will triage the slow website ticket. We will change the priority to high and the SLA to SEV-B. After we will change the department to  Network department to fix the connection issue. When we do we will no longer have access as the account we are in is not in the network department. 
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232955231-dceff127-eff8-4d84-a548-79891c3a8ffa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally we will triage the login ticket. This ticket we will update the priority to low and the SLA to SEV-C. We will not change this department. 

Next we will move on to "closing" these tickets. As these are not real issues to fix we will pretend we have fixed the issues and see how to close the ticket. 
  
Starting with the password reset as we are signed in to the support account we can respond to the ticket by saying that we have reset their password and they can now login using a new default password. On the bottom change the issue to closed and click post reply. osTicket will refresh showing our reply was posted. To check this ticket we can go to closed today and see the ticket has been closed.  
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232955334-36ca40c1-11cf-45b0-81fc-29e05cfa59b1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://user-images.githubusercontent.com/128980344/232955345-4dea89e8-3b6c-4e12-af56-991eef2ba9e3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will logout and log back in as User: Jess_Vaner Pass: Password12321 our sys admin. We will then close out the server down ticket. Open the ticket and write a response. When done click resolved issue and post reply. We can then logout and login as User: David_Bale Pass: Password12321 our network agent.  
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/232955377-93b14440-200a-4d56-b4fb-ee1f576e9094.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Simmilair to the other tickets write a response to the ticket and post a reply.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/232955376-69f169ba-7198-4896-86ed-75adaa0cb8d4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If these emails were real we could see the status by going to the other tab and clicking check ticket status. Overall we can see that a ticket gets created by a user, triaged by an agent and responded to by the correct team member. Now that we have completed the majoritry of this tutorial i reccomend playing around in osTicket to get a feel for creating tickets and making users and agents. When done you can continue this tutorial to clean up our rescources in Azure. 
</p>
<br />




<h2>Rescource Cleanup</h2>

<p>
<img src="https://user-images.githubusercontent.com/128980344/232955373-4fe22ac6-c6f8-4324-b8a2-140acc1452a0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that we are done with osTicket we can clean up our rescources. First we can disconect from our VM by right clicking and closing the windo. Then we can go to Azure.portal.com and go to the rescource group we created. 
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/232955378-5dbb6e1f-d0e0-45fd-b056-485e334610e2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We can click delete rescources and copy and paste the rescource group name into the box to confirm our deletion. When done click delete and we will delete all of the rescources for this lab. Note that it will take some time. That is the end of the tutorial. If you have any feedback or wish to contact me please leave a message or contact me on linkedin. Thank you!
</p>
<br />


