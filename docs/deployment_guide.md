# 🚀 Upwork Client Handoff & Setup Manual

## 1. GoHighLevel Private Integration
1. In your GHL Sub-Account, go to **Settings > Private Integrations > Create Integration**.
2. Grant full read/write scopes for:
   - `calendars:read`, `calendars:write`
   - `contacts:read`, `contacts:write`
   - `conversations:read`, `conversations:write`
   - `opportunities:read`, `opportunities:write`
3. Copy the bearer token and paste it into the n8n HTTP Header Auth credential (`Authorization: Bearer <TOKEN>`).

## 2. Connecting Meta & Google Ads
1. Inside GoHighLevel, navigate to **Settings > Integrations**.
2. Link your Meta Business Manager and Google Ads account.
3. Map lead form fields: `Full Name` -> `contact.name`, `Phone` -> `contact.phone`, `Budget` -> `custom_fields.lead_budget`.

## 3. Customizing the Qualification Rules
In the n8n LangChain Agent node:
- Adjust minimum budget thresholds (Default: `$2,500`).
- Update business operating hours and target calendar ID (`cal_enterprise_main_01`).
