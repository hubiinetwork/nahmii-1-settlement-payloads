# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x235782852fA9eC8a903C53a3dEBC3dFf2bb54F71`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000010a3b5354e4d155331000000000000000000000000000000000000000000000002f4573776553122570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000002f457377655312257000000000000000000000000000000000000000000000010a3b5354e4d155331694af1d8325dd0599940b95afcf8e6e368a520fd5d7a68c2a4fb200360a67b36a02712db63517507b7c120f0194f3208d1b49973e12040c4b1864a6efd78aa6e5782eea0e8fba6c58642da957c172d5cd752b86fec4adf3100bfafb5791179a4000000000000000000000000000000000000000000000000000000000000001be2200097c278c57dd24d7b2134905d67a3269d0fe3662147efe4064c4bf81116b377ecf17bc8e824e32656c293cceb75059927f7dcfd24aa752f04a94f71aba1662974888dfc8bf73b8c998578bee1fa30891c49791b62fa607234c080c5da72000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bd384b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001233c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000000d0673ef37df44b522a8000000000000000000000000000000000000000000000d0969080ee0ba3d9d5900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000c19f8b2057585a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000035f2e23828655bcc4bf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314f5445794e6d597a4f43316c4d7a63304c5455344e4463744f4755325979316c5a6a59794f44646b4e6a51794d574d6966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000235782852fa9ec8a903c53a3debc3dff2bb54f71000000000000000000000000000000000000000000000010a3b5354e4d15533100000000000000000000000000000000000000000000000daf5dfdd7f7e430da00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x694af1d8325dd0599940b95afcf8e6e368a520fd5d7a68c2a4fb200360a67b36",
      "signature": {
        "s": "0x5782eea0e8fba6c58642da957c172d5cd752b86fec4adf3100bfafb5791179a4",
        "r": "0xa02712db63517507b7c120f0194f3208d1b49973e12040c4b1864a6efd78aa6e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe2200097c278c57dd24d7b2134905d67a3269d0fe3662147efe4064c4bf81116",
      "signature": {
        "s": "0x662974888dfc8bf73b8c998578bee1fa30891c49791b62fa607234c080c5da72",
        "r": "0xb377ecf17bc8e824e32656c293cceb75059927f7dcfd24aa752f04a94f71aba1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "54500090397022298711",
    "total": "306944298588736672561"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "54500090397022298711",
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
            "amount": "15922864780074748265663"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "54500090397022298"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1OTEyNmYzOC1lMzc0LTU4NDctOGU2Yy1lZjYyODdkNjQyMWMifQ==",
    "nonce": 74556,
    "balances": {
      "current": "61509798699013510603432",
      "previous": "61564353289500929924441"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x235782852fa9ec8a903c53a3debc3dff2bb54f71",
    "nonce": 3,
    "balances": {
      "current": "306944298588736672561",
      "previous": "252444208191714373850"
    }
  },
  "blockNumber": "12400715",
  "created": "2021-05-09T14:38:38.140Z",
  "updated": "2021-05-09T14:38:38.198Z",
  "id": "6097f3ee10d28200105e29fe"
}
```
* *stageAmount*: `306944298588736672561`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000002f4573776553122570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000002f457377655312257000000000000000000000000000000000000000000000010a3b5354e4d155331694af1d8325dd0599940b95afcf8e6e368a520fd5d7a68c2a4fb200360a67b36a02712db63517507b7c120f0194f3208d1b49973e12040c4b1864a6efd78aa6e5782eea0e8fba6c58642da957c172d5cd752b86fec4adf3100bfafb5791179a4000000000000000000000000000000000000000000000000000000000000001be2200097c278c57dd24d7b2134905d67a3269d0fe3662147efe4064c4bf81116b377ecf17bc8e824e32656c293cceb75059927f7dcfd24aa752f04a94f71aba1662974888dfc8bf73b8c998578bee1fa30891c49791b62fa607234c080c5da72000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bd384b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001233c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000000d0673ef37df44b522a8000000000000000000000000000000000000000000000d0969080ee0ba3d9d5900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000c19f8b2057585a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000035f2e23828655bcc4bf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314f5445794e6d597a4f43316c4d7a63304c5455344e4463744f4755325979316c5a6a59794f44646b4e6a51794d574d6966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000235782852fa9ec8a903c53a3debc3dff2bb54f71000000000000000000000000000000000000000000000010a3b5354e4d15533100000000000000000000000000000000000000000000000daf5dfdd7f7e430da00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x694af1d8325dd0599940b95afcf8e6e368a520fd5d7a68c2a4fb200360a67b36",
      "signature": {
        "s": "0x5782eea0e8fba6c58642da957c172d5cd752b86fec4adf3100bfafb5791179a4",
        "r": "0xa02712db63517507b7c120f0194f3208d1b49973e12040c4b1864a6efd78aa6e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe2200097c278c57dd24d7b2134905d67a3269d0fe3662147efe4064c4bf81116",
      "signature": {
        "s": "0x662974888dfc8bf73b8c998578bee1fa30891c49791b62fa607234c080c5da72",
        "r": "0xb377ecf17bc8e824e32656c293cceb75059927f7dcfd24aa752f04a94f71aba1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "54500090397022298711",
    "total": "306944298588736672561"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "54500090397022298711",
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
            "amount": "15922864780074748265663"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "54500090397022298"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1OTEyNmYzOC1lMzc0LTU4NDctOGU2Yy1lZjYyODdkNjQyMWMifQ==",
    "nonce": 74556,
    "balances": {
      "current": "61509798699013510603432",
      "previous": "61564353289500929924441"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x235782852fa9ec8a903c53a3debc3dff2bb54f71",
    "nonce": 3,
    "balances": {
      "current": "306944298588736672561",
      "previous": "252444208191714373850"
    }
  },
  "blockNumber": "12400715",
  "created": "2021-05-09T14:38:38.140Z",
  "updated": "2021-05-09T14:38:38.198Z",
  "id": "6097f3ee10d28200105e29fe"
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
0x0f200f9b000000000000000000000000000000000000000000000010a3b5354e4d1553310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `306944298588736672561`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`