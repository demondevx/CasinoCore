# CasinoCore

Your community's all-in-one **economy + casino + games** companion for Discord.

Bring UnbelievaBoat-style fun to your server with premium visuals, powerful admin tools, automated backups, and a balanced money loop that keeps members engaged.

---

## ✨ Highlights
- **Rich Economy Loop** – Work, crime, timed rewards, chat income, investments, and loans.
- **Casino Suite** – Slots, Roulette, Blackjack, Russian Roulette, 50/50 Bet, Coinflip, plus wagered 1v1 mini-games.
- **Custom Store & Inventory** – Create items with stock, prices, custom replies, and per-server limits.
- **Premium Dashboards** – Crystal-clear analytics, projection charts, and luxury profile cards rendered with canvas.
- **Backups & Safety** – One-click economy snapshots, restore confirmations, audit trail, and anomaly detection.
- **Court & Police System** – Complete legal framework with judges, lawyers, police, fines, detentions, and history tracking.
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

> Need a step-by-step walkthrough? See [`docs/bot-guide.md`](docs/bot-guide.md) for a complete admin and player guide.

---

## 🧰 Features at a Glance
| Category | What's Included |
| --- | --- |
| Economy Core | `/balance`, `/work`, `/crime`, `/daily`, `/weekly`, `/monthly`, `/collect-income`, `/interest`, `/bank statement`, `/bank loan-status` |
| Banking & Finance | `/bank deposit`, `/bank withdraw`, `/bank statement`, `/bank loan-status`, `/bank freeze-list`, `/invest history`, `/loan history` |
| Casino | `/slots`, `/roulette`, `/blackjack`, `/bet`, `/coinflip`, `/russian-roulette` |
| PvP Games | `/duel-rps`, `/duel-dice`, `/duel-coinflip` with accept/decline buttons |
| Store & Items | `/create-item`, `/edit-item`, `/buy-item`, `/inventory`, custom replies & stock limits |
| Court & Police | `/fine`, `/fine history`, `/detain`, `/detain list`, `/detain history`, `/legal-info`, `/buy-license` |
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
  - [`docs/bot-guide.md`](docs/bot-guide.md) – full setup and gameplay guide.
  - [`docs/CommandReference.md`](docs/CommandReference.md) – exhaustive command list.
  - [`docs/topgg-description.md`](docs/topgg-description.md) – ready-made Top.gg listing copy.
- **Status & Logs:** Watch the audit channel plus console output for actionable warnings (e.g., backup conflicts).

---

## 🙌 Contributing & Feedback
CasinoCore's roadmap is shaped by community feedback. Drop suggestions in the support server or open a GitHub issue/PR if you spot a bug. All contributions must follow the project's coding standards (linting, tests, and docs updates where applicable).

Enjoy building your casino empire! 🎰💸

## 📖 Table of Contents

