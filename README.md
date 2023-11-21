<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://youtu.be/HBvswnch3g0)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Create Roles
- Create Departments
- Create Teams
- Create Agents
- Create Users
- Create SLAs
- Create Help Topics
<h2>Configuration Steps</h2>

<p>
<img src="https://files.catbox.moe/w17ih2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First things first: go to your osTicket agent login. The url should be http://localhost/osTicket/scp/login.php You will need to use the username and password you created in the installation process.

</p>
<br />

<p>
<img src="https://files.catbox.moe/rc52im.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once logged in, you will be greeted by this screen. Take note of all the options available to you here, and don’t hesitate to familiarize yourself with each of them.

</p>
<br />

<p>
<img src="https://files.catbox.moe/ps3215.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To start: We will be configuring roles. You can find more about roles here -> https://docs.osticket.com/en/latest/Admin/Agents/Roles.html . Go to the Admin Panel>Agents>Then Roles. You will see there are default roles already, but we will make a new one. 

</p>
<br />

<p>
<img src="https://files.catbox.moe/sainqn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click add a new role. You can name this role whatever you’d like, for this tutorial I will be naming it “Super Admin”.

Click over to the Permissions tab, and give them permissions for everything labeled under “Tickets”, “Tasks”, and “Knowledgebase” Now we have a role with capabilities to do and use everything osTicket has to offer.

</p>
<br />

<p>
<img src="https://files.catbox.moe/grubo9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

With roles out of the way, we will now be able to create a department. Admin Panel>Agents>Departments. Once more you will see some default departments, but we will be making a new one again.

</p>
<br />

<p>
<img src="https://files.catbox.moe/0dppbr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Add a new department, you can name it whatever you’d like but for the purposes of this lab I will be using “System Admins”.

Now that we have named it, you will see several different options available. Most importantly is one named “SLA”. We have not created any custom SLA’s yet but it is important to make note of.

After looking through the options, go ahead and create the department.</p>
<br />

<p>
<img src="https://files.catbox.moe/37jk1c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next up: Is making a Team. Admin Panel>Agents>Teams. As usual, there will be defaults, but we will make a new one.

</p>
<br />

<p>
<img src="https://files.catbox.moe/92f3dm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can name this team whatever you’d like. For this lab I will use the name “Level II Support” just to keep things simple.

When selecting team leads or members, we do not have any agents created yet - outside of our initial admin account. You should go ahead and add yourself to this team for now.

</p>
<br />

<p>
<img src="https://files.catbox.moe/d8dhdz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
What we want to do next, is give anybody the ability to submit a ticket. Admin Panel>Settings>User Settings.
Make sure the box labeled “Require registration and login to create tickets” is unchecked. Save changes and move on.
</p>
<br />

<p>
<img src="https://files.catbox.moe/eac8v0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will create some agent profiles that will be able to work tickets for us. Admin Panel>Agents>Add New
</p>
<br />

<p>
<img src="https://files.catbox.moe/9myed9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can name these admins whatever you’d like. The names of actual employees, famous movie characters, a cartoon, whatever. To keep things simple I will go with “Jane Doe” and “Jack Doe”

Same goes for the email as well as username. Anything is fine, but it is IMPORTANT that you remember the information you put in otherwise the account will be inaccessible to you or whoever needs to use it.

When setting a new password, uncheck both “send the agent a password reset email” and “require password change at next login”
</p>
<br />

<p>
<img src="https://files.catbox.moe/v2miee.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With login credentials created, it is now time to configure Access and Permissions. Under the “Access” Tab you will see the ability to select a department as well as a role. Fill in both of these with the respective department and role we created earlier. Give this first Agent Extended Access to all departments.
</p>
<br />

<p>
<img src="https://files.catbox.moe/s5nhaq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For this tutorial we will be leaving Permissions as default.

Under Teams, once again assign this agent to our earlier created team.


For the second agent, try putting them in one of the default departments like “Support” with the role “View Only” for the purpose of familiarizing yourself with the different access levels and their effects.
</p>
<br />

<p>
<img src="https://files.catbox.moe/wwwix3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will need to make some users. Users are the people who will actually be using osTicket to create and send tickets or requests. This time we will need to switch to the AGENT panel. Agent Panel>Users>Add New

Like with the agents the email, phone number, and name can be whatever you’d like. For the sake of simplicity: I will go with “Karen” and “Ken” in this tutorial.

</p>
<br />

<p>
<img src="https://files.catbox.moe/qhqydm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After that, we will configure SLAs. A simple description of what an  SLA (Service Level Agreement) is, you can basically think of it as a time limit for how long a ticket is active or a deadline.

Return to the Admin Panel. Admin Panel>Manage>SLA.

We will create 3 SLA’s. Sev-A, Sev-B, Sev-C.

When creating your first SLA, you will notice several options. Most importantly the grace period, and the schedule. The schedule dictates what days something needs to be addressed. For example, if something is scheduled 24/7 it doesn’t matter what day of the week it is, it needs to be handled. The grace period is the amount of time (usually hours) a particular ticket needs to be fixed within. Something sent at 10 with a 1 hour grace period must be done at 11 and so on.

SEV-A (1 Hour, 24/7)
SEV-B (4 hours, 24/7)
SEV-C (8 hours, business hour schedule)

</p>
<br />

<p>
<img src="https://files.catbox.moe/u1q942.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally we will create some Help Topics. Help Topics serve to help easily categorize issues that your users may be experiencing and sending tickets for. Things like Password Resets or Equipment Requests. Admin Panel>Manage>Help Topics

There are already a few default help topics. Add some new ones.
 
	>Business Critical Outage
	>Personal Computer Issues
	>Equipment Request
	>Password Reset
</p>
<br />

