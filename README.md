# Intuz — Your automation partner, one workflow at a time.

<p align="center">
  <picture>
    <img alt="Banner Image" src="https://github.com/user-attachments/assets/210f97fc-0fce-404a-b647-7dfe1302cd37" />
  </picture>
</p>

# Automate QuickBooks customers & sales receipts generation from a Google Sheet

Intuz helps organizations orchestrate AI, automation, and enterprise systems through scalable workflows. Our repository showcases proven implementations across healthcare, operations, customer support, document processing, sales, and back-office functions, enabling teams to accelerate automation initiatives without starting from scratch

[N8N Creator](https://n8n.io/creators/intuz/) · [AI Agent Development Company](https://www.intuz.com/ai-agents-for-business-automation/) · [n8n Workflow Automation](https://www.intuz.com/workflow-automation-services/) · [For Custom Workflow Automation](https://www.intuz.com/get-started/)

---

This n8n template from [Intuz](https://www.intuz.com) provides a complete and automated solution to streamline your sales and accounting process.

Simply add new transaction details to a designated Google Sheet, and this workflow takes over. Using specific status keywords in a column to trigger the process, it automatically creates new customer profiles and generates sales receipts in QuickBooks. This creates a complete, end-to-end system from a simple spreadsheet entry to a formal accounting record, eliminating manual data entry.

## How it works

This workflow streamlines the process of recording sales from a Google Sheet into QuickBooks Online, intelligently handling both new and existing customers.

### 1. Trigger on New Row

The workflow starts automatically whenever a new row is added to your specified Google Sheet.

### 2. Check for Existing Customer

It takes the customer’s name from the new row and searches your QuickBooks account to see if a customer with that `DisplayName` already exists.

### 3. Conditional Logic (IF Node)

Based on the search result, the workflow splits into two paths:

- **If Customer Exists (True Path):** The workflow proceeds directly to create a Sales Receipt, linking it to the existing customer’s ID found in the search.
- **If Customer Does Not Exist (False Path):** The workflow first creates a new customer in QuickBooks using the name and email from the sheet. It then uses the ID of this newly created customer to generate the corresponding Sales Receipt.

## How to Use: Quick Start Guide

### 1. Prepare Your Google Sheet

Make sure you have a Google Sheet with clear headers for your sales data. The template is configured for the following columns:

- `CustomerName`
- `Email`
- `Amount`
- `Quantity`

### 2. Import the Template

Click the **"Use Template"** button to import the workflow into your n8n instance.

### 3. Configure Google Sheet Node

- Enter the **Spreadsheet ID** from your Google Sheet’s URL.
- Enter the **Sheet Name** where your sales data is located, such as `Sheet1`.

### 4. Configure the QuickBooks Nodes

- Select your QuickBooks Online credential or create a new one for the following nodes:
  - **Search for Customer**
  - **Create Receipt for EXISTING Customer**
  - **Create New Customer**
  - **Create Receipt for NEW Customer**
- **Important:** In both **Create Receipt** nodes, you must provide a valid Product/Service ID from your QuickBooks account. Find this in the node parameters under **Line > Sales Item Line Detail > Item Ref > Value**.

### 5. Activate the Workflow

Save your changes and activate the workflow. Now, every new row you add to the Google Sheet will automatically create the necessary records in QuickBooks.

## Key Requirements to Use Template

- An active n8n instance.
- A Google account with a prepared Google Sheet.
- A QuickBooks Online account.
- A QuickBooks Developer account to obtain the API credentials needed to connect to n8n.
- At least one Product or Service item set up in your QuickBooks account to be referenced in the sales receipts.

## Connect with us

- **Website:** https://www.intuz.com/n8n-workflow-automation-templates/
- **Email:** getstarted@intuz.com
- **LinkedIn:** https://www.linkedin.com/company/intuz/
- **Get Started:** https://n8n.partnerlinks.io/intuz
- **For Custom Workflow Automation:** https://www.intuz.com/get-started/
