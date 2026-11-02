Using the existing Power BI solution and Microsoft Fabric environment,
design a translytical writeback solution for operational action management.

The user must remain inside the Power BI report.

Use:

- Power BI Translytical Task Flows
- Fabric User Data Functions
- Fabric SQL Database

Do not use Power Apps.
Do not use a separate Fabric App.

Business scenario:

A store operations manager identifies an operational or inventory issue while
analyzing the report and needs to create and track a corrective action
without leaving Power BI.

The writeback experience should be directly connected to the operational
and inventory analysis context of the report.

The writeback flow should capture:

User input:
- Action
- Owner
- Status
- Due Date
- Comment

Automatically populated or context-driven where possible:
- Store
- Issue Type
- Created Date
- Created By

The solution should support creating an operational action and,
after a successful submission, refresh the report so the newly created action can become visible to the user.

Design the proposed:

- Power BI user experience
- input controls
- Data Function button behavior
- Fabric SQL Database table schema
- Fabric User Data Function parameters
- validation logic
- writeback flow
- report refresh behavior
- success feedback
- error handling

The user experience should minimize manual input wherever the information
can already be derived from report context or the authenticated user.

Implement and validate the solution end-to-end.

IMPORTANT:
Do not modify or overwrite the existing benchmark semantic model and benchmark report.

Create a separate report for the translytical implementation named:
"Store Operations & Inventory Intelligence - [AGENT] Translytical".

Do not use any solution produced by another AI agent as a reference.
