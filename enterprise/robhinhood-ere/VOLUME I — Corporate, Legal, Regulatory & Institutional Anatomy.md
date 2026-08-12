# ROBINHOOD MARKETS, INC. — EXECUTIVE REGULATORY & ENTITY FORENSIC (EREF)
## VOLUME I — Corporate, Legal, Regulatory & Institutional Anatomy

**TL;DR**
- Robinhood Markets, Inc. (Nasdaq: HOOD) is a Delaware holding company that executes nothing itself; the "real business" is a functional stack of separately registered subsidiaries — chiefly Robinhood Financial LLC (introducing broker) and Robinhood Securities LLC (self-clearing broker) — controlled by founder-CEO Vladimir Tenev through a dual-class share structure.
- The single most consequential structural decision in the firm's history was Robinhood Securities' 2018 move to self-clearing, which put NSCC settlement-risk deposits onto Robinhood's own balance sheet and directly produced the January 2021 crisis.
- The enforcement ledger is the institutional signature: at least eight material regulatory actions (SEC 2020 $65m; FINRA 2021 $70m; NYDFS 2022 $30m; SEC 2025 $45m; FINRA 2025 $29.75m, plus others) show a recurring pattern of controls lagging growth.

---

## I.1 Institutional Identity and History

**CONFIRMED FACT.** Robinhood was founded in 2013 by Vladimir Tenev and Baiju Bhatt, Stanford physics graduates who had previously built high-frequency trading software firms (Celeris and Chronos Research) in New York. The commission-free proposition originated from their observation that incumbent brokers charged per-trade commissions while themselves paying near-zero marginal cost to execute; Robinhood proposed to eliminate the commission and monetize elsewhere.

The company used an exclusivity/waitlist launch that grew to nearly 1 million users on its referral waitlist before the mobile app's 2014 general release (the 2013 landing page reportedly drew roughly 10,000 signups within 24 hours). It raised **$5.73 billion over 14 funding rounds** (1 seed, 2 early-stage, 9 late-stage, 1 debt, 1 post-IPO) from a large investor base including DST Global, Sequoia Capital, Index Ventures, Kleiner Perkins, NEA, Thrive Capital, Ribbit Capital and others; the single largest round was the $3.4 billion Series H on January 29, 2021 (the emergency raise — see I.12).

**CONFIRMED FACT — the IPO.** Robinhood filed confidentially on March 22, 2021 and publicly on July 1, 2021. It listed on Nasdaq under "HOOD" on July 29, 2021 as a conventional underwritten IPO (not a direct listing), led by Goldman Sachs and J.P. Morgan. It priced 55 million shares at $38.00 (the low end of the $38–42 range); Robinhood itself offered 52,375,000 shares, for **net proceeds of approximately $1.89 billion** and a valuation of about $32 billion. Co-founders Vlad Tenev and Baiju Bhatt each sold about $50 million worth of stock. **The unusual feature:** Robinhood reserved up to 35% of IPO shares for its own retail customers via its IPO Access platform — an inversion of the usual practice of allocating chiefly to institutions. The stock closed down 8.37% at $34.82 on debut (having dropped as much as ~10–11% intraday), leaving a market capitalization of roughly $29 billion.

**ANALYTICAL INFERENCE.** Robinhood was built to be a commission-free retail equities app and became, by 2025–2026, a multi-product financial-services group spanning equities, options, crypto, futures/event contracts, cash management, credit cards, retirement accounts and RIA custody. The through-line is a consumer-interface company that repeatedly acquires or builds the regulated entity needed to host each new product.

## I.2 The Broker-Dealer Stack (RE-CUT)

**CONFIRMED FACT.** Robinhood Markets, Inc. is a holding company and is not itself FINRA-registered; it does not execute trades, hold crypto or lend money. In Tenev's own February 2021 written congressional testimony: "Robinhood Markets, Inc., as a parent company that wholly owns broker-dealer subsidiaries, need not be registered." The regulated activities are divided across separately registered legal persons. The material entities:

**1. Robinhood Markets, Inc. (RHM)** — Delaware holding company; Nasdaq issuer (HOOD); SEC reporting company. Function: capital-raising, group governance, ownership. No customer-facing role. Regulator: SEC (as issuer).

**2. Robinhood Financial LLC (RHF)** — the **introducing broker-dealer**. Registered with the SEC under the Exchange Act; FINRA member; SIPC member. Holds the customer relationship — it "introduces retail users to purchase and sell equities, options and cryptocurrencies through our platform" and takes customer trade orders. It is exempt from SEC Rule 15c3-3 under the (k)(2)(ii) provision (it does not itself hold customer assets or maintain the reserve). Regulators: SEC, FINRA, SIPC oversight; state securities regulators.

**3. Robinhood Securities LLC (RHS)** — the **clearing broker-dealer**. SEC-registered; FINRA member; SIPC member; NSCC/DTCC and OCC member. Registered with the SEC as a clearing broker on October 13, 2017; began clearing customer transactions on May 8, 2018. It executes customer orders received from RHF by routing them to market makers, and clears and settles trades. It holds customer assets and carries the Rule 15c3-3 possession-and-control and reserve obligations. This is the entity that received the NSCC deposit demand in January 2021.

**4. Robinhood Crypto LLC (RHC)** — the crypto entity (NMLS ID 1702840). Holds state money-transmitter licences and (historically) a NYDFS virtual-currency licence. Holds customers' cryptocurrency and routes crypto orders to market-making venues. It is NOT a FINRA or SIPC member; crypto is not SIPC-protected. Regulators: state money-transmitter regulators, NYDFS, FinCEN (BSA).

