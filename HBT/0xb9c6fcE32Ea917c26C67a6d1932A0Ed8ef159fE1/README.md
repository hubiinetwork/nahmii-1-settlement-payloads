# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb9c6fcE32Ea917c26C67a6d1932A0Ed8ef159fE1`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000033bcbcab9000000000000000000000000000000000000000000000000000000033bcbcab9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000033bcbcab9000000000000000000000000000000000000000000000000000000033bcbcab9dc98dd4ca29526730073ea80b51a355e72ae876dbdf75a62bcf4cc2888ae94b2d5734384407aaa1f845245d64a69d854c32b269ec819bd952aec94a735108d0249c82e4c96566c9c1909f79270c58b974e19756b9e73eeb0f84ceb39a912e6b7000000000000000000000000000000000000000000000000000000000000001b12ad9d2ec18764750c7301907d4aa869fe15c5bf06b4e85b9ca2ce2c3b3972ade930da41e9c702bcbb8168c1eafd574d1803fba9c4cad3d3d96addf26aba4e9159e1f266c2ff8781139f782f57dcffbbdf3e923e9227a46cf25e9e2e784a9a80000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000166800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1bcaf2fdbb8a000000000000000000000000000000000000000000000000002e1bce2f9d70b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000d3ea71000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000924d18e6c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d325a694d6a4a6859693035596d45784c5455355a475574596a4a6d5a6930315a5455304e6a4d344d446b31596a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b9c6fce32ea917c26c67a6d1932a0ed8ef159fe1000000000000000000000000000000000000000000000000000000033bcbcab9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdc98dd4ca29526730073ea80b51a355e72ae876dbdf75a62bcf4cc2888ae94b2",
      "signature": {
        "s": "0x49c82e4c96566c9c1909f79270c58b974e19756b9e73eeb0f84ceb39a912e6b7",
        "r": "0xd5734384407aaa1f845245d64a69d854c32b269ec819bd952aec94a735108d02",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x12ad9d2ec18764750c7301907d4aa869fe15c5bf06b4e85b9ca2ce2c3b3972ad",
      "signature": {
        "s": "0x59e1f266c2ff8781139f782f57dcffbbdf3e923e9227a46cf25e9e2e784a9a80",
        "r": "0xe930da41e9c702bcbb8168c1eafd574d1803fba9c4cad3d3d96addf26aba4e91",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "13888113337",
    "total": "13888113337"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13888113337",
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
            "amount": "39272418924"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13888113"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0M2ZiMjJhYi05YmExLTU5ZGUtYjJmZi01ZTU0NjM4MDk1YjkifQ==",
    "nonce": 5736,
    "balances": {
      "current": "12978407402748810",
      "previous": "12978421304750260"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb9c6fce32ea917c26c67a6d1932a0ed8ef159fe1",
    "nonce": 22,
    "balances": {
      "current": "13888113337",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:25.985Z",
  "updated": "2020-05-22T08:43:26.056Z",
  "id": "5ec790adb0c6090011d5b03d"
}
```
* *stageAmount*: `13888113337`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000033bcbcab9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000033bcbcab9000000000000000000000000000000000000000000000000000000033bcbcab9dc98dd4ca29526730073ea80b51a355e72ae876dbdf75a62bcf4cc2888ae94b2d5734384407aaa1f845245d64a69d854c32b269ec819bd952aec94a735108d0249c82e4c96566c9c1909f79270c58b974e19756b9e73eeb0f84ceb39a912e6b7000000000000000000000000000000000000000000000000000000000000001b12ad9d2ec18764750c7301907d4aa869fe15c5bf06b4e85b9ca2ce2c3b3972ade930da41e9c702bcbb8168c1eafd574d1803fba9c4cad3d3d96addf26aba4e9159e1f266c2ff8781139f782f57dcffbbdf3e923e9227a46cf25e9e2e784a9a80000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000166800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1bcaf2fdbb8a000000000000000000000000000000000000000000000000002e1bce2f9d70b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000d3ea71000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000924d18e6c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d325a694d6a4a6859693035596d45784c5455355a475574596a4a6d5a6930315a5455304e6a4d344d446b31596a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b9c6fce32ea917c26c67a6d1932a0ed8ef159fe1000000000000000000000000000000000000000000000000000000033bcbcab9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdc98dd4ca29526730073ea80b51a355e72ae876dbdf75a62bcf4cc2888ae94b2",
      "signature": {
        "s": "0x49c82e4c96566c9c1909f79270c58b974e19756b9e73eeb0f84ceb39a912e6b7",
        "r": "0xd5734384407aaa1f845245d64a69d854c32b269ec819bd952aec94a735108d02",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x12ad9d2ec18764750c7301907d4aa869fe15c5bf06b4e85b9ca2ce2c3b3972ad",
      "signature": {
        "s": "0x59e1f266c2ff8781139f782f57dcffbbdf3e923e9227a46cf25e9e2e784a9a80",
        "r": "0xe930da41e9c702bcbb8168c1eafd574d1803fba9c4cad3d3d96addf26aba4e91",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "13888113337",
    "total": "13888113337"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13888113337",
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
            "amount": "39272418924"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13888113"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0M2ZiMjJhYi05YmExLTU5ZGUtYjJmZi01ZTU0NjM4MDk1YjkifQ==",
    "nonce": 5736,
    "balances": {
      "current": "12978407402748810",
      "previous": "12978421304750260"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb9c6fce32ea917c26c67a6d1932a0ed8ef159fe1",
    "nonce": 22,
    "balances": {
      "current": "13888113337",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:25.985Z",
  "updated": "2020-05-22T08:43:26.056Z",
  "id": "5ec790adb0c6090011d5b03d"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000033bcbcab9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13888113337`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`