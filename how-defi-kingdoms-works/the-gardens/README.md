# The Gardens

In each realm, the Gardens is a place to stake Liquidity Pool tokens (“LP tokens”) in select pools to receive a share of Power Token emissions. In the JADE gardens of Serendale, players can stake to receive JADE emissions, while in the Ice Gardens of Crystalvale, CRYSTAL emissions are rewarded to those who stake.

<figure><img src="../../.gitbook/assets/serendale-gardens.png" alt=""><figcaption></figcaption></figure>

### Epochs and Emissions

Additionally, players can assign their [Hero](../../learn/gameplay/heroes/) NFTs to work in their gardens through [Gardening Quests](https://docs.defikingdoms.com/learn/gameplay/professions/gardening). Those Heroes earn additional rewards in JEWEL, CRYSTAL, or JADE based on the skill of the Hero and the amount of LP tokens staked in the garden they're tending, so players who stake LP tokens in the Gardens and quest Heroes in those same gardens have synergistic utility for their NFTs right away.

Each Power Token has its own emissions schedule. Generally speaking, emissions per minute/block are higher when the token launches, and decrease over time. This decrease in emissions is not linear, so it is important to review the emissions schedules for each token in its related Gardens subpage.

Emissions are governed by periods of time called Epochs. Each token starts in Epoch 1 on launch, which has the highest emission rate. With each Epoch, the rate may change or may remain consistent, as shown in each token's chart on its Gardens page.

Epochs are based on timestamps and last exactly one week.

### Allocations and Rewards

The total amount of each Power Token emitted per minute can be determined by Epoch, but those tokens have to go somewhere! Each individual garden (representing a specific incentivized LP pair) is assigned an allocation of the total tokens minted. The allocation for each incentivized pool can be viewed in the Seed Box on each realm. Based on the current Epoch, its emission rate, and the allocation for a specific pool, players can determine how many tokens will be emitted to that pool every second, minute, or day. From there, the pool divides those tokens among all of the players staking LP tokens in that pool proportional to their share of the total pool and distributes them as rewards. When making these calculations it is imperative to remember that players can enter or leave liquidity pools freely, so each player's share is constantly in flux as liquidity is added or removed.

#### Project Allocations

In order to fund the project and sustain rewards to players, and to avoid passing on additional fees, whenever a player claims their rewards in the Gardens, the Master Gardener contract mints an additional percentage (detailed on each token's allocation information) of the claimed token to project wallets, including the Jeweler. These mints do not come out of the Garden emissions per epoch as detailed on each realm's Gardens page, but they do count toward the token's total supply. These funds are subject to separate locking rates as follows:

* Development Fund, Marketing Fund, Jeweler - 45% locked
* Founders Fund - 95% locked

These locking rates allow for the stability and development of the project over time, while continuing to incentivize its long-term growth and success. They also provide guaranteed rewards over a lengthy period of time to players who [stake in the Jeweler](../the-jeweler/) on each realm.

### Locking Model

To balance the high emissions rates in earlier Epochs and to provide price stability, our tokenomics include a locking model on Gardens rewards. Until a certain point in each emission schedule, only a portion of the tokens grown, harvested, and distributed as Gardens rewards to LP token stakers is unlocked. Once claimed, these unlocked reward tokens transfer directly into the player’s wallet and are immediately usable. However, a portion of Gardens rewards are also locked deep underground. These rewards are allocated to the player's wallet, but cannot be traded and can only be used for certain in-game activities.

For each token, starting in Epoch 1, 5% of claimed rewards are unlocked while 95% are locked. Each Epoch, the percentage of claimed rewards that are unlocked increases by 2%, so in Epoch 2, 7% are unlocked and 93% are locked, and so on. It is important to note that these percentages are based on the Epoch at the time that the player chooses to claim, not when the rewards were allocated. If a player chooses not to claim right away, the percentage of tokens that will be unlocked that they will be able to claim increases by 2% each Epoch. Once a player does claim, however, the remainder of the claimed rewards, which are locked, remain locked until the end of Epoch 51, at which point they begin unlocking ratably over the next 52 Epochs, unless unlocked through other means, such as [Mining Quests](https://docs.defikingdoms.com/learn/gameplay/professions/jewel-mining). After Epoch 51, no further locking will occur and all newly generated rewards will be fully unlocked immediately.

#### Early Unlocking with Hero NFTs

One of the most unique features of DeFi Kingdoms is our NFTs, our [Heroes](../../learn/gameplay/heroes/), that provide true in-game utility. The Mining profession is one such use-case. Players who have locked rewards can send their Heroes on Mining Quests to unlock some of those tokens early, granting access to locked rewards before their natural unlock.

Not all Heroes will have the same level of proficiency in Mining, so it is important to learn about the various stats that Heroes use and how each profession works when looking to buy and use them. You can find more details about that in the [Profession Quests](https://docs.defikingdoms.com/learn/gameplay/professions) section of the documents.

### **Garden Staking Deposit and Withdrawal Fees**

**There are no deposit fees for staking LP tokens in the Gardens.** To protect against flash loans and pump and dumps, we have implemented withdrawal fees for withdrawing staked LP tokens. The first deposit and every subsequent withdrawal resets the fee timer. The withdrawal fees are listed below:

* **0.01%** fee if a user withdraws after **4 Epochs**
* **0.25%** fee if a user withdraws after **2 Epochs but before 4 Epochs**
* **0.5%** fee if a user withdraws after **5 days but before 2 Epochs**
* **1%** fee if a user withdraws in under **5 days.**
* **2%** fee if a user withdraws in under **3 days.**
* **4%** fee if a user withdraws in under **24 hours.**
* **8%** fee if a user withdraws in under **1 hour.**
* **25%** slashing fee if a user withdraws **during the same block.**
