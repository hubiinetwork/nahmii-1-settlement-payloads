# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6585651CC2844C4005Dd1145401cfc3BBf966961`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000146000000000000000000000000000000000000000000000000000000000000014600000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001460000000000000000000000000000000000000000000000000000000000000146001151334745278811f1ee8811ba3f36b1c0bd74670daad579cbbda399e1397237a4e45270163238f2a3914ff8d2d888b3de82e0b47844611e3227e6bed2d121b36df788a4eb301f8ea1dbab7ef3c587e72d9bccae07074e0c6d37f46db115b6bf000000000000000000000000000000000000000000000000000000000000001b02fe218f0d7e2498e0917ddb14134c5f033735d83e5413052be188d06157b640a1a1107c7ed8c327317b6700f96a53cf331dc6776d4f2e542224b85616d5752c6158da6791364226c8a3c7dc9cd2cce0b7ff0dcb8df209576d58cd5e0da67b38000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b4400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a227d21d53000000000000000000000000000000000000000000000000002e15a227d363a600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000053000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab8130fe5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d545a6b596d4a6a4f5330774f4751344c54566b595759744f4759334d4330784f4463345a474e6b5a6a6c6b4e7a676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006585651cc2844c4005dd1145401cfc3bbf9669610000000000000000000000000000000000000000000000000000000000014600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1151334745278811f1ee8811ba3f36b1c0bd74670daad579cbbda399e1397237",
      "signature": {
        "s": "0x6df788a4eb301f8ea1dbab7ef3c587e72d9bccae07074e0c6d37f46db115b6bf",
        "r": "0xa4e45270163238f2a3914ff8d2d888b3de82e0b47844611e3227e6bed2d121b3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x02fe218f0d7e2498e0917ddb14134c5f033735d83e5413052be188d06157b640",
      "signature": {
        "s": "0x6158da6791364226c8a3c7dc9cd2cce0b7ff0dcb8df209576d58cd5e0da67b38",
        "r": "0xa1a1107c7ed8c327317b6700f96a53cf331dc6776d4f2e542224b85616d5752c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "83456",
    "total": "83456"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "83456",
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
            "amount": "46037929957"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "83"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMTZkYmJjOS0wOGQ4LTVkYWYtOGY3MC0xODc4ZGNkZjlkNzgifQ==",
    "nonce": 6980,
    "balances": {
      "current": "12971635125656915",
      "previous": "12971635125740454"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6585651cc2844c4005dd1145401cfc3bbf966961",
    "nonce": 22,
    "balances": {
      "current": "83456",
      "previous": "0"
    }
  },
  "blockNumber": "10114724",
  "created": "2020-05-22T08:53:10.513Z",
  "updated": "2020-05-22T08:53:10.616Z",
  "id": "5ec792f6b0c6090011d5b1eb"
}
```
* *stageAmount*: `83456`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000014600000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001460000000000000000000000000000000000000000000000000000000000000146001151334745278811f1ee8811ba3f36b1c0bd74670daad579cbbda399e1397237a4e45270163238f2a3914ff8d2d888b3de82e0b47844611e3227e6bed2d121b36df788a4eb301f8ea1dbab7ef3c587e72d9bccae07074e0c6d37f46db115b6bf000000000000000000000000000000000000000000000000000000000000001b02fe218f0d7e2498e0917ddb14134c5f033735d83e5413052be188d06157b640a1a1107c7ed8c327317b6700f96a53cf331dc6776d4f2e542224b85616d5752c6158da6791364226c8a3c7dc9cd2cce0b7ff0dcb8df209576d58cd5e0da67b38000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b4400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a227d21d53000000000000000000000000000000000000000000000000002e15a227d363a600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000053000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab8130fe5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d545a6b596d4a6a4f5330774f4751344c54566b595759744f4759334d4330784f4463345a474e6b5a6a6c6b4e7a676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006585651cc2844c4005dd1145401cfc3bbf9669610000000000000000000000000000000000000000000000000000000000014600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1151334745278811f1ee8811ba3f36b1c0bd74670daad579cbbda399e1397237",
      "signature": {
        "s": "0x6df788a4eb301f8ea1dbab7ef3c587e72d9bccae07074e0c6d37f46db115b6bf",
        "r": "0xa4e45270163238f2a3914ff8d2d888b3de82e0b47844611e3227e6bed2d121b3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x02fe218f0d7e2498e0917ddb14134c5f033735d83e5413052be188d06157b640",
      "signature": {
        "s": "0x6158da6791364226c8a3c7dc9cd2cce0b7ff0dcb8df209576d58cd5e0da67b38",
        "r": "0xa1a1107c7ed8c327317b6700f96a53cf331dc6776d4f2e542224b85616d5752c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "83456",
    "total": "83456"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "83456",
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
            "amount": "46037929957"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "83"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMTZkYmJjOS0wOGQ4LTVkYWYtOGY3MC0xODc4ZGNkZjlkNzgifQ==",
    "nonce": 6980,
    "balances": {
      "current": "12971635125656915",
      "previous": "12971635125740454"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6585651cc2844c4005dd1145401cfc3bbf966961",
    "nonce": 22,
    "balances": {
      "current": "83456",
      "previous": "0"
    }
  },
  "blockNumber": "10114724",
  "created": "2020-05-22T08:53:10.513Z",
  "updated": "2020-05-22T08:53:10.616Z",
  "id": "5ec792f6b0c6090011d5b1eb"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000014600000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `83456`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`