# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE35C0C3794d181dBB44abcf75835CF6B5ED5ECeB`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000763f871300000000000000000000000000000000000000000000000000000000763f8713000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000763f871300000000000000000000000000000000000000000000000000000000763f871359c740f08676768e65c5d99eb2bcedf3998420307192c560e81d0632745fd2f4cef5ab39b0945a4d2742d0865021c6ca4e54dec57019390f87c73e9b9705c3a82f5dc8dfbce81a46de9801c333f559f0f3d1b3e78f7e633dfcd50379f6e3a62c000000000000000000000000000000000000000000000000000000000000001b63364255242d56b85c040100b455b3d6e82990c3cb42837fa830211a8495b6e7ba688b26f72c7f056c5c31e39aed92eb6d50432258496fa1ecedd81f8a04404414438afc157d1d4e58180be0303e3b74dfbc9f193d6161b4c268fc9e46a3ccc2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ccb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e132137a7f275000000000000000000000000000000000000000000000000002e1321ae05bf0a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e4582000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b5bfd9e6a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931597a41785a4759794e6930335a6a67334c54566d4e4445744f57557a4f4330345a6d4a694e44426a4d5455304d544d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e35c0c3794d181dbb44abcf75835cf6b5ed5eceb00000000000000000000000000000000000000000000000000000000763f8713000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x59c740f08676768e65c5d99eb2bcedf3998420307192c560e81d0632745fd2f4",
      "signature": {
        "s": "0x2f5dc8dfbce81a46de9801c333f559f0f3d1b3e78f7e633dfcd50379f6e3a62c",
        "r": "0xcef5ab39b0945a4d2742d0865021c6ca4e54dec57019390f87c73e9b9705c3a8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x63364255242d56b85c040100b455b3d6e82990c3cb42837fa830211a8495b6e7",
      "signature": {
        "s": "0x14438afc157d1d4e58180be0303e3b74dfbc9f193d6161b4c268fc9e46a3ccc2",
        "r": "0xba688b26f72c7f056c5c31e39aed92eb6d50432258496fa1ecedd81f8a044044",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1983874835",
    "total": "1983874835"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1983874835",
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
            "amount": "48787988074"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1983874"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1YzAxZGYyNi03Zjg3LTVmNDEtOWUzOC04ZmJiNDBjMTU0MTMifQ==",
    "nonce": 7371,
    "balances": {
      "current": "12968882317292149",
      "previous": "12968884303150858"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe35c0c3794d181dbb44abcf75835cf6b5ed5eceb",
    "nonce": 22,
    "balances": {
      "current": "1983874835",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:15.445Z",
  "updated": "2020-05-22T08:56:15.519Z",
  "id": "5ec793afe5756b00111b88ca"
}
```
* *stageAmount*: `1983874835`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000763f8713000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000763f871300000000000000000000000000000000000000000000000000000000763f871359c740f08676768e65c5d99eb2bcedf3998420307192c560e81d0632745fd2f4cef5ab39b0945a4d2742d0865021c6ca4e54dec57019390f87c73e9b9705c3a82f5dc8dfbce81a46de9801c333f559f0f3d1b3e78f7e633dfcd50379f6e3a62c000000000000000000000000000000000000000000000000000000000000001b63364255242d56b85c040100b455b3d6e82990c3cb42837fa830211a8495b6e7ba688b26f72c7f056c5c31e39aed92eb6d50432258496fa1ecedd81f8a04404414438afc157d1d4e58180be0303e3b74dfbc9f193d6161b4c268fc9e46a3ccc2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ccb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e132137a7f275000000000000000000000000000000000000000000000000002e1321ae05bf0a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e4582000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b5bfd9e6a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931597a41785a4759794e6930335a6a67334c54566d4e4445744f57557a4f4330345a6d4a694e44426a4d5455304d544d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e35c0c3794d181dbb44abcf75835cf6b5ed5eceb00000000000000000000000000000000000000000000000000000000763f8713000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x59c740f08676768e65c5d99eb2bcedf3998420307192c560e81d0632745fd2f4",
      "signature": {
        "s": "0x2f5dc8dfbce81a46de9801c333f559f0f3d1b3e78f7e633dfcd50379f6e3a62c",
        "r": "0xcef5ab39b0945a4d2742d0865021c6ca4e54dec57019390f87c73e9b9705c3a8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x63364255242d56b85c040100b455b3d6e82990c3cb42837fa830211a8495b6e7",
      "signature": {
        "s": "0x14438afc157d1d4e58180be0303e3b74dfbc9f193d6161b4c268fc9e46a3ccc2",
        "r": "0xba688b26f72c7f056c5c31e39aed92eb6d50432258496fa1ecedd81f8a044044",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1983874835",
    "total": "1983874835"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1983874835",
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
            "amount": "48787988074"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1983874"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1YzAxZGYyNi03Zjg3LTVmNDEtOWUzOC04ZmJiNDBjMTU0MTMifQ==",
    "nonce": 7371,
    "balances": {
      "current": "12968882317292149",
      "previous": "12968884303150858"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe35c0c3794d181dbb44abcf75835cf6b5ed5eceb",
    "nonce": 22,
    "balances": {
      "current": "1983874835",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:15.445Z",
  "updated": "2020-05-22T08:56:15.519Z",
  "id": "5ec793afe5756b00111b88ca"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000763f8713000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1983874835`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`