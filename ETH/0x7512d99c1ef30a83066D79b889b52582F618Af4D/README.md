# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7512d99c1ef30a83066D79b889b52582F618Af4D`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000479300000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000479300000000000000000000000000000000000000000000000000000000000047939c58a7c94b6c2aca2a983625cddc97455ea7882241a0b23a4fce7cba710fff135ff97f7d1db1a56dabb022c78a9034004ba8172d9ac741af02fd97723ff41ec7317546de8afd34c6793271e66daadcb36555193d6992931950f3dbdd8c8a116e000000000000000000000000000000000000000000000000000000000000001c3368f7de7ffa467efea00521904daf98c18acbf962835f6a886f213d86db9f124d4c7035196380e390a548f53054009353f9fafec6c395c9d0635c18ddfbdb694f571729a2e736b50e2348bf8a5388cb65a28d5e9038316828e1299067ff9e72000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000079800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3da49e2000000000000000000000000000000000000000000000000002386f2c3da918700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a428900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a574a6a4d7a41354d5330315a444e684c54566a4e5749744f4749795a6931684e6d55794e7a59315a54646b4d44416966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007512d99c1ef30a83066d79b889b52582f618af4d0000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9c58a7c94b6c2aca2a983625cddc97455ea7882241a0b23a4fce7cba710fff13",
      "signature": {
        "s": "0x317546de8afd34c6793271e66daadcb36555193d6992931950f3dbdd8c8a116e",
        "r": "0x5ff97f7d1db1a56dabb022c78a9034004ba8172d9ac741af02fd97723ff41ec7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3368f7de7ffa467efea00521904daf98c18acbf962835f6a886f213d86db9f12",
      "signature": {
        "s": "0x4f571729a2e736b50e2348bf8a5388cb65a28d5e9038316828e1299067ff9e72",
        "r": "0x4d4c7035196380e390a548f53054009353f9fafec6c395c9d0635c18ddfbdb69",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "672393"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZWJjMzA5MS01ZDNhLTVjNWItOGIyZi1hNmUyNzY1ZTdkMDAifQ==",
    "nonce": 1944,
    "balances": {
      "current": "10000001410943458",
      "previous": "10000001410961799"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7512d99c1ef30a83066d79b889b52582f618af4d",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114542",
  "created": "2020-05-22T08:13:14.448Z",
  "updated": "2020-05-22T08:13:14.516Z",
  "id": "5ec7899a005df800101bc4b1"
}
```
* *stageAmount*: `18323`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000479300000000000000000000000000000000000000000000000000000000000047939c58a7c94b6c2aca2a983625cddc97455ea7882241a0b23a4fce7cba710fff135ff97f7d1db1a56dabb022c78a9034004ba8172d9ac741af02fd97723ff41ec7317546de8afd34c6793271e66daadcb36555193d6992931950f3dbdd8c8a116e000000000000000000000000000000000000000000000000000000000000001c3368f7de7ffa467efea00521904daf98c18acbf962835f6a886f213d86db9f124d4c7035196380e390a548f53054009353f9fafec6c395c9d0635c18ddfbdb694f571729a2e736b50e2348bf8a5388cb65a28d5e9038316828e1299067ff9e72000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000079800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3da49e2000000000000000000000000000000000000000000000000002386f2c3da918700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a428900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a574a6a4d7a41354d5330315a444e684c54566a4e5749744f4749795a6931684e6d55794e7a59315a54646b4d44416966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007512d99c1ef30a83066d79b889b52582f618af4d0000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9c58a7c94b6c2aca2a983625cddc97455ea7882241a0b23a4fce7cba710fff13",
      "signature": {
        "s": "0x317546de8afd34c6793271e66daadcb36555193d6992931950f3dbdd8c8a116e",
        "r": "0x5ff97f7d1db1a56dabb022c78a9034004ba8172d9ac741af02fd97723ff41ec7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3368f7de7ffa467efea00521904daf98c18acbf962835f6a886f213d86db9f12",
      "signature": {
        "s": "0x4f571729a2e736b50e2348bf8a5388cb65a28d5e9038316828e1299067ff9e72",
        "r": "0x4d4c7035196380e390a548f53054009353f9fafec6c395c9d0635c18ddfbdb69",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "672393"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZWJjMzA5MS01ZDNhLTVjNWItOGIyZi1hNmUyNzY1ZTdkMDAifQ==",
    "nonce": 1944,
    "balances": {
      "current": "10000001410943458",
      "previous": "10000001410961799"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7512d99c1ef30a83066d79b889b52582f618af4d",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114542",
  "created": "2020-05-22T08:13:14.448Z",
  "updated": "2020-05-22T08:13:14.516Z",
  "id": "5ec7899a005df800101bc4b1"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18323`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``