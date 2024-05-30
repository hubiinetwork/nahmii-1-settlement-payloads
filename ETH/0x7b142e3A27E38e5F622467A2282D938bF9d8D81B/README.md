# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7b142e3A27E38e5F622467A2282D938bF9d8D81B`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001e100000000000000000000000000000000000000000000000000000000000001e1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001e100000000000000000000000000000000000000000000000000000000000001e10ab44ef16f08c0b287562f7cac60670075fca84c6ec449feac4b07d999d00a33ed8cf4ae3b20e6f9c6aa5276a165a70e4a0c758fc0da312f3d364ded90d0a07d236d90ddeb55e28b61b909c06eca0d45b9fe90f6b57b1ffcff60e02d0867319a1000000000000000000000000000000000000000000000000000000000000001bb901e4ebb95a13c6c04a6bcc90005b525f7d3facd0ab2b6b80431574315449ddbaff7c880f5a254ae6d7b4f6bb2e1443e2b9c9ab0df2fda1cbc30f34e175473755040596b1ff9488acc901ace659801030bb12a2563bbf6af613ed5fa66a327a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000032300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae4a2e1000000000000000000000000000000000000000000000000002386f2cae4c0f800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000876ec00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5464694e5455795979316c4d5749794c5456694f57557459575133597931695954426b596d4d334e4749775a54636966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007b142e3a27e38e5f622467a2282d938bf9d8d81b0000000000000000000000000000000000000000000000000000000000001e10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xab44ef16f08c0b287562f7cac60670075fca84c6ec449feac4b07d999d00a33e",
      "signature": {
        "s": "0x36d90ddeb55e28b61b909c06eca0d45b9fe90f6b57b1ffcff60e02d0867319a1",
        "r": "0xd8cf4ae3b20e6f9c6aa5276a165a70e4a0c758fc0da312f3d364ded90d0a07d2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb901e4ebb95a13c6c04a6bcc90005b525f7d3facd0ab2b6b80431574315449dd",
      "signature": {
        "s": "0x55040596b1ff9488acc901ace659801030bb12a2563bbf6af613ed5fa66a327a",
        "r": "0xbaff7c880f5a254ae6d7b4f6bb2e1443e2b9c9ab0df2fda1cbc30f34e1754737",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7696",
    "total": "7696"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7696",
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
            "amount": "554732"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "7"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiZTdiNTUyYy1lMWIyLTViOWUtYWQ3Yy1iYTBkYmM3NGIwZTcifQ==",
    "nonce": 803,
    "balances": {
      "current": "10000001529062113",
      "previous": "10000001529069816"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7b142e3a27e38e5f622467a2282d938bf9d8d81b",
    "nonce": 20,
    "balances": {
      "current": "7696",
      "previous": "0"
    }
  },
  "blockNumber": "10114510",
  "created": "2020-05-22T08:04:46.268Z",
  "updated": "2020-05-22T08:04:46.343Z",
  "id": "5ec7879e005df800101bc323"
}
```
* *stageAmount*: `7696`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000001e1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001e100000000000000000000000000000000000000000000000000000000000001e10ab44ef16f08c0b287562f7cac60670075fca84c6ec449feac4b07d999d00a33ed8cf4ae3b20e6f9c6aa5276a165a70e4a0c758fc0da312f3d364ded90d0a07d236d90ddeb55e28b61b909c06eca0d45b9fe90f6b57b1ffcff60e02d0867319a1000000000000000000000000000000000000000000000000000000000000001bb901e4ebb95a13c6c04a6bcc90005b525f7d3facd0ab2b6b80431574315449ddbaff7c880f5a254ae6d7b4f6bb2e1443e2b9c9ab0df2fda1cbc30f34e175473755040596b1ff9488acc901ace659801030bb12a2563bbf6af613ed5fa66a327a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000032300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae4a2e1000000000000000000000000000000000000000000000000002386f2cae4c0f800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000876ec00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5464694e5455795979316c4d5749794c5456694f57557459575133597931695954426b596d4d334e4749775a54636966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007b142e3a27e38e5f622467a2282d938bf9d8d81b0000000000000000000000000000000000000000000000000000000000001e10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xab44ef16f08c0b287562f7cac60670075fca84c6ec449feac4b07d999d00a33e",
      "signature": {
        "s": "0x36d90ddeb55e28b61b909c06eca0d45b9fe90f6b57b1ffcff60e02d0867319a1",
        "r": "0xd8cf4ae3b20e6f9c6aa5276a165a70e4a0c758fc0da312f3d364ded90d0a07d2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb901e4ebb95a13c6c04a6bcc90005b525f7d3facd0ab2b6b80431574315449dd",
      "signature": {
        "s": "0x55040596b1ff9488acc901ace659801030bb12a2563bbf6af613ed5fa66a327a",
        "r": "0xbaff7c880f5a254ae6d7b4f6bb2e1443e2b9c9ab0df2fda1cbc30f34e1754737",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7696",
    "total": "7696"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7696",
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
            "amount": "554732"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "7"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiZTdiNTUyYy1lMWIyLTViOWUtYWQ3Yy1iYTBkYmM3NGIwZTcifQ==",
    "nonce": 803,
    "balances": {
      "current": "10000001529062113",
      "previous": "10000001529069816"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7b142e3a27e38e5f622467a2282d938bf9d8d81b",
    "nonce": 20,
    "balances": {
      "current": "7696",
      "previous": "0"
    }
  },
  "blockNumber": "10114510",
  "created": "2020-05-22T08:04:46.268Z",
  "updated": "2020-05-22T08:04:46.343Z",
  "id": "5ec7879e005df800101bc323"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000001e100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7696`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``