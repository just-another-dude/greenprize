# DAO Implementation

## Membership

There needs to be a legal-binding contract where the relationship between the users (companies, businesses, organisations) and the DAO are explicitly stated.\
Example of such a contract in the NexusMutual project:\
https://uploads-ssl.webflow.com/62d8193ce9880895261daf4a/63d0f45aacb2752b543ddcaf\_Nexus-Mutual-DAO-Member-Agreement-FIN.pdf

## Requirements / Perks of becoming a Member:

* KYC / AML. To become a member, you will need to verify your identity through the Know-Your-Customer / Anti-Money-Laundering process. If this fails, you won’t be able to participate in GreenPrize.
* Initial membership fee (X amount of SOL, for example).
* You own part of GreenPrize. You can participate and earn more GPR by helping run GreenPrize, including voting on submitted activities, appeals, staking GPR, and voting on proposals.

## DAO Implementation

### Protocol Governance Power

Create a governance token (e.g. GPR) that allows holders to participate in the validation process of activities by way of voting, in addition to voting on proposals and possible appeals (although may be escalated to advisory board). The more tokens a user holds, the more voting power they have.\
E.g. of voting power:\
On-chain voting power = 1 + MIN (5% of GPR supply, GPR holdings)\
A single member’s voting power is capped at 5% of the total GPR supply. This is designed to prevent a large holder from having undue influence in protocol governance.

#### Advisory Board

The Advisory Board is made up of X (e.g. 5) members of GreenPrize and contains members of the founding team and other experts. The goal is to have a qualified mix of individuals covering three broad skill sets of:

* Technical expertise: smart contract security and blockchain.
* Technical expertise: ecology and natural environment.
* General expertise: legal, regulatory, corporate governance, and business management.

The Advisory Board has power in limited circumstances and is primarily there to provide qualified technical guidance to the members of the mutual on improvement proposals as well as take emergency action, should it be required. The scope of the Advisory Board’s power in governance is outlined below.

#### Scope & Power

TBD…

#### Activity completion, voting and rewards process

**Completion request submission**

When a user takes on a certain activity and completes it, a completion request is submitted.\
The user will provide physical evidence and details related to the activity, such as photos, videos, documents or any other form of evidence that indicates that indeed the activity has been completed properly.\
Before a completion request can be filed, the user will need to make a deposit denominated in the underlying's (L1) blockchain, e.g. SOL.\
If the completion request is approved, the deposit is refunded in the same transaction as the rewards payout.\
If the completion request is denied, the deposit will not be refunded.\
The deposited amount is the SOL equivalent of the GPR amount distributed as completion request assessment rewards, where the minimum deposit required is X SOL (e.g. 3-4 SOL) and the maximum amount required is a SOL deposit equivalent to X GPR.\
Completion request deposits are required to prevent people from spamming the request process with multiple requests, as there is no limit to the number of times a request can be submitted. As long as a cover holder provides a request deposit, they can file a claim as many times as preferred.

**Voting Process**

Once a claim is submitted, the voting process begins. A claim vote lasts for a minimum of three days.

**Completion Request Assessors**

Members can stake their GPR and participate as a completion request assessor.\
Completion request assessment stakes are locked for 90 days after a member’s last vote was cast.\
Assessors review the activity details, proof of it taking place according to its requirements and description, and other supporting information to determine the completion request’s validity.\
Members discuss submitted requests in the GreenPrize Discord.

**Outcomes​**

1. Accept. If a request assessor reviews the proof of completion and supporting evidence and determines a completion request is valid, they can submit their vote to approve. Once a vote to approve has been submitted, other members can submit votes to approve or deny the request. A simple majority (50%+) is required to decide an assessment vote. The assessment will last for a minimum of three days, which starts from the time the first vote to approve is submitted There is a 24-hour silent period, where no votes should be casted before an assessment vote closes If a vote is submitted during the last 24 hours of the vote, the voting period is extended with an amount of time proportional to the voter's stake, with 24 hours representing the maximum time increase This design feature prevents "rush attacks," where someone tries to overturn a completion request outcome by submitting a vote at the last minute that moves the majority outcome with no time to appeal the vote.
2. Deny. If claim assessors review the completion request submission and determine that no loss has occurred or that the claim does not meet the terms of the cover wording, no deny vote is required unless another member submits a vote to approve. If a completion request receives no votes and the three day period passes, the request will be denied by default.

**Completion Request Payouts**

TBD…

**Completion Request Rewards**

TBD…

**Fraudulent Votes**

During the cool-down period, completion request outcomes can be reviewed if fraudulent voting is suspected. If the Advisory Board finds a request assessor to have voted to deny a legitimate request or approve an illegitimate request, then a fraud penalty can be imposed. The Advisory Board can submit a merkle-tree root hash representing the fraudulent voter and their assessment stake. The fraudulent vote is reversed and the fraudulent assessor's stake is burned. Once the Advisory Board submits the merkle-tree root hash, anyone can process the fraud penalty. By processing the fraud penalty, a member is executing the transaction that burns the assessor’s stake and reverses their fraudulent vote.

## Build a community of validators

Here are some suggestions to attract validators and maintain decentralization:

* Make the validation process "gamified" by having validators level up based on their participation and accuracy of past votes. Display their ranks publicly to tap into people's competitive spirits.
* Partner with relevant eco organizations, non-profits, activism groups who can encourage their members to be early validators on the platform. Offer them incentives.
* Conduct airdrops of the governance tokens to interested users who sign up to be validators. The wider the distribution the better.
* Implement a staking mechanism where validators have to lock up token deposits in order to participate. This ensures long-term alignment.
* Cap the maximum number of assignments per month for any one validator. This prevents over-use of a small group of validators.
* Implement a bonding curve model for the token supply. As demand increases, the token price organically increases, incentivizing more validators to join while limiting token concentration.
* Develop a sophisticated algorithm for assigning validators to tasks randomly based on ratings, activity levels, concentrations, etc to prevent collusion and centralization risks.
* Leverage decentralized identity systems to validate real identities of users without compromising privacy. This prevents Sybil attacks.
* Build fraud and sybil resistance directly into the governance token economics and staking mechanisms.
* Collaborate with other ecosystems like Reputation DAO to tap into their anti-Sybil resources.

## Some Example References

https://docs.nexusmutual.io/overview/membership/\
https://docs.nexusmutual.io/governance/\
https://docs.nexusmutual.io/protocol/claims-assessment/\
https://docs.nexusmutual.io/governance/protocol-improvement-proposals/
