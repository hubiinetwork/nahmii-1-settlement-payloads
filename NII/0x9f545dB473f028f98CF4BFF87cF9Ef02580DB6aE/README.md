# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9f545dB473f028f98CF4BFF87cF9Ef02580DB6aE`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000011591761d2df5ee5e1800000000000000000000000000000000000000000000001133b9f02927ad95530000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001133b9f02927ad955300000000000000000000000000000000000000000000011591761d2df5ee5e180f76afaeca79848439dffc881a938a1282eebd0c8cf8c03943a9f1d49a5c1c852df7d5c0eeba34495b114281640cd54ef2633691d39279f3a0d16dcf553e2bfb0ce8a7f0585d576e08d07e33cc8f82fcf2b8d9be8947af76cbd7e46791c115d6000000000000000000000000000000000000000000000000000000000000001bf4bbeafe3365903c26f0ab58707e2bee496e6bbbd4dc9aa60dddc742c41b54e4bd70e50944fc07653f4c2d853cbbd7991e3dbb9d27e7ceef556feb1d65fc54844f40d4b0057c4107bf89df8abd11a1d77d82546da647c4069da7a06db46028f7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b509000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003524d2d6e618d66dee740000000000000000000000000000000000000000000035360af830ddae87f9f100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000004675a9bb06c762a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005decaa3127d5ca2b8d10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e4441354d445979595330794f574a6d4c5455794d47517459546b305969307a593251344e54417959544d335a6d516966513d3d00000000000000000000000000000000000000000000000000000000000000110000000000000000000000009f545db473f028f98cf4bff87cf9ef02580db6ae00000000000000000000000000000000000000000000011591761d2df5ee5e180000000000000000000000000000000000000000000001045dbc2d04ce40c8c500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f76afaeca79848439dffc881a938a1282eebd0c8cf8c03943a9f1d49a5c1c85",
      "signature": {
        "s": "0x0ce8a7f0585d576e08d07e33cc8f82fcf2b8d9be8947af76cbd7e46791c115d6",
        "r": "0x2df7d5c0eeba34495b114281640cd54ef2633691d39279f3a0d16dcf553e2bfb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf4bbeafe3365903c26f0ab58707e2bee496e6bbbd4dc9aa60dddc742c41b54e4",
      "signature": {
        "s": "0x4f40d4b0057c4107bf89df8abd11a1d77d82546da647c4069da7a06db46028f7",
        "r": "0xbd70e50944fc07653f4c2d853cbbd7991e3dbb9d27e7ceef556feb1d65fc5484",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "317321923479238186323",
    "total": "5120229705683533979160"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "317321923479238186323",
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
            "amount": "27721611133458246187217"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "317321923479238186"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NDA5MDYyYS0yOWJmLTUyMGQtYTk0Yi0zY2Q4NTAyYTM3ZmQifQ==",
    "nonce": 111881,
    "balances": {
      "current": "250964698962132072263284",
      "previous": "251282338207534789687793"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9f545db473f028f98cf4bff87cf9ef02580db6ae",
    "nonce": 17,
    "balances": {
      "current": "5120229705683533979160",
      "previous": "4802907782204295792837"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:47.407Z",
  "updated": "2022-05-04T09:00:47.492Z",
  "id": "627240bf7832e20011830d9a"
}
```
* *stageAmount*: `5120229705683533979160`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000001133b9f02927ad95530000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001133b9f02927ad955300000000000000000000000000000000000000000000011591761d2df5ee5e180f76afaeca79848439dffc881a938a1282eebd0c8cf8c03943a9f1d49a5c1c852df7d5c0eeba34495b114281640cd54ef2633691d39279f3a0d16dcf553e2bfb0ce8a7f0585d576e08d07e33cc8f82fcf2b8d9be8947af76cbd7e46791c115d6000000000000000000000000000000000000000000000000000000000000001bf4bbeafe3365903c26f0ab58707e2bee496e6bbbd4dc9aa60dddc742c41b54e4bd70e50944fc07653f4c2d853cbbd7991e3dbb9d27e7ceef556feb1d65fc54844f40d4b0057c4107bf89df8abd11a1d77d82546da647c4069da7a06db46028f7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b509000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003524d2d6e618d66dee740000000000000000000000000000000000000000000035360af830ddae87f9f100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000004675a9bb06c762a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005decaa3127d5ca2b8d10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e4441354d445979595330794f574a6d4c5455794d47517459546b305969307a593251344e54417959544d335a6d516966513d3d00000000000000000000000000000000000000000000000000000000000000110000000000000000000000009f545db473f028f98cf4bff87cf9ef02580db6ae00000000000000000000000000000000000000000000011591761d2df5ee5e180000000000000000000000000000000000000000000001045dbc2d04ce40c8c500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f76afaeca79848439dffc881a938a1282eebd0c8cf8c03943a9f1d49a5c1c85",
      "signature": {
        "s": "0x0ce8a7f0585d576e08d07e33cc8f82fcf2b8d9be8947af76cbd7e46791c115d6",
        "r": "0x2df7d5c0eeba34495b114281640cd54ef2633691d39279f3a0d16dcf553e2bfb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf4bbeafe3365903c26f0ab58707e2bee496e6bbbd4dc9aa60dddc742c41b54e4",
      "signature": {
        "s": "0x4f40d4b0057c4107bf89df8abd11a1d77d82546da647c4069da7a06db46028f7",
        "r": "0xbd70e50944fc07653f4c2d853cbbd7991e3dbb9d27e7ceef556feb1d65fc5484",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "317321923479238186323",
    "total": "5120229705683533979160"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "317321923479238186323",
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
            "amount": "27721611133458246187217"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "317321923479238186"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NDA5MDYyYS0yOWJmLTUyMGQtYTk0Yi0zY2Q4NTAyYTM3ZmQifQ==",
    "nonce": 111881,
    "balances": {
      "current": "250964698962132072263284",
      "previous": "251282338207534789687793"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9f545db473f028f98cf4bff87cf9ef02580db6ae",
    "nonce": 17,
    "balances": {
      "current": "5120229705683533979160",
      "previous": "4802907782204295792837"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:47.407Z",
  "updated": "2022-05-04T09:00:47.492Z",
  "id": "627240bf7832e20011830d9a"
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
0x0f200f9b00000000000000000000000000000000000000000000011591761d2df5ee5e180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5120229705683533979160`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`