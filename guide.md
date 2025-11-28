# CasinoCore Bot User Guide

Welcome to **CasinoCore**, the all-in-one Discord bot that delivers a premium UnbelievaBoat-style economy, casino, store, inventory, and games experience. This guide walks you through everything you need to know to launch and run CasinoCore smoothly in your community.

---

## 1. Getting Started

### 1.1 Invite the Bot
1. Click the official invite link (Ask the bot owner or visit the support server if you need it).
2. Select the Discord server where you want CasinoCore to operate.
3. Authorize the requested permissions (Manage Server, Manage Roles, Manage Channels, Send Messages, Embed Links, Attach Files, Add Reactions, Use External Emojis, Read Message History).

> **Tip:** Granting Administrator ensures all features work flawlessly. If you use limited scopes, make sure CasinoCore has a role that sits above roles it should manage.

### 1.2 First Login Checklist
- Confirm CasinoCore appears online.
- Run `/help` to verify the interactive menu loads.
- If you have premium access, run `/premium-info` to confirm the subscription is recognized.

---

## 2. Essential Configuration

All configuration is handled with slash commands. You can always revisit the system state with `/view-settings`.

### 2.1 Economy Basics
- `/set-currency symbol:$ name:Credits position:before`
- `/set-start-balance cash:500 bank:0`
- `/maximum-balance cash:1000000 bank:5000000`
- `/toggle-command` to enable/disable specific features per guild.

### 2.2 Reward & Fine Tuning
- `/set-payout reward type:daily amount:1000`
- `/set-fail-rate command:crime rate:0.35`
- `/set-fine-min command:rob amount:50`
- `/set-fine-max command:rob amount:600`

### 2.3 Bet Limits (Casino)
- `/set-bet-limit game:slot min:100 max:25000`
- `/set-bet-limit game:roulette min:1000 max:75000`
- `/set-bet-limit game:russian-roulette min:500 max:5000`

### 2.4 Chat Money
- `/toggle-chat-money enabled:true`
- `/chat-money-channels add channel:#general`
- `/chat-money-cooldown time:45s`

### 2.5 Store & Inventory
- `/create-item name:"VIP Pass" price:25000 description:"Unlocks VIP role" stock:10`
- `/store` to view; `/inventory` to see user holdings.
- `/buy-item`, `/sell-item`, `/use-item` for user interaction.

### 2.6 Audit & Safety
- `/audit-economy` checks for negative balances, duplicates, corrupt items.
- `/economy-analytics` (premium) shows economy snapshots.
- Configure an audit channel via `/money-audit-log channel:#economy-audit` for transaction logs.

### 2.7 Court & Police System
- `/set-judge` — Configure Judge (Tier 1) and Chief Justice (Tier 2) roles with optional daily salaries
- `/set-lawyer` — Configure Lawyer role, license price, and license duration
- `/set-police` — Configure Police role with optional daily salary
- `/legal-info` — View all court system information, roles, and configured salaries

### 2.8 Backups
- `/backup create` to snapshot the entire economy.
- `/backup list`, `/backup delete`, `/backup restore` with confirmation buttons.
- `/backup export` for an off-site copy.

---

## 3. Feature Overview

### 3.1 Currency & Balances
- `/balance`, `/bank deposit`, `/bank withdraw`, `/bank statement`, `/bank loan-status`, `/bank freeze-list`
- `/invest start`, `/invest history`, `/loan request`, `/loan history`, `/loan-repay`
- Admin tools: `/add-money`, `/remove-money`, `/reset-economy`, `/role-income`

### 3.2 Casino Games
- **Slots** (`/slots`)
- **Roulette** (`/roulette` rich bet types)
- **Coinflip** (`/coinflip`)
- **Bet** (`/bet` 50/50)
- **Blackjack** (`/blackjack` with interactive buttons)
- **Russian Roulette** multi-player lobby (`/russian-roulette join`, `start`, `cancel`)

### 3.3 PvP Mini Games
- `/duel-rps`, `/duel-dice`, `/duel-coinflip` with wagering, accept/decline buttons, audit logging.

