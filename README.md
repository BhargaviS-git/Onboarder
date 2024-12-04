# Onboarder
Onboarder Automator

Onboard Automator (Manage Azure identities and governance)
Azure Services Used:
Azure AD
Azure Logic Apps
Azure Email Service (part of Logic Apps connector)
Azure Resource Manager

Steps:
Azure AD Setup
1.	Sign in to the Azure Portal
2.	Navigate to Azure Active Directory
3.	Create a New Directory
4.	Fill in the New Tenant Information
5.	Create the Directory
6.	Access the New Azure AD Instance
7.	Switch Between Directories

Logic App Workflow Design
1.	Create a New Logic App
2.	Configure the Trigger for the Workflow
3.	Send Welcome Email to New Employee
4.	Notify HR or Other Relevant Teams
5.	Complete the Workflow and Save

Azure AD User Creation:
1.	Create a New Logic App
2.	Add the Trigger for the Workflow
3.	Add an Action to Create the New User in Azure AD
4.	Optional: Send a Welcome Email
5.	Optional: Send a Welcome Email
6.	Add Action to Notify HR (Optional)
7.	Save and Test the Logic App
8.	Monitor and Troubleshoot

Role and Group Assignment:
1.	Create the Logic App
2.	Add Conditions to Assign Roles and Groups
3.	Assign User to a Group Based on Job Title or Department
4.	Assign Roles Based on Job Title
5.	Example of Logic App Workflow
6.	Save and Test the Logic App

Resource Provisioning:
1.	Create the Logic App Workflow
2.	Add ARM Connector to Provision Resources
3.	Provisioning Resources Using the Azure Resource Manager (ARM) Connector
4.	Assign Specific Permissions or Roles to the New User
5.	Notify the Employee or Team
6.	Test and Monitor

Welcome Email:
1.	Create the Logic App
2.	Add the Email Connector
3.	Dynamic Content in the Email
4.	Add Conditions or Additional Customizations (Optional)
5.	Save and Test the Logic App

Monitoring and Review:
1.	Monitor Logic Apps Run History
2.	Monitor Azure AD Logs
3.	Best Practices for Monitoring and Review
4.	Troubleshooting Tips
