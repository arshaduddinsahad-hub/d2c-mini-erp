# D2C Mini-ERP Project Context

## Architecture

- n8n = automation and orchestration engine
- Supabase = source of truth
- Dashboard = analytics and control tower
- ChatGPT = independent QA and review layer
- GitHub = shared project memory and version-controlled project repository

## Core Principle

Routine business operations should be automated through n8n.

The dashboard should primarily be used for:
- Analytics
- Monitoring
- Alerts
- Configuration
- Exceptional/admin intervention

The dashboard should not be the main place for routine operational processing.

## Phase Status

- Phase 1 Foundation: Complete
- Phase 2A Supabase DB: Complete
- Phase 2B Dashboard UI: Complete
- Phase 3 Automation: In Progress

## Phase 3 Current Scope

- Order automation
- Customer lookup/deduplication
- Inventory reservation
- Inventory commit
- Inventory release
- Restock
- Lifecycle orchestration
- Employee tasks
- Customer notifications
- Error handling
- Idempotency
- Retry handling

## Important Rule

Do not put secrets, API keys, passwords, Supabase service-role keys, or n8n credentials in this repository.
