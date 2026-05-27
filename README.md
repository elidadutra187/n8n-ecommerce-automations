<p align="center">
  <strong>φ</strong>
</p>

# n8n E-commerce Automations

> Production-ready n8n workflow templates for e-commerce operations

## Overview

This repository contains a collection of n8n workflow templates designed for e-commerce operations. Each workflow has been tested in production environments processing real orders, inventory updates, and customer communications.

The templates cover common e-commerce automation needs: WhatsApp notifications, SEO content generation, marketplace synchronization, and order management.

## Stack

- **Platform:** n8n (self-hosted or cloud)
- **Integrations:** WhatsApp Business API, Claude API, Olist, Nuvemshop, Google Sheets
- **Triggers:** Webhooks, Schedules, Manual

## Workflows

### 1. WhatsApp Order Notifications

Sends WhatsApp alerts when new orders are placed.

```
Trigger: Webhook from ERP
  → Parse Order Data
  → Format Message
  → Send via WhatsApp Business API
  → Log to Google Sheets
```

**File:** `workflows/whatsapp-order-alert.json`

### 2. SEO Description Generator

Bulk generates SEO descriptions using Claude API.

```
Trigger: Google Sheets (new rows)
  → Read Product Data
  → Generate Description (Claude)
  → Write Back to Sheet
  → Mark as Processed
```

**File:** `workflows/seo-generator.json`

### 3. Marketplace Sync (Olist → Nuvemshop)

Synchronizes product catalog between marketplaces.

```
Trigger: Schedule (every 6h)
  → Fetch Olist Products
  → Transform Data
  → Upsert to Nuvemshop
  → Log Changes
```

**File:** `workflows/marketplace-sync.json`

### 4. Abandoned Cart Recovery

Triggers WhatsApp recovery messages for abandoned carts.

```
Trigger: Webhook (cart abandoned)
  → Wait 30 minutes
  → Check if Still Abandoned
  → Send Recovery Message
  → Schedule Follow-ups
```

**File:** `workflows/cart-recovery.json`

### 5. Inventory Sync

Keeps inventory in sync across multiple channels.

```
Trigger: Webhook (stock change)
  → Update All Channels
  → Send Alert if Low Stock
  → Log to Database
```

**File:** `workflows/inventory-sync.json`

## Quick Start

1. **Import Workflow**
   - Open n8n
   - Go to Workflows → Import from File
   - Select the `.json` file

2. **Configure Credentials**
   - Add your API credentials in n8n
   - Update the credential references in the workflow

3. **Customize Settings**
   - Adjust webhooks URLs
   - Modify message templates
   - Set your timing preferences

4. **Test & Activate**
   - Run manual test
   - Enable the workflow

## Project Structure

```
n8n-ecommerce-automations/
├── workflows/
│   ├── whatsapp-order-alert.json
│   ├── seo-generator.json
│   ├── marketplace-sync.json
│   ├── cart-recovery.json
│   └── inventory-sync.json
├── credentials/
│   └── credentials-template.md
├── docs/
│   ├── setup-guide.md
│   └── troubleshooting.md
├── README.md
└── LICENSE
```

## Required Credentials

| Workflow | Credentials Needed |
|----------|-------------------|
| WhatsApp Alerts | Meta Business API, Google Sheets |
| SEO Generator | Anthropic API, Google Sheets |
| Marketplace Sync | Olist API, Nuvemshop API |
| Cart Recovery | Meta Business API, E-commerce Webhook |
| Inventory Sync | Multiple marketplace APIs |

## Environment Variables

```env
# Meta/WhatsApp
META_ACCESS_TOKEN=your_token
PHONE_NUMBER_ID=your_phone_id

# Claude/Anthropic
ANTHROPIC_API_KEY=your_key

# Olist
OLIST_API_TOKEN=your_token

# Nuvemshop
NUVEMSHOP_ACCESS_TOKEN=your_token
NUVEMSHOP_USER_ID=your_user_id
```

## Best Practices

1. **Error Handling:** All workflows include error nodes
2. **Rate Limiting:** Respect API limits with delays
3. **Logging:** Log all critical operations
4. **Idempotency:** Handle duplicate triggers gracefully
5. **Secrets:** Never hardcode credentials

## Use Cases

- **Small E-commerce:** Order alerts, basic automation
- **Growing Stores:** Multi-channel sync, cart recovery
- **Marketplaces:** Catalog management, inventory sync
- **Agencies:** White-label automation templates

## Roadmap

- [ ] Shopify integration templates
- [ ] Inventory forecasting workflow
- [ ] Customer segmentation automation
- [ ] Returns processing workflow

## Author

**Élida Dutra**
Growth Engineer | E-commerce | AI Marketing Automation

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/elidadutra)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/elidadutra)

## License

MIT

---

<p align="center">
  <strong>φ</strong><br>
  <em>Building intelligent systems at the intersection of marketing, data, and AI</em>
</p>
