---
layout: page
title: Lab 4
# permalink: /lab4/
nav_order: 5
---
🧑‍💼 AskHR Lab 4: MCP Server
=================================================================================

This lab will teach you how you can import external tools from Model Context Protocol (MCP) servers and add them to your agents to enhance the agent's ability to accomplish tasks.

We will build an agent that uses Tavily connection to build a search training courses agent that can help employees find latest courses for their job roles.

Please refer to instructor's guidance on how to get Tavily API key.

Once you have completed this lab you will have developed skills enabling you to complete the following tasks:

*   Installing servers requiring environment variables.
*   Creating and configuring a connection.
*   Import a tool from an MCP server

Step-by-step instructions
=========================

**a) Create the tavily connection**

To connect to the Tavily server with your credentials, you must create a new connection in watsonx orchestrate. This is the most secured way to import tools not displaying your API keys and credentials publicly.

1.  Click the Main menu icon (A).

    ![image](./imgs/lab-4b/step-1.png)

1.  Expand the Manage menu (A) then select Connections (B)

    ![image](./imgs/lab-4b/step-2.png)

1.  Click Add new connection (A).

    ![image](./imgs/lab-4b/step-3.png)

1.  Enter Tavily_MCP in the Connection ID* field (A), click Save and continue (B).

    ![image](./imgs/lab-4b/step-4.png)

1.  Expand the Choose an option in the Authentication type menu (A).

    ![image](./imgs/lab-4b/step-5.png)

1.  Select Key Value Pair (A).

    ![image](./imgs/lab-4b/step-6.png)

1.  Type TAVILY_API_KEY in the Key name field (A), copy your Tavily API key from your note in the Value field (B), Click Connect (C).

    ![image](./imgs/lab-4b/step-7.png)

1.  Check that your draft connection is Connected (A), Click Next (B)

    ![image](./imgs/lab-4b/step-8.png)

1.  Repeat from Step 5 and add the credentials for the Live environment.

    ![image](./imgs/lab-4b/step-9.png)

1.  Click Add connection (A) when done.

    ![image](./imgs/lab-4b/step-10.png)

1.  Click Confirm (A).

    ![image](./imgs/lab-4b/step-11.png)

1.  Check that your connection is now ready (A), both draft and live environments will have access to your credentials in a secured way. Click the top menu (B)

    ![image](./imgs/lab-4b/step-12.png)

**b) Using Local MCP servers to run tools**

Next, you must create a new agent. This new agent will contain the Taviliy search tool you will import from the Tavily MCP server. The connection to the Tavily server will be managed through the connection you have created in the previous step.

1.  Click the Build menu (A).

    ![image](./imgs/lab-4b/step-13.png)

1.  Click Create agent (A).

    ![image](./imgs/lab-4b/step-14.png)

1.  Type the following:
    Name: \[Your Initials\]\_employee\_courses\_agent
    Description:
    ```
    This agent uses the Tavily search tool via MCP to help employees discover relevant online courses and learning resources based on their job role and skill gaps. It searches the web in real time to surface up-to-date training recommendations tailored to each employee's needs.
    ```
    ![image](./imgs/lab-4b/step-15.png)

**c) Configure an MCP Server**


1.  Click Add tool (A).

    ![image](./imgs/lab-4b/step-16.png)

1.  Click MCP Server (A).

    ![image](./imgs/lab-4b/step-17.png)

1.  Click Add MCP server (A).

    ![image](./imgs/lab-4b/step-18.png)

1.  Select Local MCP server (A), click Next (B).

    ![image](./imgs/lab-4b/step-19.png)

1.  Type 'Tavily' in the Server name (A), type 'Tavily server created for the wxO L4 labs' in the Description (B), expand the Select Connection drop down (C).

    ![image](./imgs/lab-4b/step-20.png)

1.  Select your Taviliy_MCP from the list (A).

    ![image](./imgs/lab-4b/step-21.png)

1.  Type the following in the command field (A) then click Import (B).
    ```
    npx -y tavily-mcp@0.1.3
    ```

    ![image](./imgs/lab-4b/step-22.png)

**d) Select the tools to import from the MCP server**

1.  Identify the taviliy_search tool (A) then click Add to agent (B).

    ![image](./imgs/lab-4b/step-23.png)

1.  Note that the Taviliy search tool is now added to your own tools (A). Taviliy is an advanced web search tool. More parameters can be specified in addition to the default search query. Click the option menu icon (B).

    ![image](./imgs/lab-4b/step-24.png)


**e) Preview the tool within your agent**

Your tool is now ready to be used in your agent. Let's use watsonx Orchestrate preview to play with it.

1.  Click the Preview button to test your agent.

1.  Type 'What are the top 3 courses for ai engineers?' in the chat area and press Enter.
    ```
    What are the top 3 courses for ai engineers?
    ```

1.  Expand Show reasoning (A)

    ![image](./imgs/lab-4b/step-25.png)

1.  Expand Step 1 (A)

    ![image](./imgs/lab-4b/step-26.png)

1.  Review the reasoning steps showing the agent's decision-making process.

    ![image](./imgs/lab-4b/step-27.png)

1.  View the final synthesized response with information about MCP servers. Feel free to play around with the behaviour of the agent by changing the prompt.

**Congratulations! You've successfully integrated an MCP server tool into your agent and tested it with a real query.**