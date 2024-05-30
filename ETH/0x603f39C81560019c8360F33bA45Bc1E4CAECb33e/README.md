# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x603f39C81560019c8360F33bA45Bc1E4CAECb33e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000016c9c0000000000000000000000000000000000000000000000000000000000016c9c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000016c9c0000000000000000000000000000000000000000000000000000000000016c9c6e8950b5643654063eb231d59e58021f4cb962d0f9fcc918eec0a671c16c106ba16da20ee08fcfe42fe9cc1040da8829f5e88006644d5014ab986fe474aa38f60b3be5ffda1e42a058f7db4dfc3353d675827e912491fa8a00b561d0c6f58317000000000000000000000000000000000000000000000000000000000000001b5161a389bd328ce5b61a818984f3d8936af48830d681b4301272c8975b3871a39d77a5c8a19bcbc445186f0791c5740f5570cc98f124fa6899fb733f70a6562921e8d5ff0ddc3f3db7370412224251edb8d71092021bdb0a92b3316c67043390000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004f000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7bde39a000000000000000000000000000000000000000000000000002386f2c7bf509300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000944d100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596a59304d6a4e6a4d533034597a4a6a4c5455344e446b744f5451315a4330324e6d51315954597a596d4d334e544d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000603f39c81560019c8360f33ba45bc1e4caecb33e0000000000000000000000000000000000000000000000000000000000016c9c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6e8950b5643654063eb231d59e58021f4cb962d0f9fcc918eec0a671c16c106b",
      "signature": {
        "s": "0x0b3be5ffda1e42a058f7db4dfc3353d675827e912491fa8a00b561d0c6f58317",
        "r": "0xa16da20ee08fcfe42fe9cc1040da8829f5e88006644d5014ab986fe474aa38f6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5161a389bd328ce5b61a818984f3d8936af48830d681b4301272c8975b3871a3",
      "signature": {
        "s": "0x21e8d5ff0ddc3f3db7370412224251edb8d71092021bdb0a92b3316c67043390",
        "r": "0x9d77a5c8a19bcbc445186f0791c5740f5570cc98f124fa6899fb733f70a65629",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "93340",
    "total": "93340"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "93340",
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
            "amount": "607441"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "93"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYjY0MjNjMS04YzJjLTU4NDktOTQ1ZC02NmQ1YTYzYmM3NTMifQ==",
    "nonce": 1264,
    "balances": {
      "current": "10000001476191130",
      "previous": "10000001476284563"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x603f39c81560019c8360f33ba45bc1e4caecb33e",
    "nonce": 20,
    "balances": {
      "current": "93340",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:03.660Z",
  "updated": "2020-05-22T08:08:03.732Z",
  "id": "5ec78863b0c6090011d5aa6d"
}
```
* *stageAmount*: `93340`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000016c9c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000016c9c0000000000000000000000000000000000000000000000000000000000016c9c6e8950b5643654063eb231d59e58021f4cb962d0f9fcc918eec0a671c16c106ba16da20ee08fcfe42fe9cc1040da8829f5e88006644d5014ab986fe474aa38f60b3be5ffda1e42a058f7db4dfc3353d675827e912491fa8a00b561d0c6f58317000000000000000000000000000000000000000000000000000000000000001b5161a389bd328ce5b61a818984f3d8936af48830d681b4301272c8975b3871a39d77a5c8a19bcbc445186f0791c5740f5570cc98f124fa6899fb733f70a6562921e8d5ff0ddc3f3db7370412224251edb8d71092021bdb0a92b3316c67043390000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004f000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7bde39a000000000000000000000000000000000000000000000000002386f2c7bf509300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000944d100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596a59304d6a4e6a4d533034597a4a6a4c5455344e446b744f5451315a4330324e6d51315954597a596d4d334e544d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000603f39c81560019c8360f33ba45bc1e4caecb33e0000000000000000000000000000000000000000000000000000000000016c9c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6e8950b5643654063eb231d59e58021f4cb962d0f9fcc918eec0a671c16c106b",
      "signature": {
        "s": "0x0b3be5ffda1e42a058f7db4dfc3353d675827e912491fa8a00b561d0c6f58317",
        "r": "0xa16da20ee08fcfe42fe9cc1040da8829f5e88006644d5014ab986fe474aa38f6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5161a389bd328ce5b61a818984f3d8936af48830d681b4301272c8975b3871a3",
      "signature": {
        "s": "0x21e8d5ff0ddc3f3db7370412224251edb8d71092021bdb0a92b3316c67043390",
        "r": "0x9d77a5c8a19bcbc445186f0791c5740f5570cc98f124fa6899fb733f70a65629",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "93340",
    "total": "93340"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "93340",
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
            "amount": "607441"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "93"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYjY0MjNjMS04YzJjLTU4NDktOTQ1ZC02NmQ1YTYzYmM3NTMifQ==",
    "nonce": 1264,
    "balances": {
      "current": "10000001476191130",
      "previous": "10000001476284563"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x603f39c81560019c8360f33ba45bc1e4caecb33e",
    "nonce": 20,
    "balances": {
      "current": "93340",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:03.660Z",
  "updated": "2020-05-22T08:08:03.732Z",
  "id": "5ec78863b0c6090011d5aa6d"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000016c9c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `93340`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``