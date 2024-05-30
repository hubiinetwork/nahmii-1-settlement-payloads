# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5BC2310701d013337C02555e70701e6e68cC1B62`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000575db0bebe0f42c7570000000000000000000000000000000000000000000000021243e658e615a1550000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000021243e658e615a15500000000000000000000000000000000000000000000003a1fc20e08d07699c80b28bee4cc3fdaafc33de9c1c7aaccb0d3cbbedb13ba0cdaab8c8b372df481258283e9554ac2796dbc7b86e0b34f82d7662ce7115ecaa450ffe64910a498bd6c16a72b92c00d99d345515a26d737f57d3984ac1065cd7b158006ddc1cf15dc47000000000000000000000000000000000000000000000000000000000000001c8a5472af6a06d32971ef9c64f40a70136a7dd623ee1fcf6a7065c13a1fc94e46187825d073b925517289f8df8186b08d94c66e10516c61b744ecdf89d7b395be3c26aa8de81052640ede7a644dfc29dee0939eecc459b32d459ee11fb5363e33000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0bf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bbf52dedf3ce0708f11000000000000000000000000000000000000000000004bc165aa850c22ea0cf900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000087bf765c63dc930000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d902c5d8714e4dd2190000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a6d566a4e6d51355953316d4e324a694c545535596d517459544a684e5331684e6d5a694d5467334e6a59324e47456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005bc2310701d013337c02555e70701e6e68cc1b620000000000000000000000000000000000000000000000575db0bebe0f42c7570000000000000000000000000000000000000000000000554b6cd865292d260200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0b28bee4cc3fdaafc33de9c1c7aaccb0d3cbbedb13ba0cdaab8c8b372df48125",
      "signature": {
        "s": "0x16a72b92c00d99d345515a26d737f57d3984ac1065cd7b158006ddc1cf15dc47",
        "r": "0x8283e9554ac2796dbc7b86e0b34f82d7662ce7115ecaa450ffe64910a498bd6c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8a5472af6a06d32971ef9c64f40a70136a7dd623ee1fcf6a7065c13a1fc94e46",
      "signature": {
        "s": "0x3c26aa8de81052640ede7a644dfc29dee0939eecc459b32d459ee11fb5363e33",
        "r": "0x187825d073b925517289f8df8186b08d94c66e10516c61b744ecdf89d7b395be",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "38209636933033107797",
    "total": "1072199563266831587784"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "38209636933033107797",
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
            "amount": "27614975682082843251225"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "38209636933033107"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxZmVjNmQ5YS1mN2JiLTU5YmQtYTJhNS1hNmZiMTg3NjY2NGEifQ==",
    "nonce": 110783,
    "balances": {
      "current": "357706785788910411747089",
      "previous": "357745033635480377887993"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bc2310701d013337c02555e70701e6e68cc1b62",
    "nonce": 46,
    "balances": {
      "current": "1611617839977668462423",
      "previous": "1573408203044635354626"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:54:59.517Z",
  "updated": "2022-05-04T08:54:59.622Z",
  "id": "62723f637832e20011830c29"
}
```
* *stageAmount*: `1611617839977668462423`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000021243e658e615a1550000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000021243e658e615a15500000000000000000000000000000000000000000000003a1fc20e08d07699c80b28bee4cc3fdaafc33de9c1c7aaccb0d3cbbedb13ba0cdaab8c8b372df481258283e9554ac2796dbc7b86e0b34f82d7662ce7115ecaa450ffe64910a498bd6c16a72b92c00d99d345515a26d737f57d3984ac1065cd7b158006ddc1cf15dc47000000000000000000000000000000000000000000000000000000000000001c8a5472af6a06d32971ef9c64f40a70136a7dd623ee1fcf6a7065c13a1fc94e46187825d073b925517289f8df8186b08d94c66e10516c61b744ecdf89d7b395be3c26aa8de81052640ede7a644dfc29dee0939eecc459b32d459ee11fb5363e33000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0bf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bbf52dedf3ce0708f11000000000000000000000000000000000000000000004bc165aa850c22ea0cf900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000087bf765c63dc930000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d902c5d8714e4dd2190000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a6d566a4e6d51355953316d4e324a694c545535596d517459544a684e5331684e6d5a694d5467334e6a59324e47456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005bc2310701d013337c02555e70701e6e68cc1b620000000000000000000000000000000000000000000000575db0bebe0f42c7570000000000000000000000000000000000000000000000554b6cd865292d260200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0b28bee4cc3fdaafc33de9c1c7aaccb0d3cbbedb13ba0cdaab8c8b372df48125",
      "signature": {
        "s": "0x16a72b92c00d99d345515a26d737f57d3984ac1065cd7b158006ddc1cf15dc47",
        "r": "0x8283e9554ac2796dbc7b86e0b34f82d7662ce7115ecaa450ffe64910a498bd6c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8a5472af6a06d32971ef9c64f40a70136a7dd623ee1fcf6a7065c13a1fc94e46",
      "signature": {
        "s": "0x3c26aa8de81052640ede7a644dfc29dee0939eecc459b32d459ee11fb5363e33",
        "r": "0x187825d073b925517289f8df8186b08d94c66e10516c61b744ecdf89d7b395be",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "38209636933033107797",
    "total": "1072199563266831587784"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "38209636933033107797",
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
            "amount": "27614975682082843251225"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "38209636933033107"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxZmVjNmQ5YS1mN2JiLTU5YmQtYTJhNS1hNmZiMTg3NjY2NGEifQ==",
    "nonce": 110783,
    "balances": {
      "current": "357706785788910411747089",
      "previous": "357745033635480377887993"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bc2310701d013337c02555e70701e6e68cc1b62",
    "nonce": 46,
    "balances": {
      "current": "1611617839977668462423",
      "previous": "1573408203044635354626"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:54:59.517Z",
  "updated": "2022-05-04T08:54:59.622Z",
  "id": "62723f637832e20011830c29"
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
0x0f200f9b0000000000000000000000000000000000000000000000575db0bebe0f42c7570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1611617839977668462423`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`