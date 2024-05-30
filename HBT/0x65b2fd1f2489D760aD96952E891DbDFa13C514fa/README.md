# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x65b2fd1f2489D760aD96952E891DbDFa13C514fa`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000004e750000000000000000000000000000000000000000000000000000000000004e7500000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004e750000000000000000000000000000000000000000000000000000000000004e75003f5380e159d8fd55ee4e0d2f28b2847c349c64b8202e793c3cd137b4594fba026807e57a88fe82a44fe6fdb4d17f1472c105be474999481d62807d260f48b567228ab1c20d012feeca19b65638fbb686491b9013319e5cd30d1135dd48b53715000000000000000000000000000000000000000000000000000000000000001ca248bf964e238571c26d57f82cce3f1f522ff90fa1d249a279007a248c5f3b7e3de3ec3cfbbddd574b2c16ee664f3b4d5bcfe3e09ae7bac3fd72d1b4386829271a20be4d5fc3e4c2017b67ba4d5391dd516ee78a657984b9dec4afa975793dcb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b3c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a3b4cfb5a0000000000000000000000000000000000000000000000000002e15a3b51e3eb500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000001415000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab7ad88bb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5463314e5751314d6930785a544d7a4c5456684d574d74595759784e79316a4f5759785a574579597a526c4e6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000065b2fd1f2489d760ad96952e891dbdfa13c514fa00000000000000000000000000000000000000000000000000000000004e7500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f5380e159d8fd55ee4e0d2f28b2847c349c64b8202e793c3cd137b4594fba02",
      "signature": {
        "s": "0x228ab1c20d012feeca19b65638fbb686491b9013319e5cd30d1135dd48b53715",
        "r": "0x6807e57a88fe82a44fe6fdb4d17f1472c105be474999481d62807d260f48b567",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa248bf964e238571c26d57f82cce3f1f522ff90fa1d249a279007a248c5f3b7e",
      "signature": {
        "s": "0x1a20be4d5fc3e4c2017b67ba4d5391dd516ee78a657984b9dec4afa975793dcb",
        "r": "0x3de3ec3cfbbddd574b2c16ee664f3b4d5bcfe3e09ae7bac3fd72d1b438682927",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5141760",
    "total": "5141760"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5141760",
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
            "amount": "46031276219"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5141"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZTc1NWQ1Mi0xZTMzLTVhMWMtYWYxNy1jOWYxZWEyYzRlNmMifQ==",
    "nonce": 6972,
    "balances": {
      "current": "12971641786054048",
      "previous": "12971641791200949"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x65b2fd1f2489d760ad96952e891dbdfa13c514fa",
    "nonce": 22,
    "balances": {
      "current": "5141760",
      "previous": "0"
    }
  },
  "blockNumber": "10114723",
  "created": "2020-05-22T08:53:08.872Z",
  "updated": "2020-05-22T08:53:09.008Z",
  "id": "5ec792f4b0c6090011d5b1e9"
}
```
* *stageAmount*: `5141760`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000004e7500000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004e750000000000000000000000000000000000000000000000000000000000004e75003f5380e159d8fd55ee4e0d2f28b2847c349c64b8202e793c3cd137b4594fba026807e57a88fe82a44fe6fdb4d17f1472c105be474999481d62807d260f48b567228ab1c20d012feeca19b65638fbb686491b9013319e5cd30d1135dd48b53715000000000000000000000000000000000000000000000000000000000000001ca248bf964e238571c26d57f82cce3f1f522ff90fa1d249a279007a248c5f3b7e3de3ec3cfbbddd574b2c16ee664f3b4d5bcfe3e09ae7bac3fd72d1b4386829271a20be4d5fc3e4c2017b67ba4d5391dd516ee78a657984b9dec4afa975793dcb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b3c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a3b4cfb5a0000000000000000000000000000000000000000000000000002e15a3b51e3eb500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000001415000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab7ad88bb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5463314e5751314d6930785a544d7a4c5456684d574d74595759784e79316a4f5759785a574579597a526c4e6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000065b2fd1f2489d760ad96952e891dbdfa13c514fa00000000000000000000000000000000000000000000000000000000004e7500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f5380e159d8fd55ee4e0d2f28b2847c349c64b8202e793c3cd137b4594fba02",
      "signature": {
        "s": "0x228ab1c20d012feeca19b65638fbb686491b9013319e5cd30d1135dd48b53715",
        "r": "0x6807e57a88fe82a44fe6fdb4d17f1472c105be474999481d62807d260f48b567",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa248bf964e238571c26d57f82cce3f1f522ff90fa1d249a279007a248c5f3b7e",
      "signature": {
        "s": "0x1a20be4d5fc3e4c2017b67ba4d5391dd516ee78a657984b9dec4afa975793dcb",
        "r": "0x3de3ec3cfbbddd574b2c16ee664f3b4d5bcfe3e09ae7bac3fd72d1b438682927",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5141760",
    "total": "5141760"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5141760",
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
            "amount": "46031276219"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5141"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZTc1NWQ1Mi0xZTMzLTVhMWMtYWYxNy1jOWYxZWEyYzRlNmMifQ==",
    "nonce": 6972,
    "balances": {
      "current": "12971641786054048",
      "previous": "12971641791200949"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x65b2fd1f2489d760ad96952e891dbdfa13c514fa",
    "nonce": 22,
    "balances": {
      "current": "5141760",
      "previous": "0"
    }
  },
  "blockNumber": "10114723",
  "created": "2020-05-22T08:53:08.872Z",
  "updated": "2020-05-22T08:53:09.008Z",
  "id": "5ec792f4b0c6090011d5b1e9"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000004e7500000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5141760`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`