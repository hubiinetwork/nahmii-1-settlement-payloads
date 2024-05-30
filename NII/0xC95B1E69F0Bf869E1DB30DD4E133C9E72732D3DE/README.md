# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC95B1E69F0Bf869E1DB30DD4E133C9E72732D3DE`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000e004b18141d116c000000000000000000000000000000000000000000000166e09ee119dafc00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000166e09ee119dafc0000000000000000000000000000000000000000000000000166e09ee119dafc00008901e2ab0dae6b4f7504dc6d69bec12f1b13576388d5ece84bf678f216eb44ea8a67f4a5d4532f02ce3dbf31f01f19ca0a621d558956007211cd12d9c05c2d4b183c301919cf474dd3976f6f9ce7abbc55cc2718e7543cd9d8ca122447d488d0000000000000000000000000000000000000000000000000000000000000001b0251534de56756b82f8c48963ac1e2132718434dbe280cd7d4197ec801d31e2b30ff9b857d0862cd7132ece1aea2d66f91bba2ab3d3f1a63b16cbfcd7f9a110e029a93e380b2d4102a134306ee2348c591b99dc929325f3e5549f710d5e033bb000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1e5e70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000c95b1e69f0bf869e1db30dd4e133c9e72732d3de0000000000000000000000000000000000000000000000000e004b18141d116c0000000000000000000000000000000000000000000001674a7e9042998e916c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000005bdf6410aa7580000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005bdf6410aa7580000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d54497a4e3245314e7930334d6a68684c5451785a546b745954677a5a43316c596a41794d7a5133593251354d32596966513d3d000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000028f677f1504f1632862800000000000000000000000000000000000000000000278f97526f353b36862800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8901e2ab0dae6b4f7504dc6d69bec12f1b13576388d5ece84bf678f216eb44ea",
      "signature": {
        "s": "0x183c301919cf474dd3976f6f9ce7abbc55cc2718e7543cd9d8ca122447d488d0",
        "r": "0x8a67f4a5d4532f02ce3dbf31f01f19ca0a621d558956007211cd12d9c05c2d4b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0251534de56756b82f8c48963ac1e2132718434dbe280cd7d4197ec801d31e2b",
      "signature": {
        "s": "0x029a93e380b2d4102a134306ee2348c591b99dc929325f3e5549f710d5e033bb",
        "r": "0x30ff9b857d0862cd7132ece1aea2d66f91bba2ab3d3f1a63b16cbfcd7f9a110e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6620120000000000000000",
    "total": "6620120000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6620120000000000000000",
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
            "amount": "6620120000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6620120000000000000"
      }
    },
    "wallet": "0xc95b1e69f0bf869e1db30dd4e133c9e72732d3de",
    "data": "eyJyZWYiOiJhMTIzN2E1Ny03MjhhLTQxZTktYTgzZC1lYjAyMzQ3Y2Q5M2YifQ==",
    "nonce": 14,
    "balances": {
      "current": "1008888883319738732",
      "previous": "6627749008883319738732"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 61,
    "balances": {
      "current": "193441201134378863986216",
      "previous": "186821081134378863986216"
    }
  },
  "blockNumber": "14804455",
  "created": "2022-05-19T10:34:54.995Z",
  "updated": "2022-05-19T10:34:55.180Z",
  "id": "62861d4e3592fd001130b848"
}
```
* *stageAmount*: `1008888883319738732`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000166e09ee119dafc00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000166e09ee119dafc0000000000000000000000000000000000000000000000000166e09ee119dafc00008901e2ab0dae6b4f7504dc6d69bec12f1b13576388d5ece84bf678f216eb44ea8a67f4a5d4532f02ce3dbf31f01f19ca0a621d558956007211cd12d9c05c2d4b183c301919cf474dd3976f6f9ce7abbc55cc2718e7543cd9d8ca122447d488d0000000000000000000000000000000000000000000000000000000000000001b0251534de56756b82f8c48963ac1e2132718434dbe280cd7d4197ec801d31e2b30ff9b857d0862cd7132ece1aea2d66f91bba2ab3d3f1a63b16cbfcd7f9a110e029a93e380b2d4102a134306ee2348c591b99dc929325f3e5549f710d5e033bb000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1e5e70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000c95b1e69f0bf869e1db30dd4e133c9e72732d3de0000000000000000000000000000000000000000000000000e004b18141d116c0000000000000000000000000000000000000000000001674a7e9042998e916c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000005bdf6410aa7580000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005bdf6410aa7580000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d54497a4e3245314e7930334d6a68684c5451785a546b745954677a5a43316c596a41794d7a5133593251354d32596966513d3d000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000028f677f1504f1632862800000000000000000000000000000000000000000000278f97526f353b36862800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8901e2ab0dae6b4f7504dc6d69bec12f1b13576388d5ece84bf678f216eb44ea",
      "signature": {
        "s": "0x183c301919cf474dd3976f6f9ce7abbc55cc2718e7543cd9d8ca122447d488d0",
        "r": "0x8a67f4a5d4532f02ce3dbf31f01f19ca0a621d558956007211cd12d9c05c2d4b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0251534de56756b82f8c48963ac1e2132718434dbe280cd7d4197ec801d31e2b",
      "signature": {
        "s": "0x029a93e380b2d4102a134306ee2348c591b99dc929325f3e5549f710d5e033bb",
        "r": "0x30ff9b857d0862cd7132ece1aea2d66f91bba2ab3d3f1a63b16cbfcd7f9a110e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6620120000000000000000",
    "total": "6620120000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6620120000000000000000",
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
            "amount": "6620120000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6620120000000000000"
      }
    },
    "wallet": "0xc95b1e69f0bf869e1db30dd4e133c9e72732d3de",
    "data": "eyJyZWYiOiJhMTIzN2E1Ny03MjhhLTQxZTktYTgzZC1lYjAyMzQ3Y2Q5M2YifQ==",
    "nonce": 14,
    "balances": {
      "current": "1008888883319738732",
      "previous": "6627749008883319738732"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 61,
    "balances": {
      "current": "193441201134378863986216",
      "previous": "186821081134378863986216"
    }
  },
  "blockNumber": "14804455",
  "created": "2022-05-19T10:34:54.995Z",
  "updated": "2022-05-19T10:34:55.180Z",
  "id": "62861d4e3592fd001130b848"
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
0x0f200f9b0000000000000000000000000000000000000000000000000e004b18141d116c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1008888883319738732`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`