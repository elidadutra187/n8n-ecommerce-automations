# n8n E-commerce Automations

**Workflow templates and automation logic for e-commerce operations using n8n, APIs, WhatsApp and structured data.**

This repository documents automation patterns for online stores, marketplaces and commercial operations that need to reduce manual work between orders, customer service, catalog updates and internal alerts.

Repository: [elidadutra187/n8n-ecommerce-automations](https://github.com/elidadutra187/n8n-ecommerce-automations)

---

## Business problem

E-commerce operations often depend on repetitive manual routines: checking orders, sending internal alerts, updating spreadsheets, following up with customers, organizing product data and monitoring operational status.

When these tasks are handled manually, teams lose time, information becomes fragmented and commercial opportunities are harder to track.

This project organizes reusable automation flows to connect **e-commerce, CRM, WhatsApp, spreadsheets, APIs and internal operations**.

---

## What it does

The repository proposes n8n workflows for common e-commerce needs:

- order alerts;
- WhatsApp notifications;
- customer follow-up;
- product/catalog updates;
- marketplace and store synchronization;
- operational logging;
- low-stock or status alerts;
- SEO content support through AI integrations.

---

## Stack

- **n8n** for workflow automation
- **Webhooks** for real-time triggers
- **REST APIs** for integrations
- **WhatsApp Business** for operational and customer messages
- **Google Sheets / structured tables** for logs and review
- **Claude API / AI tools** for content workflows when needed
- **E-commerce platforms** such as Nuvemshop, marketplaces and ERP systems

---

## Workflow examples

### 1. Order alert flow

```text
New order / ERP event
→ Parse order data
→ Format internal message
→ Send WhatsApp alert
→ Log status
```

### 2. Product content workflow

```text
Product row added
→ Read product data
→ Generate or validate SEO description
→ Write result back to review table
→ Mark as ready for publishing
```

### 3. Marketplace synchronization logic

```text
Scheduled trigger
→ Fetch product data
→ Normalize fields
→ Compare catalog status
→ Update destination system
→ Log changes and errors
```

---

## How it works

Each workflow is built around a simple operational principle:

1. receive an event or scheduled trigger;
2. normalize the data;
3. decide the next action;
4. send information to the right channel;
5. log the result for follow-up.

This makes the automation easier to audit and safer to adapt for different businesses.

---

## Use cases

- Small e-commerce teams that need operational alerts
- Stores using WhatsApp as a sales or support channel
- Marketplace sellers handling catalog updates
- Teams that want to connect ERP, CRM and marketing tools
- Marketing operations teams that need repeatable workflows

---

## Expected impact

- Less manual checking
- Faster response to commercial events
- Better visibility across orders and leads
- More reliable internal communication
- Easier scaling of e-commerce operations
- Stronger connection between marketing, sales and operations

---

## Status

Portfolio case / workflow library.

This project represents practical **Marketing Operations and E-commerce Automation** work, connecting tools, data and processes to improve efficiency.

---

## Author

**Élida Dutra**  
Growth · E-commerce Ops · CRM · Automation · AI Workflows

[LinkedIn](https://www.linkedin.com/in/elidadutra) · [GitHub](https://github.com/elidadutra187)
