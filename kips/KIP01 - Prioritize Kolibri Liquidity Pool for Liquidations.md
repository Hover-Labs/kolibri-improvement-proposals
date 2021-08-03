# Kolibri Improvement Proposal #01

### Preface
Hello everyone :)  
I am honored to present the first Kolibri Improvement Proposal. I feel like Satoshi in some sense right now.  
Kidding aside, I welcome and encourage everyone to participate in this and other proposals.  
Lets not forget that as kDAO holders and as a community, we are in the control of the future and success of Kolibri.  
I should also thank the Kolibri dev team for their hardwork and support.

### Summary
An onchain executable procedure to priorotize the Kolibri Liquidity Pool for oven liquidations.

### Motivation
The Kolibri Liquidity Pool (KLP) is an important and integral part of the kUSD algorithmic stable coin.  
It serves at least the following purposes :
1. Makes sure that big ovens that may not be liquidable by individuals, can be liquidated by the pooling the resources of individual kUSD investors.
2. Provides a fair return for the investors who are willing to help the kUSD ecosystem stability. 


The current implementation doesnt prioritize the KLP and individual investors compete for the liquidation of the over-collaterized ovens using high fees.  
Such implementation is not healthy for the ecosystem and will discourage the pool investors and may lead to disintegration of KLP due to small or no returns of their investment into KLP.  
In order to resolve this issue, I propose to give the KLP a X block priority for the liquidations.

### Details
In order to make an onchain executable procedure, I propose to make the Liquidation a 2 step process, Preliquidate and Liquidate.  
If an oven gets over-collaterized and is not in Preliquidation state, The Preliquidate entrypoint should be called which sets the Preliquidation state and prioritization expiry block height in the oven storage.  
The prioritization expiry block height is X blocks higher than the current block. (Can be 5 or 10 or ...)  
If an oven is in Preliquidation state and block height is less than expiry block height, only the KLP can execute the liquidate entry point.  
If an oven is in Preliquidation state and block height is higher or equal to expiry block height, meaning the prioritization duration has expired, anyone including KLP can execute the liquidate entry point.  
If an oven is in Preliquidation state but has become under-collaterized without liquidation for any reasons the ResetLiquidate entrypoint can be called which resets the Preliquidation state and expiry block height in the oven storage.  
In order to make sure these procedures are followed and executed by the community, the proper economic incentives are provided by the Kolibri DAO and users executing these procedures are awarded accordingly.  
The award can be kDAO tokens or a percentage of the successful KLP liquidations or etc.
