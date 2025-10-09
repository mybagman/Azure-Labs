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
To develop the free tier concept I used google colab to develop, write, and run my "application". During this process there were alot of issues with the free tier API as I was trying to use Open AI, but once I switched to Gemini it started to work. The quality of report that the Gemini API produces is subpar but it proves the concept.<br />
<br />
<img src="https://i.imgur.com/PX621jm.jpeg"  height="80%" width="80%" <br />
 <br />Above is an example of the script used.<br />
<br />When The script is run it uploads a blank interview performa for the API to reference. It then prompts the user to upload a document (the interview notes). It then sends the notes to the Gemini API and once analysed it downloads a doc.x file to the users device. .<br />
<br />
<img src="https://i.imgur.com/PcnpLGM.png"  height="80%" width="80%" <br />
<br /> Above is the prompt to upload the blank interview performa.<br />
