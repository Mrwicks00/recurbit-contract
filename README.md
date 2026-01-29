# RecurBit

An automated Bitcoin Dollar Cost Averaging (DCA) service built on the Stacks blockchain. Set your schedule, deposit funds, and let smart contracts automatically buy Bitcoin at regular intervals - removing emotion from investing and maximizing long-term accumulation.

## Overview

RecurBit is a trustless, automated Bitcoin purchasing service that implements the time-tested DCA strategy through Clarity smart contracts. Whether you want to buy $10 of Bitcoin every day or $1,000 every month, RecurBit handles the execution automatically, consistently, and without human intervention.

## The Problem

Bitcoin investors face several challenges with manual DCA:
- **Emotional Trading**: Fear and greed lead to poor timing decisions
- **Inconsistency**: Missing purchases disrupts the DCA strategy
- **Time Consuming**: Manual purchases require constant attention
- **High Fees**: Multiple small purchases on exchanges rack up fees
- **Centralization Risk**: Funds held on exchanges vulnerable to hacks
- **Discipline Required**: Hard to stick to a plan during volatility

## The Solution

RecurBit provides automated, trustless Bitcoin accumulation:
- **Set and Forget**: Configure once, purchases happen automatically
- **Emotion-Free**: Smart contracts execute regardless of market sentiment
- **Lower Fees**: Batched purchases reduce per-transaction costs
- **Non-Custodial**: You control your funds and Bitcoin at all times
- **Transparent**: All transactions visible on-chain
- **Flexible**: Multiple frequency options and customization

## Features

### 📅 Flexible Scheduling

#### Purchase Frequencies
- **Daily**: Buy Bitcoin every day at a specific time
- **Weekly**: Choose your day of the week (e.g., every Monday)
- **Bi-Weekly**: Every two weeks on chosen day
- **Monthly**: Specific day of month (e.g., 1st or 15th)
- **Custom Intervals**: Set any interval in blocks/days

#### Schedule Customization
- **Start Date**: Begin DCA on any future date
- **End Date**: Optional expiration for limited-time DCA
- **Pause/Resume**: Temporarily pause without canceling
- **Amount Flexibility**: Change purchase amounts anytime
- **Time of Day**: Choose execution time (morning, afternoon, evening)

### 💰 Smart Fund Management

#### Deposit System
- **Flexible Deposits**: Add funds anytime to keep DCA running
- **Auto-Withdrawal**: Unused funds returned when DCA ends
- **Balance Tracking**: Real-time view of remaining balance
- **Low Balance Alerts**: Notifications when funds running low
- **Top-Up Recommendations**: Suggested deposits based on schedule

#### Budget Controls
- **Per-Purchase Limits**: Set minimum/maximum per buy
- **Monthly Budgets**: Cap total monthly spending
- **Balance Reserves**: Keep minimum balance for fees
- **Automatic Adjustments**: Skip purchases if insufficient funds
- **Overflow Handling**: Roll unused funds to next purchase

### 🤖 Automated Execution

#### Smart Contract Automation
- **Trustless Execution**: No human intervention needed
- **Time-Locked Triggers**: Purchases execute at scheduled times
- **Fail-Safe Mechanisms**: Retry logic for failed purchases
- **Gas Optimization**: Batched operations reduce costs
- **Oracle Integration**: Real-time Bitcoin price feeds

#### Execution Features
- **Price Limits**: Optional price ceiling for purchases
- **Slippage Protection**: Maximum acceptable price deviation
- **Market Orders**: Instant execution at market price
- **Limit Orders**: Buy only below target price
- **Partial Fills**: Accept partial purchases if liquidity limited

### 📊 Portfolio Tracking

#### Performance Analytics
- **Total Invested**: Track cumulative STX spent
- **Bitcoin Acquired**: Total BTC accumulated
- **Average Price**: Your dollar-cost average
- **ROI Calculation**: Current profit/loss percentage
- **Cost Basis**: Complete purchase history for tax reporting
- **Comparison**: Performance vs. lump sum investment

#### Visualization
- **Purchase History**: Timeline of all buys
- **Price Charts**: Overlay your purchases on BTC price chart
- **Progress Tracker**: Visual progress toward goals
- **Projection Model**: Estimate future accumulation
- **Statistics Dashboard**: Key metrics at a glance