**5. Robinhood Derivatives LLC (RHD)** — the futures/event-contracts entity; a registered futures commission merchant (FCM) with the CFTC and NFA member (NFA ID 0424278). Robinhood obtained the FCM by acquiring a spare FCM entity from Marex in early 2024. Offers futures and options on futures (CME products rolled out from January 2025), and event/prediction-market contracts (through KalshiEX LLC, ForecastEX, LLC and Rothera Exchange and Clearing LLC). Regulators: CFTC, NFA.

**6. Robinhood Money LLC (RHY)** — the spending/cash-management entity (NMLS ID 1990968); a licensed money transmitter. Not a FINRA/SIPC member. Regulators: state money-transmitter regulators.

**7. Robinhood Credit, Inc. (RCT)** — the credit-card entity behind the Robinhood Gold Card. It is a financial-technology company, not a bank; the card is issued by Coastal Community Bank (Member FDIC) under a Visa licence. Regulators: bank-partner model — Coastal is the creditor/issuer (supervised by FDIC and Washington state); RCT is subject to consumer-finance rules.

**8. Robinhood Asset Management LLC (RAM, "Robinhood Strategies")** — SEC-registered investment adviser (managed portfolios; manages the cash-sweep feature).

**9. Robinhood U.K. Ltd** — England & Wales company (number 09908051); authorised and regulated by the FCA (FRN 823590). Introduces UK customers to Robinhood Securities, LLC (US) for order routing, execution, clearing, settlement, custody arrangement and margin lending. Added to the FCA's cryptoasset register on 31 July 2026 (limited to arranging/transmitting crypto orders — no exchange operation or client-asset custody permission).

**10. Robinhood Europe, UAB** — Lithuanian company (number 306377915), registered as a virtual-currency exchange operator and virtual-currency depository wallet operator; the EU crypto entity. Regulator: Bank of Lithuania.

**11. Bitstamp entities** — acquired 2025; Bitstamp holds 50+ active licences/registrations globally (Luxembourg, UK, Slovenia, Singapore, US). Brings a licensed global crypto exchange and institutional business.

**12. TradePMR** — RIA custodian acquired 2025; brings a scaled RIA custody platform (~350 firms, >$40bn AUA at announcement).

Other entities include Robinhood Non-Custodial, Ltd. (Cayman Islands — the self-custody Robinhood Wallet), Say Technologies LLC (shareholder engagement), Sherwood Media LLC (financial media, from MarketSnacks/Chartr), Robinhood Gold LLC (subscription) and Robinhood International, Ltd.

**The introducing/clearing relationship precisely (Follow-the-Order structural layer).** The customer contracts with RHF (introducing broker) — RHF "owns" the customer relationship and takes the order. RHF passes the order to RHS (clearing broker) on a fully disclosed basis. RHS routes it to a market maker for execution, then clears and settles the trade and holds the customer's cash and securities. Thus: **RHF holds the relationship; RHS holds the assets and carries the 15c3-3 protections; both are FINRA members.** Crypto sits outside this stack entirely — RHC holds the crypto under a different legal arrangement.

## I.3 Ownership, Share Structure and Control

**CONFIRMED FACT.** Robinhood has a three-class structure. Class A: one vote per share (publicly traded). Class B: ten votes per share, held only by founders Tenev and Bhatt and related entities; convertible into Class A. Class C: no votes (none outstanding at IPO). The rights are otherwise identical except voting and conversion.

At IPO (per the 424B4), Tenev held an economic interest of ~7.8–7.9% and ~26.1–26.2% of voting power; Bhatt held ~7.8–7.9% economically and ~38.9–39.0% of voting power. Together the founders controlled a majority of voting power — a controlled-company structure in substance. As of the 2024 proxy, Tenev and Bhatt together commanded over 60% of total voting power despite minority economic ownership.

**CONFIRMED FACT — Bhatt's role change.** In March 2024 Bhatt stepped down from his executive role as Chief Creative Officer to pursue other entrepreneurial interests (he founded the space-based solar-power company Aetherflux, launched ~October 2024). **Correction to a common assumption: Bhatt did NOT leave the board.** Robinhood's announcement stated he "will remain a member of Robinhood's Board of Directors," and he still serves as a director as of 2025–2026. His voting power via Class B persists.

**ANALYTICAL INFERENCE.** Control is decisively founder-held through the 10:1 Class B differential. Even after Bhatt exited management, the founders retain voting control; public Class A holders have limited ability to discipline management through the ballot. Institutional holders and index inclusion supply economic capital but not control.

## I.4 Board and Governance

**CONFIRMED FACT / THIRD-PARTY ESTIMATE.** The board comprises roughly 10 members including Tenev (Chair/CEO) and Bhatt. Governance carries standard public-company committees (audit, compensation, nominating/governance). The classified (staggered) board was set to sunset around 2024. Post-2021, Robinhood built out compliance, legal and customer-support functions (Dan Gallagher, former SEC Commissioner, became Chief Legal, Compliance and Corporate Affairs Officer) and added risk oversight — changes made in the shadow of the FINRA action and the January 2021 events.

**ANALYTICAL INFERENCE.** Governance was augmented but not fundamentally restructured after 2021: the dual-class control mechanism was preserved intact, and remediation focused on compliance staffing and systems rather than on shifting decision rights away from the founders. This is continuity of control with a thicker compliance overlay.

## I.5 Customer Assets, Custody and Protection

**CONFIRMED FACT — the asset-protection matrix.**

