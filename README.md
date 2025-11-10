# CasinoCore

Your community’s all-in-one **economy + casino + games** companion for Discord.

Bring UnbelievaBoat-style fun to your server with premium visuals, powerful admin tools, automated backups, and a balanced money loop that keeps members engaged.

---

## ✨ Highlights
- **Rich Economy Loop** – Work, crime, timed rewards, chat income, investments, and loans.
- **Casino Suite** – Slots, Roulette, Blackjack, Russian Roulette, 50/50 Bet, Coinflip, plus wagered 1v1 mini-games.
- **Custom Store & Inventory** – Create items with stock, prices, custom replies, and per-server limits.
- **Premium Dashboards** – Crystal-clear analytics, projection charts, and luxury profile cards rendered with canvas.
- **Backups & Safety** – One-click economy snapshots, restore confirmations, audit trail, and anomaly detection.
- **100% Slash Commands** – Clean, reliable, and fully documented interactions.

---

## 🚀 Quick Start
1. **Invite the bot** using the official OAuth link (ask the owner or see `/help`).
2. **Run `/help`** to open the interactive command browser with dropdown navigation.
3. **Configure essentials**:
   - `/set-currency symbol:$ name:Credits`
   - `/set-start-balance cash:500 bank:0`
   - `/toggle-command command:rob enabled:true`
4. **Preview settings** anytime with `/view-settings`.

> Need a step-by-step walkthrough? See [`guide.md`](guide.md) for a complete admin and player guide.

---

## 🧰 Features at a Glance
| Category | What’s Included |
| --- | --- |
| Economy Core | `/balance`, `/work`, `/crime`, `/daily`, `/weekly`, `/monthly`, `/collect-income`, `/interest` |
| Casino | `/slots`, `/roulette`, `/blackjack`, `/bet`, `/coinflip`, `/russian-roulette` |
| PvP Games | `/duel-rps`, `/duel-dice`, `/duel-coinflip` with accept/decline buttons |
| Store & Items | `/create-item`, `/edit-item`, `/buy-item`, `/inventory`, custom replies & stock limits |
| Admin Tools | `/set-bet-limit`, `/set-payout`, `/audit-economy`, `/backup`, `/restore`, `/toggle-command` |
| Analytics & Visuals | `/economy-analytics`, `/economy-projection`, `/economy-stats`, `/profile-card` |
| Safety & Logging | Audit channel embeds, premium-required checks, per-command permission enforcement |

For complete command descriptions, refer to [`docs/CommandReference.md`](docs/CommandReference.md).

---

## 💎 Premium Overview
CasinoCore supports both **Server Premium** and **User Premium** tiers.

- **Server Premium** unlocks advanced admin dashboards, increased store limits (100 items), backups & restore, interest automation, theme customization, and the economy analytics suite.
- **User Premium** boosts timed rewards, cuts cooldowns, enhances casino odds, extends inventory capacity, and enables luxury profile cards.
- Manage premium tokens with the owner-only `/premiumOwner` commands inside the support guild. `/premium-info` shows current status and perks.
- Votes on Top.gg grant 24–48h user premium automatically (with DM confirmation).

---

## 🔒 Safety & Best Practices
- Assign CasinoCore a high role and the required permissions so commands work reliably.
- Configure an audit log with `/money-audit-log channel:#economy-audit` to track major transactions.
- Use `/backup create` before large resets or imports. Confirmation buttons prevent accidental wipes.
- Keep chat-money channels explicit (`/chat-money-channels add channel:#general`) to avoid spam.
- Premium-required commands gracefully remind users to upgrade—no crashes or silent failures.

---

## 🤝 Support & Community
- **Support Server:** Join the official Discord from `/help` or `/premium-info` for announcements and live assistance.
- **Documentation:**
  - [`guide.md`](guide.md) – full setup and gameplay guide.
- **Status & Logs:** Watch the audit channel plus console output for actionable warnings (e.g., backup conflicts).

---

## 🙌 Contributing & Feedback
CasinoCore’s roadmap is shaped by community feedback. Drop suggestions in the support server or open a GitHub issue/PR if you spot a bug. All contributions must follow the project’s coding standards (linting, tests, and docs updates where applicable).

Enjoy building your casino empire! 🎰💸
