---
description: '主页: https://daml.com/'
---

# DAML简介

## 一门专为区块链开发而打造的语言

> DAML is a smart contract language designed to build composable applications on an abstract [DAML Ledger Model](https://docs.daml.com/concepts/ledger-model/index.html#da-ledgers).

DAML\(全称Digital Asset Modelling Language\), 是由Digital Asset专为区块链应用开发打造的一门编程语言。  
相比于其他更通用的编程语言，比如HyperLedger提供API的Go，Java，Python等，DAML让开发人员更专注于智能合约（Smart Contract）逻辑（logic）的编程。  
并且DAML可以运行在诸如HyperLedger Fabric，HyperLedger Sawtooth，Corda等区块链框架平台，甚至PostgreSQL上，真正做到一切编写，多处运行\(Write Once, Interoperate Anywhere\)  
DAML是基于Haskell打造的，有很多共通点，但也有一些不同之处。  
DAML是强类型（strong typed）的编程语言。  


{% hint style="info" %}
 DAML只是区块链编程语言，并不涉及共识算法，throughput等，共识算法取决于部署，运行的平台（比如Sawtooth，Fabric）等。
{% endhint %}

### 

## 官方教程 & 链接

* [DAML官方文档](https://docs.daml.com/)
* [DAML Youtube Channel ](https://www.youtube.com/channel/UCogfiTgCgVubpLQ1i1VmPPg)
* [DAML 官方论坛](https://discuss.daml.com/)



{% hint style="danger" %}
请注意： DAML仍处于快速迭代开发中。即便是官方文档也可能与实际SDK有出入。

比如在很多sample code中首行仍是“daml 1.2”，用以声明版本号，但在较新版本的sdk中，已经不需要再在单个file中特殊声明。  
  
所以，官方文档仍有错误，阅读时需多加思考。
{% endhint %}

