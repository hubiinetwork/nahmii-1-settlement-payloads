# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3ab7f3cBe508613fFB6dF5d66EFaAC1B3bd4B381`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000002e43ac5d5b0000000000000000000000000000000000000000000000000000002e43ac5d5b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002e43ac5d5b0000000000000000000000000000000000000000000000000000002e43ac5d5bf7c34900e4a8446a2468f38ca840a5670b7478d755f75b32abe41defe16bad74f7c0d70c0341e7c243fe2897d478937645a9592b8063e06c9c802b0fa3a51f3459ea96b8da3fbcd9b7372c6f444b9d83c312e5af2bded5d96d86ecaebbb5c9e4000000000000000000000000000000000000000000000000000000000000001c255b4677ef3dc89c4a53c09225b49b180c2e7fefac75861a05206264523337f0cb5f641184f5191a4270cb00e8fc4c89d06ae0e9537b1def366a32850290db5a25abf92e1082bd080591d3de38a3b874085f0fb164a4bfff91e93189d4117ad3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d0800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12a032c4a1af000000000000000000000000000000000000000000000000002e12ce8248fa0300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000bd7faf9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b7cfc911a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595749345a54497a4f53316d4d574a6a4c5455354e575574596d4d304d79307a4d5759794d5749355a4449315932516966513d3d00000000000000000000000000000000000000000000000000000000000000170000000000000000000000003ab7f3cbe508613ffb6df5d66efaac1b3bd4b3810000000000000000000000000000000000000000000000000000002e43ac5d5b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf7c34900e4a8446a2468f38ca840a5670b7478d755f75b32abe41defe16bad74",
      "signature": {
        "s": "0x59ea96b8da3fbcd9b7372c6f444b9d83c312e5af2bded5d96d86ecaebbb5c9e4",
        "r": "0xf7c0d70c0341e7c243fe2897d478937645a9592b8063e06c9c802b0fa3a51f34",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x255b4677ef3dc89c4a53c09225b49b180c2e7fefac75861a05206264523337f0",
      "signature": {
        "s": "0x25abf92e1082bd080591d3de38a3b874085f0fb164a4bfff91e93189d4117ad3",
        "r": "0xcb5f641184f5191a4270cb00e8fc4c89d06ae0e9537b1def366a32850290db5a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "198703865179",
    "total": "198703865179"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "198703865179",
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
            "amount": "49341567258"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "198703865"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YWI4ZTIzOS1mMWJjLTU5NWUtYmM0My0zMWYyMWI5ZDI1Y2QifQ==",
    "nonce": 7432,
    "balances": {
      "current": "12968328184504751",
      "previous": "12968527087073795"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ab7f3cbe508613ffb6df5d66efaac1b3bd4b381",
    "nonce": 23,
    "balances": {
      "current": "198703865179",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:46.872Z",
  "updated": "2020-05-22T08:56:46.945Z",
  "id": "5ec793ceb0c6090011d5b280"
}
```
* *stageAmount*: `198703865179`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000002e43ac5d5b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002e43ac5d5b0000000000000000000000000000000000000000000000000000002e43ac5d5bf7c34900e4a8446a2468f38ca840a5670b7478d755f75b32abe41defe16bad74f7c0d70c0341e7c243fe2897d478937645a9592b8063e06c9c802b0fa3a51f3459ea96b8da3fbcd9b7372c6f444b9d83c312e5af2bded5d96d86ecaebbb5c9e4000000000000000000000000000000000000000000000000000000000000001c255b4677ef3dc89c4a53c09225b49b180c2e7fefac75861a05206264523337f0cb5f641184f5191a4270cb00e8fc4c89d06ae0e9537b1def366a32850290db5a25abf92e1082bd080591d3de38a3b874085f0fb164a4bfff91e93189d4117ad3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d0800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12a032c4a1af000000000000000000000000000000000000000000000000002e12ce8248fa0300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000bd7faf9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b7cfc911a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595749345a54497a4f53316d4d574a6a4c5455354e575574596d4d304d79307a4d5759794d5749355a4449315932516966513d3d00000000000000000000000000000000000000000000000000000000000000170000000000000000000000003ab7f3cbe508613ffb6df5d66efaac1b3bd4b3810000000000000000000000000000000000000000000000000000002e43ac5d5b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf7c34900e4a8446a2468f38ca840a5670b7478d755f75b32abe41defe16bad74",
      "signature": {
        "s": "0x59ea96b8da3fbcd9b7372c6f444b9d83c312e5af2bded5d96d86ecaebbb5c9e4",
        "r": "0xf7c0d70c0341e7c243fe2897d478937645a9592b8063e06c9c802b0fa3a51f34",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x255b4677ef3dc89c4a53c09225b49b180c2e7fefac75861a05206264523337f0",
      "signature": {
        "s": "0x25abf92e1082bd080591d3de38a3b874085f0fb164a4bfff91e93189d4117ad3",
        "r": "0xcb5f641184f5191a4270cb00e8fc4c89d06ae0e9537b1def366a32850290db5a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "198703865179",
    "total": "198703865179"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "198703865179",
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
            "amount": "49341567258"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "198703865"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YWI4ZTIzOS1mMWJjLTU5NWUtYmM0My0zMWYyMWI5ZDI1Y2QifQ==",
    "nonce": 7432,
    "balances": {
      "current": "12968328184504751",
      "previous": "12968527087073795"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ab7f3cbe508613ffb6df5d66efaac1b3bd4b381",
    "nonce": 23,
    "balances": {
      "current": "198703865179",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:46.872Z",
  "updated": "2020-05-22T08:56:46.945Z",
  "id": "5ec793ceb0c6090011d5b280"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000002e43ac5d5b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `198703865179`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`