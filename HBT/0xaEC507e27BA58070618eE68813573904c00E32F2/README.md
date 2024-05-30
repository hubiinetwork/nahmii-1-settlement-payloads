# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xaEC507e27BA58070618eE68813573904c00E32F2`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000c9d1e70000000000000000000000000000000000000000000000000000000000c9d1e7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000c9d1e70000000000000000000000000000000000000000000000000000000000c9d1e7911596a5901a1cb0dd0c3fc02c6faa4c0cce8153217e5eadac1634d1bf57b21acf68af48331e9e1de9241ddd14a04f10280ae92c9bc61aff04c1b567541a0a0b611a9eebaefacc9dcc1667287edb6ec5fb07d4f23826f1ed236a598147e01d7a000000000000000000000000000000000000000000000000000000000000001baed081137c4e5a2520bf306ea3c91226e5b06bfd8553958ea9ea6e9c6e4f135a80abaaedd81ceea0cdb4e6b3e4983b3ffdd33921ea7db2620c8cf1ef2c0095b93b6a135ecda5996deb7c27f54d3a3cc26049e8b3d9ec7c57e06678419f4fdc88000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018aa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a71d1326ea8000000000000000000000000000000000000000000000000002e1a71d1fc743900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000033aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000097d158708000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977596d51354e6d4a694e793033596a4e684c545579596a4d74595751784d4330354e6a6c6b5a446b354e54686c4e6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000aec507e27ba58070618ee68813573904c00e32f20000000000000000000000000000000000000000000000000000000000c9d1e7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x911596a5901a1cb0dd0c3fc02c6faa4c0cce8153217e5eadac1634d1bf57b21a",
      "signature": {
        "s": "0x611a9eebaefacc9dcc1667287edb6ec5fb07d4f23826f1ed236a598147e01d7a",
        "r": "0xcf68af48331e9e1de9241ddd14a04f10280ae92c9bc61aff04c1b567541a0a0b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaed081137c4e5a2520bf306ea3c91226e5b06bfd8553958ea9ea6e9c6e4f135a",
      "signature": {
        "s": "0x3b6a135ecda5996deb7c27f54d3a3cc26049e8b3d9ec7c57e06678419f4fdc88",
        "r": "0x80abaaedd81ceea0cdb4e6b3e4983b3ffdd33921ea7db2620c8cf1ef2c0095b9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "13226471",
    "total": "13226471"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13226471",
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
            "amount": "40753268488"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13226"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYmQ5NmJiNy03YjNhLTUyYjMtYWQxMC05NjlkZDk5NThlNmMifQ==",
    "nonce": 6314,
    "balances": {
      "current": "12976925072060072",
      "previous": "12976925085299769"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaec507e27ba58070618ee68813573904c00e32f2",
    "nonce": 22,
    "balances": {
      "current": "13226471",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:07.779Z",
  "updated": "2020-05-22T08:48:07.849Z",
  "id": "5ec791c7b0c6090011d5b0fe"
}
```
* *stageAmount*: `13226471`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000c9d1e7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000c9d1e70000000000000000000000000000000000000000000000000000000000c9d1e7911596a5901a1cb0dd0c3fc02c6faa4c0cce8153217e5eadac1634d1bf57b21acf68af48331e9e1de9241ddd14a04f10280ae92c9bc61aff04c1b567541a0a0b611a9eebaefacc9dcc1667287edb6ec5fb07d4f23826f1ed236a598147e01d7a000000000000000000000000000000000000000000000000000000000000001baed081137c4e5a2520bf306ea3c91226e5b06bfd8553958ea9ea6e9c6e4f135a80abaaedd81ceea0cdb4e6b3e4983b3ffdd33921ea7db2620c8cf1ef2c0095b93b6a135ecda5996deb7c27f54d3a3cc26049e8b3d9ec7c57e06678419f4fdc88000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018aa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a71d1326ea8000000000000000000000000000000000000000000000000002e1a71d1fc743900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000033aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000097d158708000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977596d51354e6d4a694e793033596a4e684c545579596a4d74595751784d4330354e6a6c6b5a446b354e54686c4e6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000aec507e27ba58070618ee68813573904c00e32f20000000000000000000000000000000000000000000000000000000000c9d1e7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x911596a5901a1cb0dd0c3fc02c6faa4c0cce8153217e5eadac1634d1bf57b21a",
      "signature": {
        "s": "0x611a9eebaefacc9dcc1667287edb6ec5fb07d4f23826f1ed236a598147e01d7a",
        "r": "0xcf68af48331e9e1de9241ddd14a04f10280ae92c9bc61aff04c1b567541a0a0b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaed081137c4e5a2520bf306ea3c91226e5b06bfd8553958ea9ea6e9c6e4f135a",
      "signature": {
        "s": "0x3b6a135ecda5996deb7c27f54d3a3cc26049e8b3d9ec7c57e06678419f4fdc88",
        "r": "0x80abaaedd81ceea0cdb4e6b3e4983b3ffdd33921ea7db2620c8cf1ef2c0095b9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "13226471",
    "total": "13226471"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13226471",
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
            "amount": "40753268488"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13226"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYmQ5NmJiNy03YjNhLTUyYjMtYWQxMC05NjlkZDk5NThlNmMifQ==",
    "nonce": 6314,
    "balances": {
      "current": "12976925072060072",
      "previous": "12976925085299769"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaec507e27ba58070618ee68813573904c00e32f2",
    "nonce": 22,
    "balances": {
      "current": "13226471",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:07.779Z",
  "updated": "2020-05-22T08:48:07.849Z",
  "id": "5ec791c7b0c6090011d5b0fe"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000c9d1e7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13226471`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`