### 🎯 Goal Setting

#### Investment Goals
- **Target Amount**: Set Bitcoin accumulation goal (e.g., 1 BTC)
- **Time Horizon**: Define investment period (months/years)
- **Milestone Tracking**: Celebrate progress checkpoints
- **Goal Recommendations**: Suggested plans based on budget
- **Achievement Badges**: Gamification for long-term commitment

#### Scenario Planning
- **What-If Calculator**: Project outcomes for different scenarios
- **Risk Analysis**: Understand potential outcomes
- **Adjustment Suggestions**: Optimize schedule for goals
- **Market Simulations**: Historical backtesting

### 🔔 Notifications & Alerts

#### Activity Notifications
- **Purchase Confirmations**: Alert after each buy
- **Balance Warnings**: Low balance notifications
- **Goal Milestones**: Celebrate accumulation achievements
- **Schedule Updates**: Confirm schedule changes
- **Error Alerts**: Notify if purchase fails

#### Delivery Channels
- **Email**: Detailed transaction reports
- **SMS**: Quick purchase confirmations
- **Push Notifications**: Mobile app alerts
- **Discord/Telegram**: Bot notifications
- **Webhooks**: Custom integrations

### 🛡️ Security & Control

#### User Controls
- **Emergency Pause**: Stop all purchases instantly
- **Withdrawal Anytime**: Pull funds at any time
- **Schedule Modification**: Adjust parameters on-the-fly
- **Cancel Service**: End DCA and withdraw all funds
- **Multi-Sig Option**: Require multiple signatures for changes

#### Security Features
- **Non-Custodial**: Smart contract holds funds, not a company
- **Open Source**: Fully auditable code
- **Time Locks**: Prevent unauthorized withdrawals
- **Access Control**: Only you can modify your DCA
- **Audit Trail**: Complete history of all operations

## Use Cases

### Individual Investors
- **New to Bitcoin**: Start small with automated purchases
- **Busy Professionals**: Invest without active management
- **Long-Term Holders**: Build position systematically
- **Volatility Averse**: Avoid timing the market stress
- **Consistent Savers**: Convert savings to Bitcoin automatically

### Financial Strategies
- **Retirement Planning**: Accumulate Bitcoin for retirement
- **Emergency Fund**: Build Bitcoin-denominated reserves
- **College Savings**: Save for children's education
- **Wealth Preservation**: Protect against currency devaluation
- **Diversification**: Add Bitcoin exposure systematically

### Business Use Cases
- **Corporate Treasury**: Companies buying Bitcoin reserves
- **Payroll Conversion**: Auto-convert portion of salary to BTC
- **Vendor Payments**: Accumulate Bitcoin for supplier payments
- **Remittances**: Regular Bitcoin sending to family abroad

## How It Works

### For Users

1. **Create DCA Plan**
   - Connect your Stacks wallet
   - Choose purchase frequency (daily, weekly, monthly)
   - Set purchase amount per interval
   - Configure start/end dates (optional)

2. **Deposit Funds**
   - Deposit STX to cover planned purchases
   - Smart contract holds funds securely
   - Add more funds anytime

3. **Automated Execution**
   - Smart contract executes purchases on schedule
   - Bitcoin acquired at market price
   - All transactions recorded on-chain

4. **Receive Bitcoin**
   - BTC sent directly to your wallet after each purchase
   - Track accumulation in dashboard
   - Withdraw remaining STX anytime

### Execution Flow
```
User Creates Plan → Deposits STX → Schedule Activates → 
Smart Contract Monitors Time → Trigger Condition Met → 
Execute Purchase (STX → BTC) → Send BTC to User Wallet → 
Update Stats → Wait for Next Interval → Repeat
```

### Example DCA Strategy

**Goal**: Accumulate 0.1 BTC over 1 year
**Budget**: $3,000 total ($250/month)
**Strategy**: Buy $57.69 weekly (52 weeks)

**Setup in RecurBit**:
- Frequency: Weekly (every Monday)
- Amount: 57.69 STX equivalent (at current STX/USD rate)
- Duration: 52 weeks
- Initial Deposit: 3,000 STX equivalent

