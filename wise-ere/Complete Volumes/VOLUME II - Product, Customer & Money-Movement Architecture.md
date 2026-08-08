# VOLUME II — Product, Customer & Money-Movement Architecture: A Forensic Reverse-Engineering of Wise plc / Wise Group

*Analytical cut-off: 8 August 2026. FY2025 = year ended 31 March 2025 (IFRS, GBP, audited). FY2026 = year ended 31 March 2026 (US GAAP, USD; results released 25 June 2026). Where a base is mixed, it is flagged.*

**Evidence labels:** CONFIRMED FACT · COMPANY CLAIM · THIRD-PARTY ESTIMATE · ANALYTICAL INFERENCE · HYPOTHESIS · UNKNOWN.

---

## II.0 Orientation

Wise sells three customer-facing "solutions" built on one shared infrastructure: the **Wise Account** (personal), **Wise Business** (SMEs), and **Wise Platform** (banks/enterprises). [CONFIRMED FACT — FY2025 report] Beneath them sit shared commercial primitives: cross-border transfer, currency conversion, multi-currency balance holding, local account details, the debit card, receiving, interest/Assets, and the API. This volume takes each apart.

Central operating insight, stated up front: **a "cross-border" Wise transfer usually involves no money crossing a border for that specific customer.** Wise holds prefunded local currency pools and local payment-system access at both ends; the sender pays into a Wise account domestically, and Wise pays the recipient from a Wise account domestically in the destination country. The two domestic legs are linked only by an internal ledger entry. Money crosses borders periodically, in bulk, when Wise **rebalances** depleted pools — not per transaction. This is confirmed by Wise's own FY2025 CEO letter, which describes "a new global payments network that directly connects local banks and payment systems at both ends of every transaction, bypassing the traditional correspondent networks used by banks and other payment services, eliminating costly intermediaries and outdated processes." [CONFIRMED FACT]

---

## II.1 Product Universe

### Product decomposition

| Product / capability | Target customer | Job-to-be-done | Primary legal entity (by region) | Regulatory basis | Pricing mechanism | Revenue type | Classification |
|---|---|---|---|---|---|---|---|
| International transfer | Personal + Business | Move money abroad cheaply/fast | Wise Payments Ltd (UK EMI); Wise Europe SA (BE PI); Wise US Inc (MSB/MTL + CFSB) | E-money / payment institution + MTL | Fixed fee + variable % (from ~0.33%) on converted amount | Cross-border revenue | Monetization / Acquisition |
| Currency conversion (in-account) | Both | Convert held balances | Same as above | EMI/PI | From ~0.33–0.43% conversion fee | Cross-border revenue | Monetization |
| Multi-currency balance | Both | Hold 40+ currencies | Wise Payments Ltd etc. | E-money issuance | Free to hold | Enables interest income | Retention / Infrastructure |
| Local account details | Both | Receive "like a local" | Regional entity | Passported partnerships / direct rail access | Free (personal); one-off setup fee for some business details | Indirect (drives balances) | Acquisition / Retention |
| Wise debit card | Both (US business cards discontinued 2023) | Spend balances globally | Issued by CFSB in US; Mastercard/Visa program elsewhere | Card-scheme licence via issuer | FX conversion fee; ATM fees over allowance | Card & other revenue (interchange + fees) | Monetization / Retention / Data |
| Digital/virtual cards | Both | Online / mobile-wallet spend | Same as card | Same | Free to generate | Interchange | Retention / Data |
| Interest / Assets | Both (30 countries) | Earn yield on idle balances | Wise Assets UK Ltd; Wise Assets Europe AS | Investment-services licences (e.g. AU AFSL) | Annual mgmt fee ~0.27–0.56% | Fee + AUC growth | Retention / Defensive |
| Batch payments | Business | Pay ≤1,000 payees per file | Regional entity | PI/EMI | Per-transfer fee (each leg priced individually) | Cross-border revenue | Monetization / Retention |
| Invoicing / QuickPay (QR) | Business | Get paid | Regional entity | PI/EMI | Free feature | Indirect | Acquisition / Retention |
| Direct debits | Business (US) + EEA | Pay recurring bills | Regional entity | PI/EMI | Standard fees | Retention | Retention |
| Accounting integrations (Xero, QuickBooks, NetSuite) | Business | Reconcile automatically | N/A (software) | N/A | Free | Switching-cost driver | Retention / Defensive |
| API | Business + Platform | Automate payments | Regional entity / partner contract | PI/EMI + partner model | Same transfer fees; integration/licence fees for Platform | Cross-border + Platform | Infrastructure / Strategic optionality |
| Wise Platform | Banks, fintechs, enterprises | Embed cross-border, accounts, cards | Partner contracts with Wise entities | Correspondent / embedded / enterprise models | Cost+margin transaction fee; integration/licence fees | Cross-border (partner volume) | Infrastructure / Strategic optionality |

**Key confirmations:** batch payments up to 1,000 payees/file, each transfer priced individually [CONFIRMED FACT]; US business debit cards discontinued 2023 [CONFIRMED FACT]; card conversion fees "from 0.33%," ATM allowances vary by region (US: free up to $100/2 withdrawals then $1.50 + 2% over $100; AU: free to A$400/month then 2.69% from 1 May 2026; India travel card free to $200) [CONFIRMED FACT — Wise pricing pages]; Assets/Interest live in 30 countries since first UK launch September 2021 [CONFIRMED FACT — FY2025 report].

