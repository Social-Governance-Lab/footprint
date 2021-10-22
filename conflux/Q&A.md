# Q&A
## 存储抵押机制 (CFS, collateral for storage)

#### Q: 为何世界状态中的存储条目被更改和删除时，将返还旧所有者抵押的资产？

链上原有状态是否还可追溯，记录变更所需的空间不需要支付吗？

> 当一个存储条目从世界状态中被删除时，<u>相应的1/16 CFX押金将被解锁并返回到该条目所有者的余额中</u>。如果一个存储条目的所有权发生变化，旧所有者的1/16 CFX押金被解锁，而新的所有者必须同时锁定1/16 CFX作为押金。<br>
[Conflux的存储抵押机制](https://juejin.cn/post/6855551378123653127#heading-3)

> ... if the execution of a transaction takes up new storage space, a portion of the CFX is pledged for the use of the storage space (<u>the pledged CFX can be released under certain condition</u>).<br>
[CFX](https://developer.confluxnetwork.org/introduction/en/conflux_basics#cfx)
```
// answer
```

## 数据结构

### 账户

#### Q: 未理解账户 `basic` 部分中的字段
> `nonce`: A scalar counter recording the number of previous activities initiated by this account. For example, the number of transactions send from account's address, or the number of contract-creations if the account represents a smart contract.<br>
`stakingBalance`: A scalar value equal to the number of Drip staked.<br>
[Basics-Account](https://developer.confluxnetwork.org/introduction/en/conflux_basics#account)