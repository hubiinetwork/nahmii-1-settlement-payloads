# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3Ff45d8B69b50f76BE2b9710182974e7693e5491`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000159640000000000000000000000000000000000000000000000000000000000015964000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000159640000000000000000000000000000000000000000000000000000000000015964f900dd99ce2ffcecd67a986774e93168ed9be552c1a511cfcb705c244cb0914480dae5d69099c75fed593a1dbe510652ceaf6e2dc8d1f6f9e7e7ba12c7f026c31182ac271ebf7cd0db2dd8089bd6a618f567fa6f783b03d6fa4436671edcb6a3000000000000000000000000000000000000000000000000000000000000001bb1ab606ed54821db2eab8fcb459ee2e02600cee19f6ad874d23173fe89abb5c6f026d69a4c63c8869d2cee1e682ad9d018e526095c078f36d9402ea1ba351d700ea8669b7787c305c4362eebb8077dc000e7290e5987a8be69d1a13f8a525b4d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000de00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cdf0704f000000000000000000000000000000000000000000000000002386f2cdf1ca0b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b02400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6d52694e7a526a4e4330784e5759334c5456684f4445745957466c596930325a5463354d7a6b7a4d7a51304e6a676966513d3d000000000000000000000000000000000000000000000000000000000000000f0000000000000000000000003ff45d8b69b50f76be2b9710182974e7693e54910000000000000000000000000000000000000000000000000000000000015964000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf900dd99ce2ffcecd67a986774e93168ed9be552c1a511cfcb705c244cb09144",
      "signature": {
        "s": "0x1182ac271ebf7cd0db2dd8089bd6a618f567fa6f783b03d6fa4436671edcb6a3",
        "r": "0x80dae5d69099c75fed593a1dbe510652ceaf6e2dc8d1f6f9e7e7ba12c7f026c3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb1ab606ed54821db2eab8fcb459ee2e02600cee19f6ad874d23173fe89abb5c6",
      "signature": {
        "s": "0x0ea8669b7787c305c4362eebb8077dc000e7290e5987a8be69d1a13f8a525b4d",
        "r": "0xf026d69a4c63c8869d2cee1e682ad9d018e526095c078f36d9402ea1ba351d70",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "88420",
    "total": "88420"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "88420",
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
            "amount": "503844"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "88"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNmRiNzRjNC0xNWY3LTVhODEtYWFlYi02ZTc5MzkzMzQ0NjgifQ==",
    "nonce": 222,
    "balances": {
      "current": "10000001580167247",
      "previous": "10000001580255755"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ff45d8b69b50f76be2b9710182974e7693e5491",
    "nonce": 15,
    "balances": {
      "current": "88420",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:29.897Z",
  "updated": "2020-05-22T08:00:30.971Z",
  "id": "5ec7869d005df800101bc25b"
}
```
* *stageAmount*: `88420`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000015964000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000159640000000000000000000000000000000000000000000000000000000000015964f900dd99ce2ffcecd67a986774e93168ed9be552c1a511cfcb705c244cb0914480dae5d69099c75fed593a1dbe510652ceaf6e2dc8d1f6f9e7e7ba12c7f026c31182ac271ebf7cd0db2dd8089bd6a618f567fa6f783b03d6fa4436671edcb6a3000000000000000000000000000000000000000000000000000000000000001bb1ab606ed54821db2eab8fcb459ee2e02600cee19f6ad874d23173fe89abb5c6f026d69a4c63c8869d2cee1e682ad9d018e526095c078f36d9402ea1ba351d700ea8669b7787c305c4362eebb8077dc000e7290e5987a8be69d1a13f8a525b4d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000de00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cdf0704f000000000000000000000000000000000000000000000000002386f2cdf1ca0b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b02400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6d52694e7a526a4e4330784e5759334c5456684f4445745957466c596930325a5463354d7a6b7a4d7a51304e6a676966513d3d000000000000000000000000000000000000000000000000000000000000000f0000000000000000000000003ff45d8b69b50f76be2b9710182974e7693e54910000000000000000000000000000000000000000000000000000000000015964000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf900dd99ce2ffcecd67a986774e93168ed9be552c1a511cfcb705c244cb09144",
      "signature": {
        "s": "0x1182ac271ebf7cd0db2dd8089bd6a618f567fa6f783b03d6fa4436671edcb6a3",
        "r": "0x80dae5d69099c75fed593a1dbe510652ceaf6e2dc8d1f6f9e7e7ba12c7f026c3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb1ab606ed54821db2eab8fcb459ee2e02600cee19f6ad874d23173fe89abb5c6",
      "signature": {
        "s": "0x0ea8669b7787c305c4362eebb8077dc000e7290e5987a8be69d1a13f8a525b4d",
        "r": "0xf026d69a4c63c8869d2cee1e682ad9d018e526095c078f36d9402ea1ba351d70",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "88420",
    "total": "88420"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "88420",
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
            "amount": "503844"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "88"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNmRiNzRjNC0xNWY3LTVhODEtYWFlYi02ZTc5MzkzMzQ0NjgifQ==",
    "nonce": 222,
    "balances": {
      "current": "10000001580167247",
      "previous": "10000001580255755"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ff45d8b69b50f76be2b9710182974e7693e5491",
    "nonce": 15,
    "balances": {
      "current": "88420",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:29.897Z",
  "updated": "2020-05-22T08:00:30.971Z",
  "id": "5ec7869d005df800101bc25b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000159640000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `88420`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``