**Outcome**:
- 52 purchases over 12 months
- Average price smoothed across market cycles
- ~0.1 BTC accumulated (depending on BTC price)
- Complete purchase history for taxes

## Technical Architecture

### Smart Contracts

Built with Clarity on Stacks:
- **DCA Manager**: Main contract managing DCA plans
- **Schedule Engine**: Time-based trigger execution
- **Exchange Integration**: STX to BTC conversion
- **Fund Controller**: Manages user deposits and withdrawals
- **Stats Tracker**: Records all purchases and analytics

### Data Structures

#### DCA Plan Map
```clarity
{
  plan-id: uint,
  owner: principal,
  frequency: string-ascii,
  amount-per-purchase: uint,
  total-deposited: uint,
  total-spent: uint,
  bitcoin-acquired: uint,
  purchases-completed: uint,
  next-purchase-block: uint,
  status: string-ascii,
  created-at: uint
}
```

#### Purchase History Map
```clarity
{
  purchase-id: uint,
  plan-id: uint,
  block-height: uint,
  stx-spent: uint,
  btc-acquired: uint,
  btc-price: uint,
  timestamp: uint,
  tx-hash: (buff 32)
}
```

#### User Stats Map
```clarity
{
  user: principal,
  total-plans: uint,
  active-plans: uint,
  total-invested: uint,
  total-btc-acquired: uint,
  average-price: uint,
  first-purchase: uint,
  last-purchase: uint
}
```

### Key Functions

#### Plan Management
- `create-dca-plan(frequency, amount, start-block)` → Create new DCA plan
- `deposit-funds(plan-id, amount)` → Add funds to plan
- `pause-plan(plan-id)` → Temporarily pause purchases
- `resume-plan(plan-id)` → Resume paused plan
- `cancel-plan(plan-id)` → Cancel and withdraw remaining funds
- `update-purchase-amount(plan-id, new-amount)` → Modify purchase size

#### Execution Functions
- `execute-purchase(plan-id)` → Execute scheduled purchase
- `batch-execute(plan-ids)` → Execute multiple plans at once
- `check-due-purchases()` → Check which plans need execution
- `retry-failed-purchase(purchase-id)` → Retry failed purchase
- `emergency-withdraw(plan-id)` → Emergency fund withdrawal

#### Analytics Functions
- `get-plan-details(plan-id)` → Retrieve plan information
- `get-purchase-history(plan-id)` → View all purchases for plan
- `calculate-average-price(plan-id)` → Calculate DCA average
- `get-user-stats(principal)` → Get user statistics
- `get-roi(plan-id)` → Calculate return on investment
- `project-future-accumulation(plan-id, weeks)` → Project future BTC

### Read-Only Functions
- `get-plan(plan-id)` → Get plan details
- `get-user-plans(principal)` → List all user plans
- `get-active-plans()` → List all active plans
- `get-plan-balance(plan-id)` → Check remaining balance
- `get-next-purchase-time(plan-id)` → When next purchase occurs
- `calculate-required-deposit(frequency, amount, duration)` → Calculate needed deposit
- `estimate-btc-accumulation(amount, frequency, duration)` → Estimate BTC acquired
- `get-platform-stats()` → Platform-wide statistics

### Security Features

- ✅ Non-custodial (users control funds)
- ✅ Time-locked execution (prevents manipulation)
- ✅ Access control (only owner can modify plan)
- ✅ Balance validation (prevents overspending)
- ✅ Reentrancy protection
- ✅ Oracle price validation
- ✅ Slippage limits
- ✅ Emergency pause mechanism

## DCA Strategies

### Conservative Strategy
- **Frequency**: Monthly
- **Amount**: Small, consistent ($50-200)
- **Duration**: 5-10 years
- **Goal**: Long-term wealth preservation
- **Risk**: Low

### Moderate Strategy
- **Frequency**: Weekly
- **Amount**: Medium ($100-500)
- **Duration**: 2-5 years
- **Goal**: Balanced accumulation
- **Risk**: Medium

### Aggressive Strategy
- **Frequency**: Daily
- **Amount**: Larger ($50-200 daily)
- **Duration**: 1-2 years
- **Goal**: Rapid accumulation
- **Risk**: Higher (more price exposure)

