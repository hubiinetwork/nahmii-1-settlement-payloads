# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x588dCe6Cb745BDcda09b4802DD50FbaB93893b32`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de1bc7f2c4bdc68000000000000000000000000000000000000000000000015c54727bf768c80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000015c54727bf768c8000000000000000000000000000000000000000000000000015c54727bf768c8000d2eb7d1d7a36526c4fdb001b0cf84db2fc3813e42080b7f79d997ca31a2855b19f30cbad3acd96d290964d9d68bc1e56ac7a2e776667000e437dc6f7fc17a5c02c98f4ca1e25ce43a178e4d9a7d28ef73ed3e8cb6f6461205ff4a0fab716c89d000000000000000000000000000000000000000000000000000000000000001ce25c87cd502c2cc743d7ffa20f873c9ea22000b4d22f483c0270eeb0d417eb7f152d70235b5e9aac61787c649a67b6a932bb21f4acce4b49b0765e9a939531ec1382424ecd0616eee08898f5aebfeef1f5fe2c8dd92fdc85af3686203634b42b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1c5ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000588dce6cb745bdcda09b4802dd50fbab93893b320000000000000000000000000000000000000000000000000de1bc7f2c4bdc68000000000000000000000000000000000000000000000015d8bba696a2b52c6800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000592c257ffdcd0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000592c257ffdcd0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f474e6d5a544130596930324f446c6d4c5451775a6d51744f574934597930354e5445334d6a63304f4459784d6a556966513d3d000000000000000000000000000000000000000000000000000000000000001d000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001b305c00406dd2396247000000000000000000000000000000000000000000001b1a96b918ae5bace24700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd2eb7d1d7a36526c4fdb001b0cf84db2fc3813e42080b7f79d997ca31a2855b1",
      "signature": {
        "s": "0x2c98f4ca1e25ce43a178e4d9a7d28ef73ed3e8cb6f6461205ff4a0fab716c89d",
        "r": "0x9f30cbad3acd96d290964d9d68bc1e56ac7a2e776667000e437dc6f7fc17a5c0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe25c87cd502c2cc743d7ffa20f873c9ea22000b4d22f483c0270eeb0d417eb7f",
      "signature": {
        "s": "0x1382424ecd0616eee08898f5aebfeef1f5fe2c8dd92fdc85af3686203634b42b",
        "r": "0x152d70235b5e9aac61787c649a67b6a932bb21f4acce4b49b0765e9a939531ec",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "401597000000000000000",
    "total": "401597000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "401597000000000000000",
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
            "amount": "401597000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "401597000000000000"
      }
    },
    "wallet": "0x588dce6cb745bdcda09b4802dd50fbab93893b32",
    "data": "eyJyZWYiOiIxOGNmZTA0Yi02ODlmLTQwZmQtOWI4Yy05NTE3Mjc0ODYxMjUifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000287846642998376",
      "previous": "402998884846642998376"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 29,
    "balances": {
      "current": "128395968122510391206471",
      "previous": "127994371122510391206471"
    }
  },
  "blockNumber": "14796269",
  "created": "2022-05-18T02:39:59.395Z",
  "updated": "2022-05-18T02:39:59.480Z",
  "id": "62845c7f7832e20011830ef8"
}
```
* *stageAmount*: `1000287846642998376`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000015c54727bf768c80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000015c54727bf768c8000000000000000000000000000000000000000000000000015c54727bf768c8000d2eb7d1d7a36526c4fdb001b0cf84db2fc3813e42080b7f79d997ca31a2855b19f30cbad3acd96d290964d9d68bc1e56ac7a2e776667000e437dc6f7fc17a5c02c98f4ca1e25ce43a178e4d9a7d28ef73ed3e8cb6f6461205ff4a0fab716c89d000000000000000000000000000000000000000000000000000000000000001ce25c87cd502c2cc743d7ffa20f873c9ea22000b4d22f483c0270eeb0d417eb7f152d70235b5e9aac61787c649a67b6a932bb21f4acce4b49b0765e9a939531ec1382424ecd0616eee08898f5aebfeef1f5fe2c8dd92fdc85af3686203634b42b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1c5ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000588dce6cb745bdcda09b4802dd50fbab93893b320000000000000000000000000000000000000000000000000de1bc7f2c4bdc68000000000000000000000000000000000000000000000015d8bba696a2b52c6800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000592c257ffdcd0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000592c257ffdcd0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f474e6d5a544130596930324f446c6d4c5451775a6d51744f574934597930354e5445334d6a63304f4459784d6a556966513d3d000000000000000000000000000000000000000000000000000000000000001d000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001b305c00406dd2396247000000000000000000000000000000000000000000001b1a96b918ae5bace24700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd2eb7d1d7a36526c4fdb001b0cf84db2fc3813e42080b7f79d997ca31a2855b1",
      "signature": {
        "s": "0x2c98f4ca1e25ce43a178e4d9a7d28ef73ed3e8cb6f6461205ff4a0fab716c89d",
        "r": "0x9f30cbad3acd96d290964d9d68bc1e56ac7a2e776667000e437dc6f7fc17a5c0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe25c87cd502c2cc743d7ffa20f873c9ea22000b4d22f483c0270eeb0d417eb7f",
      "signature": {
        "s": "0x1382424ecd0616eee08898f5aebfeef1f5fe2c8dd92fdc85af3686203634b42b",
        "r": "0x152d70235b5e9aac61787c649a67b6a932bb21f4acce4b49b0765e9a939531ec",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "401597000000000000000",
    "total": "401597000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "401597000000000000000",
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
            "amount": "401597000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "401597000000000000"
      }
    },
    "wallet": "0x588dce6cb745bdcda09b4802dd50fbab93893b32",
    "data": "eyJyZWYiOiIxOGNmZTA0Yi02ODlmLTQwZmQtOWI4Yy05NTE3Mjc0ODYxMjUifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000287846642998376",
      "previous": "402998884846642998376"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 29,
    "balances": {
      "current": "128395968122510391206471",
      "previous": "127994371122510391206471"
    }
  },
  "blockNumber": "14796269",
  "created": "2022-05-18T02:39:59.395Z",
  "updated": "2022-05-18T02:39:59.480Z",
  "id": "62845c7f7832e20011830ef8"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de1bc7f2c4bdc680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000287846642998376`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`