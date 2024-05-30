# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5bfdBed17075eF1e06Fe13A6260e51c4aBdd96b3`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000004ee6a8f576a07315b70000000000000000000000000000000000000000000000000000000f6427f7a80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000f6427f7a8000000000000000000000000000000000000000000000028a70f7c9787de184608375372ccdddb627b2a9d6c77ccc56ccd261d870cb4ae6c6f91adf0b8bc2d52519d42acb0e5de248e10748a8b52083160d2c6fe096f34be8bd4f5043ff6a9254fa341f8dffd8c1f91a59d918432f6e5158af8883068ab1605e612defcdd0fa5000000000000000000000000000000000000000000000000000000000000001cef5b292322aa47a43955921df73d6b92ccdd991b8f18930ff5d576e438bbf889df0970b7cddc3ed4bb04b8459ec9e4290cd52861881225e47f575e41d87bce835d76941e1896b51911a1bb86fb8067a6a766aebbe30ad8dad99664333917ce4c000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad21000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096f1190c1aa3f626a1f20000000000000000000000000000000000000000000096f1190c1ab35e3f47ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003f0ae120000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5c7c0f0ef48e964f60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a544532596d5a695a5331694d6a4a6c4c54566a4d6d5974596d55324d793035596d457a4e324532597a49354e44636966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005bfdbed17075ef1e06fe13a6260e51c4abdd96b300000000000000000000000000000000000000000000004ee6a8f576a07315b700000000000000000000000000000000000000000000004ee6a8f5673c4b1e0f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x08375372ccdddb627b2a9d6c77ccc56ccd261d870cb4ae6c6f91adf0b8bc2d52",
      "signature": {
        "s": "0x4fa341f8dffd8c1f91a59d918432f6e5158af8883068ab1605e612defcdd0fa5",
        "r": "0x519d42acb0e5de248e10748a8b52083160d2c6fe096f34be8bd4f5043ff6a925",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xef5b292322aa47a43955921df73d6b92ccdd991b8f18930ff5d576e438bbf889",
      "signature": {
        "s": "0x5d76941e1896b51911a1bb86fb8067a6a766aebbe30ad8dad99664333917ce4c",
        "r": "0xdf0970b7cddc3ed4bb04b8459ec9e4290cd52861881225e47f575e41d87bce83",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "66104850344",
    "total": "749907740267628075078"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "66104850344",
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
            "amount": "27260234766188594947318"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "66104850"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZTE2YmZiZS1iMjJlLTVjMmYtYmU2My05YmEzN2E2YzI5NDcifQ==",
    "nonce": 109857,
    "balances": {
      "current": "712802442599052964438514",
      "previous": "712802442599119135393708"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bfdbed17075ef1e06fe13a6260e51c4abdd96b3",
    "nonce": 46,
    "balances": {
      "current": "1455466842064002684343",
      "previous": "1455466841997897833999"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:18.173Z",
  "updated": "2022-05-04T08:50:18.249Z",
  "id": "62723e4a7832e20011830afa"
}
```
* *stageAmount*: `1455466842064002684343`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000f6427f7a80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000f6427f7a8000000000000000000000000000000000000000000000028a70f7c9787de184608375372ccdddb627b2a9d6c77ccc56ccd261d870cb4ae6c6f91adf0b8bc2d52519d42acb0e5de248e10748a8b52083160d2c6fe096f34be8bd4f5043ff6a9254fa341f8dffd8c1f91a59d918432f6e5158af8883068ab1605e612defcdd0fa5000000000000000000000000000000000000000000000000000000000000001cef5b292322aa47a43955921df73d6b92ccdd991b8f18930ff5d576e438bbf889df0970b7cddc3ed4bb04b8459ec9e4290cd52861881225e47f575e41d87bce835d76941e1896b51911a1bb86fb8067a6a766aebbe30ad8dad99664333917ce4c000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad21000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096f1190c1aa3f626a1f20000000000000000000000000000000000000000000096f1190c1ab35e3f47ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003f0ae120000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5c7c0f0ef48e964f60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a544532596d5a695a5331694d6a4a6c4c54566a4d6d5974596d55324d793035596d457a4e324532597a49354e44636966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005bfdbed17075ef1e06fe13a6260e51c4abdd96b300000000000000000000000000000000000000000000004ee6a8f576a07315b700000000000000000000000000000000000000000000004ee6a8f5673c4b1e0f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x08375372ccdddb627b2a9d6c77ccc56ccd261d870cb4ae6c6f91adf0b8bc2d52",
      "signature": {
        "s": "0x4fa341f8dffd8c1f91a59d918432f6e5158af8883068ab1605e612defcdd0fa5",
        "r": "0x519d42acb0e5de248e10748a8b52083160d2c6fe096f34be8bd4f5043ff6a925",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xef5b292322aa47a43955921df73d6b92ccdd991b8f18930ff5d576e438bbf889",
      "signature": {
        "s": "0x5d76941e1896b51911a1bb86fb8067a6a766aebbe30ad8dad99664333917ce4c",
        "r": "0xdf0970b7cddc3ed4bb04b8459ec9e4290cd52861881225e47f575e41d87bce83",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "66104850344",
    "total": "749907740267628075078"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "66104850344",
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
            "amount": "27260234766188594947318"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "66104850"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZTE2YmZiZS1iMjJlLTVjMmYtYmU2My05YmEzN2E2YzI5NDcifQ==",
    "nonce": 109857,
    "balances": {
      "current": "712802442599052964438514",
      "previous": "712802442599119135393708"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bfdbed17075ef1e06fe13a6260e51c4abdd96b3",
    "nonce": 46,
    "balances": {
      "current": "1455466842064002684343",
      "previous": "1455466841997897833999"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:18.173Z",
  "updated": "2022-05-04T08:50:18.249Z",
  "id": "62723e4a7832e20011830afa"
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
0x0f200f9b00000000000000000000000000000000000000000000004ee6a8f576a07315b70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1455466842064002684343`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`