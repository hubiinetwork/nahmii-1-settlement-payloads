# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf28Fa7cFF8A73772aC7297C7355BeC720d983A17`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000e21ffed9afcb96b2900000000000000000000000000000000000000000000000141e7199c5d01dd110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000141e7199c5d01dd1100000000000000000000000000000000000000000000000e21ffed9afcb96b298596ed6f9d3db641d944cc607ea664318bd8bc17e88cee63faf49a22b1ab54f3cf97c2476ca734ecdfbaba2e6c816a5aa8c13f1392f3196fd794f97356d0755855bf23091b3451709e97a850db6a0ca6f58d1e826b1f0fd388ee7a8c0b166f33000000000000000000000000000000000000000000000000000000000000001c554b9f152a50759192e80254b0828245aebc6d3a2e8eb8fc030c930dca434d329f56e4f0fd299f5f2f4696f25d8ea49108de3d3a91c8b9bb518b86613d18c4eb66a5f555360b9253245f945d671bbc6709a7ba07da6425cb575922ba2facb298000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bfc5dc00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012cac000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000298d4a5fff26cef4393100000000000000000000000000000000000000000000298e8c9980fae14d628200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000526837b5574c400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038e0a676042ba85f53e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d5751355a574d34596930305a6d59344c5455774f4759744f474d355a43316a597a51344d7a426a596a45334d6a556966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000f28fa7cff8a73772ac7297c7355bec720d983a1700000000000000000000000000000000000000000000000e21ffed9afcb96b2900000000000000000000000000000000000000000000000ce018d3fe9fb78e1800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8596ed6f9d3db641d944cc607ea664318bd8bc17e88cee63faf49a22b1ab54f3",
      "signature": {
        "s": "0x55bf23091b3451709e97a850db6a0ca6f58d1e826b1f0fd388ee7a8c0b166f33",
        "r": "0xcf97c2476ca734ecdfbaba2e6c816a5aa8c13f1392f3196fd794f97356d07558",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x554b9f152a50759192e80254b0828245aebc6d3a2e8eb8fc030c930dca434d32",
      "signature": {
        "s": "0x66a5f555360b9253245f945d671bbc6709a7ba07da6425cb575922ba2facb298",
        "r": "0x9f56e4f0fd299f5f2f4696f25d8ea49108de3d3a91c8b9bb518b86613d18c4eb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "23195536565161024785",
    "total": "260704355004167318313"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23195536565161024785",
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
            "amount": "16787286780778385896766"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "23195536565161024"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzMWQ5ZWM4Yi00ZmY4LTUwOGYtOGM5ZC1jYzQ4MzBjYjE3MjUifQ==",
    "nonce": 76972,
    "balances": {
      "current": "196223375994672240671025",
      "previous": "196246594726773966856834"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf28fa7cff8a73772ac7297c7355bec720d983a17",
    "nonce": 11,
    "balances": {
      "current": "260704355004167318313",
      "previous": "237508818439006293528"
    }
  },
  "blockNumber": "12568028",
  "created": "2021-06-04T12:44:56.517Z",
  "updated": "2021-06-04T12:44:56.592Z",
  "id": "60ba20483a79970010e7b026"
}
```
* *stageAmount*: `260704355004167318313`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000141e7199c5d01dd110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000141e7199c5d01dd1100000000000000000000000000000000000000000000000e21ffed9afcb96b298596ed6f9d3db641d944cc607ea664318bd8bc17e88cee63faf49a22b1ab54f3cf97c2476ca734ecdfbaba2e6c816a5aa8c13f1392f3196fd794f97356d0755855bf23091b3451709e97a850db6a0ca6f58d1e826b1f0fd388ee7a8c0b166f33000000000000000000000000000000000000000000000000000000000000001c554b9f152a50759192e80254b0828245aebc6d3a2e8eb8fc030c930dca434d329f56e4f0fd299f5f2f4696f25d8ea49108de3d3a91c8b9bb518b86613d18c4eb66a5f555360b9253245f945d671bbc6709a7ba07da6425cb575922ba2facb298000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bfc5dc00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012cac000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000298d4a5fff26cef4393100000000000000000000000000000000000000000000298e8c9980fae14d628200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000526837b5574c400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038e0a676042ba85f53e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d5751355a574d34596930305a6d59344c5455774f4759744f474d355a43316a597a51344d7a426a596a45334d6a556966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000f28fa7cff8a73772ac7297c7355bec720d983a1700000000000000000000000000000000000000000000000e21ffed9afcb96b2900000000000000000000000000000000000000000000000ce018d3fe9fb78e1800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8596ed6f9d3db641d944cc607ea664318bd8bc17e88cee63faf49a22b1ab54f3",
      "signature": {
        "s": "0x55bf23091b3451709e97a850db6a0ca6f58d1e826b1f0fd388ee7a8c0b166f33",
        "r": "0xcf97c2476ca734ecdfbaba2e6c816a5aa8c13f1392f3196fd794f97356d07558",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x554b9f152a50759192e80254b0828245aebc6d3a2e8eb8fc030c930dca434d32",
      "signature": {
        "s": "0x66a5f555360b9253245f945d671bbc6709a7ba07da6425cb575922ba2facb298",
        "r": "0x9f56e4f0fd299f5f2f4696f25d8ea49108de3d3a91c8b9bb518b86613d18c4eb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "23195536565161024785",
    "total": "260704355004167318313"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23195536565161024785",
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
            "amount": "16787286780778385896766"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "23195536565161024"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzMWQ5ZWM4Yi00ZmY4LTUwOGYtOGM5ZC1jYzQ4MzBjYjE3MjUifQ==",
    "nonce": 76972,
    "balances": {
      "current": "196223375994672240671025",
      "previous": "196246594726773966856834"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf28fa7cff8a73772ac7297c7355bec720d983a17",
    "nonce": 11,
    "balances": {
      "current": "260704355004167318313",
      "previous": "237508818439006293528"
    }
  },
  "blockNumber": "12568028",
  "created": "2021-06-04T12:44:56.517Z",
  "updated": "2021-06-04T12:44:56.592Z",
  "id": "60ba20483a79970010e7b026"
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
0x0f200f9b00000000000000000000000000000000000000000000000e21ffed9afcb96b290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `260704355004167318313`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`