# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb3bC37A32F0b5413254f1315Efb7a93688166114`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001b2a00dadd1443b50300000000000000000000000000000000000000000000000000000005216115530000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000052161155300000000000000000000000000000000000000000000000e6a2308f6a77fd3c180157096ebe1f258754e9946ba7724e546e5af00652c4a767aa3770e29cdede186b263319ca0f40dd263670b1f442b59dd28dcddb32fd4a933e664a6559c4c117df472d9decb3244066a2bba6b5f46580b3e9f8e88285354db5468af7adf3b9f000000000000000000000000000000000000000000000000000000000000001c2f16678b0ab13e59a881d85088b64f538c49dd4b279f951a8403a78b5fbed4c81f74625112dc4aa9f648324ab026c5fbcfdd3f45fb90258e2d3869a407d277807b96f68502e069c8abb645f91de1f7af6f111175349b54fc2184cab7388e27e8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adb9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096632e081d31064880050000000000000000000000000000000000000000000096632e081d3628f9cef700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000150399f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ec0c63c2e66f1d180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d4467354f474e695a5331684d5745324c545669596a637459575a6c4d4330794d325a685a6a49355a6a686a4d7a456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000b3bc37a32f0b5413254f1315efb7a9368816611400000000000000000000000000000000000000000000001b2a00dadd1443b50300000000000000000000000000000000000000000000001b2a00dad7f2e29fb000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x80157096ebe1f258754e9946ba7724e546e5af00652c4a767aa3770e29cdede1",
      "signature": {
        "s": "0x7df472d9decb3244066a2bba6b5f46580b3e9f8e88285354db5468af7adf3b9f",
        "r": "0x86b263319ca0f40dd263670b1f442b59dd28dcddb32fd4a933e664a6559c4c11",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2f16678b0ab13e59a881d85088b64f538c49dd4b279f951a8403a78b5fbed4c8",
      "signature": {
        "s": "0x7b96f68502e069c8abb645f91de1f7af6f111175349b54fc2184cab7388e27e8",
        "r": "0x1f74625112dc4aa9f648324ab026c5fbcfdd3f45fb90258e2d3869a407d27780",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "22034847059",
    "total": "265902383479604106177"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "22034847059",
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
            "amount": "27262850076450420104472"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "22034847"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhMDg5OGNiZS1hMWE2LTViYjctYWZlMC0yM2ZhZjI5ZjhjMzEifQ==",
    "nonce": 110009,
    "balances": {
      "current": "710184517026965982052357",
      "previous": "710184517026988038934263"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3bc37a32f0b5413254f1315efb7a93688166114",
    "nonce": 46,
    "balances": {
      "current": "501088749582813476099",
      "previous": "501088749560778629040"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:51:04.779Z",
  "updated": "2022-05-04T08:51:04.861Z",
  "id": "62723e783592fd001130b44a"
}
```
* *stageAmount*: `501088749582813476099`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000005216115530000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000052161155300000000000000000000000000000000000000000000000e6a2308f6a77fd3c180157096ebe1f258754e9946ba7724e546e5af00652c4a767aa3770e29cdede186b263319ca0f40dd263670b1f442b59dd28dcddb32fd4a933e664a6559c4c117df472d9decb3244066a2bba6b5f46580b3e9f8e88285354db5468af7adf3b9f000000000000000000000000000000000000000000000000000000000000001c2f16678b0ab13e59a881d85088b64f538c49dd4b279f951a8403a78b5fbed4c81f74625112dc4aa9f648324ab026c5fbcfdd3f45fb90258e2d3869a407d277807b96f68502e069c8abb645f91de1f7af6f111175349b54fc2184cab7388e27e8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adb9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096632e081d31064880050000000000000000000000000000000000000000000096632e081d3628f9cef700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000150399f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ec0c63c2e66f1d180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d4467354f474e695a5331684d5745324c545669596a637459575a6c4d4330794d325a685a6a49355a6a686a4d7a456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000b3bc37a32f0b5413254f1315efb7a9368816611400000000000000000000000000000000000000000000001b2a00dadd1443b50300000000000000000000000000000000000000000000001b2a00dad7f2e29fb000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x80157096ebe1f258754e9946ba7724e546e5af00652c4a767aa3770e29cdede1",
      "signature": {
        "s": "0x7df472d9decb3244066a2bba6b5f46580b3e9f8e88285354db5468af7adf3b9f",
        "r": "0x86b263319ca0f40dd263670b1f442b59dd28dcddb32fd4a933e664a6559c4c11",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2f16678b0ab13e59a881d85088b64f538c49dd4b279f951a8403a78b5fbed4c8",
      "signature": {
        "s": "0x7b96f68502e069c8abb645f91de1f7af6f111175349b54fc2184cab7388e27e8",
        "r": "0x1f74625112dc4aa9f648324ab026c5fbcfdd3f45fb90258e2d3869a407d27780",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "22034847059",
    "total": "265902383479604106177"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "22034847059",
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
            "amount": "27262850076450420104472"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "22034847"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhMDg5OGNiZS1hMWE2LTViYjctYWZlMC0yM2ZhZjI5ZjhjMzEifQ==",
    "nonce": 110009,
    "balances": {
      "current": "710184517026965982052357",
      "previous": "710184517026988038934263"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3bc37a32f0b5413254f1315efb7a93688166114",
    "nonce": 46,
    "balances": {
      "current": "501088749582813476099",
      "previous": "501088749560778629040"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:51:04.779Z",
  "updated": "2022-05-04T08:51:04.861Z",
  "id": "62723e783592fd001130b44a"
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
0x0f200f9b00000000000000000000000000000000000000000000001b2a00dadd1443b5030000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `501088749582813476099`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`