### Custom Strategy
- **Frequency**: Flexible
- **Amount**: Variable based on income
- **Duration**: Ongoing
- **Goal**: Personalized to situation
- **Risk**: Adjustable

## Benefits of DCA

### Psychological Benefits
- **Removes Emotion**: No panic selling or FOMO buying
- **Reduces Stress**: No need to time the market
- **Builds Discipline**: Consistent investing habit
- **Prevents Paralysis**: Eliminates analysis paralysis
- **Long-Term Focus**: Encourages holding mentality

### Financial Benefits
- **Lower Average Cost**: Buy at various prices, averaging out volatility
- **Risk Mitigation**: Spread purchases across time
- **No Timing Required**: Works regardless of market conditions
- **Compound Growth**: More time in market = more potential growth
- **Dollar-Cost Smoothing**: Reduces impact of volatility

### Practical Benefits
- **Automation**: No manual intervention needed
- **Flexibility**: Adjust strategy as circumstances change
- **Accessibility**: Start with any amount
- **Consistency**: Never miss a purchase
- **Transparency**: Full record of investments

## DCA vs. Lump Sum

### DCA Advantages
- Lower risk of buying at peak
- Psychologically easier to execute
- Accessible for regular income earners
- Reduces volatility impact
- No need to time market

### Lump Sum Advantages
- Historically higher average returns
- More time in market
- Lower transaction fees (one purchase)
- Simple execution

**RecurBit Recommendation**: DCA is ideal for most investors who:
- Receive regular income (salary, business revenue)
- Want to reduce emotional stress
- Are risk-averse
- Don't have large lump sums available
- Prefer consistent, disciplined approach

## Getting Started

### Prerequisites
- Stacks wallet (Hiro Wallet, Leather, or Xverse)
- STX tokens for purchases and fees
- Basic understanding of DCA strategy
- Long-term investment mindset

### Quick Start Guide
```bash
# 1. Connect wallet
Visit app.recurbit.io

# 2. Create your first DCA plan
- Choose frequency (daily, weekly, monthly)
- Set purchase amount
- Define duration (or leave ongoing)

# 3. Deposit funds
- Calculate required deposit
- Send STX to smart contract
- Confirm transaction

# 4. Monitor and adjust
- Track purchases in dashboard
- Adjust amount as needed
- Pause/resume as circumstances change
```

### Example Setup

**Conservative Beginner**:
```
Frequency: Monthly
Amount: 100 STX per purchase
Duration: 12 months
Initial Deposit: 1,200 STX
Goal: Accumulate Bitcoin steadily
```

**Moderate Accumulator**:
```
Frequency: Weekly  
Amount: 50 STX per purchase
Duration: 24 months (ongoing)
Initial Deposit: 2,600 STX (6 months)
Goal: Build Bitcoin position
```

**Aggressive Stacker**:
```
Frequency: Daily
Amount: 20 STX per purchase
Duration: Ongoing
Initial Deposit: 600 STX (monthly top-up)
Goal: Maximum accumulation
```

## Smart Contract Examples

### Create DCA Plan
```clarity
(contract-call? .recurbit create-dca-plan
  "weekly"                         ; frequency
  u50000000                        ; 50 STX per purchase
  u144                            ; start in 144 blocks (~1 day)
)
```

### Deposit Funds
```clarity
(contract-call? .recurbit deposit-funds
  u1                              ; plan-id
  u2600000000                     ; deposit 2,600 STX
)
```

### Execute Purchase (automated, but can be called manually)
```clarity
(contract-call? .recurbit execute-purchase u1)
```

### Check Plan Status
```clarity
(contract-call? .recurbit get-plan u1)
;; Returns: {owner, frequency, amount, balance, btc-acquired, ...}
```

### View Purchase History
```clarity
(contract-call? .recurbit get-purchase-history u1)
;; Returns: list of all purchases with prices and amounts
```

## Fee Structure

### Platform Fees
- **Service Fee**: 0.5% per purchase (covers execution costs)
- **Network Fee**: Standard STX transaction fees
- **No Hidden Fees**: Complete transparency

