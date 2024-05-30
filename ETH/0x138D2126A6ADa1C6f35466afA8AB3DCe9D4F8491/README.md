# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x138D2126A6ADa1C6f35466afA8AB3DCe9D4F8491`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000003000000000000000000000000000000000000000000000000000000000000000300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000003000000000000000000000000000000000000000000000000000000000000000328217c5da6042a19af2b7a29f2530c5255a1e617e316c401c51b52dcb36dcf9acb4047edbdb47a96333390e524d16d3d5ee65c67c5aca1a24d9b02916eee067e469e5203b8f542b61d4c9c13f1ab8b44f3d38eddffe1444fa9091bb5bee0daaa000000000000000000000000000000000000000000000000000000000000001c3e8bfaf40bfe241e553042b5d672b7d39f94423364a0c455d5c649b9a4d1daf45b630e677a6e6c5b498f78cb98ec3a8b0ec489a678260bfeac43b5a18be139a81d6017362dc190c26ae20cf38f16ecfaf2d47ce0f537424c701a83aba6b7e52c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008ff00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc55d725000000000000000000000000000000000000000000000000002386f2bc55d72900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a4749344d7a6777595330774f4463324c54566a5a444174596a646d4d6930304e7a557a4e54686d5a6d59314e54676966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000138d2126a6ada1c6f35466afa8ab3dce9d4f84910000000000000000000000000000000000000000000000000000000000000003000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x28217c5da6042a19af2b7a29f2530c5255a1e617e316c401c51b52dcb36dcf9a",
      "signature": {
        "s": "0x469e5203b8f542b61d4c9c13f1ab8b44f3d38eddffe1444fa9091bb5bee0daaa",
        "r": "0xcb4047edbdb47a96333390e524d16d3d5ee65c67c5aca1a24d9b02916eee067e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3e8bfaf40bfe241e553042b5d672b7d39f94423364a0c455d5c649b9a4d1daf4",
      "signature": {
        "s": "0x1d6017362dc190c26ae20cf38f16ecfaf2d47ce0f537424c701a83aba6b7e52c",
        "r": "0x5b630e677a6e6c5b498f78cb98ec3a8b0ec489a678260bfeac43b5a18be139a8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3",
    "total": "3"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3",
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
            "amount": "798290"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZGI4MzgwYS0wODc2LTVjZDAtYjdmMi00NzUzNThmZmY1NTgifQ==",
    "nonce": 2303,
    "balances": {
      "current": "10000001284822821",
      "previous": "10000001284822825"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x138d2126a6ada1c6f35466afa8ab3dce9d4f8491",
    "nonce": 4,
    "balances": {
      "current": "3",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:37.204Z",
  "updated": "2020-05-22T08:15:37.268Z",
  "id": "5ec78a29b0c6090011d5abcd"
}
```
* *stageAmount*: `3`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000003000000000000000000000000000000000000000000000000000000000000000328217c5da6042a19af2b7a29f2530c5255a1e617e316c401c51b52dcb36dcf9acb4047edbdb47a96333390e524d16d3d5ee65c67c5aca1a24d9b02916eee067e469e5203b8f542b61d4c9c13f1ab8b44f3d38eddffe1444fa9091bb5bee0daaa000000000000000000000000000000000000000000000000000000000000001c3e8bfaf40bfe241e553042b5d672b7d39f94423364a0c455d5c649b9a4d1daf45b630e677a6e6c5b498f78cb98ec3a8b0ec489a678260bfeac43b5a18be139a81d6017362dc190c26ae20cf38f16ecfaf2d47ce0f537424c701a83aba6b7e52c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008ff00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc55d725000000000000000000000000000000000000000000000000002386f2bc55d72900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a4749344d7a6777595330774f4463324c54566a5a444174596a646d4d6930304e7a557a4e54686d5a6d59314e54676966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000138d2126a6ada1c6f35466afa8ab3dce9d4f84910000000000000000000000000000000000000000000000000000000000000003000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x28217c5da6042a19af2b7a29f2530c5255a1e617e316c401c51b52dcb36dcf9a",
      "signature": {
        "s": "0x469e5203b8f542b61d4c9c13f1ab8b44f3d38eddffe1444fa9091bb5bee0daaa",
        "r": "0xcb4047edbdb47a96333390e524d16d3d5ee65c67c5aca1a24d9b02916eee067e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3e8bfaf40bfe241e553042b5d672b7d39f94423364a0c455d5c649b9a4d1daf4",
      "signature": {
        "s": "0x1d6017362dc190c26ae20cf38f16ecfaf2d47ce0f537424c701a83aba6b7e52c",
        "r": "0x5b630e677a6e6c5b498f78cb98ec3a8b0ec489a678260bfeac43b5a18be139a8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3",
    "total": "3"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3",
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
            "amount": "798290"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZGI4MzgwYS0wODc2LTVjZDAtYjdmMi00NzUzNThmZmY1NTgifQ==",
    "nonce": 2303,
    "balances": {
      "current": "10000001284822821",
      "previous": "10000001284822825"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x138d2126a6ada1c6f35466afa8ab3dce9d4f8491",
    "nonce": 4,
    "balances": {
      "current": "3",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:37.204Z",
  "updated": "2020-05-22T08:15:37.268Z",
  "id": "5ec78a29b0c6090011d5abcd"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``