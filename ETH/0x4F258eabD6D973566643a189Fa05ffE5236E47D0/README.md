# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4F258eabD6D973566643a189Fa05ffE5236E47D0`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000e160000000000000000000000000000000000000000000000000000000000000e1600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000e160000000000000000000000000000000000000000000000000000000000000e1668eefdfb585c2d61accbc08bf479705a1a5636cf92bed0a805e11f7681daa6bd8ffa65348d2fe635dab88d7af4546c5328259b2031ae1f6354b056e32609714b3e4f213af1d3c1d759e2aa13287906c4a600c6a607b1a6cdf9f59300cecb406b000000000000000000000000000000000000000000000000000000000000001bd46f72de87439911a3a56a66ace30ed6c9b8a0548e1f9497b82630693be178adfbc63e208dbc4909969bcebf9f4e370c6dbd078dc5d63eafb9e1165bb25e386c3bbe1ef07391c4d38fcac2235eff44bb9df02dfd37526b392b78fc722e4f47b1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000089400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc7019ae000000000000000000000000000000000000000000000000002386f2bc7027c700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c27a300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a4a684d3251305a5330354d5445314c5456684f5451744f4759785a43316b5a6a56695a5759344d6a41794d57596966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000004f258eabd6d973566643a189fa05ffe5236e47d00000000000000000000000000000000000000000000000000000000000000e16000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x68eefdfb585c2d61accbc08bf479705a1a5636cf92bed0a805e11f7681daa6bd",
      "signature": {
        "s": "0x3e4f213af1d3c1d759e2aa13287906c4a600c6a607b1a6cdf9f59300cecb406b",
        "r": "0x8ffa65348d2fe635dab88d7af4546c5328259b2031ae1f6354b056e32609714b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd46f72de87439911a3a56a66ace30ed6c9b8a0548e1f9497b82630693be178ad",
      "signature": {
        "s": "0x3bbe1ef07391c4d38fcac2235eff44bb9df02dfd37526b392b78fc722e4f47b1",
        "r": "0xfbc63e208dbc4909969bcebf9f4e370c6dbd078dc5d63eafb9e1165bb25e386c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3606",
    "total": "3606"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3606",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "796579"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNjJhM2Q0ZS05MTE1LTVhOTQtOGYxZC1kZjViZWY4MjAyMWYifQ==",
    "nonce": 2196,
    "balances": {
      "current": "10000001286543790",
      "previous": "10000001286547399"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4f258eabd6d973566643a189fa05ffe5236e47d0",
    "nonce": 8,
    "balances": {
      "current": "3606",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:14:57.879Z",
  "updated": "2020-05-22T08:14:57.949Z",
  "id": "5ec78a01b0c6090011d5abab"
}
```
* *stageAmount*: `3606`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000e1600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000e160000000000000000000000000000000000000000000000000000000000000e1668eefdfb585c2d61accbc08bf479705a1a5636cf92bed0a805e11f7681daa6bd8ffa65348d2fe635dab88d7af4546c5328259b2031ae1f6354b056e32609714b3e4f213af1d3c1d759e2aa13287906c4a600c6a607b1a6cdf9f59300cecb406b000000000000000000000000000000000000000000000000000000000000001bd46f72de87439911a3a56a66ace30ed6c9b8a0548e1f9497b82630693be178adfbc63e208dbc4909969bcebf9f4e370c6dbd078dc5d63eafb9e1165bb25e386c3bbe1ef07391c4d38fcac2235eff44bb9df02dfd37526b392b78fc722e4f47b1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000089400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc7019ae000000000000000000000000000000000000000000000000002386f2bc7027c700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c27a300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a4a684d3251305a5330354d5445314c5456684f5451744f4759785a43316b5a6a56695a5759344d6a41794d57596966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000004f258eabd6d973566643a189fa05ffe5236e47d00000000000000000000000000000000000000000000000000000000000000e16000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x68eefdfb585c2d61accbc08bf479705a1a5636cf92bed0a805e11f7681daa6bd",
      "signature": {
        "s": "0x3e4f213af1d3c1d759e2aa13287906c4a600c6a607b1a6cdf9f59300cecb406b",
        "r": "0x8ffa65348d2fe635dab88d7af4546c5328259b2031ae1f6354b056e32609714b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd46f72de87439911a3a56a66ace30ed6c9b8a0548e1f9497b82630693be178ad",
      "signature": {
        "s": "0x3bbe1ef07391c4d38fcac2235eff44bb9df02dfd37526b392b78fc722e4f47b1",
        "r": "0xfbc63e208dbc4909969bcebf9f4e370c6dbd078dc5d63eafb9e1165bb25e386c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3606",
    "total": "3606"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3606",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "796579"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNjJhM2Q0ZS05MTE1LTVhOTQtOGYxZC1kZjViZWY4MjAyMWYifQ==",
    "nonce": 2196,
    "balances": {
      "current": "10000001286543790",
      "previous": "10000001286547399"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4f258eabd6d973566643a189fa05ffe5236e47d0",
    "nonce": 8,
    "balances": {
      "current": "3606",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:14:57.879Z",
  "updated": "2020-05-22T08:14:57.949Z",
  "id": "5ec78a01b0c6090011d5abab"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000e160000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3606`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``