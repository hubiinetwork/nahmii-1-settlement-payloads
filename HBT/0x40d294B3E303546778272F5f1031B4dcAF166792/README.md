# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x40d294B3E303546778272F5f1031B4dcAF166792`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000005caed394000000000000000000000000000000000000000000000000000000005caed394000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000005caed394000000000000000000000000000000000000000000000000000000005caed3944aba1c81851ee0069979735502270ecd3e1d6609cd696889bb58e1c16b29d39d40e4ae5ad80a1f84eb471122b83eecf52ccef5aa5e687cc9964df839d75f58a816050809b358a915b2c00e7da6fb0a97e9a09101bf6da4ea1eb4fe3f0afd83c8000000000000000000000000000000000000000000000000000000000000001bc97f64b60299e183d67458effeb05e16596b1afba1040f177be1bf62973e8e682cdfd3c32369146ef5f7c30683e6970b30a5f12f6d9bda1e9960fe8f394cfd785b3721532da01b4535585bed8ad6ea5baef83d24f6916590582bb1790fffa31d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e9300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b02cad3af12000000000000000000000000000000000000000000000000002e0b03279a3cb700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000017ba11000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f89354c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694933596a59304d6d566b595331684d7a4e6d4c5455305a446b744f54457a5a43316c5a5755334d6a6b354f5463785a47456966513d3d000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000040d294b3e303546778272f5f1031b4dcaf166792000000000000000000000000000000000000000000000000000000005caed394000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4aba1c81851ee0069979735502270ecd3e1d6609cd696889bb58e1c16b29d39d",
      "signature": {
        "s": "0x16050809b358a915b2c00e7da6fb0a97e9a09101bf6da4ea1eb4fe3f0afd83c8",
        "r": "0x40e4ae5ad80a1f84eb471122b83eecf52ccef5aa5e687cc9964df839d75f58a8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc97f64b60299e183d67458effeb05e16596b1afba1040f177be1bf62973e8e68",
      "signature": {
        "s": "0x5b3721532da01b4535585bed8ad6ea5baef83d24f6916590582bb1790fffa31d",
        "r": "0x2cdfd3c32369146ef5f7c30683e6970b30a5f12f6d9bda1e9960fe8f394cfd78",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1554961300",
    "total": "1554961300"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1554961300",
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
            "amount": "57705837900"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1554961"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3YjY0MmVkYS1hMzNmLTU0ZDktOTEzZC1lZWU3Mjk5OTcxZGEifQ==",
    "nonce": 7827,
    "balances": {
      "current": "12959955549400850",
      "previous": "12959957105917111"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x40d294b3e303546778272f5f1031b4dcaf166792",
    "nonce": 12,
    "balances": {
      "current": "1554961300",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:50.710Z",
  "updated": "2020-05-22T08:59:51.789Z",
  "id": "5ec79486005df800101bcc7d"
}
```
* *stageAmount*: `1554961300`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000005caed394000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000005caed394000000000000000000000000000000000000000000000000000000005caed3944aba1c81851ee0069979735502270ecd3e1d6609cd696889bb58e1c16b29d39d40e4ae5ad80a1f84eb471122b83eecf52ccef5aa5e687cc9964df839d75f58a816050809b358a915b2c00e7da6fb0a97e9a09101bf6da4ea1eb4fe3f0afd83c8000000000000000000000000000000000000000000000000000000000000001bc97f64b60299e183d67458effeb05e16596b1afba1040f177be1bf62973e8e682cdfd3c32369146ef5f7c30683e6970b30a5f12f6d9bda1e9960fe8f394cfd785b3721532da01b4535585bed8ad6ea5baef83d24f6916590582bb1790fffa31d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e9300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b02cad3af12000000000000000000000000000000000000000000000000002e0b03279a3cb700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000017ba11000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f89354c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694933596a59304d6d566b595331684d7a4e6d4c5455305a446b744f54457a5a43316c5a5755334d6a6b354f5463785a47456966513d3d000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000040d294b3e303546778272f5f1031b4dcaf166792000000000000000000000000000000000000000000000000000000005caed394000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4aba1c81851ee0069979735502270ecd3e1d6609cd696889bb58e1c16b29d39d",
      "signature": {
        "s": "0x16050809b358a915b2c00e7da6fb0a97e9a09101bf6da4ea1eb4fe3f0afd83c8",
        "r": "0x40e4ae5ad80a1f84eb471122b83eecf52ccef5aa5e687cc9964df839d75f58a8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc97f64b60299e183d67458effeb05e16596b1afba1040f177be1bf62973e8e68",
      "signature": {
        "s": "0x5b3721532da01b4535585bed8ad6ea5baef83d24f6916590582bb1790fffa31d",
        "r": "0x2cdfd3c32369146ef5f7c30683e6970b30a5f12f6d9bda1e9960fe8f394cfd78",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1554961300",
    "total": "1554961300"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1554961300",
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
            "amount": "57705837900"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1554961"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3YjY0MmVkYS1hMzNmLTU0ZDktOTEzZC1lZWU3Mjk5OTcxZGEifQ==",
    "nonce": 7827,
    "balances": {
      "current": "12959955549400850",
      "previous": "12959957105917111"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x40d294b3e303546778272f5f1031b4dcaf166792",
    "nonce": 12,
    "balances": {
      "current": "1554961300",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:50.710Z",
  "updated": "2020-05-22T08:59:51.789Z",
  "id": "5ec79486005df800101bcc7d"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000005caed394000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1554961300`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`