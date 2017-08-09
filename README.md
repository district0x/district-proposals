# District Proposals
The district0x Network Token allows holders to signal for new districts to be built by the district0x Team. Prior to the launch of Aragon Core on the MainNet, signaling will be conducted via a custom CarbonVote implementation. The CarbonVote implementation will be manually populated with proposals that have been deemed as 'qualifying'.

## Qualifying Proposals
To be deemed as a 'qualifying proposal' the following conditions must be met:
* The proposal was submitted as an issue in the [district0x/district-proposals](https://github.com/district0x/district-proposals) repository
* The proposed district adheres to the [District Proposal Standard template](#district-proposal-standard)
* The proposed district is not unethical, as defined by the [district0x Network Code of Ethics](#district0x-network-code-of-ethics)
* The proposed district has obtained quorum

## District Proposal Standard
The District Proposal Standard is a template for proposals designed to ensure that submissions have been well thought through and contain a sufficient amount of supporting details for the community to make an informed decision in regards to its potential utility afforded. All proposals should be structured as follows:

**Name**: the name of the proposed district

**Purpose**: the purpose of the proposed district

**Description**: describe how the district should operate in detail

## district0x Network Code of Ethics
See [DGP 1](https://github.com/district0x/governance/issues/1) in 'issues' in the [district0x/governance](https://github.com/district0x/governance/) repository

## Quorum
Quorum is currently defined as: number of :thumbsup: for issue ≥ (district0x Slack member count / 50) 

## Proposal Incentives
To incentivize the submission of thoughtful district proposals, the following rewards will be issued:
* 2500   DNT = Proposal submitted as issue, adheres to District Proposal Standard, and is ethical
* 50000  DNT = Proposal obtains quorum
* 500000 DNT = Proposal is launched as a new district on the district0x Network

Note: Proposal incentive reward amounts are subject to change in the event of abuse of the system

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
7. Send the transaction. **No Ether or DNT is required to send**. The recommended gas limit is 100000   