### 3.4 Work & Crime Loop
- `/work`, `/crime`, `/slut`, `/rob`, `/beg`, `/search`
- Fines always draw from bank with full transaction tracing.

### 3.5 Store System
- Category-aware store with pagination, custom replies, stock control, and guide button.
- Custom per-item purchase responses with placeholders (`{user}`, `{item}`, `{price}`, etc.).

### 3.6 Premium Perks
- **Server Premium** unlocks expanded store limits, analytics, projection charts, backup/restore, interest controls, economy automation (`/economy-analytics`, `/economy-projection`, `/economy-stats`, `/interest`, `/economy-analytics`, `/backup`, `/restore`).
- **User Premium** boosts earnings, cooldown reductions, casino odds, inventory slots, premium profile cards.
- Manage tokens via `/premium-activate-server`, `/premium-deactivate-server`, `/premium-activate-user`, `/premium-list`, `/vote-reward`.

### 3.7 Visual Dashboards
- `/economy-analytics` renders premium charts (doughnut + bar graphs) using canvas.
- `/economy-projection` provides a 30-day forecast with glass-style line chart.
- `/profile-card` generates a premium art card (HiDPI) for users.

### 3.8 Server Bank & Finance Tools
- Automatic tax routing to the **State Bank of <ServerName>**.
- `/bank-info`, `/bank-deposit`, `/bank-withdraw` for treasury management.
- `/bank statement` — Generate personal bank statements with transaction history (last 30 days)
- `/bank loan-status <user>` — Check loan status for any user
- `/bank freeze-list` — List all frozen accounts (Judge/Chief Justice only)
- Investment & loan suite: `/investment`, `/loan-system`, `/invest start`, `/invest history`, `/loan request`, `/loan history`, `/loan-repay`.

### 3.9 Court & Police System
- **Judge/Chief Justice Commands:**
  - `/fine apply user:<target> amount:<amount>` — Issue fines to users (adds to court recovery reserve)
  - `/fine history user:<target>` — View complete fine history for any user (Judge/Chief Justice/Admin only)
  - `/release user:<target>` — Release detained users from custody
  - `/revoke-license user:<target>` — Revoke active lawyer licenses
  - `/bank freeze-list` — List all frozen bank accounts
- **Police Commands:**
  - `/detain user user:<target>` — Detain users who have attempted robbery (checks rob logs)
  - `/detain list` — List all currently detained users (Police/Judge/Chief Justice only)
  - `/detain history user:<target>` — View detain history for any user (Police/Judge/Chief Justice only)
- **User Commands:**
  - `/buy-license` — Purchase a lawyer license (requires Lawyer role to be configured)
  - `/show-license` — Display your lawyer license card (Canvas-generated image with user details)
  - `/legal-info` — View court system information, roles, salaries, and license details
- **Daily Salary System:**
  - Judges, Chief Justices, and Police officers automatically receive daily salary payouts every 24 hours
  - Salaries are configured per role via `/set-judge` and `/set-police`
  - All recipients receive DM receipts with payment confirmation
- **License System:**
  - Lawyer licenses expire automatically after the configured duration
  - Licenses can be revoked by judges using `/revoke-license`
  - License cards are generated with Canvas and include user information
- **History & Tracking:**
  - All court actions are logged to a dedicated court logs channel (configurable via `/legal-info legal-setup`)
  - Fine history tracks all fines issued with amounts, reasons, and timestamps
  - Detain history records all detentions with amounts recovered and dates

### 3.10 Backups & Restore Workflow
- Hourly job enforces backup locks.
- Confirmation buttons (restore/delete) are restricted to command invoker and timeout after 60 seconds.
- Audit logs record every action.

---

## 4. Command Reference (High-Level)

