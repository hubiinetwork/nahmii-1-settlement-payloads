# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6541E75Ff1A06396DDbD84f3DBC4c9047e3B33b1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000ded2000000000000000000000000000000000000000000000000000000000000ded20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000ded2000000000000000000000000000000000000000000000000000000000000ded201e304f3fb255ec8f8ff679136ded4f52add34e71b2be832b4d486219f73681c35381a43bf28ef636d5c6c7d4a7e8acf36e3117733ea085b4a9d2e72f997b9e461f35f6ad16b5e87650d8177c27da62f04d89fcc0602f98239755eb897e0a93ee000000000000000000000000000000000000000000000000000000000000001ba803a5c134b583157e7142bc04cb157e88ee3a20ff7a050699a9eade0fcb9a2665a869c3a404785fd4f2451c0117ab8b3d903ad4128063d8cd05941be55afc546c362ce7bc140e0e6ec4c6d42c52a61c5c0963339b0e8dc6ba58d17236ca48a2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001c200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbef63d4000000000000000000000000000000000000000000000000002386f2cbfd548400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000039000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008333f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e575a684d6d526d4d4330795a5756684c5455784f575174596a45355a4330335a6d55784e4451795a6a566c4e47456966513d3d000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000006541e75ff1a06396ddbd84f3dbc4c9047e3b33b100000000000000000000000000000000000000000000000000000000000ded20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1e304f3fb255ec8f8ff679136ded4f52add34e71b2be832b4d486219f73681c3",
      "signature": {
        "s": "0x1f35f6ad16b5e87650d8177c27da62f04d89fcc0602f98239755eb897e0a93ee",
        "r": "0x5381a43bf28ef636d5c6c7d4a7e8acf36e3117733ea085b4a9d2e72f997b9e46",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa803a5c134b583157e7142bc04cb157e88ee3a20ff7a050699a9eade0fcb9a26",
      "signature": {
        "s": "0x6c362ce7bc140e0e6ec4c6d42c52a61c5c0963339b0e8dc6ba58d17236ca48a2",
        "r": "0x65a869c3a404785fd4f2451c0117ab8b3d903ad4128063d8cd05941be55afc54",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "912672",
    "total": "912672"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "912672",
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
            "amount": "537407"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "912"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNWZhMmRmMC0yZWVhLTUxOWQtYjE5ZC03ZmUxNDQyZjVlNGEifQ==",
    "nonce": 450,
    "balances": {
      "current": "10000001546544084",
      "previous": "10000001547457668"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6541e75ff1a06396ddbd84f3dbc4c9047e3b33b1",
    "nonce": 14,
    "balances": {
      "current": "912672",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:07.242Z",
  "updated": "2020-05-22T08:02:07.347Z",
  "id": "5ec786ffb0c6090011d5a962"
}
```
* *stageAmount*: `912672`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000ded20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000ded2000000000000000000000000000000000000000000000000000000000000ded201e304f3fb255ec8f8ff679136ded4f52add34e71b2be832b4d486219f73681c35381a43bf28ef636d5c6c7d4a7e8acf36e3117733ea085b4a9d2e72f997b9e461f35f6ad16b5e87650d8177c27da62f04d89fcc0602f98239755eb897e0a93ee000000000000000000000000000000000000000000000000000000000000001ba803a5c134b583157e7142bc04cb157e88ee3a20ff7a050699a9eade0fcb9a2665a869c3a404785fd4f2451c0117ab8b3d903ad4128063d8cd05941be55afc546c362ce7bc140e0e6ec4c6d42c52a61c5c0963339b0e8dc6ba58d17236ca48a2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001c200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbef63d4000000000000000000000000000000000000000000000000002386f2cbfd548400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000039000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008333f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e575a684d6d526d4d4330795a5756684c5455784f575174596a45355a4330335a6d55784e4451795a6a566c4e47456966513d3d000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000006541e75ff1a06396ddbd84f3dbc4c9047e3b33b100000000000000000000000000000000000000000000000000000000000ded20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1e304f3fb255ec8f8ff679136ded4f52add34e71b2be832b4d486219f73681c3",
      "signature": {
        "s": "0x1f35f6ad16b5e87650d8177c27da62f04d89fcc0602f98239755eb897e0a93ee",
        "r": "0x5381a43bf28ef636d5c6c7d4a7e8acf36e3117733ea085b4a9d2e72f997b9e46",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa803a5c134b583157e7142bc04cb157e88ee3a20ff7a050699a9eade0fcb9a26",
      "signature": {
        "s": "0x6c362ce7bc140e0e6ec4c6d42c52a61c5c0963339b0e8dc6ba58d17236ca48a2",
        "r": "0x65a869c3a404785fd4f2451c0117ab8b3d903ad4128063d8cd05941be55afc54",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "912672",
    "total": "912672"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "912672",
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
            "amount": "537407"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "912"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNWZhMmRmMC0yZWVhLTUxOWQtYjE5ZC03ZmUxNDQyZjVlNGEifQ==",
    "nonce": 450,
    "balances": {
      "current": "10000001546544084",
      "previous": "10000001547457668"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6541e75ff1a06396ddbd84f3dbc4c9047e3b33b1",
    "nonce": 14,
    "balances": {
      "current": "912672",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:07.242Z",
  "updated": "2020-05-22T08:02:07.347Z",
  "id": "5ec786ffb0c6090011d5a962"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000ded200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `912672`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``