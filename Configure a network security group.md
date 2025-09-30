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
<br /> I then Associated the network Security group to the Subnet on the Vnet. This was done through the Network security group<br/>
<br />
<img src="https://i.imgur.com/usW5zVN.png" height="80%" width="80%" <br /> 
<br />
<br />I then associated the application security group to the resource group on the Linux virtual machine we are using. This was done trough the virtual machine .<br />
<br />
 <img src="https://i.imgur.com/7MXUZtr.png"  height="80%" width="80%"<br />
 <br />
<br />
<br />
From here I tried connecting to the Linux virtual machine through cloud shell. The request timed out as the network security group did not have an incoming rule to allow SSH<br/>
<br />
<br /> <img src="https://i.imgur.com/y0198OS.png"  height="80%" width="80%" <br />
<br />
<br />I then created an Inbound Rule to allow SSH traffic<br />
<br />
-<br /><img src=https://i.imgur.com/1h4gylR.png"  height="80%" width="80%" <br />
 <br />
<br /> The last thing I did was to test the connection to confirm that the Inbound rule was active.<br />
<br />
<br /><img src="https://i.imgur.com/zmr9ihE.png"80%" width="80%"<br /> 
<br />
<br />
End<br/>

