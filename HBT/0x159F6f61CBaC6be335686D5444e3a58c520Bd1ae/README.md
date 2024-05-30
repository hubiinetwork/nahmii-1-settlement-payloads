# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x159F6f61CBaC6be335686D5444e3a58c520Bd1ae`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000eea29a26e38e2bbfa9483dd5f015f86ba9c7dc8dc95caa8a2a51667f87139f43214eaec6302944401ef9150113d025fd508aa8c26dc164abd1518fd43fb6a3cff41ec69685a83d3ffdc8ce79045e930a48b07f55b85636069ebeabbf6764673f4000000000000000000000000000000000000000000000000000000000000001b6c130bb8dcb13e6396a1eac162ad8f4d87c3dff623697b7e665da8276f711e5e8462fc60f336e6c4ef3a1927e328666273a8d8c483d0398199b71f109da5dfcf3f849db4b5569ce1b899756ec83a99da1dfc46efe202de476619272b7ccccd98000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000193c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e180829c6d710000000000000000000000000000000000000000000000000002e180829c6d71f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1b0ba903000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596a41784d4445334e7930784f4759334c54557a59325574596a64684e533169597a49334e44526b596a517a5a57516966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000159f6f61cbac6be335686d5444e3a58c520bd1ae000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xea29a26e38e2bbfa9483dd5f015f86ba9c7dc8dc95caa8a2a51667f87139f432",
      "signature": {
        "s": "0x41ec69685a83d3ffdc8ce79045e930a48b07f55b85636069ebeabbf6764673f4",
        "r": "0x14eaec6302944401ef9150113d025fd508aa8c26dc164abd1518fd43fb6a3cff",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6c130bb8dcb13e6396a1eac162ad8f4d87c3dff623697b7e665da8276f711e5e",
      "signature": {
        "s": "0x3f849db4b5569ce1b899756ec83a99da1dfc46efe202de476619272b7ccccd98",
        "r": "0x8462fc60f336e6c4ef3a1927e328666273a8d8c483d0398199b71f109da5dfcf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14",
    "total": "14"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14",
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
            "amount": "43403421955"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYjAxMDE3Ny0xOGY3LTUzY2UtYjdhNS1iYzI3NDRkYjQzZWQifQ==",
    "nonce": 6460,
    "balances": {
      "current": "12974272268392208",
      "previous": "12974272268392223"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x159f6f61cbac6be335686d5444e3a58c520bd1ae",
    "nonce": 21,
    "balances": {
      "current": "14",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:17.817Z",
  "updated": "2020-05-22T08:49:17.888Z",
  "id": "5ec7920db0c6090011d5b132"
}
```
* *stageAmount*: `14`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000eea29a26e38e2bbfa9483dd5f015f86ba9c7dc8dc95caa8a2a51667f87139f43214eaec6302944401ef9150113d025fd508aa8c26dc164abd1518fd43fb6a3cff41ec69685a83d3ffdc8ce79045e930a48b07f55b85636069ebeabbf6764673f4000000000000000000000000000000000000000000000000000000000000001b6c130bb8dcb13e6396a1eac162ad8f4d87c3dff623697b7e665da8276f711e5e8462fc60f336e6c4ef3a1927e328666273a8d8c483d0398199b71f109da5dfcf3f849db4b5569ce1b899756ec83a99da1dfc46efe202de476619272b7ccccd98000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000193c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e180829c6d710000000000000000000000000000000000000000000000000002e180829c6d71f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1b0ba903000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596a41784d4445334e7930784f4759334c54557a59325574596a64684e533169597a49334e44526b596a517a5a57516966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000159f6f61cbac6be335686d5444e3a58c520bd1ae000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xea29a26e38e2bbfa9483dd5f015f86ba9c7dc8dc95caa8a2a51667f87139f432",
      "signature": {
        "s": "0x41ec69685a83d3ffdc8ce79045e930a48b07f55b85636069ebeabbf6764673f4",
        "r": "0x14eaec6302944401ef9150113d025fd508aa8c26dc164abd1518fd43fb6a3cff",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6c130bb8dcb13e6396a1eac162ad8f4d87c3dff623697b7e665da8276f711e5e",
      "signature": {
        "s": "0x3f849db4b5569ce1b899756ec83a99da1dfc46efe202de476619272b7ccccd98",
        "r": "0x8462fc60f336e6c4ef3a1927e328666273a8d8c483d0398199b71f109da5dfcf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14",
    "total": "14"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14",
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
            "amount": "43403421955"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYjAxMDE3Ny0xOGY3LTUzY2UtYjdhNS1iYzI3NDRkYjQzZWQifQ==",
    "nonce": 6460,
    "balances": {
      "current": "12974272268392208",
      "previous": "12974272268392223"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x159f6f61cbac6be335686d5444e3a58c520bd1ae",
    "nonce": 21,
    "balances": {
      "current": "14",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:17.817Z",
  "updated": "2020-05-22T08:49:17.888Z",
  "id": "5ec7920db0c6090011d5b132"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`