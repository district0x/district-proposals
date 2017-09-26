# District Proposals
The district0x Network Token allows holders to signal for new districts to be built by the district0x team. Prior to the launch of Aragon Core on the MainNet, signaling will be conducted via a custom CarbonVote implementation. The CarbonVote implementation is hosted at https://vote.district0x.io/ and is automatically populated with proposals that have been deemed as 'qualifying'. Before you get started, be sure to familiarize yourself with the 'District Proposal Standard' as well as what is deemed a 'Qualifying proposal'. When ready, simply [submit your proposal as a new issue](https://github.com/district0x/district-proposals/issues/new) in this repo.

## Qualifying Proposals
To be deemed as a 'qualifying proposal' the following conditions must be met:
* The proposal was submitted as an issue in the [district0x/district-proposals](https://github.com/district0x/district-proposals) repository
* The proposed district adheres to the [District Proposal Standard template](#district-proposal-standard)
* The proposed district is not unethical, as defined by the [district0x Network Code of Ethics](#district0x-network-code-of-ethics)

Proposals not adhereing to these standards will be closed out and the 'Invalid' label will be attached. 

## District Proposal Standard
The District Proposal Standard is a template for proposals designed to ensure that submissions have been well thought through and contain a sufficient amount of supporting details for the community to make an informed decision in regards to its potential utility afforded. All proposals should be structured as follows:

**Name**: Provide a name of the proposed district. Ideally this would also be listed in the issue title/description.

**Purpose**: Define a purpose of the proposed district. Try to include a one liner with an additional paragraph if needed.

**Description**: Describe how the district should operate in detail. Include relationships between the district and users, tokenholders, and any other parts of the district0x network.

## district0x Network Code of Ethics
See [DGP 1](https://github.com/district0x/governance/issues/1) in 'issues' in the [district0x/governance](https://github.com/district0x/governance/) repository

## Proposal Incentives
To incentivize the submission of thoughtful district proposals, the following rewards will be issued:
* 250   DNT = Proposal submitted as issue, adheres to District Proposal Standard, and is ethical
* 500000 DNT = Proposal is launched as a new district on the district0x Network

If you would like your proposal to be considered for a reward, please be sure to include an ETH address in your proposal or in the comments. Alternatively, after completing the proposal, you may reach out to a district0x team member with this information on Slack.

Note: Proposal incentive reward amounts are subject to change in the event of abuse of the system

## Proposal Labels
[Proposal Labels](https://github.com/district0x/district-proposals/labels) are used to highlight similar proposals as well as offer an easy way to collaborate. If you feel your proposal is incorrectly labeled, please comment with the correct market label or a newly suggested label that better describes your target market segment. To expedite this, feel free to reach out to a community manager on Slack, Reddit or Telegram.

**The following labels are active:**
* **Yellow Market Label** - Market segment/category or community type
* **Blue 'Community' Label** - This label's purpose is to highlight the fact that the proposal is meant to operate as a community more than a market place with a specific market function and could encompass any community that requires a more robust form of governance using token access rules/bylaws. 
* **Pink 'Duplicate' tag** - Indicates that a very similar proposal has already been submitted. A less thought out or developed duplicate may be closed.
* **Purple 'Elaborate' Label** - This label will be added to a proposal if it needs more work and development or the market function is not clear. The proposal will then be closed, removing it from the voting app. A closed proposal will only be reopened if a significant amount of effort has been put into developing the idea. A sure fire way to get your proposal reopened is to make mock ups, wireframes or other content that can better conceptualize the idea. Technical details of tools or processes will also be considered if they are sound and realistic approaches.
* **Green 'Curation Market' Label** - This will highlight the fact that a proposal is meant to be or could potentially operate as a [curation maket](https://medium.com/@simondlr/introducing-curation-markets-trade-popularity-of-memes-information-with-code-70bf6fed9881).
* **Orange 'Invalid' Label** - Will be added to proposals that do not adhere to the district proposal standards outlined in this document. These proposals will be closed.
* **Green 'Merge' Label** - The ‘Merge’ tag has now been added for people taking the initiative to merge ideas and proposals into a single district. These proposals will be closed after an effort to collaborate and work on the new proposal has been finalized. To request an official "Merge", reach out to a community manger of Slack, Telegram or Reddit.
* **Red 'Spam' Label** - This tag will be to flag people who have been submitting spam proposals, refusing to respond to our inquiries or a refusal to adhere to proposal standards. Upon receiving the spam tag, your account will be blocked from interacting with the GitHub repo. Continued abuse in any form will result in a report to GitHub staff to investigate the account(s).

These labels and purpose are subject to change often and we will update everyone to those changes in our [weekly publication](https://blog.district0x.io/).

## How to vote from MyEtherWallet
1. Go to https://www.myetherwallet.com/#contracts
2. In the `Contract Address` field insert the contract address displayed on the voting interface
3. In the ABI / JSON Interface enter the following:
```
[{"constant":false,"inputs":[{"name":"candidate","type":"uint256"}],"name":"vote","outputs":[],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"offset","type":"uint256"},{"name":"limit","type":"uint256"}],"name":"getVoters","outputs":[{"name":"_voters","type":"address[]"},{"name":"_candidates","type":"uint256[]"}],"payable":false,"type":"function"},{"constant":true,"inputs":[],"name":"votersCount","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"address"}],"name":"votes","outputs":[{"name":"","type":"uint256"}],"payable":false,"type":"function"},{"constant":true,"inputs":[{"name":"","type":"uint256"}],"name":"voters","outputs":[{"name":"","type":"address"}],"payable":false,"type":"function"},{"anonymous":false,"inputs":[{"indexed":true,"name":"voter","type":"address"},{"indexed":true,"name":"candidate","type":"uint256"}],"name":"onVote","type":"event"}]
```
4. Press `Access`
5. Select function -> `vote`
6. In the `Candidate` field put the number of your selection, which is shown as the `ID:` on the voting interface
7. Send the transaction. **No DNT is required to send**, but please ensure you have a very small amount of ETH (<0.001) to cover for the gas fee. The recommended gas limit is 100000.
