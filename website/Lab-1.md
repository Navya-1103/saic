---
layout: page
title: Lab 1
# permalink: /lab1/
nav_order: 2
---
# 🧑‍💼 AskHR Lab 1: Using Prebuilt Agents and Tools

Please refer to [Lab 1 Explanations](./pdfs/Lab%201-explanation.pdf) before starting.

## Objective

The **IBM watsonx Orchestrate catalog** serves as a vast repository of prebuilt AI agents and tools, tailored to address a wide array of use cases and requirements. This extensive collection helps you discover agents, tools, or a blend of both that align with your specific needs. In this lab, we will use one of the prebuilt agents to demonstrate how easy it is for a user to start the agent-building journey.

Each watsonx Orchestrate prebuilt agent and tool is connected to a service. Services require connections to be established. For this lab, we have already created the necessary connections.

### Key features of prebuilt agents include:
- **Pre-configured**: Prebuilt agents come with pre-defined settings and configurations for easy setup.  
- **Reusable**: Prebuilt agents can be used across multiple workflows, reducing the need to recreate similar tasks.  
- **Task-specific**: Each prebuilt agent is designed to perform a specific task or set of tasks, such as data processing, API calls, or notifications.  

## Discovering the Catalog

1.	From the hamburger menu on the top left corner, select “Discover”

    ![image](./imgs/lab-1/step-1.png)
2.	You will be presented with this view

    ![image](./imgs/lab-1/step-2.png)
3.	Currently, all the prebuilt agents and tools are separated into 4 domains/categories. Feel free to click on one of the categories and see what is available for you. 
4.	In this lab, we will be using prebuilt agents and tools from the HR category.

## Building an Employee Address Agent

1. Go back to the hamburger menu and click on “Discover” again if you’ve navigated away.  
2. On the search bar, search for “Employee Address” and hit Enter. Click on the Employee Address once the search result comes back.  

   ![image](./imgs/lab-1/step-6.png)  

3. Once you clicked on the Employee Address, you will be presented with this view.  

   ![image](./imgs/lab-1/step-7.png)  

4. You will be able to see what this agent is doing, the tools it is using. From this page, we will be able to assess if this agent is suitable for your use case.  
5. To use this agent, click on the “Use as template” button on the top right.  

   ![image](./imgs/lab-1/step-9.png)  

6. You will be presented with the Agent Builder page.  

   ![image](./imgs/lab-1/step-10.png)  

7. Edit the name so that it is unique. Change the agent’s name to `[Your Initial]_Employee Address` and save.  

   ![image](./imgs/lab-1/step-11.png)  

8. Keep the rest of the agent set up as it is and let’s try the agent.  
9. In the “Preview” panel on the right, let’s try one query. 

```
Update my address
```
   ![image](./imgs/lab-1/step-13.png)  
10. If you face any problem with step 9, please alert one of your friendly instructors.  
11. Prebuilt agents present an easy way to build an agent. However, we can also edit the prebuilt agent. Let’s try to add an extra tool into the agent.  
12. Scroll down to the toolset and click on “Add tool”.  
   ![image](./imgs/lab-1/step-16.png)  
13. Click on “Add from catalog”.  
   ![image](./imgs/lab-1/step-17.png)  
14. On the search bar, type in “Personal Details”. Select “Get personal details in SAP SuccessFactors” from the search result.  
   ```
   personal details
   ```
 Select “Get personal details in SAP SuccessFactors” from the search result.  
   ![image](./imgs/lab-1/step-18.png)  
15. After you click on the tool, you will be able to see the input and output the tool is expecting. Once you’re ready, click on “Add to agent” on the bottom right.  
   ![image](./imgs/lab-1/step-19.png)  
16. Once returned to the agent builder page, you will see the additional tool added to the tools list.  
   ![image](./imgs/lab-1/step-20.png)  
17. After building the agent, we can deploy our agent. Click the “Deploy” button on the top right. Keep all default settings when being asked.  
   ![image](./imgs/lab-1/step-21.png)  
18. Once the deployment is ready, navigate to “Chat” from the left-hand hamburger menu.  
19. From the dropdown menu, select your agent.  
   ![image](./imgs/lab-1/step-23.png)  
20. Let’s try out the agent. Here are some queries you can use:  
 a.  
 ```
 Get personal details for Jamie Tan
 ```
   ![image](./imgs/lab-1/step-24a.png)  
 b.  
 ```
 Update my address
 ```  
 When asked, you can use any address type, address, city, and any start date.  
 Country code must be **SGP**. As an example, you can put in:  
 ```
 mailing
 ```
 ```
 205 ABC St 46 02-576 778225 SGP
 ```
 ```
 today
 ```  
 ```
 Singapore
 ```

 ![image](./imgs/lab-1/step-24b.png)  

 If you are asked to input an email address, use 
 ``` 
 jamie.tan@bestrun.sg  
 ```
 ![image](./imgs/lab-1/step-24-b-2.png)  

 If asked for confirmation, input:  
 ```
 yes
 ```
 

## **Conclusion**

The above practice is to demonstrate the ease to build an agent using prebuilt templates and to edit the agent with extra tools or external documentation to help with the agent’s answer.
