# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xfd2418617b08030AFB197F64EC6325673B539F7c`.

The ordered steps of contract function invocations are included below and in
the corresponding [steps.json](./steps.json). Please read [the general recipe
for settling Nahmii 1 balance](../../README.md) before starting on the first
step of settlement.

## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000e43d4bb6f65d000000000000000000000000000000000000000000000000000005694ae2a8110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000005694ae2a811000000000000000000000000000000000000000000000000000097d8a7b13e39d820bdb63a415b72fac4e884203b5e3729381c0b1922528d503b933f0db861c1c03d87527524405b3be08cc29038f0e2240db6abc8a5e1b0f8b4521cc27e476269ba3a4e0116d35494611a4e645e9e8083bfef663d571beacff7d63cba261504000000000000000000000000000000000000000000000000000000000000001c3d3906a5c6cd7e096b2783cdf51b03a4e176c464fea6069dc67fa2ae7ef8a225c7ec258523d00e71b3ee15cf448b2199aa5828454be83bd4a07709407037a4dc683be6d3c075cb6cfb0740e72636a2e96803b3d85b4596d2c1a538ae6f07df96000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abb5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c1b22be6fe81dfb5cb5000000000000000000000000000000000000000000009c1b22be7552cb808c9f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000162a287d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c475a66bdccd9a6a5f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a6a4e695a6d4a6c5a533031596d59344c5455794e544d744f5451314e43316a5a6d59775a54677a5a444e6d4f44496966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000fd2418617b08030afb197f64ec6325673b539f7c0000000000000000000000000000000000000000000000000000e43d4bb6f65d0000000000000000000000000000000000000000000000000000ded400d44e4c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd820bdb63a415b72fac4e884203b5e3729381c0b1922528d503b933f0db861c1",
      "signature": {
        "s": "0x69ba3a4e0116d35494611a4e645e9e8083bfef663d571beacff7d63cba261504",
        "r": "0xc03d87527524405b3be08cc29038f0e2240db6abc8a5e1b0f8b4521cc27e4762",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3d3906a5c6cd7e096b2783cdf51b03a4e176c464fea6069dc67fa2ae7ef8a225",
      "signature": {
        "s": "0x683be6d3c075cb6cfb0740e72636a2e96803b3d85b4596d2c1a538ae6f07df96",
        "r": "0xc7ec258523d00e71b3ee15cf448b2199aa5828454be83bd4a07709407037a4dc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5949786073105",
    "total": "166956782140985"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5949786073105",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27235871834739956148831"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5949786073"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhZjNiZmJlZS01YmY4LTUyNTMtOTQ1NC1jZmYwZTgzZDNmODIifQ==",
    "nonce": 109493,
    "balances": {
      "current": "737189736979140401913013",
      "previous": "737189736985096137772191"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfd2418617b08030afb197f64ec6325673b539f7c",
    "nonce": 45,
    "balances": {
      "current": "250951914419805",
      "previous": "245002128346700"
    }
  },
  "blockNumber": "14709942",
  "created": "2022-05-04T08:48:24.007Z",
  "updated": "2022-05-04T08:48:24.085Z",
  "id": "62723dd83592fd001130b3a9"
}
```
* *stageAmount*: `250951914419805`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000005694ae2a8110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000005694ae2a811000000000000000000000000000000000000000000000000000097d8a7b13e39d820bdb63a415b72fac4e884203b5e3729381c0b1922528d503b933f0db861c1c03d87527524405b3be08cc29038f0e2240db6abc8a5e1b0f8b4521cc27e476269ba3a4e0116d35494611a4e645e9e8083bfef663d571beacff7d63cba261504000000000000000000000000000000000000000000000000000000000000001c3d3906a5c6cd7e096b2783cdf51b03a4e176c464fea6069dc67fa2ae7ef8a225c7ec258523d00e71b3ee15cf448b2199aa5828454be83bd4a07709407037a4dc683be6d3c075cb6cfb0740e72636a2e96803b3d85b4596d2c1a538ae6f07df96000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abb5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c1b22be6fe81dfb5cb5000000000000000000000000000000000000000000009c1b22be7552cb808c9f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000162a287d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c475a66bdccd9a6a5f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a6a4e695a6d4a6c5a533031596d59344c5455794e544d744f5451314e43316a5a6d59775a54677a5a444e6d4f44496966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000fd2418617b08030afb197f64ec6325673b539f7c0000000000000000000000000000000000000000000000000000e43d4bb6f65d0000000000000000000000000000000000000000000000000000ded400d44e4c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd820bdb63a415b72fac4e884203b5e3729381c0b1922528d503b933f0db861c1",
      "signature": {
        "s": "0x69ba3a4e0116d35494611a4e645e9e8083bfef663d571beacff7d63cba261504",
        "r": "0xc03d87527524405b3be08cc29038f0e2240db6abc8a5e1b0f8b4521cc27e4762",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3d3906a5c6cd7e096b2783cdf51b03a4e176c464fea6069dc67fa2ae7ef8a225",
      "signature": {
        "s": "0x683be6d3c075cb6cfb0740e72636a2e96803b3d85b4596d2c1a538ae6f07df96",
        "r": "0xc7ec258523d00e71b3ee15cf448b2199aa5828454be83bd4a07709407037a4dc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5949786073105",
    "total": "166956782140985"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5949786073105",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27235871834739956148831"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5949786073"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhZjNiZmJlZS01YmY4LTUyNTMtOTQ1NC1jZmYwZTgzZDNmODIifQ==",
    "nonce": 109493,
    "balances": {
      "current": "737189736979140401913013",
      "previous": "737189736985096137772191"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfd2418617b08030afb197f64ec6325673b539f7c",
    "nonce": 45,
    "balances": {
      "current": "250951914419805",
      "previous": "245002128346700"
    }
  },
  "blockNumber": "14709942",
  "created": "2022-05-04T08:48:24.007Z",
  "updated": "2022-05-04T08:48:24.085Z",
  "id": "62723dd83592fd001130b3a9"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000000e43d4bb6f65d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `250951914419805`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`