| Category | Highlight Commands |
| --- | --- |
| Economy | `/balance`, `/work`, `/crime`, `/collect-income`, `/interest`, `/economy-projection` |
| Banking | `/bank deposit`, `/bank withdraw`, `/bank statement`, `/bank loan-status`, `/bank freeze-list` |
| Finance | `/invest start`, `/invest history`, `/loan request`, `/loan history`, `/loan-repay` |
| Casino | `/slots`, `/roulette`, `/blackjack`, `/russian-roulette`, `/bet` |
| Court & Police | `/legal-info`, `/buy-license`, `/show-license`, `/fine apply`, `/fine history`, `/detain user`, `/detain list`, `/detain history` |
| Store & Items | `/create-item`, `/edit-item`, `/delete-item`, `/buy-item`, `/inventory` |
| Admin | `/set-payout`, `/set-fail-rate`, `/set-bet-limit`, `/set-judge`, `/set-police`, `/toggle-command`, `/view-settings` |
| Premium | `/premium-info`, `/premium-list`, `/economy-analytics`, `/profile-card` |
| Utilities | `/help`, `/ping`, `/backup`, `/restore`, `/audit-economy` |

> For the full command tree with examples, refer to `docs/CommandReference.md`.

---

## 5. Premium & Voting

1. **Activation:** Owners can activate server or user premium with the `/premiumOwner` suite in the support guild.
2. **Duration:** `/premium-info` shows remaining time. Server premium defaults to the value configured in `.env` (e.g., 30 days).
3. **Voting:** The Top.gg webhook automatically grants 24h (weekday) or 48h (weekend) user premium. Users receive a DM on activation and expiry.
4. **Perks Summary:**
   - Expanded store limit (100 items)
   - Advanced analytics & projections
   - Faster cooldowns & higher payouts
   - Premium-only admin tools (interest, economy analytics, backup suite)
   - Premium profile card themes

---

## 6. Safety & Best Practices

- **Permissions:** Limit admin commands to trusted staff. CasinoCore respects Discord permissions, but always double-check role assignments.
- **Audit Logs:** Configure `/money-audit-log` to keep an immutable trail of major transactions.
- **Backups:** Keep a fresh backup before performing risky operations (mass edits, economy resets, imports).
- **Rate Limits:** Avoid spamming high-frequency commands; Discord enforces interaction rate limits.
- **Privacy:** CasinoCore never stores message content beyond what is required for chat-money ID tracking.

---

## 7. Troubleshooting

| Issue | Possible Fix |
| --- | --- |
| `/help` shows “expired” immediately | Ensure buttons are clicked within 60 seconds. Run `/help` again to refresh. |
| Casino command says “Premium required” | Server lacks premium. Activate via `/premium-info` or owner commands. |
| Chat money not rewarding | Verify `/toggle-chat-money enabled:true` and eligible channels are configured. Also ensure cooldown hasn’t been exceeded. |
| Backup restore fails | Confirm no other backup process is running, check audit logs for detailed stack traces. |
| Slash commands missing | Re-run command deployment script or re-invite the bot with the `applications.commands` scope. |

---

## 8. Support & Resources

- **Support Server:** Join the official Discord for updates and live help.
- **Documentation:**
  - `docs/CommandReference.md` – detailed command breakdown.
  - `docs/topgg-description.md` – listing copy for Top.gg.
  - `README.md` – community-friendly overview and quick links.
- **Logging:** Review `/view-settings` and audit channel for the current configuration.

---

## 9. FAQ (Quick Answers)

**Q: How do I reset the entire economy?**  
Use `/reset-economy` (Manage Server required). A confirmation dialog prevents accidental wipes.

**Q: Can I disable certain commands?**  
Yes. `/toggle-command command:<name> enabled:false` disables a specific command.

**Q: How do custom item purchase replies work?**  
Add them via `/create-item` or `/edit-item` with `custom-reply`. Supported placeholders: `{user}`, `{username}`, `{item}`, `{price}`, `{currency}`, `{quantity}`.

**Q: Does CasinoCore work in DMs?**  
No. All commands are guild-scoped for safety.

**Q: What happens when premium expires?**  
Premium-only features lock automatically, timers cancel, and users receive a DM notification.

---

Need more help? Reach out in the support server or run `/help` anytime. Enjoy building your economy with CasinoCore! 🎰💸
