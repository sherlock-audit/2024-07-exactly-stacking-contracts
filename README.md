
# Exactly Stacking Contracts contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
op mainnet
___

### Q: If you are integrating tokens, are you allowing only whitelisted tokens to work with the codebase or any complying with the standard? Are they assumed to have certain properties, e.g. be non-reentrant? Are there any types of [weird tokens](https://github.com/d-xo/weird-erc20) you want to integrate?
only fully ERC-20 compliant tokens without weird traits.
___

### Q: Are there any limitations on values set by admins (or other roles) in the codebase, including restrictions on array lengths?
no
___

### Q: Are there any limitations on values set by admins (or other roles) in protocols you integrate with, including restrictions on array lengths?
no
___

### Q: For permissioned functions, please list all checks and requirements that will be made before calling the function.
n/a
___

### Q: Is the codebase expected to comply with any EIPs? Can there be/are there any deviations from the specification?
ERC-20 strict compliance (stEXA)
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, arbitrage bots, etc.)?
no
___

### Q: Are there any hardcoded values that you intend to change before (some) deployments?
no
___

### Q: If the codebase is to be deployed on an L2, what should be the behavior of the protocol in case of sequencer issues (if applicable)? Should Sherlock assume that the Sequencer won't misbehave, including going offline?
assume the sequencer won't misbehave
___

### Q: Should potential issues, like broken assumptions about function behavior, be reported if they could pose risks in future integrations, even if they might not be an issue in the context of the scope? If yes, can you elaborate on properties/invariants that should hold?
no
___

### Q: Please discuss any design choices you made.
n/a
___

### Q: Please list any known issues and explicitly state the acceptable risks for each known issue.
n/a
___

### Q: We will report issues where the core protocol functionality is inaccessible for at least 7 days. Would you like to override this value?
n/a
___

### Q: Please provide links to previous audits (if any).
https://github.com/exactly/audits
___

### Q: Please list any relevant protocol resources.
https://docs.exact.ly
___

### Q: Additional audit information.
Key features:
* Distribution of protocol fees: The fees collected from loans will be partly allocated to the Staking Program. A specified fraction (θ) of these fees will be assigned to the staking pool, with a further division between the dividend subprogram and the liquidity provider staking subprogram. This ensures a balanced and fair distribution of rewards.
* Dividend module: Users who stake their EXA tokens will receive dividends based on the staking duration. The dividend index updates regularly, ensuring that participants who stake for longer periods receive proportional rewards. This module supports multiple assets, although a single-asset approach can simplify the dividend distribution.
* Penalty function for early withdrawals: The program will incorporate a penalty function to encourage longer staking periods. Early withdrawals within a predefined minimum period (Tmin) will incur penalties, reducing the dividends awarded. This mechanism helps maintain the stability and longevity of the staking pool.
* Enhanced voting power: Stakers will gain additional voting power, directly influencing protocol decisions. The voting power increases with the staking duration, incentivizing users to stake for extended periods.
* Extra rewards: Aside from dividends, stakes will earn additional rewards in other tokens, providing further incentives for long-term participation.
___



# Audit scope


[protocol @ 0872c11bc7fc6bcdbe630f072c688a448beacbe0](https://github.com/exactly/protocol/tree/0872c11bc7fc6bcdbe630f072c688a448beacbe0)
- [protocol/contracts/Auditor.sol](protocol/contracts/Auditor.sol)
- [protocol/contracts/InterestRateModel.sol](protocol/contracts/InterestRateModel.sol)
- [protocol/contracts/Market.sol](protocol/contracts/Market.sol)
- [protocol/contracts/RewardsController.sol](protocol/contracts/RewardsController.sol)
- [protocol/contracts/StakedEXA.sol](protocol/contracts/StakedEXA.sol)
- [protocol/contracts/utils/FixedLib.sol](protocol/contracts/utils/FixedLib.sol)


