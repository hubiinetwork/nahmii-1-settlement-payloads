# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5f92890A6df5263AeEd00E5d00b47ce67710a14a`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000188ece99441e05855000000000000000000000000000000000000000000000000565971a7c15402b30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000565971a7c15402b300000000000000000000000000000000000000000000000188ece99441e0585513016f066568f14899d9f22934c75ca1f2254715f94b98a33e643b62d44260a9be38f8b43f1ace73656cadd7bd43d6345d4d2bea5ec8dab8aabd281cf2a6744c4027772b62d66d4d9606975530bf15b14ad7a25b7dead346cdc9244ab53dc831000000000000000000000000000000000000000000000000000000000000001b7fce72d80dcaaa6728979ab495d51ddf9a102a526ac10eb6ff5e39d20506cec86b05c7c392a0e42a078bce82d229161bb6416bfcf70391fe9922417e198d84734f8e22bd9dd402b7faf781b981f04afc3eb0bddf366e8fb6c393716f2cd31121000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7f4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000001085ca6c0eaf52226e8b00000000000000000000000000000000000000000000108620db9b5573a7ef3200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000161afe60317df40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e8283f704eaa8397490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d7a59354f54686b596930324e6a566c4c54566d5a5459744f4467334d5330795a6a42684f5749795a6d5a6d596a4d6966513d3d00000000000000000000000000000000000000000000000000000000000000050000000000000000000000005f92890a6df5263aeed00e5d00b47ce67710a14a00000000000000000000000000000000000000000000000188ece99441e05855000000000000000000000000000000000000000000000001329377ec808c55a200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x13016f066568f14899d9f22934c75ca1f2254715f94b98a33e643b62d44260a9",
      "signature": {
        "s": "0x4027772b62d66d4d9606975530bf15b14ad7a25b7dead346cdc9244ab53dc831",
        "r": "0xbe38f8b43f1ace73656cadd7bd43d6345d4d2bea5ec8dab8aabd281cf2a6744c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7fce72d80dcaaa6728979ab495d51ddf9a102a526ac10eb6ff5e39d20506cec8",
      "signature": {
        "s": "0x4f8e22bd9dd402b7faf781b981f04afc3eb0bddf366e8fb6c393716f2cd31121",
        "r": "0x6b05c7c392a0e42a078bce82d229161bb6416bfcf70391fe9922417e198d8473",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6222129325506036403",
    "total": "28313261780341119061"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6222129325506036403",
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
            "amount": "27894377199617062442825"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6222129325506036"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MzY5OThkYi02NjVlLTVmZTYtODg3MS0yZjBhOWIyZmZmYjMifQ==",
    "nonce": 112628,
    "balances": {
      "current": "78025866737157000031883",
      "previous": "78032095088611831574322"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5f92890a6df5263aeed00e5d00b47ce67710a14a",
    "nonce": 5,
    "balances": {
      "current": "28313261780341119061",
      "previous": "22091132454835082658"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:52.603Z",
  "updated": "2022-05-04T09:04:52.684Z",
  "id": "627241b4bbd75600116d082e"
}
```
* *stageAmount*: `28313261780341119061`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000565971a7c15402b30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000565971a7c15402b300000000000000000000000000000000000000000000000188ece99441e0585513016f066568f14899d9f22934c75ca1f2254715f94b98a33e643b62d44260a9be38f8b43f1ace73656cadd7bd43d6345d4d2bea5ec8dab8aabd281cf2a6744c4027772b62d66d4d9606975530bf15b14ad7a25b7dead346cdc9244ab53dc831000000000000000000000000000000000000000000000000000000000000001b7fce72d80dcaaa6728979ab495d51ddf9a102a526ac10eb6ff5e39d20506cec86b05c7c392a0e42a078bce82d229161bb6416bfcf70391fe9922417e198d84734f8e22bd9dd402b7faf781b981f04afc3eb0bddf366e8fb6c393716f2cd31121000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7f4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000001085ca6c0eaf52226e8b00000000000000000000000000000000000000000000108620db9b5573a7ef3200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000161afe60317df40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e8283f704eaa8397490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d7a59354f54686b596930324e6a566c4c54566d5a5459744f4467334d5330795a6a42684f5749795a6d5a6d596a4d6966513d3d00000000000000000000000000000000000000000000000000000000000000050000000000000000000000005f92890a6df5263aeed00e5d00b47ce67710a14a00000000000000000000000000000000000000000000000188ece99441e05855000000000000000000000000000000000000000000000001329377ec808c55a200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x13016f066568f14899d9f22934c75ca1f2254715f94b98a33e643b62d44260a9",
      "signature": {
        "s": "0x4027772b62d66d4d9606975530bf15b14ad7a25b7dead346cdc9244ab53dc831",
        "r": "0xbe38f8b43f1ace73656cadd7bd43d6345d4d2bea5ec8dab8aabd281cf2a6744c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7fce72d80dcaaa6728979ab495d51ddf9a102a526ac10eb6ff5e39d20506cec8",
      "signature": {
        "s": "0x4f8e22bd9dd402b7faf781b981f04afc3eb0bddf366e8fb6c393716f2cd31121",
        "r": "0x6b05c7c392a0e42a078bce82d229161bb6416bfcf70391fe9922417e198d8473",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6222129325506036403",
    "total": "28313261780341119061"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6222129325506036403",
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
            "amount": "27894377199617062442825"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6222129325506036"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MzY5OThkYi02NjVlLTVmZTYtODg3MS0yZjBhOWIyZmZmYjMifQ==",
    "nonce": 112628,
    "balances": {
      "current": "78025866737157000031883",
      "previous": "78032095088611831574322"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5f92890a6df5263aeed00e5d00b47ce67710a14a",
    "nonce": 5,
    "balances": {
      "current": "28313261780341119061",
      "previous": "22091132454835082658"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:52.603Z",
  "updated": "2022-05-04T09:04:52.684Z",
  "id": "627241b4bbd75600116d082e"
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
0x0f200f9b00000000000000000000000000000000000000000000000188ece99441e058550000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `28313261780341119061`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`