# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5469DEb14D5ee75b1e1e8B3d3C482cF7b4c0A5C3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001096abdbded120661000000000000000000000000000000000000000000000000674c41344fd74c1c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000674c41344fd74c1c000000000000000000000000000000000000000000000001096abdbded1206610940971f811a4e264830c5970fd8d099a7b07de0b9e58551885b0a91533db89eb3b0ae70f7ffebaccd72a53aab30f1730f869c445c1165a1890367187a1c24ca20f46d1250a6ffb1450a96e9ece6163c33dde4b98411fed5c45e72f0666d159d000000000000000000000000000000000000000000000000000000000000001cdd1fb954d60d0c1780db75e2890e587ffbbe0d02fc783049c3e0dfd879fdc658dfcd52cfefb6ac5eb3045bd746f2a95bb1cf57a82b714058a42e3b0be86ae89126553ba0f74109f039892d7291fbdc3f3c16392837d6e336ed242c6204b5fe17000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf9500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013a13000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023770234272057450147000000000000000000000000000000000000000000002377699ada0f543f13dc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001a71baad22c6790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c5c0d96ebf43a072bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a4463354e5751784f43316c5a57566d4c5455344f574d74595467315a6930344d4463314e546b7a4e5467784e6d496966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000005469deb14d5ee75b1e1e8b3d3c482cf7b4c0a5c3000000000000000000000000000000000000000000000001096abdbded120661000000000000000000000000000000000000000000000000a21e7c899d3aba4500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0940971f811a4e264830c5970fd8d099a7b07de0b9e58551885b0a91533db89e",
      "signature": {
        "s": "0x20f46d1250a6ffb1450a96e9ece6163c33dde4b98411fed5c45e72f0666d159d",
        "r": "0xb3b0ae70f7ffebaccd72a53aab30f1730f869c445c1165a1890367187a1c24ca",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdd1fb954d60d0c1780db75e2890e587ffbbe0d02fc783049c3e0dfd879fdc658",
      "signature": {
        "s": "0x26553ba0f74109f039892d7291fbdc3f3c16392837d6e336ed242c6204b5fe17",
        "r": "0xdfcd52cfefb6ac5eb3045bd746f2a95bb1cf57a82b714058a42e3b0be86ae891",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7443395977070201884",
    "total": "19125307391006082657"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7443395977070201884",
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
            "amount": "17815004291022698083003"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7443395977070201"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmZDc5NWQxOC1lZWVmLTU4OWMtYTg1Zi04MDc1NTkzNTgxNmIifQ==",
    "nonce": 80403,
    "balances": {
      "current": "167478148240115740508487",
      "previous": "167485599079488787780572"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5469deb14d5ee75b1e1e8b3d3c482cf7b4c0a5c3",
    "nonce": 3,
    "balances": {
      "current": "19125307391006082657",
      "previous": "11681911413935880773"
    }
  },
  "blockNumber": "12767125",
  "created": "2021-07-05T11:15:16.369Z",
  "updated": "2021-07-05T11:15:16.465Z",
  "id": "60e2e9c4abca510010d04477"
}
```
* *stageAmount*: `19125307391006082657`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000674c41344fd74c1c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000674c41344fd74c1c000000000000000000000000000000000000000000000001096abdbded1206610940971f811a4e264830c5970fd8d099a7b07de0b9e58551885b0a91533db89eb3b0ae70f7ffebaccd72a53aab30f1730f869c445c1165a1890367187a1c24ca20f46d1250a6ffb1450a96e9ece6163c33dde4b98411fed5c45e72f0666d159d000000000000000000000000000000000000000000000000000000000000001cdd1fb954d60d0c1780db75e2890e587ffbbe0d02fc783049c3e0dfd879fdc658dfcd52cfefb6ac5eb3045bd746f2a95bb1cf57a82b714058a42e3b0be86ae89126553ba0f74109f039892d7291fbdc3f3c16392837d6e336ed242c6204b5fe17000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf9500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013a13000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023770234272057450147000000000000000000000000000000000000000000002377699ada0f543f13dc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001a71baad22c6790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c5c0d96ebf43a072bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a4463354e5751784f43316c5a57566d4c5455344f574d74595467315a6930344d4463314e546b7a4e5467784e6d496966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000005469deb14d5ee75b1e1e8b3d3c482cf7b4c0a5c3000000000000000000000000000000000000000000000001096abdbded120661000000000000000000000000000000000000000000000000a21e7c899d3aba4500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0940971f811a4e264830c5970fd8d099a7b07de0b9e58551885b0a91533db89e",
      "signature": {
        "s": "0x20f46d1250a6ffb1450a96e9ece6163c33dde4b98411fed5c45e72f0666d159d",
        "r": "0xb3b0ae70f7ffebaccd72a53aab30f1730f869c445c1165a1890367187a1c24ca",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdd1fb954d60d0c1780db75e2890e587ffbbe0d02fc783049c3e0dfd879fdc658",
      "signature": {
        "s": "0x26553ba0f74109f039892d7291fbdc3f3c16392837d6e336ed242c6204b5fe17",
        "r": "0xdfcd52cfefb6ac5eb3045bd746f2a95bb1cf57a82b714058a42e3b0be86ae891",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7443395977070201884",
    "total": "19125307391006082657"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7443395977070201884",
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
            "amount": "17815004291022698083003"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7443395977070201"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmZDc5NWQxOC1lZWVmLTU4OWMtYTg1Zi04MDc1NTkzNTgxNmIifQ==",
    "nonce": 80403,
    "balances": {
      "current": "167478148240115740508487",
      "previous": "167485599079488787780572"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5469deb14d5ee75b1e1e8b3d3c482cf7b4c0a5c3",
    "nonce": 3,
    "balances": {
      "current": "19125307391006082657",
      "previous": "11681911413935880773"
    }
  },
  "blockNumber": "12767125",
  "created": "2021-07-05T11:15:16.369Z",
  "updated": "2021-07-05T11:15:16.465Z",
  "id": "60e2e9c4abca510010d04477"
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
0x0f200f9b000000000000000000000000000000000000000000000001096abdbded1206610000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `19125307391006082657`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`