# Ledgerly

> *"Upload a statement. Understand your money."*

Ledgerly is a personal finance web application that turns bank statement CSVs into categorized transactions, budgets, and dashboards. Upload a file, preview the auto-categorized results, fix anything that's off, and confirm. Duplicates are skipped automatically, and every import can be undone.

## Why Ledgerly?

| Problem | Ledgerly's Answer |
|---|---|
| Bank apps show raw, uncategorized data | Rule-based auto-categorization you control |
| Budgeting apps demand your bank login | Zero credentials needed — just upload a CSV |
| CSV import is an afterthought everywhere | CSV is the **core** workflow, not a side feature |
| No preview before saving | Full preview table with inline editing before anything is saved |
| Duplicate mess when re-uploading | SHA-256 fingerprinting detects duplicates automatically |
| Can't undo a bad import | One-click batch rollback for any import |

## Features

- **Smart CSV Import** — handles different bank formats via saved profiles
- **Duplicate Protection** — re-uploading overlapping statements never creates double entries
- **Rule-Based Categories** — set a rule once, every future import follows it
- **Preview Before Save** — nothing is stored until you confirm
- **Undo an Import** — remove a whole upload with one action
- **Budgets & Alerts** — monthly limits per category with overspend warnings
- **Dashboard** — spending by category, income vs. expense, and trends over time

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Spring Boot 3.x (Java 21) |
| Frontend | React 18 + TypeScript + Vite |
| Database | PostgreSQL 16 |
| UI | Shadcn/UI + Tailwind CSS |
| Charts | Recharts |
| Auth | Spring Security + JWT |
| CSV Parsing | Apache Commons CSV + PapaParse |
| Deployment | Docker + Docker Compose |

## Documentation

📄 **[Project Documentation (PDF)](docs/Ledgerly_Project_Documentation.pdf)** — 45-page detailed document covering:

- Competitive analysis of 6 existing apps (Mint, YNAB, Firefly III, Monarch Money, Wallet, Actual Budget)
- Gap analysis showing where Ledgerly uniquely fits
- Data Flow Diagrams (Level-0 and Level-1)
- System Architecture (3-tier diagram)
- Use Case Diagram with 12 use cases
- ER Diagram with 7 entities and design rationale
- Import pipeline deep-dive (7-stage flow)
- Full REST API specification
- Security design
- 10-week development roadmap

## How It Works

```
1. Download a statement CSV from your bank
2. Upload it to Ledgerly → map the columns once (saved as a Bank Profile)
3. Ledgerly deduplicates, categorizes, and shows you a preview
4. Review, fix anything, then confirm
5. Dashboard and budgets update automatically
```

## License

MIT
