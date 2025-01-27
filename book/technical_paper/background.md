# Background

Nutbox 最终的目的是支持多个 PoS 链的资产抵押，并让区块链社区能够在基于各自所运行的 PoS 链的质押模型上构建自己的质押经济业务。因此，Nutbox 协议需要部署到支持跨链互操作的区块链网络中，而我们发现，这正是 Polkadot 所做的事情。polkadot 由 ethereum 黄皮书起草者，parity 公司创始人 Gavin Wood 博士创立，与 ethereum2.0 专注于采用分片技术提高网络可扩展性不同，polkadot 引入 relaychain 和 parachain，relaychain 由 parity 公司开发运营，所有人可以加入成为网络验证者，网络基于 NPoS 算法[3]选择每一个 session 的验证者集合，被选中的验证者负责本轮区块的验证，并获取奖励；parachain 由任意团队或个人开发，与一般区块链网络不同的是，parachain 没有自己的共识机制，parachain 区块由 relaychain 进行验证，parachain 区块构建后，将其以 PoV 格式广播给 relaychain 的验证者，通过验证后的区块将会被存储在 parachain 的网络中。Polkadot Relaychain 像每个 Parachain 的安全管家，负责各个 Parachain 的共识安全，让 Parachain 可以专注自己的业务。

 ![Image text](http://wherein.mobi/wp-content/uploads/2021/03/parachain-framework.png)
 
 图 2 Polkadot Parachain Framework

Nutbox 将以”Nutbox Contracts“或”Nutbox Parachain“两种方式的一种模式运行。Nutbox Contracts 模式是在 Nutbox blockchain 尚未开发完成，并且没有成功获取到 Polkadot 的平行链插槽时的运行方式，它将作为智能合约部署到支持EVM的区块链网络中；Nutbox Parachian 模式是当 Nutbox blockchain 通过 Polkadot 平行链插槽拍卖获取到了平行链插槽（slot）后，以 Polkadot 平行链身份接入到区块链网络，将不会有自己的共识模块，而是由 Polkadot 提供共识安全并验证 Nutbox blockchain 的区块。Nutbox 在两种模式下都将支持多个 PoS 链资产的抵押，只是两种模式下的实现方式有些许差异。

## Nutbox Contracts

当 Nutbox 未能以 Polkadot 平行链的形式运行时，它将以合约的形式部署在一条支持 EVM 虚拟机的区块链网络中。这个时候所有跨链的功能都将由 LTBSV 跨链桥协议提供支持。并且在 Nutbox 设计初期便会考虑到从合约到平行链的无缝迁移。

## Nutbox Parachain

当 Nutbox 作为运行在 Polkadot 生态里的 parachain 时，Nutbox 的部分跨链资产转移将直接采用 Polkadot 的跨链消息协议 XCM数学公式: $ [4] $来实现。假如 Nutbox 支持的另外一条链恰好也是一条 Polkadot 平行链，那么两条链之间将直接通过 XCM 协议的指令完成跨链转账；如果另一条链不是 Polkadot 平行链，那么 Nutbox 将使用下文描述的 LTBSV 跨链桥协议实现资产跨链转移。


