<h1>Azure Network Security Group</h1>

<h2>Problem</h2>
Needed a solution that would keep servers secure while still making it easy for administrators to log in.<br />

<h2>Solution</h2>
- Created an Application Security Group(ASG), which allowed me to group the virtual machines for easier management.<br />
- Created a security group for the network, controlling the traffic allowed in and out.<br />
- Linked the network security group to the subnet so that everything can follow the same rules.<br />
- Linked the network security group to the virtual machine's network card so rules apply to the server.<br />
- Added a rule that only allows secure shell (SSH) traffic from trusted sources, blocked everything else.<br />

<h2>Results</h2>
- Better security: Only trusted connections can reach the servers.<br />
- Less Manual work: automated rules for servers even when adding more.<br />
- Cost Savings: reduction in outages and security breaches.<br />


<h2>Tools Used </h2>

- <b>Azure</b>
- <b>Linux Virtual Machine</b>
- <b>Cloudshell</b>

<h2>walk-through:</h2>

<p align="center">
First I created two security groups in Microsoft Azure.<br />
<br />
<img src="https://i.imgur.com/wRz0ApG.png"  height="80%" width="80%" <br />
<br />An application Security Group.<br />
<br />
<img src="https://i.imgur.com/6Pz8rP0.png"  height="80%" width="80%" <br />
<br />
And a network Security Group.<br />
<br /> Once I had signed in with my IAM account I could start the task actual. Which begun by creating a DynamoDB table. To do this I navigated to DynamoDB using the AWS console, created a table, selected a name, and Partition key. As I am using a free teir I inspected the cost calculator. I turned off auto scaling for the read/write capacity this will ensure my account stays within the free teir limits.<br/>
<br />
<img src="https://i.imgur.com/g0UKGkh.png"  height="80%" width="80%" <br /> 
<br />
<br />I then created an item, gave it a name, and gave it an attribute.<br />
<br />
 <img src="https://i.imgur.com/5CHoY9K.png"  height="80%" width="80%"  
 <br />
<br />
<br />
From here I opened up CloudShell and ran a script to automate table creation. I created 4 different tables with different names, attributes, and one with a sort key<br/>
<br />
<br /> <img src="https://i.imgur.com/ND0g1NZ.png"  height="80%" width="80%" <br />
<br />
<br />I then confirmed that these tables were created by running a wait command in cloud shell. I went back to the console.<br />
<br />
-<br /><img src="https://i.imgur.com/cl2hre1.png"  height="80%" width="80%" <br />
 <br />
<br /> To populate the tables with data I used cloudshell to download and unzip a file that contained data for my tables. I used batch-write-item cmd to insert multiple items into the tables.<br />
<br />
<br /><img src="https://i.imgur.com/1TjHlSa.png"  height="80%" width="80%"<br /> 
<br />
<br />
I then had alook at the tables in the console adjusted some attributes. To end I deleted all the content in this project using cloudshell<br/>
<br /><img src="https://i.imgur.com/mFiYohf.png"  height="80%" width="80%" <br />
<br />
 <br /> End<br />
<br />

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
