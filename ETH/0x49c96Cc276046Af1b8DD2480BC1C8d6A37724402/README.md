# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x49c96Cc276046Af1b8DD2480BC1C8d6A37724402`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000001d73d000000000000000000000000000000000000000000000000000000000001d73d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001d73d000000000000000000000000000000000000000000000000000000000001d73d8f92496ef46b2e23eed3717da03d7541252989c56ab3f168168c6398cd0087bbdfe6fabd9ec57743c24cafeb6e4cf0ba9fd9e4292ba6cf879b971be15261a5c82b82eef7fd6b67e93a30838ca6582c532121d79cdc35c76d4c08e71a7078160b000000000000000000000000000000000000000000000000000000000000001ce7b480ef94bf0a6a6e61c3f85c3e653c006d5b332daa8eb9a6b3325bec3274c5b30f32e333b037eaf7393fb7bec3ab89d96a868d478b0ccdc2c1611a2155e60e149a65e80bb4d65742c4c71801bcf8a40df227b47d8b5baf66fee799c37e4cb4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c6000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001f800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb5eaa9e000000000000000000000000000000000000000000000000002386f2cb60825300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000007800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008582c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a57526b4d7a49774f5330304d4759354c54566a5a4449745957597a5a5330774f54566a597a686d595449305954676966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000049c96cc276046af1b8dd2480bc1c8d6a37724402000000000000000000000000000000000000000000000000000000000001d73d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8f92496ef46b2e23eed3717da03d7541252989c56ab3f168168c6398cd0087bb",
      "signature": {
        "s": "0x2b82eef7fd6b67e93a30838ca6582c532121d79cdc35c76d4c08e71a7078160b",
        "r": "0xdfe6fabd9ec57743c24cafeb6e4cf0ba9fd9e4292ba6cf879b971be15261a5c8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe7b480ef94bf0a6a6e61c3f85c3e653c006d5b332daa8eb9a6b3325bec3274c5",
      "signature": {
        "s": "0x149a65e80bb4d65742c4c71801bcf8a40df227b47d8b5baf66fee799c37e4cb4",
        "r": "0xb30f32e333b037eaf7393fb7bec3ab89d96a868d478b0ccdc2c1611a2155e60e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "120637",
    "total": "120637"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "120637",
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
            "amount": "546860"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "120"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZWRkMzIwOS00MGY5LTVjZDItYWYzZS0wOTVjYzhmYTI0YTgifQ==",
    "nonce": 504,
    "balances": {
      "current": "10000001537059486",
      "previous": "10000001537180243"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x49c96cc276046af1b8dd2480bc1c8d6a37724402",
    "nonce": 20,
    "balances": {
      "current": "120637",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:27.628Z",
  "updated": "2020-05-22T08:02:27.694Z",
  "id": "5ec78713b0c6090011d5a976"
}
```
* *stageAmount*: `120637`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000001d73d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001d73d000000000000000000000000000000000000000000000000000000000001d73d8f92496ef46b2e23eed3717da03d7541252989c56ab3f168168c6398cd0087bbdfe6fabd9ec57743c24cafeb6e4cf0ba9fd9e4292ba6cf879b971be15261a5c82b82eef7fd6b67e93a30838ca6582c532121d79cdc35c76d4c08e71a7078160b000000000000000000000000000000000000000000000000000000000000001ce7b480ef94bf0a6a6e61c3f85c3e653c006d5b332daa8eb9a6b3325bec3274c5b30f32e333b037eaf7393fb7bec3ab89d96a868d478b0ccdc2c1611a2155e60e149a65e80bb4d65742c4c71801bcf8a40df227b47d8b5baf66fee799c37e4cb4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c6000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001f800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb5eaa9e000000000000000000000000000000000000000000000000002386f2cb60825300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000007800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008582c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a57526b4d7a49774f5330304d4759354c54566a5a4449745957597a5a5330774f54566a597a686d595449305954676966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000049c96cc276046af1b8dd2480bc1c8d6a37724402000000000000000000000000000000000000000000000000000000000001d73d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8f92496ef46b2e23eed3717da03d7541252989c56ab3f168168c6398cd0087bb",
      "signature": {
        "s": "0x2b82eef7fd6b67e93a30838ca6582c532121d79cdc35c76d4c08e71a7078160b",
        "r": "0xdfe6fabd9ec57743c24cafeb6e4cf0ba9fd9e4292ba6cf879b971be15261a5c8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe7b480ef94bf0a6a6e61c3f85c3e653c006d5b332daa8eb9a6b3325bec3274c5",
      "signature": {
        "s": "0x149a65e80bb4d65742c4c71801bcf8a40df227b47d8b5baf66fee799c37e4cb4",
        "r": "0xb30f32e333b037eaf7393fb7bec3ab89d96a868d478b0ccdc2c1611a2155e60e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "120637",
    "total": "120637"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "120637",
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
            "amount": "546860"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "120"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZWRkMzIwOS00MGY5LTVjZDItYWYzZS0wOTVjYzhmYTI0YTgifQ==",
    "nonce": 504,
    "balances": {
      "current": "10000001537059486",
      "previous": "10000001537180243"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x49c96cc276046af1b8dd2480bc1c8d6a37724402",
    "nonce": 20,
    "balances": {
      "current": "120637",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:27.628Z",
  "updated": "2020-05-22T08:02:27.694Z",
  "id": "5ec78713b0c6090011d5a976"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000001d73d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `120637`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``