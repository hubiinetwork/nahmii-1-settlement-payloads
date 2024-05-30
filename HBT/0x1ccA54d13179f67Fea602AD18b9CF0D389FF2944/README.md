# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1ccA54d13179f67Fea602AD18b9CF0D389FF2944`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000184eed91f0000000000000000000000000000000000000000000000000000000184eed91f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000184eed91f0000000000000000000000000000000000000000000000000000000184eed91fe4e3929f668450032ed1b2b617ab8bd853e5df1e31707784a3f69f0f71cab5fad3c865dab230932c3ce92abf725b09005c7de9f6ea1c28f521fbf31bd846f9dc3e2019b427389e6cfe9e8b93f9cd4f735cb177ad2eb130743422fa104683d975000000000000000000000000000000000000000000000000000000000000001c0c81e4c9ba0f84e196a945f9e9bef1208fd74940fa39ac4316e74e2e2c9911e1fa2d5411304ad8b7a863c1d4b6b59d9216ee32eee31f3f51d4fd16aca56a57622c7c39aabd3f4464d71482b0d46c337ec0da3af42b97da14f46073ebcc6257c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5665000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014f300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e215e86763415000000000000000000000000000000000000000000000000002e21600bc89e5000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000063911c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b7b965c4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6a51344f575531595330324e4459794c5455304f5459744f544d334d79316b4e3251795a444a6d5a6a6b7a4e474d6966513d3d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000001cca54d13179f67fea602ad18b9cf0d389ff29440000000000000000000000000000000000000000000000000000000184eed91f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe4e3929f668450032ed1b2b617ab8bd853e5df1e31707784a3f69f0f71cab5fa",
      "signature": {
        "s": "0x3e2019b427389e6cfe9e8b93f9cd4f735cb177ad2eb130743422fa104683d975",
        "r": "0xd3c865dab230932c3ce92abf725b09005c7de9f6ea1c28f521fbf31bd846f9dc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0c81e4c9ba0f84e196a945f9e9bef1208fd74940fa39ac4316e74e2e2c9911e1",
      "signature": {
        "s": "0x2c7c39aabd3f4464d71482b0d46c337ec0da3af42b97da14f46073ebcc6257c9",
        "r": "0xfa2d5411304ad8b7a863c1d4b6b59d9216ee32eee31f3f51d4fd16aca56a5762",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6525212959",
    "total": "6525212959"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6525212959",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "33147151812"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6525212"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNjQ4OWU1YS02NDYyLTU0OTYtOTM3My1kN2QyZDJmZjkzNGMifQ==",
    "nonce": 5363,
    "balances": {
      "current": "12984538795226133",
      "previous": "12984545326964304"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1cca54d13179f67fea602ad18b9cf0d389ff2944",
    "nonce": 28,
    "balances": {
      "current": "6525212959",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:34.032Z",
  "updated": "2020-05-22T08:40:34.096Z",
  "id": "5ec79002e5756b00111b8654"
}
```
* *stageAmount*: `6525212959`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000184eed91f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000184eed91f0000000000000000000000000000000000000000000000000000000184eed91fe4e3929f668450032ed1b2b617ab8bd853e5df1e31707784a3f69f0f71cab5fad3c865dab230932c3ce92abf725b09005c7de9f6ea1c28f521fbf31bd846f9dc3e2019b427389e6cfe9e8b93f9cd4f735cb177ad2eb130743422fa104683d975000000000000000000000000000000000000000000000000000000000000001c0c81e4c9ba0f84e196a945f9e9bef1208fd74940fa39ac4316e74e2e2c9911e1fa2d5411304ad8b7a863c1d4b6b59d9216ee32eee31f3f51d4fd16aca56a57622c7c39aabd3f4464d71482b0d46c337ec0da3af42b97da14f46073ebcc6257c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5665000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014f300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e215e86763415000000000000000000000000000000000000000000000000002e21600bc89e5000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000063911c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b7b965c4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6a51344f575531595330324e4459794c5455304f5459744f544d334d79316b4e3251795a444a6d5a6a6b7a4e474d6966513d3d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000001cca54d13179f67fea602ad18b9cf0d389ff29440000000000000000000000000000000000000000000000000000000184eed91f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe4e3929f668450032ed1b2b617ab8bd853e5df1e31707784a3f69f0f71cab5fa",
      "signature": {
        "s": "0x3e2019b427389e6cfe9e8b93f9cd4f735cb177ad2eb130743422fa104683d975",
        "r": "0xd3c865dab230932c3ce92abf725b09005c7de9f6ea1c28f521fbf31bd846f9dc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0c81e4c9ba0f84e196a945f9e9bef1208fd74940fa39ac4316e74e2e2c9911e1",
      "signature": {
        "s": "0x2c7c39aabd3f4464d71482b0d46c337ec0da3af42b97da14f46073ebcc6257c9",
        "r": "0xfa2d5411304ad8b7a863c1d4b6b59d9216ee32eee31f3f51d4fd16aca56a5762",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6525212959",
    "total": "6525212959"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6525212959",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "33147151812"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6525212"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNjQ4OWU1YS02NDYyLTU0OTYtOTM3My1kN2QyZDJmZjkzNGMifQ==",
    "nonce": 5363,
    "balances": {
      "current": "12984538795226133",
      "previous": "12984545326964304"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1cca54d13179f67fea602ad18b9cf0d389ff2944",
    "nonce": 28,
    "balances": {
      "current": "6525212959",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:34.032Z",
  "updated": "2020-05-22T08:40:34.096Z",
  "id": "5ec79002e5756b00111b8654"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000184eed91f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6525212959`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`