- **Customer securities and cash (equities/options):** held by Robinhood Securities LLC, the clearing broker, subject to SEC Rule 15c3-3 (possession-and-control of fully-paid securities and the special reserve bank account for customer cash). RHF is exempt from 15c3-3 under (k)(2)(ii) because RHS carries the assets.
- **SIPC:** RHF and RHS are SIPC members. SIPC protects securities customers up to $500,000 including up to $250,000 for cash claims. SIPC covers broker failure — NOT market losses. Robinhood also carries additional/"excess SIPC" private insurance (aggregate up to $1 billion, with per-customer limits including $1.9 million for uninvested cash).
- **Cash sweep / FDIC pass-through:** uninvested cash can be swept to a network of program banks (Goldman Sachs Bank USA, Wells Fargo, Citibank, U.S. Bank, Truist, Bank of Baroda, Bank of India), where it becomes eligible for FDIC pass-through insurance up to $2.5 million (individual) / $5 million (joint), at $250,000 per bank. Critically: once swept to a program bank, cash is NO LONGER SIPC-protected; before sweep it sits in the brokerage account under SIPC. FDIC covers bank failure, not investment loss, and pass-through requires Robinhood to maintain FDIC-acceptable records.
- **Spending account / Cash Card:** Robinhood Money LLC; not FINRA/SIPC; funds held at Sutton Bank / JPMorgan Chase may be FDIC pass-through eligible up to $250,000.
- **Crypto — the critical distinction.** Cryptocurrency is held by Robinhood Crypto LLC, which is NOT a FINRA or SIPC member. Crypto is NOT protected by SIPC and NOT by FDIC. Robinhood's own disclosure: "Crypto positions through Robinhood Crypto and futures positions through Robinhood Derivatives aren't protected by SIPC." Customers rely on RHC's internal security and custody arrangements, not federal insurance.
- **Futures:** held via Robinhood Derivatives under CFTC customer-segregation rules (not SIPC).

**ANALYTICAL INFERENCE (the retail-narrative gap).** The retail user experiences one app and assumes uniform "Robinhood" protection. Legally, protections vary sharply by product and entity: securities (SIPC + 15c3-3 at RHS), swept cash (FDIC pass-through, not SIPC), crypto (neither), futures (CFTC segregation). This is the single most misunderstood feature of the customer relationship.

## I.6 The Regulator Inventory (RE-CUT)

Nine categories of regulator with authority over parts of the group:

1. **SEC** — supervises RHF and RHS as broker-dealers (registration, 15c3-3, net capital, Reg SHO, recordkeeping, Reg S-P/S-ID, best execution, Rules 605/606); RHM as issuer. Sanctions: censure, fines, disgorgement, undertakings, bars.
2. **FINRA** — SRO membership authority over RHF and RHS: supervision, communications (Rules 2210/2220), options suitability, AML, arbitration. Sanctions: fines, restitution, suspensions, expulsion.
3. **CFTC** — supervises RHD as an FCM (futures, event contracts). Sanctions: fines, registration action; can order product rollbacks (as with the Super Bowl event contract, Feb 2025).
4. **NFA** — SRO for RHD (FCM compliance).
5. **State securities regulators** — including the Massachusetts Secretary of the Commonwealth (fiduciary-rule action) and blue-sky enforcement.
6. **State money-transmitter regulators (via NMLS)** — license and supervise RHC and RHY across states.
7. **NYDFS** — supervises RHC's New York virtual-currency and money-transmission activity (virtual-currency licence, cybersecurity 23 NYCRR 500, transaction monitoring 23 NYCRR 504). Sanctions: consent orders, monetary penalties, monitors.
8. **Banking regulators (indirect)** — the credit-card and cash products run through partner banks (Coastal Community Bank, Sutton Bank, JPMorgan Chase) supervised by the FDIC/OCC/state banking; FinCEN administers BSA.
9. **Non-US authorities** — the FCA (Robinhood U.K. Ltd) and the Bank of Lithuania (Robinhood Europe, UAB); plus Bitstamp's multi-jurisdiction licensors (e.g., Luxembourg's CSSF).

**ANALYTICAL INFERENCE.** The aggregate supervisory burden is unusually heavy and fragmented for a company of Robinhood's age because each product line sits in a differently-regulated entity. Perimeters overlap most sharply on AML (FinCEN + NYDFS + FINRA + SEC all reached the same underlying failures) and on the crypto-securities question (SEC vs. state money-transmission framing).

## I.7 The Self-Clearing Decision (NEW SECTION — pivotal)

**CONFIRMED FACT — chronology.** Robinhood formed Robinhood Securities in 2016; RHS registered with the SEC as a clearing broker on October 13, 2017 and began clearing customer transactions on May 8, 2018. The company announced "Clearing by Robinhood" publicly on October 10, 2018, and converted customers from Apex Clearing Corporation to RHS beginning on or about November 10, 2018, completing the migration by end of 2018. Roughly 70–100 employees in Lake Mary, Florida built the system (product lead Christine Hall called it "the single most complex regulatory and engineering challenge that we've undertaken"); it required approvals from FINRA, the DTCC and the OCC.

**What it changed legally.** Before self-clearing, Apex was the clearing firm — Apex carried the customer assets, the 15c3-3 obligations and the NSCC/DTCC settlement obligations; Robinhood Financial was a fully-disclosed introducing broker relying on a third party. After self-clearing, RHS became the clearing firm of record: it holds customer assets, carries the 15c3-3 reserve and possession-and-control obligations, and is itself a member of NSCC/DTCC and OCC — meaning it must post NSCC clearing-fund and margin deposits daily.

