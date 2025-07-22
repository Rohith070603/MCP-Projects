MODEL CONTEXT PROTOCOL(MCP)
MCP:- 
                       MCP, in the context of AI and large language models (LLMs), stands for Model Context Protocol. It's an open standard that allows AI systems to access external data, tools, and services in a standardized way. Think of it as a universal connector, similar to a USB port, that enables AI models to interact with the real world beyond their training data.
•	What is LLM?
       LLM stands for Large Language Model. It is a type of artificial intelligence model, specifically a subset of deep learning, that is trained on massive amounts of text data to generate human-like text and perform various natural language processing (NLP) tasks. LLMs are designed to understand, generate, and manipulate human language, enabling them to perform tasks like text completion, translation, question answering, and more. 
                        User Input => LLM=> Output 
Limitations:
	LLM’s cannot access real time or live data on their own,they only know what was in their training data.
	If we want to get the live data or the real time information we have to use,function calling with GPT model.
	We have to add all different functions for every real time information like weather etc 
This creates a messy code which leads to confusion and difficult in understanding and execution.
1.	Messy code
2.	Difficult to scale 
3.	Security Risks
4.	Hard To Maintain

In handing this Drawbacks the MCP has been used .
MCP(Model Context Protocol):
                                   MCP is an open protocol that Standardizes how applications provide context to LLMS.A protocol is a set of rules that every service or tool provides must follow when creating their MCP servers.
	MCP is like a USB-C port for Al applications. Just as USB-C Provides a standardized way to connect your devices to various Peripherals and accessories. MCP provides a standardized way to Connect Al models to different tool
MCP Architecture we have 4 components:
1.	MCP Host
2.	MCP Client
3.	MCP Servers
4.	Tools/Servers
•	MCP Host is the platform that acts as a bridge between the user and the LLM and the MCP server.
              Eg, Cursor IDE, WindSurf, Claude(Anthropic).
•	MCP Client maintains one on one connections with servers.
Eg,Internal code in the cursor IDE that communicates with MCP sservers.


 
Advantages of MCP:-
•	Instead of writing a new Function schema per service, developers deploy an MCP server that wraps the service.
•	All MCP servers - regardless of the underlying system Speaks same protocol This eliminates Fragmentation.
•	when any service updates its MEP Server with new meth Hase now methods automatically available to you, without changing your code of prompts



COMMUNICATION FLOW OF MCP:

 
1. User Prompt :-User types a question in the MCP host.
2.Ask For tools :-The MCP Host asks the MCP Server Por available tools.
3. Tool list Received :- The MCP server sends back a list of tools.
4. send to LLM :-  The MCP Host sends the users Prompt tools list to LLM.
5. LLM chooses a Tool :- LLM chooses needed tool based on the Prompt and sends back the tool name.
6. Run the tool :-MCP host makes a call to corresponding MCP Server & server returns result to MCP host.
7.Get the Result :- The MCP host sends this tool output back to the LLM and the LLM Uses it to generate final human readable format.
8 output shown





Cursor Installation:  
1.	Install Cursor AI Editor: https://www.cursor.com/downloads For Windows 


Initial Setup in Cursor IDE:
1.	Open Cursor IDE: After launching the editor, you'll be greeted with the welcome screen. 
•	Click on Skip and then Continue to proceed.
 
2.	Customize Theme:
•	Click Continue
3.	Quick Start:
•	Click Continue
4.	Data Sharing:
•	Click Continue
5.	Review Settings:
•	Click Continue

Access Cursor Settings: 1. Click on the Settings icon in the top-right corner of Cursor IDE.  
2.	Navigate to Cursor Settings.
3.	In the settings panel, click on Tools & Integrations.  


4.	Under this section, click on Add Custom MCP.  
Add a new MCP server: We will get these MCP servers from the pipedream.


Steps to Get the MCP Server URL:
1.	Go to Pipedream: Open Pipedream
2.	Create an Account: Sign up for a Pipedream account if you haven't already
3.	Search for the Tool: Use the search bar to find the tool you want to integrate (e.g., Gmail).
4.	Connect Account: Click Connect Account and authenticate the desired tool.  
5.	Copy the MCP Server URL: 
•	Select the “Cursor” Tab from the list of available MCP clients (e.g, Claude, OpenAI, Cursor, etc.)  
6.	Copy the MCP server config shown under the "Cursor" tab.Copy only the Gmail-related server
7.	Add MCP Server to Cursor IDE: 
•	Paste the MCP Configuration: 
a.	In the Cursor IDE, paste the copied MCP configuration into the MCP Servers section.
b.	Save it by pressing Ctrl + S.
URL must be your authenticated URL from Pipedream, which you had earlier copied
 
Add New MCP Services:
1.	To add a new MCP service:
•	Add a new entry in the "mcpServers" object after the last server (e.g., YouTube Data).
•	Add a comma after the last server and use the following format:
 
3. Using MCP Servers in Cursor IDE: 
Opening the AI Panel: In Cursor IDE, go to the top-right corner and click New Chat to open the AI panel (usually open by default). If it's not open, press Ctrl + Alt + B to open it.  
Examples of Instructions Using MCP Servers: You can now use different MCP servers in Cursor. Here are some example prompts:
1.	Send Email via Gmail:
•	"Send an email to my team using Gmail summarizing today's meeting notes."
2.	Get Emails from Gmail:
•	"Get the last 5 emails from my Gmail inbox and display them here."
3.	Push Code to GitHub:
•	"Push the current code to my GitHub repository with the commit message ‘MCP Integration Done".
4.	Schedule Calendar Event:
•	"Schedule a calendar event for tomorrow at 3 PM using Google Calendar."
5.	Translate Text via Email:
•	"Translate this paragraph into French and send it via email."
________________________________________
Important Notes:
•	Confidentiality: Do not share your Pipedream URLs with anyone. These URLs contain sensitive information for authenticating your MCP servers.

        
Project-1: LinkedIn Post Creation with image:-  
Project-2: Gmail
Project-3: Railway Train Schedule
Project-4: Eleven Labs
Project-5: Learning Path Generator

