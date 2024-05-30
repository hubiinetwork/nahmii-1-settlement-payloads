# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6Df93ee3C3C9eaA723410489d8FF8E9CBe29a571`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000004f486e5ec088665ae000000000000000000000000000000000000000000000000000000023a545c950000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000023a545c9500000000000000000000000000000000000000000000000000000033fe4f379c996fa8aa7d676f29cda4316c5ba8ab4d639dea843c6cc841a3139b8f2220e4467d17398eab5cd74a6117e0494105a91e1571449fae7b7690bd279f83d72fe59f0784009cd5fa695d68f6af3b21b02ae98b975a3eb1362ba219d40e46eaf609c6000000000000000000000000000000000000000000000000000000000000001b6dcc3cf9e36b39f93dec066d2fe0b5ffeabb7eca8a4859a59b7adb8764c914b380242cefa36602fc2800b76f960a62c2d959d65c355f2bac294b868f9f2a947845e030987c353e37bdc21d90977a5f49e390e0457eb7dd5c30e232db99497c30000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b38a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bcfa9538ae250dc1610000000000000000000000000000000000000000000003bcfa9538ae48bc273c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000092011d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd161f7ec2b917bee20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d54566a4e7a686b4f533033596d45334c5456694d7a59744f444d7a5a6930774e545a684e4749774d54566a5a57456966513d3d000000000000000000000000000000000000000000000000000000000000001f0000000000000000000000006df93ee3c3c9eaa723410489d8ff8e9cbe29a571000000000000000000000000000000000000000000000004f486e5ec088665ae000000000000000000000000000000000000000000000004f486e5e9ce32091900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x996fa8aa7d676f29cda4316c5ba8ab4d639dea843c6cc841a3139b8f2220e446",
      "signature": {
        "s": "0x0784009cd5fa695d68f6af3b21b02ae98b975a3eb1362ba219d40e46eaf609c6",
        "r": "0x7d17398eab5cd74a6117e0494105a91e1571449fae7b7690bd279f83d72fe59f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6dcc3cf9e36b39f93dec066d2fe0b5ffeabb7eca8a4859a59b7adb8764c914b3",
      "signature": {
        "s": "0x45e030987c353e37bdc21d90977a5f49e390e0457eb7dd5c30e232db99497c30",
        "r": "0x80242cefa36602fc2800b76f960a62c2d959d65c355f2bac294b868f9f2a9478",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9568541845",
    "total": "223309936540"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9568541845",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27690156986805943516898"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "9568541"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMTVjNzhkOS03YmE3LTViMzYtODMzZi0wNTZhNGIwMTVjZWEifQ==",
    "nonce": 111498,
    "balances": {
      "current": "282450299761087045441040",
      "previous": "282450299761096623551426"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6df93ee3c3c9eaa723410489d8ff8e9cbe29a571",
    "nonce": 31,
    "balances": {
      "current": "91406999688889918894",
      "previous": "91406999679321377049"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:37.426Z",
  "updated": "2022-05-04T08:58:37.493Z",
  "id": "6272403d7832e20011830d16"
}
```
* *stageAmount*: `91406999688889918894`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000023a545c950000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000023a545c9500000000000000000000000000000000000000000000000000000033fe4f379c996fa8aa7d676f29cda4316c5ba8ab4d639dea843c6cc841a3139b8f2220e4467d17398eab5cd74a6117e0494105a91e1571449fae7b7690bd279f83d72fe59f0784009cd5fa695d68f6af3b21b02ae98b975a3eb1362ba219d40e46eaf609c6000000000000000000000000000000000000000000000000000000000000001b6dcc3cf9e36b39f93dec066d2fe0b5ffeabb7eca8a4859a59b7adb8764c914b380242cefa36602fc2800b76f960a62c2d959d65c355f2bac294b868f9f2a947845e030987c353e37bdc21d90977a5f49e390e0457eb7dd5c30e232db99497c30000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b38a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bcfa9538ae250dc1610000000000000000000000000000000000000000000003bcfa9538ae48bc273c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000092011d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd161f7ec2b917bee20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d54566a4e7a686b4f533033596d45334c5456694d7a59744f444d7a5a6930774e545a684e4749774d54566a5a57456966513d3d000000000000000000000000000000000000000000000000000000000000001f0000000000000000000000006df93ee3c3c9eaa723410489d8ff8e9cbe29a571000000000000000000000000000000000000000000000004f486e5ec088665ae000000000000000000000000000000000000000000000004f486e5e9ce32091900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x996fa8aa7d676f29cda4316c5ba8ab4d639dea843c6cc841a3139b8f2220e446",
      "signature": {
        "s": "0x0784009cd5fa695d68f6af3b21b02ae98b975a3eb1362ba219d40e46eaf609c6",
        "r": "0x7d17398eab5cd74a6117e0494105a91e1571449fae7b7690bd279f83d72fe59f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6dcc3cf9e36b39f93dec066d2fe0b5ffeabb7eca8a4859a59b7adb8764c914b3",
      "signature": {
        "s": "0x45e030987c353e37bdc21d90977a5f49e390e0457eb7dd5c30e232db99497c30",
        "r": "0x80242cefa36602fc2800b76f960a62c2d959d65c355f2bac294b868f9f2a9478",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9568541845",
    "total": "223309936540"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9568541845",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27690156986805943516898"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "9568541"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMTVjNzhkOS03YmE3LTViMzYtODMzZi0wNTZhNGIwMTVjZWEifQ==",
    "nonce": 111498,
    "balances": {
      "current": "282450299761087045441040",
      "previous": "282450299761096623551426"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6df93ee3c3c9eaa723410489d8ff8e9cbe29a571",
    "nonce": 31,
    "balances": {
      "current": "91406999688889918894",
      "previous": "91406999679321377049"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:37.426Z",
  "updated": "2022-05-04T08:58:37.493Z",
  "id": "6272403d7832e20011830d16"
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
0x0f200f9b000000000000000000000000000000000000000000000004f486e5ec088665ae0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `91406999688889918894`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`