**What it created financially/operationally.** (1) Net-capital obligations at RHS as a carrying broker. (2) Direct NSCC/DTCC membership and daily clearing-fund/margin deposits. (3) Fee savings — Robinhood eliminated the per-trade clearing fees Apex charged (Tenev framed it as controlling its "destiny" and cost savings; e.g., the bank-reversal fee dropped from $30 to $9). (4) End-to-end control of statements, confirmations and application approval (24/7).

**The mechanism that mattered.** NSCC requires each member to post a daily deposit sized to cover settlement risk. The core component is a value-at-risk (VaR) charge on the member's unsettled portfolio. NSCC can additionally impose an **excess capital premium (ECP)** charge on members whose required deposit exceeds their excess net capital — per the SEC's October 2021 staff report, ECP charges are "designed to address significant, temporary increases in a Member's Required Deposit based upon any one day of activity." A federal court described the ECP as "the difference between the member's excess net capital and its core clearing fund charge… The more the core charges exceed the member's capital cushion, the larger the [excess] capital premium charge. To avoid incurring the latter charge the member must either reduce the level of risk or raise additional capital."

**ANALYTICAL INFERENCE.** Self-clearing moved settlement risk onto Robinhood's own balance sheet. This is precisely why, in January 2021, the NSCC deposit demand landed on Robinhood Securities rather than on Apex. Under the old model the January 2021 collateral shock would have been Apex's problem; under self-clearing it was Robinhood's, and Robinhood lacked the capital to meet it without restricting trading and raising emergency capital. Self-clearing bought cost savings and control at the price of bearing tail settlement risk directly.

## I.8 Non-US Expansion and the Perimeter

**CONFIRMED FACT.** Robinhood U.K. Ltd was FCA-authorised as a broker in August 2019 (FRN 823590). It then **abandoned its planned 2020 UK launch**, leaving a waitlist of roughly 250,000, to focus on US problems. A 2022 attempt to acquire UK crypto/e-money firm Ziglu collapsed. Robinhood re-entered, announcing a UK launch in November 2023 and launching brokerage to all UK customers in March 2024. UK customers are introduced to Robinhood Securities, LLC (US) for execution and custody; UK FSCS protection does not apply (US SIPC/FDIC frameworks apply instead). On 31 July 2026, Robinhood U.K. Ltd was added to the FCA cryptoasset register — a permission limited to arranging/transmitting crypto orders, with no authorisation to operate an exchange or hold client digital assets in custody.

The EU crypto entity is Robinhood Europe, UAB, registered in Lithuania (Bank of Lithuania) as a virtual-currency exchange and depository wallet operator. The 2025 Bitstamp acquisition added 50+ global licences (Luxembourg, UK, Slovenia, Singapore, US) and an institutional business, extending the footprint across the EU, UK, US and Asia.

**ANALYTICAL INFERENCE.** Product availability is regulator-constrained: full equities/options in the US; UK brokerage introduces to the US clearing entity; crypto in the EU runs through the Lithuanian entity and (post-Bitstamp) Bitstamp's licences. PFOF's illegality in the UK/EU reshapes the economics abroad (see I.10).

## I.9 Acquisitions and Corporate Development

**CONFIRMED FACT / THIRD-PARTY ESTIMATE — acquisition table (consideration where disclosed):**

- **MarketSnacks (2019)** → became Robinhood Snacks / later Sherwood Media LLC; financial-media/newsletter. Consideration undisclosed.
- **Say Technologies (2021)** — ~$140 million (widely reported THIRD-PARTY ESTIMATE); shareholder-engagement/communications technology.
- **Ziglu (agreed 2022)** — UK e-money/crypto; **deal collapsed/abandoned** (did not close).
- **Chartr and other tuck-ins** — data-visualization media, folded into Sherwood.
- **Marex FCM entity (early 2024)** — off-the-shelf futures commission merchant acquired from Marex to enable the futures business (Robinhood Derivatives). Marex had a spare FCM to offload following its acquisition of ED&F Man Capital Markets.
- **X1 Inc. (announced June 22, 2023; closed July 3, 2023)** — ~$95 million cash; credit-card platform → Robinhood Credit / Gold Card. X1 co-founder Deepak Rao became GM of Credit Cards.
- **Bitstamp (announced June 2024; closed June 2, 2025)** — ~$200 million cash; global crypto exchange with 50+ licences and institutional business. Robinhood's largest deal to date. Advisers: Barclays (Robinhood), Galaxy Digital (Bitstamp).
- **TradePMR (announced Nov 2024; closed 2025)** — RIA custody platform (~350 firms, >$40bn AUA); consideration in the ~$300 million range (THIRD-PARTY ESTIMATE), plus ~$120 million post-close equity compensation disclosed by Robinhood.

**ANALYTICAL INFERENCE.** The acquisition pattern is "buy the regulated wrapper": Robinhood repeatedly acquires the licensed entity or platform needed to launch a product (an FCM for futures, a card platform + bank partner for credit, a licensed exchange for global crypto, an RIA custodian for wealth). Strategy = convert a single-product retail app into a full-stack financial-services group while minimizing time-to-market on licensing.

## I.10 The Order-Routing Legal Architecture (Follow-the-Order)

**CONFIRMED FACT.** When a US customer places an equity/option order: RHF (introducing broker) accepts it → passes to RHS (clearing broker) → RHS routes to wholesale market makers (Citadel Securities, Virtu, Two Sigma Securities, Wolverine, etc.) for execution → RHS clears and settles. The market makers pay Robinhood **payment for order flow (PFOF)** — consideration flowing from the wholesaler to Robinhood in exchange for the order. This is the "commission-free trade is not free" mechanism: the customer pays no commission, but the market maker pays Robinhood, and the customer's execution price is where any cost surfaces. Robinhood collected $331 million in PFOF in Q1 2021 alone; PFOF has historically been its largest revenue source.

