# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x57381401a323E4Ef2a7B97663980B905EB425b9E`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000008239000000000000000000000000000000000000000000000000000000000000823900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000008239000000000000000000000000000000000000000000000000000000000000823918922fd84a8e5656dcd7537c711db95fc77854f871b4c66e7361822cc9e7b00c888d7126c7f4c66cacd1a0a96dc2973ff7fff1b5aa5900c76112b0114a800d01185a37851de2eec7335ee7acccb98d3f16c9df2bbf14afd4676304217c61f23c000000000000000000000000000000000000000000000000000000000000001b277e906756ffc044b641d0f6214a1dc28e1764f89f28af0fb6a5e25de78bd7dc7477f7b1cb5314eb10163eb69276e5c374a87730b8a680238d8c4cbb0804c32e27270abdf41bd9f912b458df7d1448f025ae609a898c7533df1934cf0b7fc0b2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000085600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcc6dd33000000000000000000000000000000000000000000000000002386f2bcc75f8d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000210000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c117e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335954686959545268595330785a6d55314c54566c4d544d744f54646c5a5330304e6a4d32596d5a684f475269597a6b6966513d3d000000000000000000000000000000000000000000000000000000000000001300000000000000000000000057381401a323e4ef2a7b97663980b905eb425b9e0000000000000000000000000000000000000000000000000000000000008239000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x18922fd84a8e5656dcd7537c711db95fc77854f871b4c66e7361822cc9e7b00c",
      "signature": {
        "s": "0x185a37851de2eec7335ee7acccb98d3f16c9df2bbf14afd4676304217c61f23c",
        "r": "0x888d7126c7f4c66cacd1a0a96dc2973ff7fff1b5aa5900c76112b0114a800d01",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x277e906756ffc044b641d0f6214a1dc28e1764f89f28af0fb6a5e25de78bd7dc",
      "signature": {
        "s": "0x27270abdf41bd9f912b458df7d1448f025ae609a898c7533df1934cf0b7fc0b2",
        "r": "0x7477f7b1cb5314eb10163eb69276e5c374a87730b8a680238d8c4cbb0804c32e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "33337",
    "total": "33337"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "33337",
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
            "amount": "790910"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "33"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3YThiYTRhYS0xZmU1LTVlMTMtOTdlZS00NjM2YmZhOGRiYzkifQ==",
    "nonce": 2134,
    "balances": {
      "current": "10000001292229939",
      "previous": "10000001292263309"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x57381401a323e4ef2a7b97663980b905eb425b9e",
    "nonce": 19,
    "balances": {
      "current": "33337",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:34.955Z",
  "updated": "2020-05-22T08:14:36.021Z",
  "id": "5ec789ea005df800101bc4e7"
}
```
* *stageAmount*: `33337`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000823900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000008239000000000000000000000000000000000000000000000000000000000000823918922fd84a8e5656dcd7537c711db95fc77854f871b4c66e7361822cc9e7b00c888d7126c7f4c66cacd1a0a96dc2973ff7fff1b5aa5900c76112b0114a800d01185a37851de2eec7335ee7acccb98d3f16c9df2bbf14afd4676304217c61f23c000000000000000000000000000000000000000000000000000000000000001b277e906756ffc044b641d0f6214a1dc28e1764f89f28af0fb6a5e25de78bd7dc7477f7b1cb5314eb10163eb69276e5c374a87730b8a680238d8c4cbb0804c32e27270abdf41bd9f912b458df7d1448f025ae609a898c7533df1934cf0b7fc0b2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000085600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcc6dd33000000000000000000000000000000000000000000000000002386f2bcc75f8d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000210000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c117e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335954686959545268595330785a6d55314c54566c4d544d744f54646c5a5330304e6a4d32596d5a684f475269597a6b6966513d3d000000000000000000000000000000000000000000000000000000000000001300000000000000000000000057381401a323e4ef2a7b97663980b905eb425b9e0000000000000000000000000000000000000000000000000000000000008239000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x18922fd84a8e5656dcd7537c711db95fc77854f871b4c66e7361822cc9e7b00c",
      "signature": {
        "s": "0x185a37851de2eec7335ee7acccb98d3f16c9df2bbf14afd4676304217c61f23c",
        "r": "0x888d7126c7f4c66cacd1a0a96dc2973ff7fff1b5aa5900c76112b0114a800d01",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x277e906756ffc044b641d0f6214a1dc28e1764f89f28af0fb6a5e25de78bd7dc",
      "signature": {
        "s": "0x27270abdf41bd9f912b458df7d1448f025ae609a898c7533df1934cf0b7fc0b2",
        "r": "0x7477f7b1cb5314eb10163eb69276e5c374a87730b8a680238d8c4cbb0804c32e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "33337",
    "total": "33337"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "33337",
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
            "amount": "790910"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "33"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3YThiYTRhYS0xZmU1LTVlMTMtOTdlZS00NjM2YmZhOGRiYzkifQ==",
    "nonce": 2134,
    "balances": {
      "current": "10000001292229939",
      "previous": "10000001292263309"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x57381401a323e4ef2a7b97663980b905eb425b9e",
    "nonce": 19,
    "balances": {
      "current": "33337",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:34.955Z",
  "updated": "2020-05-22T08:14:36.021Z",
  "id": "5ec789ea005df800101bc4e7"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000082390000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `33337`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``