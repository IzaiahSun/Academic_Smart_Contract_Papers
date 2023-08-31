
# 23_8_31
# ndss23 | Smarter Contracts: Detecting Vulnerabilities in Smart Contracts with Deep Transfer Learning
* Motivation: How to efficiently, fine-grained and scalable detect vulnerabilities in smart contracts.
* Prior work: Non-machine learning methods, such as program analysis, are inefficient and not scalable; machine learning-based methods rely on source code and intelligently perform binary classification.
* Approach: The author utilizes transfer learning to quickly and lightweightly train a network containing new vulnerabilities while ensuring multi-classification of vulnerabilities.
* Implement：The author first obtains the contract bytecode from the blockchain, then uses the existing vulnerability detection tools (e.g., Oyente, Mythril, Vandal, Maian) to label the contract, and finally sends it to the neural network for training.
* Evaluation：The tool from this study can detect 11 vulnerability classes in 0.15 s per smart contract on average and yields an average F1 score of 97 % across all evaluated classes.

# 23_8_30
## ndss23 | Double and Nothing: Understanding and Detecting Cryptocurrency Giveaway Scams.
* Motivation: The authors measure and investigate the current state of attackers using websites to phish victims with high cryptocurrency rebates.
* Approach: The author used the certificate information to obtain a large number of phishing websites of attackers, and then conducted a lot of analysis on the information of these websites. In addition, the author also analyzed the relevant transactions of the attacker's wallet account to assess the loss.
* Observation1: During the six months the authors studied, a total of 10,079 phishing sites were observed, an average of 55.7 phishing sites per day.
* Observation2: During the six months the authors studied, attackers have stolen the equivalent of tens of millions of dollars.
* Observation3: The author extracts the transactions corresponding to 2,266 wallets belonging to scammers.

# 23_8_29
## sec23 | A Large Scale Study of the Ethereum Arbitrage Ecosystem
* Motivation: How will the current large-scale arbitrage affect the blockchain ecology.
* Background: Arbitrage is defined as the simultaneous purchase and sale of the same asset in two different markets for advantageously different prices.
* Key idea1：The author proposes a method based on graph analysis to identify arbitrage behavior. First, the author identifies token behavior, then constructs a token transaction graph, then finds whether there is a cycle in the graph, and finally extracts arbitrage information.
* Key idea2：The author replays historical transactions to identify arbitrage opportunities that have existed in the past.
* Observation 1: The income generated by current arbitrage may be enough to make miners evil, because it far exceeds the income generated by consensus mining.
* Observation 2: The current arbitrage benefits may make oracle price manipulation attacks easier to implement.


# 23_8_28
## sp22 | Quantifying Blockchain Extractable Value: How dark is the forest?
* Motivation：Quantify and expand the profits of current blockchain extractable value (BEV) and analyze the harm of BEV to the current blockchain consensus.
* Measurement：The author quantifies the profits brought by miner arbitrage, sandwich attacks, and  liquidation.
* Key Idea: The author proposes an algorithm for repeated transactions to estimate the profits that are not calculated by BEV.
* Contribution: The author formalizes the BEV relay concept as an extension of the P2P transaction fee auction model.
* Conclusion: BEV relay not only did not alleviate the network load, but jeopardized the consensus of the blockchain. The algorithm from author extends the total captured BEV by 35.18M USD.



# issta22_SPCon 
## issta22 | Finding permission bugs in smart contracts with role mining.
* Motivation：This research focuses on verifying whether the access control policy design of smart contracts is reasonable.
* Key Idea：The author mines the corresponding role permission structure from historical transactions, and conducts a conformance testing on these role permissions to see if there are flaw.
* Technical challenge: The role and permission information provided by historical transactions is incomplete.
* Solution：The author abstracts the process of recovering from a partial role permission model to a complete model as an optimization problem, and adopts genetic algorithm to obtain the optimal solution.
* Implements and evaluation: The author implements SPCon and evaluate it on the sampled 50 smart contracts within the role mining benchmark. The results show that SPCon can largely reduce the number of mined with better accuracy.

# sp23_WeRLman
## sp23 | WeRLman: To Tackle Whale (Transactions), Go Deep (RL).
* Motivation: This research mainly studies the security impact of the abnormal miner reward brought by MEV on the Proof-of-Work (POW) mechanism.
* Previous Work: Previous work did not consider miner rewards for MEV anomalies, and modeled them with constant rewards.
* Key Idea：The author adopts deep Reinforcement Learning (RL) to build a POW reward model to evaluate possible security issues in the POW mechanism, especially the collapse of the POW reward mechanism caused by MEV.
* Technical challenge：The high reward (i.e., the amount) for miners by MEV will cause the state space that needs to be simulated to become very large.
* Solution: The author obtains a simplified model by simplifying the behavior of miners. The model is two orders of magnitude smaller than the full model and can be solved by dynamic programming.
* Evalution and conlusion：The authors analyzed the historical records of Bitcoin and reveal that the security threshold of Bitcoin (the proportion of computing power required to attack the network) is declining sharply through their proposed model.

# sp23_CF
## sp23 | Clockwork Finance: Automated Analysis of Economic Security in Smart Contracts.
* Motivation: Detect and identify financial security issues of DeFi smart contracts.
* Previous work: Existing works can only detect known and limited DeFi smart contract vulnerabilities.
* Key Idea: The author uses formal verification techniques to automatically reason about and quantify the financial security problems that contracts may encounter.
* Implements：The author instantiate Clockwork Finance Framework (CFF) in the K framework for mechanized proofs.
* Insight: CFF uncovers on average an expected $56 million of EV per month in the recent past.

# ccs22_vrust
## ccs22 | VRust: Automated Vulnerability Detection for Solana Smart Contracts.
* Motivation：Detect security issues with smart contracts on the solana chain.
* Background: Solana is a stateless blockchain, which requires callers to provide the data they need in the parameters of the interface of the contract, which leads to a new attack surface.
* Key Idea：The author developed a static contract verification tool VRust, after converting the contract into the form of MIR, and then comparing the eight fixed vulnerability patterns proposed by the author to detect security issues.
* Evalution： VRust has been evaluated on over a hundred of Solana projects, and it has revealed 12 previously unknown vulnerabilities, including 3 critical vulnerabilities in the official Solana Programming Library confirmed by core developers

# 23_8_27
## sp23 | Three Birds with One Stone: Efficient Partitioning Attacks on Interdependent Cryptocurrency Networks.
* Motivation：This study explores the threat to the security of the blockchain itself if the autonomous systems (ASes) of the blockchain network is not independent.
* Background：ASes own a series of IPs, usually telecom operators or cloud service providers.
* Key Idea: The author exploits characteristics of different blockchains sharing the same ASes, and further partitions Bitcoin and Ethereum by launching a partition attack on the Ripple blockchain first.
* Technical challenge：Blockchain networks are often overlapping and thus it is not easy to mine topological data.
* Solution: Ripple's network information is publicly disclosed, so attacks are launched through Ripple.
* Evalution: 9.4K blockchain nodes can be attacked by partitions.

  