<h1>AI Report Generation</h1>

<h2>Problem</h2>
- Report writing for candidate interviews is one of many things that a recruiter must do. It takes alot of hours to write reports, which may mean that recruiters are working longer hours or having to prioritise writing reports over other processing, or attraction opportunities. This could lead to missing targets, poor candidate experiences, or recruiter burnout. <br />

<h2>Solution</h2>
- Create a AI interview report generator that is embedded into SalesForce which is easy to use, intergrates into existing workflows, and keeps candidate information private and secure. It will also produce objectional scoring, with clear, and concise section summarys, which still remain editable.<br />

<h2>Steps</h2>

1. Develop free tier concept using google colab, and Gemeni API's.<br />
2. Demonstrate to Manager, Gain access to salesforce.<br />
3. Develop Application with salesforce intergration.<br />
4. Test Application and work through bugs.<br />
5. Deploy Application for use in the wider organisation.<br />

<h2>Results</h2>
- Increased Efficiency: 100's of hours saved for recruiters.<br />
- Increased Output: Recruiters can spend more time in other functions such as attraction and mentoring.<br />


<h2>Tools Used </h2>

- <b>Google Colab</b>
- <b>Gemini API</b>
- <b>SalesForce</b>

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

