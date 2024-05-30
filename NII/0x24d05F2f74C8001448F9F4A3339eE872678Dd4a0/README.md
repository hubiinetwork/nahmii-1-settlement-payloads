# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x24d05F2f74C8001448F9F4A3339eE872678Dd4a0`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de13142e786186800000000000000000000000000000000000000000000001237f6b26754a100000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001237f6b26754a100000000000000000000000000000000000000000000000000486dc0602d334100000b2d8e35a261202efd0433539120a226d5ae9dc5b56fe42e5d223bb1b7d921245114500fc7be0f115a008f2f4a07974ceaefe116afac0facef796c91c74eebb052f2550eccc64ed2e9053ac902ac585d4ca329a894eb8045b792992e6875b3da000000000000000000000000000000000000000000000000000000000000001cc8b488a458422342ca23d282af4ab2e5949604fca3e148d04d6a890b5d68f32fe67b547a5077772c9489db399db6dfa8f6a3738910a221d536d8f44210f1f0ab32513f6ed596fa102c284961bdf25d4c3d3a81ec04192de027877f5b0bc3c3ad000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e2120e0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000003000000000000000000000000024d05f2f74c8001448f9f4a3339ee872678dd4a00000000000000000000000000000000000000000000000000de13142e78618680000000000000000000000000000000000000000000000124a81dd2ff865b86800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000004a9f985bc3ea0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000128ab03963a2a0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935596a51794e7a6b794d5330354d5446684c54526a4d6a417459544134596930345957526b4f4745775a545a6d4f44496966513d3d000000000000000000000000000000000000000000000000000000000000005a000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000553bcfe655d456cd9be800000000000000000000000000000000000000000000552997efa36d022c9be800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0b2d8e35a261202efd0433539120a226d5ae9dc5b56fe42e5d223bb1b7d92124",
      "signature": {
        "s": "0x52f2550eccc64ed2e9053ac902ac585d4ca329a894eb8045b792992e6875b3da",
        "r": "0x5114500fc7be0f115a008f2f4a07974ceaefe116afac0facef796c91c74eebb0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc8b488a458422342ca23d282af4ab2e5949604fca3e148d04d6a890b5d68f32f",
      "signature": {
        "s": "0x32513f6ed596fa102c284961bdf25d4c3d3a81ec04192de027877f5b0bc3c3ad",
        "r": "0xe67b547a5077772c9489db399db6dfa8f6a3738910a221d536d8f44210f1f0ab",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "336074000000000000000",
    "total": "1336074000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "336074000000000000000",
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
            "amount": "1336074000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "336074000000000000"
      }
    },
    "wallet": "0x24d05f2f74c8001448f9f4a3339ee872678dd4a0",
    "data": "eyJyZWYiOiI5YjQyNzkyMS05MTFhLTRjMjAtYTA4Yi04YWRkOGEwZTZmODIifQ==",
    "nonce": 48,
    "balances": {
      "current": "1000134755674888296",
      "previous": "337410208755674888296"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 90,
    "balances": {
      "current": "402504489699849678986216",
      "previous": "402168415699849678986216"
    }
  },
  "blockNumber": "14815758",
  "created": "2022-05-21T06:35:38.217Z",
  "updated": "2022-05-21T06:35:38.301Z",
  "id": "6288883a3592fd001130b85e"
}
```
* *stageAmount*: `1000134755674888296`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000001237f6b26754a100000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001237f6b26754a100000000000000000000000000000000000000000000000000486dc0602d334100000b2d8e35a261202efd0433539120a226d5ae9dc5b56fe42e5d223bb1b7d921245114500fc7be0f115a008f2f4a07974ceaefe116afac0facef796c91c74eebb052f2550eccc64ed2e9053ac902ac585d4ca329a894eb8045b792992e6875b3da000000000000000000000000000000000000000000000000000000000000001cc8b488a458422342ca23d282af4ab2e5949604fca3e148d04d6a890b5d68f32fe67b547a5077772c9489db399db6dfa8f6a3738910a221d536d8f44210f1f0ab32513f6ed596fa102c284961bdf25d4c3d3a81ec04192de027877f5b0bc3c3ad000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e2120e0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000003000000000000000000000000024d05f2f74c8001448f9f4a3339ee872678dd4a00000000000000000000000000000000000000000000000000de13142e78618680000000000000000000000000000000000000000000000124a81dd2ff865b86800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000004a9f985bc3ea0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000128ab03963a2a0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935596a51794e7a6b794d5330354d5446684c54526a4d6a417459544134596930345957526b4f4745775a545a6d4f44496966513d3d000000000000000000000000000000000000000000000000000000000000005a000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000553bcfe655d456cd9be800000000000000000000000000000000000000000000552997efa36d022c9be800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0b2d8e35a261202efd0433539120a226d5ae9dc5b56fe42e5d223bb1b7d92124",
      "signature": {
        "s": "0x52f2550eccc64ed2e9053ac902ac585d4ca329a894eb8045b792992e6875b3da",
        "r": "0x5114500fc7be0f115a008f2f4a07974ceaefe116afac0facef796c91c74eebb0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc8b488a458422342ca23d282af4ab2e5949604fca3e148d04d6a890b5d68f32f",
      "signature": {
        "s": "0x32513f6ed596fa102c284961bdf25d4c3d3a81ec04192de027877f5b0bc3c3ad",
        "r": "0xe67b547a5077772c9489db399db6dfa8f6a3738910a221d536d8f44210f1f0ab",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "336074000000000000000",
    "total": "1336074000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "336074000000000000000",
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
            "amount": "1336074000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "336074000000000000"
      }
    },
    "wallet": "0x24d05f2f74c8001448f9f4a3339ee872678dd4a0",
    "data": "eyJyZWYiOiI5YjQyNzkyMS05MTFhLTRjMjAtYTA4Yi04YWRkOGEwZTZmODIifQ==",
    "nonce": 48,
    "balances": {
      "current": "1000134755674888296",
      "previous": "337410208755674888296"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 90,
    "balances": {
      "current": "402504489699849678986216",
      "previous": "402168415699849678986216"
    }
  },
  "blockNumber": "14815758",
  "created": "2022-05-21T06:35:38.217Z",
  "updated": "2022-05-21T06:35:38.301Z",
  "id": "6288883a3592fd001130b85e"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de13142e78618680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000134755674888296`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`