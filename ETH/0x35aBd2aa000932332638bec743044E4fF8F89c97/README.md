# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x35aBd2aa000932332638bec743044E4fF8F89c97`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000e0ccb00000000000000000000000000000000000000000000000000000000000e0ccb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000e0ccb00000000000000000000000000000000000000000000000000000000000e0ccbdc9f8de28e37f67186cf82fc8c02866b3cfa1cca3e55ac21a8dc45963a0604f1959d47e1b28f0eebfc35dad3b266d7ba0ec15988bb3734ba025974ed1971dc5269840a4cacf828b0e39ee253b1e1bb86545224c295f8c9eeb68319e1e11b2d26000000000000000000000000000000000000000000000000000000000000001c59e4a219155128277448e24a3f2f1e635098dc87a65350ad3fd96131cbd43341fc9634292244dfaef054b0b01caddfdb1058e4169a483a5f3a85107be3372eb8673c823938428882a99be36e7aa1c3a6fbd7e078e05a9476c87f16da714bbf16000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000d600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cf20e567000000000000000000000000000000000000000000000000002386f2cf2ef5ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000039800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007624900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d5463314e7a49325a53316a4e4455784c5455774e6a6b744f47566b595331684d575a6b4e4463785a6a52684e6a416966513d3d000000000000000000000000000000000000000000000000000000000000001800000000000000000000000035abd2aa000932332638bec743044e4ff8f89c9700000000000000000000000000000000000000000000000000000000000e0ccb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdc9f8de28e37f67186cf82fc8c02866b3cfa1cca3e55ac21a8dc45963a0604f1",
      "signature": {
        "s": "0x69840a4cacf828b0e39ee253b1e1bb86545224c295f8c9eeb68319e1e11b2d26",
        "r": "0x959d47e1b28f0eebfc35dad3b266d7ba0ec15988bb3734ba025974ed1971dc52",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x59e4a219155128277448e24a3f2f1e635098dc87a65350ad3fd96131cbd43341",
      "signature": {
        "s": "0x673c823938428882a99be36e7aa1c3a6fbd7e078e05a9476c87f16da714bbf16",
        "r": "0xfc9634292244dfaef054b0b01caddfdb1058e4169a483a5f3a85107be3372eb8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "920779",
    "total": "920779"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "920779",
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
            "amount": "483913"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "920"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMTc1NzI2ZS1jNDUxLTUwNjktOGVkYS1hMWZkNDcxZjRhNjAifQ==",
    "nonce": 214,
    "balances": {
      "current": "10000001600120167",
      "previous": "10000001601041866"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x35abd2aa000932332638bec743044e4ff8f89c97",
    "nonce": 24,
    "balances": {
      "current": "920779",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:27.428Z",
  "updated": "2020-05-22T08:00:27.495Z",
  "id": "5ec7869b005df800101bc258"
}
```
* *stageAmount*: `920779`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000e0ccb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000e0ccb00000000000000000000000000000000000000000000000000000000000e0ccbdc9f8de28e37f67186cf82fc8c02866b3cfa1cca3e55ac21a8dc45963a0604f1959d47e1b28f0eebfc35dad3b266d7ba0ec15988bb3734ba025974ed1971dc5269840a4cacf828b0e39ee253b1e1bb86545224c295f8c9eeb68319e1e11b2d26000000000000000000000000000000000000000000000000000000000000001c59e4a219155128277448e24a3f2f1e635098dc87a65350ad3fd96131cbd43341fc9634292244dfaef054b0b01caddfdb1058e4169a483a5f3a85107be3372eb8673c823938428882a99be36e7aa1c3a6fbd7e078e05a9476c87f16da714bbf16000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000d600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cf20e567000000000000000000000000000000000000000000000000002386f2cf2ef5ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000039800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007624900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d5463314e7a49325a53316a4e4455784c5455774e6a6b744f47566b595331684d575a6b4e4463785a6a52684e6a416966513d3d000000000000000000000000000000000000000000000000000000000000001800000000000000000000000035abd2aa000932332638bec743044e4ff8f89c9700000000000000000000000000000000000000000000000000000000000e0ccb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdc9f8de28e37f67186cf82fc8c02866b3cfa1cca3e55ac21a8dc45963a0604f1",
      "signature": {
        "s": "0x69840a4cacf828b0e39ee253b1e1bb86545224c295f8c9eeb68319e1e11b2d26",
        "r": "0x959d47e1b28f0eebfc35dad3b266d7ba0ec15988bb3734ba025974ed1971dc52",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x59e4a219155128277448e24a3f2f1e635098dc87a65350ad3fd96131cbd43341",
      "signature": {
        "s": "0x673c823938428882a99be36e7aa1c3a6fbd7e078e05a9476c87f16da714bbf16",
        "r": "0xfc9634292244dfaef054b0b01caddfdb1058e4169a483a5f3a85107be3372eb8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "920779",
    "total": "920779"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "920779",
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
            "amount": "483913"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "920"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMTc1NzI2ZS1jNDUxLTUwNjktOGVkYS1hMWZkNDcxZjRhNjAifQ==",
    "nonce": 214,
    "balances": {
      "current": "10000001600120167",
      "previous": "10000001601041866"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x35abd2aa000932332638bec743044e4ff8f89c97",
    "nonce": 24,
    "balances": {
      "current": "920779",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:27.428Z",
  "updated": "2020-05-22T08:00:27.495Z",
  "id": "5ec7869b005df800101bc258"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000e0ccb0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `920779`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``