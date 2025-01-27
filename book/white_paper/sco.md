# Staking coin offering

Staking coin offering（SCO）是一种全新的链上资产发行方式。在ICO中，项目发起者要说服投资者一次性购买发行的新代币。而在SCO中，项目发起者需要说服投资者将资产质押到代币发行机构，并用质押收益持续购买项目的代币。

## Staking reward与Staking coin offering

Staking reward让SCO成为一个激动人心的创新。非技术项目创始人可以使用SCO智能合约在链上发行项目代币（communityToken，简称cToken）并以Staking的方式进行分发。用户只需质押PoS链资产到项目的链上节点（投票或代理等），就可以赚取cToken，项目方则获得Staking reward。比如，在Polkadot中，使用质押DOT提名Nutbox的验证者，可定期获得cToken。

与IEO、IDO、ICO不同，SCO延长了代币发行周期，以现金流方式支持项目方，降低了项目违约风险。SCO作为一种加密货币项目融资的方式，亦可解决以往的一些经典问题，例如缺乏问责制和流动性，以及代币投放市场初期的不完善价格发现机制。

## SCO的几种形式

根据PoS机制的不同，SCO主要有以下情形（cToken以Peanut社区PNUT为例）：

### 投票社区验证者获cToken

用户可以使用Staking Token的投票权，为可信的社区验证者（或见证人）投票获得cToken。例如用钱包里Staking Token（质押的DOT）通过SCO协议投票Nutbox.validator_peanut，获得PNUT。

<p align="center">

![Image text](http://wherein.mobi/wp-content/uploads/2021/03/Selecting-trustworthy-validators.png)

</p>

### 代理Staking Token获cToken

对于某些PoS共识链，Staking Token的使用权可以进行代理，用户可将Staking Token的使用权代理给Peanut社区（Nutbox v1）获得PNUT。例如将钱包里的Staking Token代理给peanut.mine，获得PNUT。

![Image text](http://wherein.mobi/wp-content/uploads/2021/03/Delegation-SP-Mint-cToken.png)

## 多链或多种形式开启SCO

对于社区用户拥有不同PoS链资产，或者同一条链有不同的质押方式的情况，Nutbox SCO通过多矿池对此进行支持。SCO将根据各矿池Staking reward的比例，对各矿池分发不同数量的cToken。

![Image text](http://wherein.mobi/wp-content/uploads/2021/03/cToken.png)

Nutbox通过Staking_pool_ratio（质押奖励挖矿比，简称spr）决定各矿池cToken分发的比例。spr与质押资产的价格（Staking_Token_price）、质押奖励（Staking_Token_reward）和挖矿系数（Mining_Token_ratio）有关。

假设Peanut社区支持ETH和Polkadot两条PoS链，参与ETH2.0以及质押DOT投票都可以获得PNUT（Peanut社区cToken）。使用质押DOT通过Peanut投票Nutbox.validator的矿池记为dPNUT，则：

![Image text](http://wherein.mobi/wp-content/uploads/2021/03/spr.png)

dPNUT=Spr（dPNUT）× PNUT

Spr将由系统根据各链和矿池数据，每6小时更新一次。

多池SCO可帮助社区成员支持其项目，而无需更改抵押资产组合的结构。 它还扩大了社区项目的财政资源。比如Polkadot的项目一样支持ETH2.0上的利息支持。

## Staking reward回购cToken

cToken的价值是以社区权益为价值支撑的。社区获得了用户Staking Token的Staking reward后可以选择用Staking reward回购cToken。Nutbox提供了触发式交易、荷兰式拍卖等多种合约，帮助社区建立回购策略。

回购的cToken可以进行销毁或为cToken的交易对提供流动性，还可以作为“库藏代币”保留，日后移作他用，这将由cToken持有人决定。

## cToken - 社区成长涡轮

使用SCO发行社区代币（cToken）的项目，cToken采用衰减式发行，质押挖矿的收益却随着Staking挖矿规模的增长而增长。如果采用收益回购模式下，将带来cToken价格机制性上涨。用户拥有持有cToken投资动机，而延迟兑付将提高质押挖矿的收益率。

同时，所有代币持有者就拥有了cToken这个共同利益。只有让社区壮大，社区Staking挖矿规模增加，才能让cToken增值。即使不考虑任何的引流模型，每一个投资社区Staking挖矿的成员都有动力增加社区Staking挖矿的规模。cToken本身就是一个社区成长的加速涡轮。
