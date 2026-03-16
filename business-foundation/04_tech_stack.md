# Technology Stack

---

## Core Platform

**n8n (self-hosted on Hetzner)**

Why:
- You already have it running
- Full control (no vendor lock-in)
- Integrations with 400+ apps
- Can build complex workflows
- Affordable at scale

Setup:
- Domain: Already configured
- Backup: Regular backups of workflows & data

---

## Essential Integrations (Priority Order)

### Tier 1: Most Common for SMBs
These cover 80% of initial client projects:

1. **Google Workspace** (Sheets, Gmail, Drive, Calendar)
   - Why: Every SMB uses it
   - Use: Data sync, email triggers, file automation

2. **CRM Systems**
   - Pipedrive (most common SMB choice)
   - HubSpot Free Tier (if clients use it)
   - Brevo/Sendinblue (email + CRM combo)
   - Why: Lead handling, follow-up automation

3. **Webhooks & HTTP**
   - Why: Connect custom systems, form submissions
   - Example: Contact form → CRM → Email

4. **REST APIs** (generic)
   - Why: Adapt to any system via direct API calls
   - Example: Custom databases, smaller tools

### Tier 2: High-Value When Needed
Use after first 2–3 clients:

5. **Email Platforms**
   - Brevo, Mailchimp, ActiveCampaign
   - Why: Bulk campaigns, follow-up sequences

6. **Accounting Software**
   - Sevdesk, FastBill (Austrian/German focus)
   - Why: Invoice automation, expense tracking

7. **Document Generation**
   - Google Docs API, Pdfshift
   - Why: Auto-create proposals, contracts, invoices

8. **Communication**
   - WhatsApp Business API (via n8n)
   - Telegram, Slack
   - Why: Client notifications, team alerts

### Tier 3: Nice-to-Have
Only implement if specific client needs it:

9. **Payment Processors** (Stripe, PayPal)
10. **Project Management** (Asana, Monday.com, Trello)
11. **Social Media** (Facebook, LinkedIn via API)
12. **Calendar Sync** (Calendly, Google Calendar)

---

## AI Integration Strategy

**When to use AI (real value only):**

✅ **Do:**
- AI node in n8n for email classification (spam filter)
- Summarize customer feedback automatically
- Generate follow-up email templates (for approval)
- Extract data from unstructured text
- Smart lead scoring

❌ **Don't:**
- Use AI just because it's cool
- Overkill for simple rules-based logic
- Expensive token usage for small workflows

**Tool:** Claude API via n8n (when needed)

---

## Infrastructure

**Hosting:**
- n8n: Hetzner VPS (already running)
- Database: PostgreSQL (local)
- Backups: Weekly automated

**Domain & Security:**
- SSL certificate (automated via Let's Encrypt)
- Basic auth for n8n dashboard
- API keys stored securely in n8n

---

## Development Tools

**You'll also use:**
- **JSON:** For API payloads & data structures
- **Regular expressions:** For data cleaning
- **Cron syntax:** For scheduling workflows
- **SQL (optional):** Advanced data filtering if needed

**Optional but helpful:**
- Postman (test APIs before n8n)
- VS Code (edit configs, small scripts)
- Git (version control workflows—later)

---

## What NOT to Buy/Build (MVP Phase)

❌ Custom website with complex features
❌ Mobile app
❌ Custom CRM
❌ Complex database infrastructure
❌ Expensive software licenses

**Why:** Bootstrap business, focus on core service (automation).

---

## Scaling Checklist (After First 3 Clients)

- [ ] Performance: Are workflows running slow?
- [ ] Reliability: Any errors or missed triggers?
- [ ] Cost: Is Hetzner VPS still sufficient?
- [ ] Documentation: Can clients understand their workflows?
- [ ] Backup: Is data actually being backed up?

If any "no," fix before taking on more clients.
