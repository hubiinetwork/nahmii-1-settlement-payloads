# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xaeD9075d1BdD046bC1AF03c476517EBB2768aCf7`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de5cfb248bb65450000000000000000000000000000000000000000000000a0209208f588fd00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000a0209208f588fd00000000000000000000000000000000000000000000000000a0209208f588fd0000486ce154eae64f9954fd861f8f7d038ec94dcd8eaabe5a359fd1a78a663660a6578263a36b9cdd8c0f363e14c80ca56b8b28329b9cff48d5096ced13d07620ab4298f21c9e91bba18c9844354102c96d58257c105c372df758bc3249769c38dd000000000000000000000000000000000000000000000000000000000000001bb19840eaea3b6448e4ab088c0d663b1ca72290554303b166db63ded164742ddd3ac79435a55b2e4a897ca1369bf99952a088af72e26bbc640e018e5291753ab72a8454e62af7cb01e957cd2f363e84a23d9e09dd67076c48539baaff7d3e79d9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e271f900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000031000000000000000000000000aed9075d1bdd046bc1af03c476517ebb2768acf70000000000000000000000000000000000000000000000000de5cfb248bb65450000000000000000000000000000000000000000000000a05775f1c0a408854500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000028fe1918d25020000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000028fe1918d25020000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e475a6c4d7a55324e7930774e6d55354c54513059546774596a68694e4330334d5441334e545a6a593259335954676966513d3d0000000000000000000000000000000000000000000000000000000000000097000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000078c737b9e7645ebdf9400000000000000000000000000000000000000000000078271727de6ed5c0f94000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x486ce154eae64f9954fd861f8f7d038ec94dcd8eaabe5a359fd1a78a663660a6",
      "signature": {
        "s": "0x4298f21c9e91bba18c9844354102c96d58257c105c372df758bc3249769c38dd",
        "r": "0x578263a36b9cdd8c0f363e14c80ca56b8b28329b9cff48d5096ced13d07620ab",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb19840eaea3b6448e4ab088c0d663b1ca72290554303b166db63ded164742ddd",
      "signature": {
        "s": "0x2a8454e62af7cb01e957cd2f363e84a23d9e09dd67076c48539baaff7d3e79d9",
        "r": "0x3ac79435a55b2e4a897ca1369bf99952a088af72e26bbc640e018e5291753ab7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2953826000000000000000",
    "total": "2953826000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2953826000000000000000",
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
            "amount": "2953826000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2953826000000000000"
      }
    },
    "wallet": "0xaed9075d1bdd046bc1af03c476517ebb2768acf7",
    "data": "eyJyZWYiOiI5NGZlMzU2Ny0wNmU5LTQ0YTgtYjhiNC03MTA3NTZjY2Y3YTgifQ==",
    "nonce": 49,
    "balances": {
      "current": "1001434856791172421",
      "previous": "2957781260856791172421"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 151,
    "balances": {
      "current": "570358895509986676177216",
      "previous": "567405069509986676177216"
    }
  },
  "blockNumber": "14840313",
  "created": "2022-05-25T06:27:19.356Z",
  "updated": "2022-05-25T06:27:19.461Z",
  "id": "628dcc477832e20011830f4a"
}
```
* *stageAmount*: `1001434856791172421`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000a0209208f588fd00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000a0209208f588fd00000000000000000000000000000000000000000000000000a0209208f588fd0000486ce154eae64f9954fd861f8f7d038ec94dcd8eaabe5a359fd1a78a663660a6578263a36b9cdd8c0f363e14c80ca56b8b28329b9cff48d5096ced13d07620ab4298f21c9e91bba18c9844354102c96d58257c105c372df758bc3249769c38dd000000000000000000000000000000000000000000000000000000000000001bb19840eaea3b6448e4ab088c0d663b1ca72290554303b166db63ded164742ddd3ac79435a55b2e4a897ca1369bf99952a088af72e26bbc640e018e5291753ab72a8454e62af7cb01e957cd2f363e84a23d9e09dd67076c48539baaff7d3e79d9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e271f900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000031000000000000000000000000aed9075d1bdd046bc1af03c476517ebb2768acf70000000000000000000000000000000000000000000000000de5cfb248bb65450000000000000000000000000000000000000000000000a05775f1c0a408854500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000028fe1918d25020000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000028fe1918d25020000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e475a6c4d7a55324e7930774e6d55354c54513059546774596a68694e4330334d5441334e545a6a593259335954676966513d3d0000000000000000000000000000000000000000000000000000000000000097000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000078c737b9e7645ebdf9400000000000000000000000000000000000000000000078271727de6ed5c0f94000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x486ce154eae64f9954fd861f8f7d038ec94dcd8eaabe5a359fd1a78a663660a6",
      "signature": {
        "s": "0x4298f21c9e91bba18c9844354102c96d58257c105c372df758bc3249769c38dd",
        "r": "0x578263a36b9cdd8c0f363e14c80ca56b8b28329b9cff48d5096ced13d07620ab",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb19840eaea3b6448e4ab088c0d663b1ca72290554303b166db63ded164742ddd",
      "signature": {
        "s": "0x2a8454e62af7cb01e957cd2f363e84a23d9e09dd67076c48539baaff7d3e79d9",
        "r": "0x3ac79435a55b2e4a897ca1369bf99952a088af72e26bbc640e018e5291753ab7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2953826000000000000000",
    "total": "2953826000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2953826000000000000000",
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
            "amount": "2953826000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2953826000000000000"
      }
    },
    "wallet": "0xaed9075d1bdd046bc1af03c476517ebb2768acf7",
    "data": "eyJyZWYiOiI5NGZlMzU2Ny0wNmU5LTQ0YTgtYjhiNC03MTA3NTZjY2Y3YTgifQ==",
    "nonce": 49,
    "balances": {
      "current": "1001434856791172421",
      "previous": "2957781260856791172421"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 151,
    "balances": {
      "current": "570358895509986676177216",
      "previous": "567405069509986676177216"
    }
  },
  "blockNumber": "14840313",
  "created": "2022-05-25T06:27:19.356Z",
  "updated": "2022-05-25T06:27:19.461Z",
  "id": "628dcc477832e20011830f4a"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de5cfb248bb65450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1001434856791172421`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`