**Strategic classification logic.** *Acquisition:* international transfer (the original wedge; word-of-mouth driven — Wise's FY2025 report states "In FY2025 our marketing spend was £53.8 million, an increase of 47%, with our Marketing team growing by 30%" [CONFIRMED FACT — Wise FY2025 report]). *Retention:* Wise Account balances, card, Assets, business integrations. *Monetization:* transfer fees, card FX/interchange, interest income. *Infrastructure/optionality:* Wise Platform and the API.

---

## II.2 Customer Segmentation

FY2025 headline: **15.6m active customers** (Personal 14.87m; Business 0.697m). [CONFIRMED FACT] FY2026 (Wise Group plc FY2026 results, 25 June 2026): "support 19 million people and businesses move $243 billion across the world last year… Customer holdings grew 40% in FY26 to $39 billion and card spend grew 37% to $44 billion." [CONFIRMED FACT] Personal was ~73% of volume (£106.4bn of £145.2bn) and Business ~27% (£38.8bn) in FY2025. [CONFIRMED FACT]

| Segment | Geography (typical) | Main use case | Frequency | Product mix | Acquisition | Switching cost | Price sensitivity |
|---|---|---|---|---|---|---|---|
| Migrants / remittance senders | UK/EU/US/AU → India, Philippines, LatAm, Africa | Send money home | High, recurring | Transfer only | Word-of-mouth | Low | High |
| Expats / dual-life | UK-EU, US-anywhere | Hold multiple currencies, local details | Medium | Account + card + transfer | WoM / organic | Medium-high | Medium |
| International workers / digital nomads | Global | Receive salary, spend abroad | High | Account + card + local details | Organic | Medium-high | Medium |
| Travelers | Global (esp. AU, UK, EU) | Spend abroad without FX markup | Bursty | Card + balances | WoM | Low-medium | Medium |
| Freelancers / sole proprietors | India, LatAm, EE Europe, SE Asia | Get paid by foreign clients | Medium-high | Business receive + convert | Organic / marketplace | Medium | Medium |
| SMEs | Global | Pay suppliers/contractors, receive | Medium-high | Business account, batch, cards, API | Organic / referral | High (integrations) | Medium |
| Larger businesses / marketplaces | Global | Mass payouts | High | API, batch | Sales | High | Low-medium |
| Banks / fintechs / enterprises (Platform) | Global | Embed cross-border | Continuous | Platform API / SWIFT | Enterprise sales | Very high | Low |

Personal VPC (volume per customer) Q4 FY2025 = £3,200, +7% YoY. [CONFIRMED FACT — FY2025 report] Business generates far higher volume per customer: ~£55.6k (£38.8bn / 0.697m) vs Personal ~£7.2k. [ANALYTICAL INFERENCE from FY2025 figures]

---

## II.3 Jobs to Be Done (matrix)

| Segment | Trigger | Functional job | Economic job | Emotional/trust job | Workaround | Switch trigger | Repeat reason | Churn reason |
|---|---|---|---|---|---|---|---|---|
| Migrant | Payday / family need | Get NGN/INR/PHP to a bank account | Maximise amount delivered | "Will it arrive safely?" | Bank wire, MoneyGram, hawala | Discovered hidden bank markup | Predictable low cost, speed | Corridor suspended (e.g. NGN history) |
| Expat | Move country / paid in 2 currencies | Hold + convert | Avoid double FX | Bank-like reliability | Two bank accounts | Mid-market rate + card | Balances + card daily use | Wants deposit insurance |
| Freelancer | Foreign client invoice | Receive USD/EUR/GBP locally | Avoid PayPal 3–4% | Legitimacy/compliance (RBI purpose code) | PayPal, Payoneer | Local account details | Reconciliation, low fees | Compliance friction |
| SME | Scaling cross-border payables | Batch-pay suppliers/contractors | FX transparency, treasury control | Audit trail | Bank + spreadsheets | Accounting integration | Switching cost of integrations | Compliance holds; no lending |
| Bank (Platform) | Legacy correspondent too slow/costly | Offer instant cross-border in-app | New fee income, retention | Regulatory comfort | SWIFT correspondent | Wants speed without rebuild | Deep integration | Build own rails |

Usage archetypes to distinguish (per prompt): transfer utility; primary multi-currency account; travel tool; business operating account; cross-border payable/receivable tool; embedded infrastructure. FY2025: ~50% of personal and ~60% of business customers use multiple features — evidence of migration from single-use "transfer utility" to "account." [CONFIRMED FACT — FY2025 report]

---

## II.4 Customer Journey (stage-by-stage)

| Stage | Customer action | Wise system | Entity | Data generated | Compliance obligation | Friction / failure point | Cost / KPI |
|---|---|---|---|---|---|---|---|
| Discovery | Comparison, WoM | Web / pricing calculator | Marketing | Intent, corridor | — | Price disbelief | CAC; WoM % |
| Signup | Create account | Onboarding | Regional entity | PII | KYC prep | Abandonment | Signup conversion |
| Verification | Upload ID | KYC/KYB engine | Regional entity | ID docs, selfie | KYC/AML, CDD | Doc rejection; KYB up to 10 days | Verification pass rate |
| Funding | Pay in | Pay-in rails (FPS, SEPA, ACH, card) | Regional entity | Payment event | Source-of-funds | Funding fails, card decline | Instant-funding % |
| Currency select | Choose corridor | Quote API | Regional entity | Quote | — | Rate confusion | — |
| Conversion | Confirm | FX/pricing engine | Regional entity | Locked rate (30 min) | — | Rate expiry | Take rate |
| Transfer | Submit | Transfer engine | Regional entity | Transfer object | Purpose code (India), sanctions | — | Volume |
| Authorization | — | State machine | Regional entity | State transitions | — | — | — |
| Compliance/fraud | (invisible) | Screening | Regional entity | Screening result | Sanctions, transaction monitoring | Compliance hold | False-positive rate |
| Clearing/settlement | (invisible) | Payout + Treasury Ledger | Regional entity | Ledger postings | Safeguarding | Payout-rail outage | Instant % |
| Beneficiary receipt | Recipient credited | Local-rail payout | Local entity/partner | Confirmation | — | Wrong details, bounce-back | Delivery time |
| Notification | Push/email | Notifications | — | Event | — | — | — |
| Support/exception | Contact support | Support/ops | — | Ticket | — | Manual intervention | Contact rate |
| Repeat/cross-sell | Reuse / adopt card | Growth | — | Behavior | — | — | Retention, feature adoption |

Rate lock: mid-market rate locked at authenticated quote, "typically remains valid for 30 minutes"; if unfunded and the rate moves ≥5% adversely, Wise auto-cancels and refunds. [CONFIRMED FACT — Wise API docs + Help Centre] Instant-delivery KPI: Wise's FY2025 report states "approximately 65% of transactions being completed in under 20 seconds"; this rose to "75% of our Q4 payments globally completed in under 20 seconds" (Wise Group plc FY2026 results, 25 June 2026). [CONFIRMED FACT]

---

## II.5 Money-Flow Reconstruction (six-layer separation)

For each corridor we separate **(A) customer-facing event, (B) actual cash movement, (C) internal ledger movement, (D) banking-system movement, (E) payment-system movement, (F) accounting recognition.**

### Corridor 1 — EUR → GBP (balanced, both ends direct rail)
- **A:** Sender in Germany pays EUR; recipient in UK gets GBP; sees mid-market rate, upfront fee, often "instant."
- **B:** EUR moves domestically from sender's bank to Wise's EUR account (SEPA / SEPA Instant); GBP moves domestically from Wise's GBP account to the recipient via UK Faster Payments. No EUR or GBP crosses a border for this transaction.
- **C:** Wise Europe SA's EUR pool credited; Wise Payments Ltd's GBP pool debited; internal FX conversion booked at wholesale rate; the two legs linked by a single ledger transaction ID.
- **D:** Wise's EUR safeguarding account (JPMorgan Chase is the named EU-cash bank per Volume I) receives; Wise's GBP account / Bank of England settlement account pays.
- **E:** Inbound SEPA / SEPA Instant; outbound UK Faster Payments (Wise is a direct participant with a Bank of England settlement account).
- **F:** Wise recognises fee revenue on conversion; the spread between the customer mid-market rate and wholesale execution is a treasury item; the customer balance is a liability throughout.
- **Cross-border reality:** ~0% for this transaction; periodic rebalancing only. [ANALYTICAL INFERENCE + CONFIRMED FACT on rail access]

### Corridor 2 — GBP → USD
Inbound GBP via Faster Payments to Wise UK; outbound USD via US rails (ACH / wire) from Wise US Inc's USD account. Sender-contracting entity = Wise Payments Ltd (UK); payout entity = Wise US Inc. Internal ledger links the legs; the USD pool depletes over time and needs rebalancing.

### Corridor 3 — USD → EUR
Inbound USD via ACH to Wise US; outbound EUR via SEPA from Wise Europe SA — the reverse of Corridor 1's dollar leg.

### Corridor 4 — Africa / emerging-market payout (NGN status)
- **NGN caveat (per prompt):** Wise's NGN history is stop-start — naira payouts launched 2015, suspended May 2016, resumed October 2017, suspended 2020, USD-to-Nigeria suspended November 2022, and NGN payouts resumed 2024 after the Central Bank of Nigeria's January 2024 directive requiring remittances be paid in naira (to bank accounts, or cash below the $200 equivalent). As of 2026 Wise supports **sending to Nigeria in NGN** (recipient credited in naira "directly from Wise's local bank account"), but **NGN is not a supported *sending* currency** and Wise does not offer NGN balances/cards to Nigerian-resident users. [CONFIRMED FACT — Wise send-money page + Tekedia / Fintech Magazine Africa] Why NGN is hard: FX scarcity, repeated regulatory reversals, inability to source true mid-market liquidity, and reliance on local partners. [CONFIRMED FACT]
- **Six-layer:** Sender pays USD/GBP/EUR domestically; Wise converts; the NGN payout is made locally through a Nigerian partner/liquidity arrangement to the recipient's bank account. The inbound leg never reaches Nigeria; only the NGN payout is local.

### Corridor 5 — USD → INR (regulatorily distinctive)
- **Inward to India** runs under RBI's cross-border regime. **Wise Payments India Private Limited** holds RBI **Payment Aggregator – Cross-Border (PA-CB Inward)** authorisation (in-principle June 2025) for business receipts; historically Wise UK worked with **local partner banks in India** — e.g. **IndusInd Bank's "Indus Fast Remit"** platform, integrated via Wise Platform from June 2023 (Wise's first India partner) — to deliver inward remittances with RBI approval. **Vaho Forex Private Limited** holds RBI **Authorised Dealer Category II (AD-II)** for **outward** remittance and forex cards. [CONFIRMED FACT — Wise regulatory page + IndusInd/PRNewswire]
- **Purpose codes:** every inbound INR credit must carry an RBI purpose code (e.g. family maintenance, P0802 software services, P1002 commissions); Wise builds purpose-code selection into the flow. [CONFIRMED FACT — Wise India blog]
- **Payout rails:** INR delivered to bank accounts (including NRE/NRO) or UPI IDs via India's domestic rails (IMPS/NEFT and UPI). [CONFIRMED FACT]
- **Outward from India:** operationalised under AD-II in FY2025, removing the historical ~US$5,000 per-transaction cap; per-transaction limit later ~₹25 lakh (~$30,000) after the June 2025 PA-CB approval; subject to LRS and permitted-purpose constraints (education, travel, medical). [CONFIRMED FACT — FY2025 report + third-party]
- **Six-layer:** Sender in the US pays USD domestically to Wise US; Wise converts USD→INR; the INR payout is made locally in India via partner/rails to the beneficiary. Documentation (purpose code and beneficiary details for inward; LRS declarations for outward) is required.

### Corridor 6 — Wise Business payment (batch)
An SME uploads a file of ≤1,000 payees; each payment is a discrete transfer object priced individually; funding is one debit from the business's Wise balance; each payout routes to the cheapest local rail. The ledger books each leg; reconciliation is by transfer ID.

### Corridors 7–9 — card purchase, ATM withdrawal, Wise Platform transaction — see II.11 and II.13.

---

## II.6 Transaction Teardown (representative EUR→GBP, ~18 steps)

1. Sender initiates; the **Quote API** returns a locked mid-market rate + fee (30-min validity). [CONFIRMED FACT]
2. Sender selects recipient; recipient added to quote (fees, delivery estimate, payout network confirmed).
3. Sender funds via SEPA / SEPA Instant into Wise Europe SA's EUR account. Transfer state = `incoming_payment_waiting`. [CONFIRMED FACT — Wise API]
4. Funds arrive; state → `processing`; **the exchange rate locks and the transfer can no longer be cancelled via API.** [CONFIRMED FACT]
5. **KYC status** confirmed (already-verified sender).
6. **Sanctions screening** on sender, recipient, and payment.
7. **Transaction monitoring / fraud scoring** (Wise: "Processing… means we're doing behind-the-scene activities before the money gets sent to the recipient, such as AML, compliance and fraud checks"). [CONFIRMED FACT]
8. On pass, state → `funds_converted` (FX booked source→target). [CONFIRMED FACT]
9. The **Treasury Ledger** posts double-entry: EUR pool +, GBP pool −, at wholesale rate, "calculating our assets and liabilities with unwavering accuracy and in real time" and feeding "trading teams to manage foreign exchange exposure risks and to ensure each entity has enough liquidity." [CONFIRMED FACT — Wise Treasury Ledger engineering job specs]
10. Liquidity check on the GBP pool; payout initiated.
11. Outbound GBP via **UK Faster Payments** from Wise's settlement account. State → `outgoing_payment_sent` — "the final state… it doesn't mean the money has arrived in the recipient's bank account, just that we have sent it from ours." [CONFIRMED FACT]
12. Recipient's bank credits recipient (often <20s).
13. **Notification** to sender and (if email given) recipient.
14. **Reconciliation:** ledger postings matched to bank-statement lines / payment-system position (events reconciled by `occurred_at` since ordering isn't guaranteed). [CONFIRMED FACT]
15. **Fee** recognised as revenue; **FX spread** recognised as treasury income/cost.
16. **Third-party cost:** rail fees (Faster Payments marginal cost is very low), any partner cost.
17. **Failure branches:** `bounced_back` (wrong details) → redelivery or `funds_refunded`; `charged_back` (pay-in problem, "can happen from any other state"); `cancelled` (never funded). Rollback transitions supported. [CONFIRMED FACT]
18. **Counterparty / liquidity risk** borne by Wise on its pools and safeguarding banks; the customer bears authorised push-payment fraud risk.

The full Wise API happy-path state chain is `incoming_payment_waiting → processing → funds_converted → outgoing_payment_sent`, with the unhappy path `outgoing_payment_sent → bounced_back → processing → cancelled → funds_refunded`, plus `charged_back` and `unknown`. [CONFIRMED FACT — Wise API docs]

---

## II.7 Local Payment-Rail Architecture

| Rail | Access type | Entity / mechanism | Significance |
|---|---|---|---|
| UK Faster Payments | **Direct** participant since 2018 — first non-bank, with a Bank of England RTGS settlement account | Wise Payments Ltd | Instant GBP in/out; foundational |
| CHAPS | Indirect / via BoE where needed | Wise Payments Ltd | High-value GBP |
| SEPA / SEPA Instant | Access in EEA | Wise Europe SA | EUR in/out |
| Hungary (MNB instant) | Direct (2020) | Wise Europe SA | First non-bank in HU |
| Singapore FAST | Direct | Wise Asia-Pacific | SGD instant |
| Australia NPP | Direct | Wise Australia | AUD instant |
| Philippines InstaPay / PesoNet | Direct (2024) | Local arrangement | PHP instant — sixth direct connection |
| Brazil Pix | Direct (approval FY2025, live) | Wise Brasil | BRL instant |
| Japan Zengin | Direct (first non-bank approval FY2025) | Wise Payments Japan | JPY |
| Malaysia PayNet | Direct | Local arrangement | MYR |
| US ACH / Fedwire / RTP / FedNow | **Indirect** via CFSB / partner banks | Wise US Inc + CFSB | USD — no direct Fed access |
| India IMPS / NEFT / UPI | **Indirect** via partner banks | Wise India / Vaho / partners | INR payout |
| Canada | Payments Canada member (for the upcoming Real-Time Rail) | Wise entity | Prospective |

**Direct-connection count is a moving target.** The FY2025 report says the Philippines was "our sixth direct integration to date" and that Brazil Pix and Japan Zengin "will increase our direct connections to eight once live"; some marketing materials still cite "5 direct connections." [CONFIRMED FACT — disagreement reflects timing] **Do not infer direct access from the ability to pay a market** — most markets are reached via partners/local pools. [CONFIRMED — prompt discipline]

Faster Payments mechanics: as a directly connected settling participant, Wise holds a Bank of England settlement account and prefunds cash to cover its maximum possible net debit position — which is why it can settle GBP without a sponsor bank and capture the marginal-cost advantage. Wise was the first non-bank PSP granted a BoE RTGS settlement account (2018), a change enabled by the 2017 opening of RTGS to non-banks. [CONFIRMED FACT — Pay.UK / Bank of England / UK Finance / Forbes]

---

## II.8 Wise's Cross-Border Network

**Traditional correspondent banking (baseline):** a payment hops through multiple nostro/vostro-holding banks over SWIFT; each hop adds fees, an FX markup, delay, and opacity. Wise replaces the multi-hop chain with **two synchronized domestic payments** linked by an internal ledger.

**Wise architecture components:** local collection accounts; local payout accounts; prefunded local currency pools; internal matching/netting; treasury rebalancing; residual correspondent usage for thin corridors; direct payment-system connectivity in up to 8 markets; liquidity buffers; safeguarding accounts; operational reconciliation. Wise cites "50+ local liquidity partners" and "90+ banking partners." [CONFIRMED FACT]

**Answers to the prompt's network questions:**
- **What actually crosses a border?** For an individual transaction on a well-covered corridor, essentially nothing — both legs are domestic. Cross-border movement occurs only in periodic bulk **rebalancing**. [ANALYTICAL INFERENCE, strongly supported]
- **When can Wise satisfy both sides from local pools?** When corridor flows are roughly balanced or the target pool has liquidity (GBP-EUR, USD-CAD are near-symmetric). [THIRD-PARTY ESTIMATE]
- **When must funds move internationally?** When a pool is structurally depleted by one-directional flow (e.g. net-outbound remittance corridors), requiring wholesale FX + international funding to top up.
- **What creates rebalancing needs?** Net directional imbalance in a corridor.
- **How does scale affect matching?** Higher volume raises the probability of internal offset and reduces the share of flow needing external FX/rebalancing — a genuine scale economy that lowers unit cost, which Wise recycles into lower prices. Evidence: the take rate fell from 0.67% to 0.53% in Q4 FY2025 (Wise's CEO letter: "this year, our global take rate reduced from 0.67% to 0.53% in Q4 FY2025 — our lowest to date"), then to ~0.52% by Q1 FY2026 and averaged ~52bps for FY2026. [CONFIRMED FACT]
- **Where does Wise still depend on correspondents?** Thin/illiquid or tightly regulated corridors (parts of Africa, some emerging markets), and USD, where it relies on CFSB and partner banks.

---

## II.9 FX Engine

**Five-way rate decomposition (per prompt):**
1. **Reference/mid-market rate** — the midpoint of interbank buy/sell. Wise states it sources this from "multiple independent rate providers," updated in real time during market hours, to 6 significant digits (rounding the 7th digit ≥5 up). [CONFIRMED FACT — Wise Help Centre] Wise does **not** name a specific vendor (Reuters/Bloomberg). [UNKNOWN]
2. **Customer quoted rate** = the mid-market rate (no markup) — Wise's core promise.
3. **Explicit fee** = fixed + variable %, shown upfront.
4. **Wholesale execution rate** — the rate at which Wise actually converts/holds inventory.
5. **Wise's realized economic spread** = the gap between wholesale execution and the customer mid-market rate, plus net treasury gains/losses on inventory.

**Operational meaning of "mid-market rate":** it is not a marketing abstraction but a real, externally verifiable benchmark Wise commits to give customers, monetising via the visible fee rather than a hidden spread. This is the structural reason Wise is cheaper than banks: its cost is the visible fee, whereas banks bury a 2–5% markup in the rate. [CONFIRMED FACT]

**Rate refresh & lock:** the public converter refreshes roughly every 60 seconds; a transaction quote locks for ~30 minutes; a 5% adverse-move safeguard auto-cancels unfunded transfers ("If the mid-market rate drops by 5% or more before we receive your funds, we will automatically cancel and refund your transfer"). The market closes Friday 5pm New York and reopens Monday 9am Auckland. [CONFIRMED FACT — Wise Help Centre]

**Treasury, exposure & hedging:** the Treasury Ledger feeds trading teams that "manage foreign exchange exposure risks" and "ensure each entity has enough liquidity." [CONFIRMED FACT — Wise engineering job specs] Wise's US Form 20-F confirms exposure to FX and interest-rate market risk and mitigation "through financial hedges or collateralization." [CONFIRMED FACT — Wise Group plc 20-F draft] Internal matching/netting reduces net open exposure; residual exposure is short-duration and hedged. [ANALYTICAL INFERENCE] A discrete FX-trading P&L line is not separately disclosed in preliminary results. [UNKNOWN]

---

## II.10 The Wise Account — Legal & Economic Model

**What it legally is:** an **e-money / payment account**, NOT a bank deposit. In the UK the contract is with **Wise Payments Ltd** (FCA-authorised EMI, FRN 900507), governed by English law. [CONFIRMED FACT]

**Why it looks bank-like but isn't:** it offers local account details (IBAN, sort code, US routing/account number), a debit card, direct debits, and multi-currency balances — but Wise **does not lend out** customer money. Instead it **safeguards**: 100% of customer funds held separately from Wise's own money. Wise's own framing: "We don't lend out your money. Banks do… Because we're not lending your money, we handle it differently by safeguarding it." [CONFIRMED FACT]

**Follow-the-money — safeguarding structure:** roughly ~60% in secure liquid assets (government securities/MMFs) and ~40% cash at banks (Volume-I figure). The UK entity's named safeguarding institutions: Barclays Bank PLC (cash + secure liquid assets), Citibank N.A., JPMorgan Chase Bank N.A., Deutsche Bank AG London, Hamburg Commercial Bank, Bank of America. [CONFIRMED FACT — Wise UK safeguarding disclosure] Assets/Interest money (Wise Assets UK Ltd) is held differently as investment products, with distinct FSCS treatment. [CONFIRMED FACT]

**Deposit insurance:** **No FSCS/FDIC deposit insurance** on Wise balances (they are e-money, not deposits). US customers may receive **FDIC pass-through** insurance where funds sit at FDIC-insured partner banks under specific conditions. [CONFIRMED FACT — Wise blogs] On insolvency, safeguarded funds are ring-fenced from Wise's creditors; an administrator returns them to customers, typically over weeks, with no top-up if a shortfall arises inside the pool. [CONFIRMED FACT]

**Customer holdings scale:** £21.5bn customer holdings FY2025 (incl. £4.5bn Assets under custody); Wise states "As of 30 June 2025, our customers are trusting us with the equivalent of 18.1 billion GBP in their Wise accounts." FY2026: $39bn customer holdings, of which ~$9bn in Wise Assets (Volume I). [CONFIRMED FACT]

---

## II.11 Wise Card — Transaction Teardown

**Issuance & network:** In the US the card is issued by **Community Federal Savings Bank (CFSB), member FDIC, under licence from Mastercard International**; you must hold a Wise Account with a ≥$20 balance to obtain a card; the Cardholder Agreement (v2.2, last updated 21 August 2025) is between the customer and CFSB, with Wise providing servicing "on behalf of CFSB." [CONFIRMED FACT] Elsewhere Wise issues via Mastercard/Visa programs through regional BIN sponsorship. [CONFIRMED FACT]

**Processing:** Wise built the **world's first cloud-based card processing** (AWS/Kubernetes microservices), moving processing in-house to shorten the message chain and cut per-transaction cost. Its services cover card ordering, authorization, and scheme settlement; a "Mastercard connector" normalises scheme messages into a unified Wise interface. [CONFIRMED FACT — Wise Engineering; Kravtsov, Weiming, Menon; Sep 2022]

**Authorization + balance-check + conversion waterfall:**
1. Terminal → acquirer → scheme (Mastercard/Visa) → Wise (as processor/issuer via CFSB in the US).
2. Wise checks the available balance in the transaction currency.
3. **Currency selection logic:** if the customer holds enough of the spending currency, no conversion (free). If not, "smart conversion" converts from the balance carrying the **lowest possible fee**, at the mid-market rate. [CONFIRMED FACT — Wise Help/AU blog]
4. Fraud/limit checks; approve/decline flows back to the terminal in seconds.
5. Customers are advised to always pay in the **local currency** to avoid merchant dynamic currency conversion (DCC). Independent research (German consumer group Stiftung Warentest, reported by The Motley Fool) found DCC raised prices "by amounts ranging from 2.6% to 12.0%," with extreme cases to 18%. [THIRD-PARTY — Stiftung Warentest]

**Economics:**
- **Interchange:** merchant-side; flows to the issuer (CFSB) and is shared with Wise — a "card & other" revenue stream. Wise's investor materials confirm revenue "from our account features, such as debit card interchange fees." [CONFIRMED FACT]
- **FX conversion fee:** from 0.33% when the held currency is insufficient.
- **ATM:** region-specific free allowances then percentage fees (US: $1.50 + 2% over $100 / 2 withdrawals; AU: 2.69% over A$400/month from 1 May 2026; India travel card free to $200).
- **Scheme/processor fees:** paid to Mastercard/Visa; reduced by in-house processing.
- **Chargebacks/fraud:** handled via scheme dispute rules; card fraud loss borne partly by Wise/issuer per scheme allocation. [ANALYTICAL INFERENCE]

**Strategic role:** the card is primarily a **retention + balance-usage + data** tool that also monetises via interchange/FX — it converts a transfer utility into a daily-use account. FY2026 card spend grew 37% to $44bn (Wise Group FY2026 results). [CONFIRMED FACT]

---

## II.12 Wise Business

**Segment & onboarding:** SMEs, incorporated freelancers, e-commerce sellers, marketplaces, agencies paying contractors. Onboarding requires KYB (registration docs, directors, 25%+ shareholders); complex structures can take up to 10 business days. [CONFIRMED FACT] A one-off setup fee unlocks "Advanced"/receiving features (e.g. £50 UK, $31 US); no monthly fee. UK pricing was restructured on 26 November 2025 (free "Essential" plan without receiving; paid "Advanced"). [CONFIRMED FACT]

**Features:** multi-currency hold (40+); local details (up to ~9–10 send currencies / 20+ receiving); batch payments (≤1,000); multi-user permissions; business debit/expense cards (not US business); direct debits (US); invoicing; QuickPay QR; accounting integrations (Xero, QuickBooks, NetSuite); API. [CONFIRMED FACT]

**Economics vs Personal:** Business is **structurally superior** on volume per customer (~£55.6k vs £7.2k) and holds large balances (£6.6bn FY2025). But it grows slower in customer count (+11% vs Personal +22% FY2025) and has faced onboarding/compliance friction in Europe (paused registrations at points). Business underlying income was £321.8m FY2025 (~24% of £1,362.3m group underlying income). Higher frequency + accounting integrations create higher switching costs and retention. [CONFIRMED FACT / ANALYTICAL INFERENCE]

---

## II.13 Wise Platform (substantial depth)

**What it is:** Wise's infrastructure-as-a-service offering — banks, fintechs, and enterprises embed Wise's cross-border payments, multi-currency accounts, and card issuing via API or SWIFT. [CONFIRMED FACT]

**Three integration models (Wise docs):**
1. **Embedded** — regulated FIs/fintechs offer Wise inside their own UI; the partner's customers have Wise accounts linked to the partner platform, which transacts on their behalf.
2. **Enterprise** — a business uses the API to move its **own** funds (payroll, vendors); Wise's relationship is with the enterprise only, not its customers/recipients.
3. **Correspondent** — regulated FIs (Tier-1 banks, challengers, EMIs, brokerages) route their customers' cross-border payments through Wise; the partner holds a Wise account; the originators usually "are often not aware that Wise is being used to process their transactions." Includes **Correspondent Services** (launched at Sibos with SWIFT) — banks redirect MT/MX (SWIFT) messages to Wise, which "translate[s] them into a local payout executed on Wise's network." [CONFIRMED FACT — Wise docs]

**KYC ownership:** depends on model — Wise-performed or partner-performed CDD/KYC, defined per integration; regulated partners typically retain CDD. [CONFIRMED FACT — Wise docs]

**Settlement/prefunding:** for correspondent, a settlement journal (a list of transfer IDs) precedes a single bank payment; on linking, transfers move to `processing`; with prefunding, "settlement funds must reach Wise before the payout is initiated to the recipient." Sender-name mismatches on the incoming bank payment may require manual intervention. [CONFIRMED FACT — Wise docs]

**Named public partners (role/date where public):**
- **Correspondent/enterprise banks:** Morgan Stanley (corporate cross-border settlements, Dec 2024), Standard Chartered (SC Remit via Wise Platform API), Raiffeisen Bank International (Central/Eastern Europe), UniCredit, BPCE (France), Shinhan Bank (Korea), IndusInd Bank (India inward, June 2023 — first India partner).
- **Embedded accounts/cards:** Nubank (Brazil — global account + international debit card for premium clients), Bank Mandiri (Indonesia), Mox (Standard Chartered's HK digital bank), Tiger Brokers (Singapore debit card), Interactive Brokers (US), Google Pay, Monzo, N26.
- **Other/SME distribution:** Qonto (France — doubled international-transfer adoption), Swan (embedded international payments across Europe), Allica Bank (UK), Moin (Korea), Brex, Bolt, EQ Bank and Wealthsimple (Canada), Itaú Unibanco (Brazil).
- Wise reported **85+ Platform partners** by the Nubank announcement. [CONFIRMED FACT — Finextra / Wise / press]

**Commercial model (Wise's own words):** "Wise Platform pricing follows a cost+margin framework. Because Wise Platform leverages the exact same underlying payment network and infrastructure built for our direct consumers, the marginal cost of processing partner volumes is extremely low, leading to highly attractive unit economics." Revenue = transaction fees + "potential integration and software licensing fees depending on the partnership structure." [CONFIRMED FACT — Wise investor-topics page]

**Scale:** Wise's H1 FY2026 interim report (6 Nov 2025) states: "around 5% of Wise's cross-border volume is driven by Wise Platform, up from 4% as reported at our Owners' Day… we continue to expect this to increase materially, to around 10% in the medium term, and over 50% in our long-term vision." (FY2025 ≈ 4%, up from 3%.) [CONFIRMED FACT] Implementation is quoted in "weeks or months." [COMPANY CLAIM]

**Strategic verdict:** Platform **does** transform Wise from a consumer fintech into payments infrastructure / a financial network. Because Wise monetises regardless of whether the end customer chooses Wise or a partner wrapper (Monzo and N26 run cross-border on Wise rails), Platform is a **flywheel amplifier**: partner volume lowers network unit cost, which funds lower consumer prices, which drives volume. It is plausibly **more strategically valuable long-term than direct consumer distribution** — Wise's own "over 50% in our long-term vision" target for Platform volume signals this — even though the Personal segment (~78% of revenue/income) dwarfs it today. [ANALYTICAL INFERENCE, well-supported]

---

## II.14 Product Dependency / Flywheel Map

Verified loops:
1. **Transfer → Account → Balances → Card → Frequency → Retention.** Supported: ~50% personal / ~60% business use multiple features; card spend $44bn FY2026; balances £17.1bn FY2025. [CONFIRMED FACT]
2. **Balances → Interest income → Profit → Price cuts → Volume.** Supported: interest income is material (FY2025 "first 1% yield" £150.4m + "above first 1% yield" £443.9m); take rate cut to 0.53% (Q4 FY2025) and ~0.52% (FY2026). [CONFIRMED FACT]
3. **Business → Integrations/API → Switching costs → Retention.** Supported: accounting integrations, batch, permissions. [CONFIRMED FACT]
4. **Infrastructure → Platform partners → Volume → Lower unit cost → Better consumer pricing.** Supported by Wise's cost+margin statement and the take-rate trend. [CONFIRMED FACT / INFERENCE]
5. **Internal matching improves with scale → fewer external FX/rebalancing legs → lower cost.** [ANALYTICAL INFERENCE]

---

## II.15 Product Economics by Use Case

| Use case | Fee mechanism | Direct payment cost | FX cost | Card/network cost | Support/fraud/compliance | Contribution economics | Capital/liquidity need |
|---|---|---|---|---|---|---|---|
| Major-corridor transfer (EUR-GBP) | Fixed + ~0.33–0.43% | Very low (direct rails) | Near-zero (matched) | — | Low (automated) | High margin | Prefunded pools |
| Thin-corridor transfer | Higher variable % | Partner fees | Wholesale FX + rebalancing | — | Higher | Lower margin | Higher buffers |
| Card spend (currency held) | Free | — | 0 | Scheme fee (offset by interchange) | Fraud loss | Interchange-positive | Balance float |
| Card spend (conversion) | 0.33%+ | — | Small | Scheme fee | Fraud | Positive | Float |
| ATM over allowance | $1.50 + 2% (US) | ATM operator | Small | Scheme | Low | Positive | Float |
| Business batch | Per-leg fee | Local rails | Matched/wholesale | — | Medium | High | Pools |
| Platform | Cost+margin txn fee (+ integration/licence) | Shared infra (near-zero marginal) | Matched | Optional card | Partner-shared | "Highly attractive" | Shared |
| Interest/Assets | 0.27–0.56% mgmt fee | — | — | — | Low | Fee + retention | Custody |

FY2025 group economics: underlying income £1,362.3m; underlying gross profit £1,025.1m (75% margin); underlying PBT £282.1m (21% margin); reported PBT £564.8m; profit £416.7m; cost of sales £328.1m. [CONFIRMED FACT — FY2025 report]

---

## II.16 Failure & Exception Paths

| Failure | Owner | Customer experience | Money location | Ledger state | Regulatory obligation | Loss exposure |
|---|---|---|---|---|---|---|
| Failed funding | Wise/customer | Transfer stalls | Never left sender bank | `cancelled` | — | None |
| Rate expiry (unfunded) | Wise | Re-quote | With sender | Refund/cancel | — | None |
| ≥5% adverse move | Wise | Auto-cancel + refund | Returned | `funds_refunded` | — | Wise avoids FX loss |
| Compliance hold | Wise | Balance frozen pending review | In safeguarding | `processing` | AML/sanctions | Reputational |
| Sanctions match | Wise | Blocked/reported | Held | `processing` | Report to authority | Regulatory |
| Fraud suspicion | Wise | Delay/review | Held | `processing` | SAR | Fraud loss |
| Wrong beneficiary details | Customer/Wise | Delay or return | Payout bank / en route | `bounced_back` → redelivery or refund | — | Possible mis-payment |
| Beneficiary bank rejection | Beneficiary bank | Returned | Returned to Wise | `bounced_back` → `funds_refunded` | — | Low |
| Card dispute/chargeback | Issuer/scheme | Provisional credit process | Merchant/issuer | `charged_back` | Scheme rules | Shared |
| Payout-rail outage | Rail/Wise | Delay | In Wise pool | `processing` | — | Operational |
| Insufficient pool liquidity | Wise treasury | Delay | Pool | `processing` | — | Rebalancing cost |

Rollback transitions let transfers return to prior states; events are reconciled by `occurred_at` timestamp since ordering isn't guaranteed. [CONFIRMED FACT — Wise API]

---

## II.17 Volume II Reconstruction

**1. Product architecture:** one infrastructure (licences + banking partners + rail connections + Treasury Ledger + FX engine + card processing) → three solutions (Account, Business, Platform) → shared primitives (transfer, convert, hold, receive, card, interest, API).

**2. Customer-segment map:** see II.2 — remittance senders, expats, workers/nomads, travelers, freelancers, SMEs, larger businesses/marketplaces, Platform FIs.

**3. Jobs-to-be-done matrix:** see II.3.

**4. Customer lifecycle:** see II.4.

**5. End-to-end transfer maps:** see II.5–II.6 (EUR-GBP, GBP-USD, USD-EUR, Nigeria/NGN, USD-INR, business batch).

**6. Money vs ledger vs accounting:** the customer-facing balance (a liability), the internal Treasury Ledger (double-entry, real-time), the bank-account balances (safeguarding + operating), the payment-system position, the settlement obligation, and the GL recognition **do not move simultaneously** — the ledger and customer view update in seconds while actual bank/rail settlement and rebalancing lag. [CONFIRMED FACT]

**7. Local payment-rail map:** see II.7 — up to 8 direct connections; US/India/Nigeria via partners.

**8. Wise network architecture:** local pools + two synchronized domestic legs + periodic rebalancing; see II.8.

**9. FX architecture:** mid-market from multiple independent providers; five-way rate decomposition; matching + short-duration hedging; see II.9.

**10. Wise Account legal/economic model:** e-money, safeguarded, not deposit-insured; see II.10.

**11. Card transaction map:** CFSB-issued (US), cloud processing, conversion waterfall; see II.11.

**12. Wise Business architecture:** see II.12.

**13. Wise Platform architecture:** three models, 85+ partners, cost+margin; see II.13.

**14. Product dependency/flywheel:** see II.14.

**15. Exception/failure map:** see II.16.

**16. Major dependencies:** (i) CFSB for US issuing/USD access (the OCC denied Wise's national trust-bank charter in July 2026 per Volume I, preserving CFSB dependency); (ii) safeguarding banks (Barclays, Citi, JPMorgan, Deutsche, Hamburg Commercial, Bank of America); (iii) Mastercard/Visa schemes; (iv) local rails + 90+ banking partners + 50+ liquidity partners; (v) partner banks in India/Nigeria/US; (vi) 65–70+ regulatory licences; (vii) SWIFT for correspondent Platform; (viii) cloud (AWS).

**17. Key unknowns:** exact FX-trading P&L; precise wholesale-execution mechanics and rate vendor; per-corridor internal-match rates; per-partner Platform revenue; exact interchange split with CFSB; internal reconciliation algorithm details.

**18. Ten most important conclusions:**
1. A Wise "cross-border" transfer is two domestic payments; money crosses borders only in periodic rebalancing.
2. Scale improves internal matching, lowering unit cost — a genuine, self-reinforcing moat, evidenced by the take-rate decline from 0.67% to 0.53% (Q4 FY2025) and ~0.52% (FY2026).
3. The Wise Account (e-money, safeguarded, not deposit-insured) is the retention engine that turned a transfer utility into an account; balances (£17.1bn FY2025 / holdings £21.5bn; $39bn FY2026) now drive material interest income.
4. Interest income on customer balances is a large, rate-sensitive profit contributor — and a strategic vulnerability if rates fall.
5. The card is a retention/data/interchange tool, not primarily a standalone revenue engine; in-house cloud processing lowers its cost.
6. Wise Business has structurally superior unit economics (VPC ~£55.6k) but slower customer growth and heavier compliance friction.
7. Wise Platform is the strongest infrastructure play and likely the highest strategic-optionality product, monetising even when competitors win the end customer.
8. Direct payment-rail membership (especially UK Faster Payments with a BoE settlement account) is the hard-won, hard-to-replicate core of the speed/cost advantage.
9. Emerging-market corridors (NGN, and to a lesser degree INR) remain the fragile edge — regulation and FX liquidity, not technology, are the binding constraints.
10. Wise is best understood as **payments infrastructure with a consumer distribution front-end** — a network, not a remittance app.

**Prompt questions answered:**
- **What part is actually cross-border?** Essentially none for a given transaction on covered corridors; only periodic bulk rebalancing.
- **Central operating insight?** Convert one cross-border payment into two synchronized domestic payments linked by an internal ledger, and net flows at scale.
- **Strongest retention product?** The Wise Account (balances + card + local details + Assets).
- **Strongest infrastructure product?** Wise Platform (and the rail/licence/ledger stack beneath it).
- **Most strategically important despite not being the largest?** Wise Platform.
- **What is Wise?** A cross-border **payments network / infrastructure platform** with multi-currency accounts and a consumer/business distribution layer on top — not merely a remittance product.

---

## Caveats
- FY2026 figures (19m customers; $243bn volume; $39bn holdings; $44bn card spend) are US-GAAP/USD; FY2025 figures are IFRS/GBP audited. Mixing bases requires care.
- Several mechanism details (wholesale FX rate vendor, internal reconciliation algorithm, per-partner Platform economics, the interchange split with CFSB, discrete FX P&L) are not publicly disclosed and are labelled UNKNOWN or ANALYTICAL INFERENCE.
- Rail-connection counts and Platform partner counts are time-sensitive and cited as of FY2025/2026 sources; the "5 vs 6 vs 8 direct connections" discrepancy reflects go-live timing, not conflicting facts.
- The DCC cost range (2.6–12%, up to 18%) is from a Stiftung Warentest study reported by third parties, not a Wise publication.
- The Belgian AML criminal investigation of Wise Europe SA (disclosed 1 June 2026, per Volume I) is regulatory context, not a product mechanism, and is not analysed here.
- This is Volume II only. Volume III is not begun.