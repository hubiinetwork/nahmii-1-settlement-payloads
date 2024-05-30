# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAE459B4A8b3EE346e0C05dca5f1749D01Fb722b8`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000020b100000000000000000000000000000000000000000000000000000000000020b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000020b100000000000000000000000000000000000000000000000000000000000020b190b4d571b4229d483456bf2388a7829722fa68f0f718cba925cd7d44a87e47a9a8cbe116c09b5dcec63c812c2b238cfd39ba489120a01bfcb74d82d893c4dde511abeef584f573b51ec33b31effbfe0c3142a246139d9d33cee4d001a2d2a332000000000000000000000000000000000000000000000000000000000000001b1f853edfb5ec567902a9bf48b664ab59aa3076435ae322b591a31727d9dd131136d235d1ba1e482bf7cfc7fd0250bf2acda4f81bdfd98e9a87cc2d59f4ea5b643b150ca707246cc254428d82e33d0a138deb343bf5c39fb92d16bf9b89024d23000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000090800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc556d87000000000000000000000000000000000000000000000000002386f2bc558e4000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e7100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a4d314d474e6d595330324d6d55314c54566a4d6d4574595459325a4330785a474e6c5a6d45785a57457a596d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000ae459b4a8b3ee346e0c05dca5f1749d01fb722b800000000000000000000000000000000000000000000000000000000000020b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x90b4d571b4229d483456bf2388a7829722fa68f0f718cba925cd7d44a87e47a9",
      "signature": {
        "s": "0x11abeef584f573b51ec33b31effbfe0c3142a246139d9d33cee4d001a2d2a332",
        "r": "0xa8cbe116c09b5dcec63c812c2b238cfd39ba489120a01bfcb74d82d893c4dde5",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1f853edfb5ec567902a9bf48b664ab59aa3076435ae322b591a31727d9dd1311",
      "signature": {
        "s": "0x3b150ca707246cc254428d82e33d0a138deb343bf5c39fb92d16bf9b89024d23",
        "r": "0x36d235d1ba1e482bf7cfc7fd0250bf2acda4f81bdfd98e9a87cc2d59f4ea5b64",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8369",
    "total": "8369"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8369",
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
            "amount": "798321"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZjM1MGNmYS02MmU1LTVjMmEtYTY2ZC0xZGNlZmExZWEzYmMifQ==",
    "nonce": 2312,
    "balances": {
      "current": "10000001284795783",
      "previous": "10000001284804160"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xae459b4a8b3ee346e0c05dca5f1749d01fb722b8",
    "nonce": 4,
    "balances": {
      "current": "8369",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:42.910Z",
  "updated": "2020-05-22T08:15:42.986Z",
  "id": "5ec78a2ee5756b00111b8260"
}
```
* *stageAmount*: `8369`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000020b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000020b100000000000000000000000000000000000000000000000000000000000020b190b4d571b4229d483456bf2388a7829722fa68f0f718cba925cd7d44a87e47a9a8cbe116c09b5dcec63c812c2b238cfd39ba489120a01bfcb74d82d893c4dde511abeef584f573b51ec33b31effbfe0c3142a246139d9d33cee4d001a2d2a332000000000000000000000000000000000000000000000000000000000000001b1f853edfb5ec567902a9bf48b664ab59aa3076435ae322b591a31727d9dd131136d235d1ba1e482bf7cfc7fd0250bf2acda4f81bdfd98e9a87cc2d59f4ea5b643b150ca707246cc254428d82e33d0a138deb343bf5c39fb92d16bf9b89024d23000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000090800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc556d87000000000000000000000000000000000000000000000000002386f2bc558e4000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e7100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a4d314d474e6d595330324d6d55314c54566a4d6d4574595459325a4330785a474e6c5a6d45785a57457a596d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000ae459b4a8b3ee346e0c05dca5f1749d01fb722b800000000000000000000000000000000000000000000000000000000000020b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x90b4d571b4229d483456bf2388a7829722fa68f0f718cba925cd7d44a87e47a9",
      "signature": {
        "s": "0x11abeef584f573b51ec33b31effbfe0c3142a246139d9d33cee4d001a2d2a332",
        "r": "0xa8cbe116c09b5dcec63c812c2b238cfd39ba489120a01bfcb74d82d893c4dde5",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1f853edfb5ec567902a9bf48b664ab59aa3076435ae322b591a31727d9dd1311",
      "signature": {
        "s": "0x3b150ca707246cc254428d82e33d0a138deb343bf5c39fb92d16bf9b89024d23",
        "r": "0x36d235d1ba1e482bf7cfc7fd0250bf2acda4f81bdfd98e9a87cc2d59f4ea5b64",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8369",
    "total": "8369"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8369",
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
            "amount": "798321"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZjM1MGNmYS02MmU1LTVjMmEtYTY2ZC0xZGNlZmExZWEzYmMifQ==",
    "nonce": 2312,
    "balances": {
      "current": "10000001284795783",
      "previous": "10000001284804160"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xae459b4a8b3ee346e0c05dca5f1749d01fb722b8",
    "nonce": 4,
    "balances": {
      "current": "8369",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:42.910Z",
  "updated": "2020-05-22T08:15:42.986Z",
  "id": "5ec78a2ee5756b00111b8260"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000020b10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8369`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``