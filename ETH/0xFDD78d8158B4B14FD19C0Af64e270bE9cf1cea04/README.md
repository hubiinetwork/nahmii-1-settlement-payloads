# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFDD78d8158B4B14FD19C0Af64e270bE9cf1cea04`.

The ordered steps of contract function invocations are included below and in
the corresponding [steps.json](./steps.json). Please read [the general recipe
for settling Nahmii 1 balance](../../README.md) before starting on the first
step of settlement.

## Ordered steps
### Step 1
#### Contract
*NullSettlementChallengeByPayment* ([0x34fe0c8100dc8ec65e50ff195faa93297ebf4f19](https://etherscan.io/address/0x34fe0c8100dc8ec65e50ff195faa93297ebf4f19))
#### Method name
*startChallenge*
#### Method payload
```
0xc1c681650000000000000000000000000000000000000000000000000429d069189e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *stageAmount*: `300000000000000000`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
### Step 2
#### Contract
*NullSettlement* ([0x4dd0200874480fa4a6e72a6a9a4d020aff338085](https://etherscan.io/address/0x4dd0200874480fa4a6e72a6a9a4d020aff338085))
#### Method name
*settleNull*
#### Method payload
```
0x66a83a6f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000429d069189e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `300000000000000000`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``