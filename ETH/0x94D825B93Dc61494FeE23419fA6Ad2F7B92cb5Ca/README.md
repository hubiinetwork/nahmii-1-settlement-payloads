# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x94D825B93Dc61494FeE23419fA6Ad2F7B92cb5Ca`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000005e200000000000000000000000000000000000000000000000000000000000005e2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000005e200000000000000000000000000000000000000000000000000000000000005e26e5a23f47491b851629d1a5bec58a972d7661750b7b05efde6331e26834e931d190f9d688867f0c5554f11b17ad95ba1b909e24d378c54ee0c59d7a90c6c86df280ce4eb0d3d42b3c86a8be1863137e82ac69c02431fa767590bb9b1ea60eabe000000000000000000000000000000000000000000000000000000000000001b905cd8fe19ebdc16c57de8f47be0317e4e234b7783157c71309fc2700b0e0b7e22c10513195f3c8c9e538399a8a595ed59b265e5727a8fbafc6c3f9e3665bf410d85f0231eca90750c28bde9b497c87c8cb7f7f7e05949cbf4af0de93dcff619000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000092000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc518471000000000000000000000000000000000000000000000000002386f2bc518a5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2f7600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a4445314d3245334e7930304d6d526b4c5455334d7a4d744f546b785a693030596d55314d6a59304d4752694f444d6966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000094d825b93dc61494fee23419fa6ad2f7b92cb5ca00000000000000000000000000000000000000000000000000000000000005e2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6e5a23f47491b851629d1a5bec58a972d7661750b7b05efde6331e26834e931d",
      "signature": {
        "s": "0x280ce4eb0d3d42b3c86a8be1863137e82ac69c02431fa767590bb9b1ea60eabe",
        "r": "0x190f9d688867f0c5554f11b17ad95ba1b909e24d378c54ee0c59d7a90c6c86df",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x905cd8fe19ebdc16c57de8f47be0317e4e234b7783157c71309fc2700b0e0b7e",
      "signature": {
        "s": "0x0d85f0231eca90750c28bde9b497c87c8cb7f7f7e05949cbf4af0de93dcff619",
        "r": "0x22c10513195f3c8c9e538399a8a595ed59b265e5727a8fbafc6c3f9e3665bf41",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1506",
    "total": "1506"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1506",
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
            "amount": "798582"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzZDE1M2E3Ny00MmRkLTU3MzMtOTkxZi00YmU1MjY0MGRiODMifQ==",
    "nonce": 2336,
    "balances": {
      "current": "10000001284539505",
      "previous": "10000001284541012"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x94d825b93dc61494fee23419fa6ad2f7b92cb5ca",
    "nonce": 3,
    "balances": {
      "current": "1506",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:51.568Z",
  "updated": "2020-05-22T08:15:51.864Z",
  "id": "5ec78a37b0c6090011d5abdb"
}
```
* *stageAmount*: `1506`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000005e2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000005e200000000000000000000000000000000000000000000000000000000000005e26e5a23f47491b851629d1a5bec58a972d7661750b7b05efde6331e26834e931d190f9d688867f0c5554f11b17ad95ba1b909e24d378c54ee0c59d7a90c6c86df280ce4eb0d3d42b3c86a8be1863137e82ac69c02431fa767590bb9b1ea60eabe000000000000000000000000000000000000000000000000000000000000001b905cd8fe19ebdc16c57de8f47be0317e4e234b7783157c71309fc2700b0e0b7e22c10513195f3c8c9e538399a8a595ed59b265e5727a8fbafc6c3f9e3665bf410d85f0231eca90750c28bde9b497c87c8cb7f7f7e05949cbf4af0de93dcff619000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000092000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc518471000000000000000000000000000000000000000000000000002386f2bc518a5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2f7600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a4445314d3245334e7930304d6d526b4c5455334d7a4d744f546b785a693030596d55314d6a59304d4752694f444d6966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000094d825b93dc61494fee23419fa6ad2f7b92cb5ca00000000000000000000000000000000000000000000000000000000000005e2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6e5a23f47491b851629d1a5bec58a972d7661750b7b05efde6331e26834e931d",
      "signature": {
        "s": "0x280ce4eb0d3d42b3c86a8be1863137e82ac69c02431fa767590bb9b1ea60eabe",
        "r": "0x190f9d688867f0c5554f11b17ad95ba1b909e24d378c54ee0c59d7a90c6c86df",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x905cd8fe19ebdc16c57de8f47be0317e4e234b7783157c71309fc2700b0e0b7e",
      "signature": {
        "s": "0x0d85f0231eca90750c28bde9b497c87c8cb7f7f7e05949cbf4af0de93dcff619",
        "r": "0x22c10513195f3c8c9e538399a8a595ed59b265e5727a8fbafc6c3f9e3665bf41",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1506",
    "total": "1506"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1506",
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
            "amount": "798582"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzZDE1M2E3Ny00MmRkLTU3MzMtOTkxZi00YmU1MjY0MGRiODMifQ==",
    "nonce": 2336,
    "balances": {
      "current": "10000001284539505",
      "previous": "10000001284541012"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x94d825b93dc61494fee23419fa6ad2f7b92cb5ca",
    "nonce": 3,
    "balances": {
      "current": "1506",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:51.568Z",
  "updated": "2020-05-22T08:15:51.864Z",
  "id": "5ec78a37b0c6090011d5abdb"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000005e20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1506`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``