- [Getting Started](#getting-started)
- [Economy Commands](#-economy-commands)
- [Casino Games](#-casino-games)
- [1v1 Games](#-1v1-games)
- [Store & Inventory](#-store--inventory)
- [Admin Commands](#-admin--configuration)
- [Tips & Tricks](#tips--tricks)
- [Support](#support)

---

## 🚀 Getting Started

### First Steps

1. **Check Your Balance**
   - Use `/money` to see your current cash and bank balance
   - You can also check other users' balances: `/money user:@Username`

2. **Start Earning Money**
   - Try `/work` to earn your first coins
   - Use `/daily` to claim your daily reward
   - Explore `/beg` or `/search` for quick cash

3. **View the Help Menu**
   - Use `/help` to see all available commands
   - Navigate through categories using the buttons
   - Use `/help category:economy` to jump to a specific section

---

## 💰 Economy Commands

### Managing Your Money

**`/money [user]`** - View your balance or another user's balance
- Shows your cash, bank, and total net worth
- Example: `/money user:@Demon`

**`/deposit <amount>`** - Move money from cash to your bank
- Bank is safer and can have higher limits
- Example: `/deposit amount:500`

**`/withdraw <amount>`** - Move money from bank to cash
- Use this when you need cash for transactions
- Example: `/withdraw amount:250`

**`/give <user> <amount>`** - Send money to another user
- Great for trading or helping friends
- Example: `/give user:@Friend amount:100`

### Earning Money

**`/work`** - Work for money
- Earn random amounts based on server settings
- Has a cooldown (usually 1 hour)
- Small chance to fail and pay a fine

**`/crime`** - Commit a crime for higher rewards
- Riskier than work but pays more
- Higher chance of failure and fines
- Example: Rob a store, steal from someone

**`/slut`** - Earn money (NSFW themed)
- Similar to crime with different rewards
- Has failure chance

**`/rob <user>`** - Try to steal from another user
- High risk, high reward
- If you fail, you pay a fine
- If you succeed, you get their cash
- Example: `/rob user:@Target`

**`/beg`** - Beg for small amounts
- Quick way to get small amounts
- Short cooldown
- Always succeeds (no failure)

**`/search`** - Search for money
- Find random amounts of cash
- Short cooldown
- Always succeeds

### Timed Rewards

**`/daily`** - Claim daily reward
- Available every 24 hours
- Usually gives 500 coins
- Don't miss it!

**`/weekly`** - Claim weekly reward
- Available every 7 days
- Usually gives 2,500 coins
- Bigger payout than daily

**`/monthly`** - Claim monthly reward
- Available every 30 days
- Usually gives 10,000 coins
- Biggest timed reward!

### Role Income

**`/role-income list`** - View configured role income
- See which roles earn periodic income
- Check income amounts and intervals

**`/collect-income`** - Collect income from your roles
- If you have roles with income configured, collect it here
- Income accumulates over time based on role settings

### Statistics & Leaderboards

**`/leaderboard [type]`** - View the richest members
- Options: `net` (total wealth), `cash`, or `bank`
- See who's the wealthiest in your server
- Example: `/leaderboard type:net`

**`/economy-stats`** - View server economy statistics
- Total users, total money in circulation
- Recent transaction counts
- Great for seeing the server's economy health

---

## 🎰 Casino Games

All casino games have a chance to win or lose. Gamble responsibly!

### Simple Games

**`/bet <amount>`** - 50/50 chance game
- Win: Get 2x your bet (minus tax)
- Lose: Lose everything
- Example: `/bet amount:200`

**`/coinflip <choice> <amount>`** - Predict heads or tails
- Choose `heads` or `tails`
- Win: Get 2x your bet (minus tax)
- Lose: Lose your bet
- Example: `/coinflip choice:heads amount:100`

**`/slots <amount>`** - Slot machine game
- Match symbols to win multipliers
- 💎 = 10x, ⭐ = 5x, 7️⃣ = 20x
- Example: `/slots amount:50`

**`/roulette <bet-type> <amount> [number]`** - Bet on roulette
- Bet types: `red`, `black`, `green`, or `number` (0-36)
- Red/Black: 2x payout
- Green/Number: 36x payout
- Example: `/roulette bet-type:red amount:100`

### Interactive Games

**`/blackjack <amount>`** - Play blackjack against the bot
- Get as close to 21 as possible without going over
- Use **Hit** button to draw cards
- Use **Stand** button to end your turn
- Blackjack (21 on first two cards) = 2.5x payout
- Example: `/blackjack amount:200`

**`/russian-roulette <amount>`** - High-risk gamble
- 1 in 6 chance to survive and win 5x your bet
- 5 in 6 chance to lose everything
- Only for the brave!
- Example: `/russian-roulette amount:500`

---

## ⚔️ 1v1 Games

Challenge other players to duels! Both players must have enough money for the wager.

### How Duels Work

1. Challenge someone with a wager amount
2. They receive a message with **Accept** or **Decline** buttons
3. If accepted, play the game
4. Winner takes all (both wagers combined, minus tax)
5. If declined or timeout, money is refunded

### Available Duels

**`/duel-coinflip <user> <amount>`** - Coinflip duel
- Both players' choices are randomly generated
- Closest to the result wins
- Example: `/duel-coinflip user:@Friend amount:500`

**`/duel-rps <user> <amount>`** - Rock Paper Scissors
- Both players choose Rock, Paper, or Scissors
- Standard RPS rules apply
- Example: `/duel-rps user:@Friend amount:300`

**`/duel-dice <user> <amount>`** - Dice roll duel
- Both players roll a 6-sided die
- Highest roll wins
- Ties result in refunds
- Example: `/duel-dice user:@Friend amount:250`

---

## 🏪 Store & Inventory

### Browsing the Store

**`/store`** - View all available items
- See all items with prices
- Navigate through pages if there are many items
- Items are sorted by price

**`/item-info <item>`** - Get detailed information
- See price, sell price, description
- Check if item is usable
- See role rewards if applicable
- Example: `/item-info item:Sword`

### Buying & Selling

**`/buy-item <item> [quantity]`** - Buy from store
- Purchase items with your cash
- Some items grant roles when purchased
- Example: `/buy-item item:Sword quantity:1`

**`/sell-item <item> [quantity]`** - Sell items back
- Not all items can be sold
- Get sell price (usually less than purchase price)
- Example: `/sell-item item:Sword quantity:1`

### Managing Inventory

**`/inventory [user]`** - View inventory
- See all items you own
- Check quantities
- View other users' inventories too
- Example: `/inventory user:@Friend`

**`/use-item <item>`** - Use an item
- Only usable items can be used
- Some items grant roles when used
- Limited-use items are consumed
- Example: `/use-item item:Health Potion`

**`/give-item <item> <user> [quantity]`** - Give items to friends
- Transfer items from your inventory
- Great for trading
- Example: `/give-item item:Sword user:@Friend quantity:1`

---

## ⚙️ Admin & Configuration

*These commands require Administrator or Manage Server permissions*

### Currency & Balance Settings

**`/set-currency`** - Configure currency display
- Set symbol ($, €, £, etc.)
- Set currency name (coins, dollars, etc.)
- Choose position (before or after amount)
- Example: `/set-currency symbol:$ name:Dollars position:before`

**`/set-start-balance`** - Set starting money for new users
- Configure cash and bank starting amounts
- Example: `/set-start-balance cash:1000 bank:500`

**`/maximum-balance`** - Set balance limits
- Prevent users from having too much money
- Set max cash and/or max bank
- Example: `/maximum-balance cash:1000000 bank:5000000`

### Money Management

**`/add-money`** - Give money to a user
- Add cash or bank to specific users
- Example: `/add-money user:@User amount:1000 type:cash`

**`/add-money-role`** - Give money to all users with a role
- Bulk money distribution
- Uses role selector menu
- Example: `/add-money-role amount:500 role:@VIP`

**`/remove-money`** - Take money from a user
- Remove cash or bank from users
- Example: `/remove-money user:@User amount:500 type:cash`

**`/remove-money-role`** - Take money from all users with a role
- Bulk money removal
- Example: `/remove-money-role amount:200 role:@Member`

**`/reset-money`** - Reset a user's balance
- Sets user's cash and bank to 0
- Requires confirmation
- Example: `/reset-money user:@User`

**`/reset-economy`** - Reset entire server economy
- Deletes all user economy data
- **WARNING: Cannot be undone!**
- Requires confirmation
- Example: `/reset-economy`

### Command Configuration

**`/set-cooldown`** - Set command cooldowns
- Configure how long users must wait between uses
- Example: `/set-cooldown command:work time:1h`

**`/set-payout`** - Set earning ranges
- Configure min/max payouts for work, crime, etc.
- Example: `/set-payout command:work min:50 max:200`

**`/set-fail-rate`** - Set failure chances
- Configure how often risky commands fail (0-1)
- Example: `/set-fail-rate command:crime rate:0.3` (30% fail rate)

**`/set-fine-amount`** - Set fine amounts
- Configure how much users pay when they fail
- Example: `/set-fine-amount command:crime amount:200`

**`/set-fine-type`** - Set where fines come from
- Choose `cash` or `bank`
- Example: `/set-fine-type command:crime type:cash`

### Custom Messages

**`/add-reply`** - Add custom success messages
- Customize what users see when commands succeed
- Use `{amount}` placeholder for dynamic values
- Example: `/add-reply command:work reply:You worked hard and earned {amount}!`

**`/add-fail-reply`** - Add custom failure messages
- Customize failure messages
- Example: `/add-fail-reply command:crime reply:You got caught and lost {amount}!`

**`/delete-reply`** - Remove custom messages
- Delete specific custom replies
- Example: `/delete-reply command:work index:1`

**`/default-replies`** - Reset to default messages
- Restore original bot messages
- Example: `/default-replies command:work`

**`/list-custom-replies`** - View all custom messages
- See all configured custom replies
- Example: `/list-custom-replies`

### Advanced Features

**`/role-income`** - Configure role-based income
- Give roles periodic money automatically
- Set amount and interval (e.g., every 24h)
- Example: `/role-income add role:@VIP amount:100 interval:24h`

**`/chat-money-amount`** - Configure chat rewards
- Set min/max amounts users earn from chatting
- Example: `/chat-money-amount min:1 max:10`

**`/chat-money-channels`** - Set chat reward channels
- Choose which channels give money for messages
- Uses channel selector menu
- Example: `/chat-money-channels add channel:#general`

**`/chat-money-cooldown`** - Set chat reward cooldown
- How long between chat rewards
- Example: `/chat-money-cooldown time:1m`

**`/set-tax`** - Configure taxes
- Set tax on transfers and/or winnings
- Percentage-based (0-100)
- Example: `/set-tax transfer:5 winnings:10`

**`/toggle-command`** - Enable/disable commands
- Turn commands on or off for your server
- Example: `/toggle-command command:rob enabled:true`

**`/set-rob`** - Configure rob command
- Set min/max rob amounts
- Configure fail rate
- Example: `/set-rob min:100 max:1000 fail-rate:0.4`

**`/money-audit-log`** - Set audit log channel
- Log all money transactions to a channel
- Uses channel selector menu
- Example: `/money-audit-log channel:#audit-log`

### Store Management

**`/create-item`** - Create store items
- Set name, price, description
- Configure sell price, role rewards, uses
- Example: `/create-item name:Sword price:500 description:A sharp sword`

**`/edit-item`** - Edit existing items
- Modify any item property
- Example: `/edit-item item:Sword option:price value:600`

**`/delete-item`** - Remove items from store
- Delete items permanently
- Requires confirmation
- Example: `/delete-item item:Sword`

**`/item-options`** - View item details
- See all item properties
- Example: `/item-options item:Sword`

**`/take-item`** - Remove items from users
- Take items from user inventories
- Example: `/take-item user:@User item:Sword quantity:1`

---

## 💡 Tips & Tricks

### Maximizing Your Earnings

1. **Claim Timed Rewards Daily**
   - Don't forget `/daily`, `/weekly`, and `/monthly`
   - Set reminders if needed!

2. **Use the Bank**
   - Deposit money to protect it from robbers
   - Some servers have higher bank limits

3. **Work Regularly**
   - `/work` is safe and reliable
   - Lower risk than crime/rob

4. **Join Income Roles**
   - If your server has role income, collect it regularly
   - Use `/collect-income` to get your earnings

5. **Smart Gambling**
   - Start with small bets to learn games
   - Don't bet more than you can afford to lose
   - Remember: taxes reduce winnings

### Playing Games Wisely

1. **1v1 Duels**
   - Only challenge players you trust
   - Make sure you both have enough money
   - Duels timeout after 5 minutes

2. **Casino Games**
   - `/bet` and `/coinflip` are 50/50
   - `/blackjack` requires strategy
   - `/russian-roulette` is very risky!

3. **Store Items**
   - Some items grant roles - check before buying
   - Sell items you don't need
   - Limited-use items are consumed when used

### Staying Safe

1. **Watch Out for Robbers**
   - Keep important money in the bank
   - Rob has a fail rate, but it's risky

2. **Check Cooldowns**
   - Commands have cooldowns to prevent spam
   - Wait times vary by server settings

3. **Read Error Messages**
   - The bot will tell you if something goes wrong
   - Insufficient balance, cooldowns, etc.

---

## 🆘 Support

### Need Help?

- **Support Server**: [Join our Discord](https://discord.gg/AR8HkshRtW)
- **Documentation**: [View on GitHub](https://github.com/demondevx/Casino-Bot)
- **Use `/help`**: Get interactive command help in Discord

### Common Issues

**"Insufficient Balance"**
- You don't have enough money for that action
- Check your balance with `/money`
- Make sure you have cash (not just bank) for some commands

**"You are on cooldown"**
- Wait for the cooldown to expire
- Cooldown times vary by command and server settings

**"Command Disabled"**
- The server admin has disabled this command
- Contact server admins if you think this is an error

**"Permission Denied"**
- You don't have permission for that command
- Admin commands require Administrator or Manage Server permission

---

## 📝 Notes

- All money amounts are examples - actual values depend on server settings
- Commands may vary slightly based on server configuration
- Some features require server admins to configure them first
- Always gamble responsibly!

---

**Bot Created by DEMON**

Enjoy using the Economy Bot! 🎉
