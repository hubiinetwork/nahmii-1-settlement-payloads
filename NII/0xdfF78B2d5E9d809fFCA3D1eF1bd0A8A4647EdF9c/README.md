# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdfF78B2d5E9d809fFCA3D1eF1bd0A8A4647EdF9c`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000840a2d33f2d1615ac0000000000000000000000000000000000000000000000000000000180e5bc660000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000180e5bc660000000000000000000000000000000000000000000000048412c5b5563cd29850596e2dc74e11eef3b6c71d528f2c9dc5e7adc9a11c5ecae3dda06de355610fb0254c9cf306b56919dfd83a1eb525e018eed2fc80f53870a2666f11469af29d35ad0829d14a619564f3e6dd0a21ab46b07451aaa395729c896823710004f4c7000000000000000000000000000000000000000000000000000000000000001c48fa58c11bc6071804499e2689f0573b9985aa7f2c4433a88dc344335a797ce9007c87dc01399a7ae1f69afb35fcec9cbb88628f1e23f08381f811f8f454915b327e065f69b62a58a001fdd8dabe980dd6dc7c66aca537cbb7116ce21024c7bb000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5ab000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003344170b5913397917e4000000000000000000000000000000000000000000003344170b5914bac15cec00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000006288a20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df4594f4326f34bd510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e4451774d574e6d5a693032597a56694c54557a5a545574596d5a6c4e7930304f4755345a574d344e4749794d6a516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000dff78b2d5e9d809ffca3d1ef1bd0a8a4647edf9c00000000000000000000000000000000000000000000000840a2d33f2d1615ac00000000000000000000000000000000000000000000000840a2d33dac30594600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x50596e2dc74e11eef3b6c71d528f2c9dc5e7adc9a11c5ecae3dda06de355610f",
      "signature": {
        "s": "0x35ad0829d14a619564f3e6dd0a21ab46b07451aaa395729c896823710004f4c7",
        "r": "0xb0254c9cf306b56919dfd83a1eb525e018eed2fc80f53870a2666f11469af29d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x48fa58c11bc6071804499e2689f0573b9985aa7f2c4433a88dc344335a797ce9",
      "signature": {
        "s": "0x327e065f69b62a58a001fdd8dabe980dd6dc7c66aca537cbb7116ce21024c7bb",
        "r": "0x007c87dc01399a7ae1f69afb35fcec9cbb88628f1e23f08381f811f8f454915b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6457506918",
    "total": "83303862640052064920"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6457506918",
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
            "amount": "27730470243568077552977"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6457506"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmNDQwMWNmZi02YzViLTUzZTUtYmZlNy00OGU4ZWM4NGIyMjQifQ==",
    "nonce": 112043,
    "balances": {
      "current": "242096729742190875056100",
      "previous": "242096729742197339020524"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdff78b2d5e9d809ffca3d1ef1bd0a8a4647edf9c",
    "nonce": 46,
    "balances": {
      "current": "152231469822623749548",
      "previous": "152231469816166242630"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:01:43.301Z",
  "updated": "2022-05-04T09:01:43.498Z",
  "id": "627240f7bbd75600116d076c"
}
```
* *stageAmount*: `152231469822623749548`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000180e5bc660000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000180e5bc660000000000000000000000000000000000000000000000048412c5b5563cd29850596e2dc74e11eef3b6c71d528f2c9dc5e7adc9a11c5ecae3dda06de355610fb0254c9cf306b56919dfd83a1eb525e018eed2fc80f53870a2666f11469af29d35ad0829d14a619564f3e6dd0a21ab46b07451aaa395729c896823710004f4c7000000000000000000000000000000000000000000000000000000000000001c48fa58c11bc6071804499e2689f0573b9985aa7f2c4433a88dc344335a797ce9007c87dc01399a7ae1f69afb35fcec9cbb88628f1e23f08381f811f8f454915b327e065f69b62a58a001fdd8dabe980dd6dc7c66aca537cbb7116ce21024c7bb000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5ab000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003344170b5913397917e4000000000000000000000000000000000000000000003344170b5914bac15cec00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000006288a20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df4594f4326f34bd510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e4451774d574e6d5a693032597a56694c54557a5a545574596d5a6c4e7930304f4755345a574d344e4749794d6a516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000dff78b2d5e9d809ffca3d1ef1bd0a8a4647edf9c00000000000000000000000000000000000000000000000840a2d33f2d1615ac00000000000000000000000000000000000000000000000840a2d33dac30594600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x50596e2dc74e11eef3b6c71d528f2c9dc5e7adc9a11c5ecae3dda06de355610f",
      "signature": {
        "s": "0x35ad0829d14a619564f3e6dd0a21ab46b07451aaa395729c896823710004f4c7",
        "r": "0xb0254c9cf306b56919dfd83a1eb525e018eed2fc80f53870a2666f11469af29d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x48fa58c11bc6071804499e2689f0573b9985aa7f2c4433a88dc344335a797ce9",
      "signature": {
        "s": "0x327e065f69b62a58a001fdd8dabe980dd6dc7c66aca537cbb7116ce21024c7bb",
        "r": "0x007c87dc01399a7ae1f69afb35fcec9cbb88628f1e23f08381f811f8f454915b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6457506918",
    "total": "83303862640052064920"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6457506918",
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
            "amount": "27730470243568077552977"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6457506"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmNDQwMWNmZi02YzViLTUzZTUtYmZlNy00OGU4ZWM4NGIyMjQifQ==",
    "nonce": 112043,
    "balances": {
      "current": "242096729742190875056100",
      "previous": "242096729742197339020524"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdff78b2d5e9d809ffca3d1ef1bd0a8a4647edf9c",
    "nonce": 46,
    "balances": {
      "current": "152231469822623749548",
      "previous": "152231469816166242630"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:01:43.301Z",
  "updated": "2022-05-04T09:01:43.498Z",
  "id": "627240f7bbd75600116d076c"
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
0x0f200f9b00000000000000000000000000000000000000000000000840a2d33f2d1615ac0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `152231469822623749548`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`