### Fee Comparison
- **Traditional Exchange**: 0.5-2% per trade + withdrawal fees
- **Managed DCA Services**: 1-3% ongoing management fees
- **RecurBit**: 0.5% execution only, no ongoing fees

### Example Cost Calculation
```
Purchase Amount: 100 STX
Platform Fee (0.5%): 0.5 STX
Network Fee: ~0.1 STX
Total Cost: 0.6 STX
Effective Fee: ~0.6%
```

## Calculator Tools

### Required Deposit Calculator
```
Frequency: Weekly
Amount per Purchase: 50 STX
Duration: 52 weeks
Required Deposit: 2,600 STX + ~31 STX fees = 2,631 STX
```

### BTC Accumulation Estimator
```
Weekly Investment: $50
Duration: 1 year (52 weeks)
Assumed Avg BTC Price: $50,000
Estimated BTC Accumulated: 0.052 BTC
(Actual amount varies with price)
```

### Average Price Calculator
```
Total Invested: $2,600
BTC Acquired: 0.052 BTC
Your Average Price: $50,000/BTC
Current BTC Price: $60,000
Profit: $520 (20%)
```

## Tax Reporting

### What RecurBit Provides
- **Complete Purchase History**: All transactions with dates and amounts
- **Cost Basis Tracking**: Each purchase tracked separately
- **CSV Export**: Download data for tax software
- **Realized Gains**: If you sell/trade BTC
- **Annual Summaries**: Year-end tax reports

### Tax Considerations
- **Capital Gains**: Selling BTC creates taxable event
- **FIFO/LIFO**: Choose accounting method
- **Holding Periods**: Long-term vs short-term rates
- **Record Keeping**: Maintain complete transaction history

**Note**: RecurBit is not tax advice. Consult with a tax professional for your situation.

## Roadmap

### Phase 1: Core Platform (Q2 2026)
- [x] DCA smart contracts
- [x] Basic scheduling (daily, weekly, monthly)
- [ ] Web interface
- [ ] STX to BTC exchange integration
- [ ] Testnet launch

### Phase 2: Enhanced Features (Q3 2026)
- [ ] Mobile app (iOS/Android)
- [ ] Advanced scheduling options
- [ ] Portfolio analytics dashboard
- [ ] Price limit orders
- [ ] Mainnet launch

### Phase 3: Automation & Integration (Q4 2026)
- [ ] Auto-rebalancing
- [ ] Multi-asset DCA (other tokens)
- [ ] Yield integration (earn on deposits)
- [ ] Social features (share strategies)
- [ ] API for developers

### Phase 4: Advanced Tools (Q1 2027)
- [ ] AI-powered optimization
- [ ] Tax loss harvesting
- [ ] Portfolio rebalancing
- [ ] Institutional features
- [ ] Cross-chain DCA

## Case Studies

### Case Study 1: The Consistent Saver

**Profile**: Sarah, Software Engineer, 28
**Goal**: Accumulate 0.5 BTC over 3 years
**Strategy**: $100 weekly DCA

**Results After 1 Year**:
- Invested: $5,200
- BTC Acquired: 0.104 BTC (varied by price)
- Average Price: $50,000
- Current Value: $6,240 (at $60,000/BTC)
- Gain: $1,040 (20%)

**Key Insight**: Automated purchases prevented Sarah from panic selling during dips, and she continued buying through volatility.

### Case Study 2: The Market Timer (Failed)

**Profile**: John, Day Trader, 35
**Goal**: Beat DCA by timing the market
**Strategy**: Wait for "perfect" entry

**Results After 1 Year**:
- Waited for $30,000 BTC (never came)
- Made 3 panic buys at local tops
- Average Price: $65,000
- BTC Acquired: 0.08 BTC
- Missed 30% gains waiting for dip

**Key Insight**: Trying to time the market resulted in worse performance than simple DCA strategy.

## Security & Audits

- **Smart Contract Audit**: Completed by [Audit Firm] - [Date]
- **Economic Security Review**: Game theory analysis of DCA mechanism
- **Penetration Testing**: Completed by [Security Firm] - [Date]
- **Bug Bounty**: Up to $50,000 for critical vulnerabilities
- **Insurance**: $5M coverage for smart contract failures

## Best Practices