**Legal basis and obligations.** PFOF is legal in the US (SEC Rule 606 requires disclosure of routing and PFOF arrangements; Rule 605 requires execution-quality statistics). The broker owes a **duty of best execution** — to seek the most favorable terms reasonably available. The December 2020 SEC action (see I.11) found Robinhood breached both disclosure and best-execution duties: unusually high PFOF rates meant customers received inferior prices costing them ~$34.1 million even net of commission savings.

**Jurisdictional constraint.** PFOF is banned/restricted in the UK and the EU (the EU's MiFIR is phasing out PFOF). In those markets Robinhood cannot monetize via PFOF and instead routes UK customer orders to Robinhood Securities in the US and monetizes via other means (securities lending, FX/interest spread on USD balances, subscription/Gold).

**ANALYTICAL INFERENCE.** Volume I establishes the legal architecture: the permission (PFOF is lawful in the US with disclosure), the obligation (best execution owed by the executing/introducing brokers), and the perimeter (PFOF prohibited abroad, forcing a different revenue model). Volume II will quantify the economics.

## I.11 The Enforcement Ledger (RE-CUT, PRIORITY DEPTH)

A dated ledger of material actions. Each entry: date / authority / entity / conduct / outcome / admission.

**1. December 2019 — FINRA — RHF — best execution.** FINRA fined Robinhood Financial $1.25 million for best-execution failures relating to routing of customer equity orders. Neither admitted nor denied.

**2. June 2020 — death of Alex Kearns.** Kearns, a 20-year-old options customer, died by suicide in June 2020 after mistakenly believing he owed $730,000 on his Robinhood account and being unable to reach support. His family sued (February 2021) for wrongful death, negligent infliction of emotional distress and unfair business practices. Robinhood settled in late May 2021; the case was dismissed with prejudice on June 21, 2021 (terms undisclosed). Product changes followed: interface changes to options, live phone support, an education specialist. This event is repeatedly cited in later regulatory actions.

**3. December 16, 2020 — Massachusetts Secretary of the Commonwealth — RHF — administrative complaint.** Secretary William Galvin's Securities Division filed the state's first enforcement action under its March 2020 fiduciary-duty rule, alleging "dishonest and unethical" practices, gamification, aggressive targeting of inexperienced investors, and failure to prevent outages. (As of December 8, 2020, Robinhood had 486,598 Massachusetts accounts worth $1.6 billion.) **Appellate history:** Robinhood sued (April 2021) to invalidate the fiduciary rule; Suffolk Superior Court (Judge Ricciuti, March 30, 2022) held the Secretary exceeded his authority and the rule invalid; the Massachusetts Supreme Judicial Court (*Robinhood Financial LLC v. Secretary of the Commonwealth*, SJC-13381, August 25, 2023) **reversed**, holding the Secretary acted within his MUSA authority, that the rule does not override common-law protections, is not an impermissible delegation, and is not preempted — remanding for further proceedings. The underlying enforcement matter thus survived.

**4. December 17, 2020 — SEC — RHF — PFOF/best execution.** The SEC charged Robinhood Financial with misleading statements/omissions (2015–late 2018) about PFOF being its largest revenue source, and failure to satisfy best execution. Finding: inferior prices cost customers ~$34.1 million net of commission savings. **Outcome: $65 million civil penalty**; Robinhood neither admitted nor denied; agreed to retain an independent compliance consultant.

**5. January 27–29, 2021 — trading restrictions / meme-stock episode.** (Full account in I.12.) RHS restricted buying in GameStop, AMC, BlackBerry, Nokia, Koss and others on January 28, 2021 after the NSCC deposit demand. Consequences: 100+ class actions and a federal multidistrict litigation (*In re January 2021 Short Squeeze Trading Litigation*, S.D. Fla.); congressional hearings (House Financial Services Committee, February 18 and March 2021); and the June 2022 majority staff report "Game Stopped."

**6. June 30, 2021 — FINRA — RHF — largest FINRA penalty then ordered.** FINRA ordered ~$70 million total: a **$57 million fine plus approximately $12.6 million in restitution (plus interest)** — "the largest financial penalty ever ordered by FINRA" — for "systemic supervisory failures": false/misleading communications to millions of customers (Rules 2210/2220), the March 2020 systems outages, and improper approval of thousands of customers for options trading (approval bots relying on inconsistent/illogical information; a single principal reportedly approved more than half of 5.5 million new accounts). FINRA enforcement head Jessica Hopper stated: "Compliance with these rules is not optional and cannot be sacrificed for the sake of innovation or a willingness to 'break things.'" Kearns's death was referenced. Neither admitted nor denied. (123-page AWC.)

**7. August 1–2, 2022 — NYDFS — RHC — first NYDFS crypto enforcement action.** $30 million penalty plus an independent-consultant requirement (18 months), for BSA/AML failures (understaffed program; manual transaction monitoring inadequate for volumes — reviewing 106,000+ transactions/day worth $5.3m in September 2019), Cybersecurity Regulation (23 NYCRR 500) and Transaction Monitoring (23 NYCRR 504) violations, plus failure to disclose regulatory investigations under its supervisory agreement and inadequate consumer-complaint handling.

**8. May 4, 2024 — SEC Wells notice — RHC — crypto listings.** RHC received a Wells notice stating the staff's preliminary determination to recommend an enforcement action alleging violations of Sections 15(a) and 17A of the Exchange Act (unregistered broker/clearing agency), following subpoenas on crypto listings, custody and operations. **Outcome: on February 21, 2025 the SEC's Enforcement Division closed the investigation with no action** (part of the post-2024 change in SEC crypto posture). No penalty; no admission.

**9. January 13, 2025 — SEC — RHS and RHF — recordkeeping and multiple provisions.** $45 million combined ($33.5m RHS + $11.5m RHF), for violating more than 10 separate provisions: late suspicious-activity reporting (Jan 2020–Mar 2022); identity-theft protection failures (Reg S-ID, Apr 2019–Jul 2022); failure to address a cybersecurity vulnerability that led to the November 2021 data breach (millions of customers); off-channel-communications recordkeeping failures; brokerage-data retention failures; failure to maintain customer communications; RHS electronic blue-sheet failures (5+ years, 11,849+ deficient submissions affecting 392m+ transactions); and RHS Reg SHO violations (close-out, order-marking, locate; May 2019–Dec 2023, including 15m+ mismarked short sales). **Both firms admitted certain findings and agreed to be censured** — a notable departure from the usual neither-admit-nor-deny; both agreed to internal audits of off-channel communications and RHS agreed to certify Reg SHO remediation.

**10. March 7, 2025 — FINRA — RHF and RHS.** FINRA ordered a **$26 million fine (RHF + RHS jointly) plus $3.75 million restitution (RHF), total $29.75 million**, for: inaccurate/incomplete disclosures on "collaring" market orders (converting them to limit orders, then canceling — customers who re-entered received inferior prices); unreasonable AML programs at both firms (failure to detect/investigate/report suspicious activity, manipulative trading, account-takeover by third-party hackers); RHF's unreasonable customer-identification program (thousands of accounts opened without verified identity; a lookback of ~2 million accounts and 100,000+ closures); RHS's failure to supervise its clearing technology (which suffered "severe latency in January 2021 due to a surge in trading volume and volatility"); RHF's failure to supervise/retain paid social-media-influencer communications ("promissory or not fair and balanced, and thus misleading"); and RHS blue-sheet/trade-reporting/CAT failures. Head of Enforcement Bill St. Louis: "compliance with core regulatory obligations remains critical to safeguarding and serving all investors." **Consented without admitting or denying; agreed to certify remediation.**

**ANALYTICAL SYNTHESIS.** The aggregate record shows a control environment that chronically lagged growth. The failures are not isolated: AML/SAR failures recur across NYDFS (2022), SEC (2025) and FINRA (2025); disclosure/communications failures recur across SEC (2020), FINRA (2021) and FINRA (2025); options/supervision failures anchor the 2021 FINRA action and the Kearns tragedy. The pattern is **systemic rather than episodic** — the same root cause (systems and compliance not keeping pace with user growth) surfaces repeatedly. Post-2021 there is partial genuine remediation (compliance build-out; the 2025 SEC admissions signal a more cooperative posture; the crypto investigation closed with no action) but also continuity: the FINRA March 2025 action reached conduct extending to 2023–2024, showing the remediation lag persisted well past the 2021 reckoning.

## I.12 The January 2021 Events — Legal and Structural Account

**CONFIRMED FACT — reconstruction.** Through late January 2021, coordinated retail buying (organized on Reddit's r/WallStreetBets) drove GameStop and other heavily-shorted stocks to extreme highs; GME peaked around $325 on January 27. Volatility and concentration sharply raised Robinhood Securities' NSCC settlement-risk exposure.

At approximately 5:11 a.m. EST on January 28, 2021, NSCC sent RHS an automated notice of a deposit deficit of approximately $3 billion. Per Tenev's congressional testimony, that comprised a VaR-based requirement of nearly $1.3 billion (up from $696 million the prior day) plus an **excess capital premium charge of over $2.2 billion**. (Some analyses cite an intraday gross figure near $3.7 billion, comprising a ~$1.3bn VaR charge and a ~$2.3bn ECP charge.)

**Robinhood's response.** RHS could not meet a $3bn+ demand (it had raised roughly $2bn in venture capital to that point). It moved eight securities (GME, AMC, BB, NOK, KOSS and others) to "position-close-only" (PCO) — customers could sell but not buy. Shortly after 9:00 a.m. EST, NSCC informed RHS that the excess capital premium charge had been **waived entirely for that day** (NSCC waived ECP charges broadly to reduce systemic risk). The requirement fell to roughly $1.4 billion gross, netting to about $700 million ($734 million per Datos Insights' reconstruction) after the waiver. The House Republican memorandum noted the waived ECP charges "bore no relationship to actual settlement risk posed by Robinhood Securities and other members at the time."

**Emergency capital.** On January 29–February 1, 2021 Robinhood raised $3.4 billion in emergency capital (an initial $1 billion announced January 29 plus $2.4 billion more — the Series H), from Ribbit Capital, Sequoia, Index Ventures, ICONIQ and others, via convertible notes — shoring up the balance sheet and enabling restrictions to ease. Restrictions were lifted in early February (Robinhood eased curbs on February 5).

**What was legally required vs. discretionary.** **Legally required:** RHS had to post the NSCC deposit or face being unable to clear — meeting the clearinghouse demand was non-negotiable. **Discretionary (contested):** the *choice* to restrict buying in the specific meme stocks (rather than, e.g., raise margin requirements or manage risk differently) was a risk-management decision by Robinhood; NSCC did not order it. Robinhood's failure to have modeled the ECP charge in advance is central to the criticism — per the "Game Stopped" report, Robinhood operational staff "first accessed and utilized the publicly available formula that the NSCC uses to calculate Excess Capital Premium charges" only on the morning of January 28, and only incorporated it into a mathematical model on February 18, 2021, three weeks after the event. The shock was foreseeable given self-clearing.

**Scrutiny.** House Financial Services Committee hearings (February 18 and March 2021) with Tenev testifying; SEC staff report (October 14, 2021); House majority staff report "Game Stopped" (June 24, 2022), which criticized Robinhood's risk management and inadequate capitalization; the S.D. Fla. MDL (largely dismissed on the antitrust/negligence theories).

**ANALYTICAL INFERENCE.** January 2021 was not primarily a scandal of bad faith but a **structural consequence of self-clearing**: a self-clearing broker with thin capital, explosive concentrated volume, and no model for the ECP charge was always vulnerable to exactly this collateral shock. The novelty of Robinhood's interface (which drove the volume) collided with the century-old plumbing of NSCC settlement (which demanded the collateral), and the firm's 2018 decision to own that plumbing itself put the loss on its own balance sheet.

## I.13 Volume I Reconstruction

**(1) Entity and Registration Map.** RHM (holding co / issuer) owns: RHF (introducing BD; SEC/FINRA/SIPC); RHS (clearing BD; SEC/FINRA/SIPC/NSCC/DTCC/OCC); RHC (crypto; NMLS/NYDFS/state MT); RHD (FCM; CFTC/NFA); RHY (money transmitter; NMLS); RCT (credit; via Coastal Community Bank/Visa); RAM (RIA; SEC); Robinhood U.K. Ltd (FCA); Robinhood Europe UAB (Bank of Lithuania); Bitstamp (50+ global licences); TradePMR (RIA custody); Robinhood Non-Custodial Ltd (Cayman); Say Technologies; Sherwood Media; Robinhood Gold LLC.

**(2) Ownership and Control Map.** Class A (1 vote, public); Class B (10 votes, Tenev + Bhatt only); founders together >60% voting power on minority economics. Tenev is Chair/CEO; Bhatt remains a director after stepping down as CCO in March 2024.

**(3) Customer Asset Protection Matrix.** Securities → RHS, 15c3-3 + SIPC ($500k/$250k cash) + excess SIPC (up to $1bn aggregate). Swept cash → program banks, FDIC pass-through ($2.5m/$5m), not SIPC. Spending account → Sutton/JPMorgan, FDIC pass-through, not SIPC. Crypto → RHC, NO SIPC, NO FDIC. Futures → RHD, CFTC segregation, not SIPC.

**(4) Regulator Inventory.** SEC; FINRA; CFTC; NFA; state securities regulators (incl. Massachusetts); state money-transmitter regulators; NYDFS; banking regulators (FDIC/OCC/FinCEN via partners); FCA + Bank of Lithuania (+ foreign licensors).

**(5) Self-Clearing Structural Analysis.** Registered as clearing broker Oct 13, 2017; clearing began May 8, 2018; announced Oct 10, 2018; Apex→RHS conversion from ~Nov 10, 2018. Bought fee savings + control; cost = NSCC settlement risk on own balance sheet → January 2021.

**(6) Jurisdictional Product Availability Matrix.** US: equities, options, crypto, futures/event contracts, cash, credit, retirement, RIA custody. UK: brokerage (introduces to US RHS), ISA, futures; crypto (arranging only) from July 31, 2026. EU: crypto via Lithuania/Bitstamp. PFOF monetization only where lawful (US), not UK/EU.

**(7) Acquisition Table.** MarketSnacks 2019; Say Technologies 2021 (~$140m est.); Ziglu 2022 (collapsed); Marex FCM early 2024; X1 2023 (~$95m); Bitstamp 2024→2025 (~$200m); TradePMR 2024→2025 (~$300m est.).

**(8) Order-Routing Legal Architecture.** RHF→RHS→market makers; PFOF lawful in US with Rule 606/605 disclosure; best execution owed; PFOF banned UK/EU.

**(9) Enforcement Ledger.** FINRA 2019 $1.25m; Kearns 2020 (settled 2021); Massachusetts Dec 2020 (rule upheld by SJC 2023); SEC Dec 2020 $65m; Jan 2021 restrictions + litigation; FINRA June 2021 $70m; NYDFS Aug 2022 $30m; SEC Wells notice May 2024 (closed no-action Feb 2025); SEC Jan 2025 $45m (admissions); FINRA Mar 2025 $29.75m.

**(10) January 2021 Timeline.** Jan 27 GME ~$325; Jan 28 5:11am NSCC ~$3bn demand (VaR ~$1.3bn + ECP >$2.2bn); ~9am ECP waived, net ~$700m; Jan 28 PCO restrictions on 8 stocks; Jan 29–Feb 1 $3.4bn emergency raise; Feb 5 restrictions lifted; Feb 18 & March congressional hearings; Oct 2021 SEC report; June 2022 "Game Stopped."

**(11) Key Unknowns.** Precise current board roster and committee-independence percentages (2025–2026 proxy); exact TradePMR and Say Technologies consideration; the full state-by-state money-transmitter licence count for RHC/RHY; the current excess-SIPC insurer terms; whether any post-mid-2026 enforcement actions exist beyond the July 2026 FCA crypto registration.

**(12) Ten Most Important Conclusions.**
1. Robinhood Markets is a holding company that does nothing operational; the real businesses are RHF (relationship) and RHS (assets + clearing).
2. Control is founder-locked via 10:1 Class B shares; Bhatt's 2024 management exit did not change that — he remains a director.
3. Self-clearing (2018) is the pivotal structural fact — it internalized NSCC settlement risk and set up January 2021.
4. What a customer "owns" and against whom they have a claim varies by product: SIPC/15c3-3 for securities (RHS), FDIC pass-through for swept cash (banks), and neither for crypto (RHC).
5. Crypto is the great protection gap: no SIPC, no FDIC, different entity, different custody.
6. The SEC and FINRA (over RHF/RHS) are the regulators that matter most; NYDFS matters most for crypto; the CFTC now matters for futures/event contracts.
7. The enforcement record is systemic, not episodic: AML, disclosure and supervision failures recur across 2019–2025.
8. PFOF is the engine of "commission-free": the market maker pays; the customer's cost, if any, is in the execution price; lawful in the US, banned in UK/EU.
9. The acquisition strategy is "buy the regulated wrapper" to compress time-to-market for each new product.
10. January 2021 is best understood as a structural consequence, not merely a scandal.

**What is Robinhood, legally?** A Delaware holding company (RHM) over a functional stack of separately-registered financial-services subsidiaries. **Which entity is the real business?** RHF holds the customer; RHS holds the assets, clears and settles, and bears the settlement risk — RHS is the load-bearing entity. **Who controls it?** Vladimir Tenev (Chair/CEO) with Baiju Bhatt, via Class B super-voting shares (>60% combined voting power). **What does a customer own, and against whom?** Securities held at RHS (SIPC + 15c3-3 claim); swept cash at program banks (FDIC claim, not against Robinhood); crypto at RHC (a contractual claim against RHC, no federal insurance). **Which regulator matters most?** The SEC and FINRA for the core brokerage; NYDFS for crypto historically; increasingly the CFTC. **What did self-clearing buy and cost?** It bought fee savings, 24/7 control and product velocity; it cost the assumption of NSCC settlement risk on Robinhood's own balance sheet — the direct cause of the January 2021 near-failure.

**The central question.** Is the commission-free brokerage a genuinely new institutional form, or a conventional broker-dealer whose novelty is in its interface and its choice of who to charge? **ANALYTICAL CONCLUSION: substantially the latter.** Structurally, Robinhood is an entirely conventional introducing-broker/clearing-broker pair that clears through NSCC/DTCC like any other self-clearing broker, earns PFOF like other retail brokers, sweeps cash to partner banks, and holds customer securities under Rule 15c3-3. Its genuine innovations are (a) the mobile-native interface and gamified UX that mobilized an unprecedented retail cohort, (b) the decision to charge the market maker (PFOF) rather than the customer (commission), and (c) the aggressive multi-entity expansion into crypto, credit and event contracts. The novelty is real but sits in the interface, the revenue-incidence choice, and the product breadth — not in the underlying institutional plumbing, which is orthodox broker-dealer architecture. The January 2021 events proved the point: when the novel front-end collided with the conventional back-end, it was the conventional back-end (NSCC collateral) that dictated outcomes.

---

## Recommendations (for an analyst/counterparty using this Volume)

**Stage 1 — Entity-level diligence.** Treat "Robinhood" claims skeptically; always attribute to the specific entity. Pull the FINRA BrokerCheck records for RHF (CRD) and RHS separately, the latest Form X-17A-5 (FOCUS) for RHS to verify net capital and the 15c3-3 reserve, and the current DEF 14A for board and voting confirmation. *Threshold that would change the assessment:* any Class B conversion or founder sell-down reducing combined voting power below 50% would materially alter the control conclusion.

**Stage 2 — Customer-protection communication.** If advising retail users or a distribution partner, foreground the crypto/futures protection gap explicitly: securities are SIPC/15c3-3 protected at RHS; swept cash is FDIC (bank, not Robinhood); crypto and futures have neither. *Threshold:* federal crypto-custody legislation or SIPC-equivalent crypto insurance would change this.

**Stage 3 — Clearing/settlement risk monitoring.** Watch RHS net capital versus NSCC exposure during any high-volatility, high-concentration episode; the January 2021 vulnerability recurs whenever concentrated meme-style volume meets thin excess net capital. *Threshold:* the pending move to T+1 (already effective) reduces but does not eliminate ECP exposure; a return to episodic buy-restrictions would signal the structural risk is unresolved.

**Stage 4 — Enforcement-trajectory tracking.** Monitor for post-mid-2026 actions (CFTC event-contracts posture, any FCA/EU action, state money-transmitter matters). *Threshold:* a new AML or supervision action reaching post-2024 conduct would confirm remediation has still not caught up with growth; a clean 2026–2027 record would support the "genuine remediation" reading.

## Caveats
- Financial figures are US GAAP in USD with a 31 December year-end unless noted; Adjusted EBITDA and similar are non-GAAP and are not mixed with GAAP figures here.
- Several consideration figures (Say Technologies ~$140m; TradePMR ~$300m) are THIRD-PARTY ESTIMATES; consult the relevant 10-K/8-K for exact amounts.
- The January 2021 top-line NSCC figure varies by source ($3bn initial automated notice vs. ~$3.7bn intraday gross); the authoritative Congressional/SEC figure is ~$3bn (VaR ~$1.3bn + ECP >$2.2bn), netting to ~$700m after the ECP waiver.
- Board composition and voting percentages should be confirmed against the latest DEF 14A.
- Some corporate-development figures and the FCA crypto-registration date (31 July 2026) derive from trade press and should be reconfirmed against primary registers where used for decisions.
- This is Volume I (structure/law/regulation). The economics (revenue decomposition, unit economics, PFOF quantification) are reserved for Volume II; operational/risk analysis of January 2021 for Volume III.