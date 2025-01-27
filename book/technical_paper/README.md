# Introduction

一直以来，无论是在传统社区还是区块链社区里，社区运营者都苦恼于如何使社区能够活跃起来，最初因为区块链通证经济的兴起，社区会选择发行自己的社区代币，以激励参与到社区里的用户，促使社区能在社区代币的驱动下拥有更高的活跃度，更高的价值捕获。比如，一个运行共享应用软件的社区会发行自己的代币，共享和租赁物品都可以获取到社区的代币，通过这种方式，社区成员在使用产品的同时，也获取到了额外的经济激励。

然而就目前来看，社区只是发行自己的代币是远远不够的。社区发行自己的代币后，短期能够起到刺激社区活跃度、提高社区价值的作用，长期来看，社区代币最终往往因为缺乏一个完整的价格支撑体系或者说没有形成良好的经济内循环，而不能给社区带来实质性的改变。因此让社区代币能够真正的在社区里健康的流通起来成为了行业急需解决的难题。

PoS共识算法[1]的流行给我们提供了一套新的解决思路。PoS 共识算法用来解决区块链网络在原有的 PoW 共识算法[2]下 TPS 低，系统可扩展性差等问题。不同于 PoW 共识算法任何人只要提供硬件设备便可以接入区块链网络成为验证者，在基于 PoS 共识算法的区块链网络中，用户需要抵押一定数量的网络资产，然后再成为了验证者后通过验证区块获取奖励；当退出作为验证者时，仍然可以取回自己抵押的资产。在 PoS 共识系统下，参与到网络中节点不用再进行硬件竞赛，以至于耗费大量的电力资源。这种抵押区块链网络原生资产并在此基础上获取收益的经济模型，具有良好的经济闭环，能够使区块链网络在一个健康的经济循环下长久稳定的运行下去。

遗憾的是目前这种经济模式只被用于区块链网络本身的共识系统，它并没有为运行在区块链网络中的应用即背后所代表的一个个区块链应用社区带来直接的价值。而 Nutbox 要做的，便是构建一个开放的资产质押协议，能够让区块链社区在基于 PoS 共识算法的区块链网络中，为自己的社区资产构建质押经济模型。

 ![Image text](http://wherein.mobi/wp-content/uploads/2021/03/staking-factory.png)

图1 一个运行在PoS区块链网络中的Staking工厂