### For New Users
1. **Start Small**: Begin with amounts you're comfortable with
2. **Stay Consistent**: Don't stop during downturns
3. **Think Long-Term**: DCA works best over years, not weeks
4. **Top Up Regularly**: Keep balance funded for uninterrupted purchases
5. **Don't Obsess**: Check dashboard weekly, not hourly

### For Advanced Users
1. **Tax Planning**: Consider tax implications of purchase frequency
2. **Rebalancing**: Adjust amounts as income changes
3. **Multiple Plans**: Run different strategies simultaneously
4. **Price Limits**: Use limit orders in extreme volatility
5. **Partial Withdrawals**: Take profits systematically if desired

### Common Mistakes to Avoid
- ❌ Stopping DCA during bear markets
- ❌ Increasing amounts dramatically near tops
- ❌ Constantly changing strategy
- ❌ Forgetting to top up balance
- ❌ Checking price after every purchase

## FAQ

**Q: How is RecurBit different from exchange DCA features?**
A: RecurBit is non-custodial, transparent, and built on Bitcoin-secured blockchain. You control your funds and Bitcoin at all times.

**Q: What happens if I run out of funds?**
A: Purchases are skipped until you deposit more. Your plan remains active and resumes when funded.

**Q: Can I change my purchase amount?**
A: Yes, modify your plan anytime. Changes apply to future purchases, not past ones.

**Q: Is DCA better than lump sum investing?**
A: DCA reduces risk and volatility impact, but historically lump sum has slightly higher returns. DCA is ideal for regular income earners.

**Q: What if Bitcoin price crashes?**
A: DCA shines during crashes - you buy more Bitcoin at lower prices, lowering your average cost.

**Q: Can I withdraw my Bitcoin anytime?**
A: Bitcoin is sent to your wallet after each purchase. You own it immediately and can use it however you want.

**Q: What are the fees?**
A: 0.5% per purchase plus network fees. No subscription or management fees.

**Q: Is my Bitcoin held by RecurBit?**
A: No, Bitcoin is sent directly to your wallet after each purchase. RecurBit only holds STX temporarily for scheduled purchases.

**Q: Can businesses use RecurBit?**
A: Yes, businesses can use RecurBit for treasury management or recurring Bitcoin purchases.

**Q: What exchanges does RecurBit use?**
A: RecurBit integrates with DEXs on Stacks for trustless STX→BTC conversion.

## Contributing

We welcome contributions from the community!

### How to Contribute
1. Fork the repository
2. Create a feature branch
3. Write tests for new features
4. Submit a pull request
5. Participate in code review

### Development Areas
- Smart contract features
- Frontend development
- Exchange integrations
- Analytics tools
- Documentation

## Community

- **Website**: [recurbit.io](https://recurbit.io)
- **Documentation**: [docs.recurbit.io](https://docs.recurbit.io)
- **Discord**: [discord.gg/recurbit](https://discord.gg/recurbit)
- **Twitter**: [@RecurBit](https://twitter.com/recurbit)
- **Telegram**: [t.me/recurbit](https://t.me/recurbit)
- **GitHub**: [github.com/recurbit](https://github.com/recurbit)

## Support

- **Email**: support@recurbit.io
- **Help Center**: [help.recurbit.io](https://help.recurbit.io)
- **FAQ**: Comprehensive FAQ section
- **Tutorial Videos**: Step-by-step guides
- **Community Forum**: Ask questions and share strategies

## License

MIT License - see [LICENSE](LICENSE) file for details

## Resources

- [Stacks Documentation](https://docs.stacks.co)
- [Clarity Language Reference](https://docs.stacks.co/clarity)
- [Dollar Cost Averaging Guide](https://www.investopedia.com/terms/d/dollarcostaveraging.asp)
- [Bitcoin Investment Strategies](https://bitcoin.org)

## Disclaimer

RecurBit is a tool for automated Bitcoin purchases. Cryptocurrency investing involves risk of loss. Past performance does not guarantee future results. Only invest what you can afford to lose. This is not financial advice - consult with a financial advisor for personalized guidance.

---

**RecurBit** - Automate your Bitcoin journey. Stack sats, not stress. 🔄₿

*Set it. Forget it. Stack it.*
