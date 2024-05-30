# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB6ce5aAF300C4f8aD22B56384E20836cD19723E7`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000004ed00000000000000000000000000000000000000000000000000000000000004ed0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004ed00000000000000000000000000000000000000000000000000000000000004ed0b9974c6b3760fd757ee16168b4e703fef7dd0f4ed9e26bd9cbb2aa27c6adb0105ffb3e95531e083181241b55ebc2b12753e00e41a3b7ae5df60366187c570456572f3f7d6839c842ca75af7ccf286a418cce7346c22b0d8a653217f99ce2ac5b000000000000000000000000000000000000000000000000000000000000001ccf010ef8d7e0842964c519cdd3ca60e173061f0978589205a076ab8feae1551b539ccb5815fc1ddb3e442caae8ace85e83a7e87627418779582e58dde47bec253c0bbd7e7b1a9113dddfa471f256acc9d9d2fcce0fca15f42cfa68a05cf94422000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d3200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0c1cd1792314000000000000000000000000000000000000000000000000002e0c1cd17971f800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000014000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d2768d25b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a4e684d32526d597930784e6d45314c5455304e324d744f47526a4d793032596a417a5a446c694d546b7a5a6d556966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000b6ce5aaf300c4f8ad22b56384e20836cd19723e70000000000000000000000000000000000000000000000000000000000004ed0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb9974c6b3760fd757ee16168b4e703fef7dd0f4ed9e26bd9cbb2aa27c6adb010",
      "signature": {
        "s": "0x572f3f7d6839c842ca75af7ccf286a418cce7346c22b0d8a653217f99ce2ac5b",
        "r": "0x5ffb3e95531e083181241b55ebc2b12753e00e41a3b7ae5df60366187c570456",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcf010ef8d7e0842964c519cdd3ca60e173061f0978589205a076ab8feae1551b",
      "signature": {
        "s": "0x3c0bbd7e7b1a9113dddfa471f256acc9d9d2fcce0fca15f42cfa68a05cf94422",
        "r": "0x539ccb5815fc1ddb3e442caae8ace85e83a7e87627418779582e58dde47bec25",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "20176",
    "total": "20176"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20176",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "56495755867"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "20"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MzNhM2RmYy0xNmE1LTU0N2MtOGRjMy02YjAzZDliMTkzZmUifQ==",
    "nonce": 7474,
    "balances": {
      "current": "12961166841684756",
      "previous": "12961166841704952"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6ce5aaf300c4f8ad22b56384e20836cd19723e7",
    "nonce": 6,
    "balances": {
      "current": "20176",
      "previous": "0"
    }
  },
  "blockNumber": "10114741",
  "created": "2020-05-22T08:57:07.915Z",
  "updated": "2020-05-22T08:57:07.979Z",
  "id": "5ec793e3e5756b00111b88ee"
}
```
* *stageAmount*: `20176`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004ed0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004ed00000000000000000000000000000000000000000000000000000000000004ed0b9974c6b3760fd757ee16168b4e703fef7dd0f4ed9e26bd9cbb2aa27c6adb0105ffb3e95531e083181241b55ebc2b12753e00e41a3b7ae5df60366187c570456572f3f7d6839c842ca75af7ccf286a418cce7346c22b0d8a653217f99ce2ac5b000000000000000000000000000000000000000000000000000000000000001ccf010ef8d7e0842964c519cdd3ca60e173061f0978589205a076ab8feae1551b539ccb5815fc1ddb3e442caae8ace85e83a7e87627418779582e58dde47bec253c0bbd7e7b1a9113dddfa471f256acc9d9d2fcce0fca15f42cfa68a05cf94422000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d3200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0c1cd1792314000000000000000000000000000000000000000000000000002e0c1cd17971f800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000014000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d2768d25b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a4e684d32526d597930784e6d45314c5455304e324d744f47526a4d793032596a417a5a446c694d546b7a5a6d556966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000b6ce5aaf300c4f8ad22b56384e20836cd19723e70000000000000000000000000000000000000000000000000000000000004ed0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb9974c6b3760fd757ee16168b4e703fef7dd0f4ed9e26bd9cbb2aa27c6adb010",
      "signature": {
        "s": "0x572f3f7d6839c842ca75af7ccf286a418cce7346c22b0d8a653217f99ce2ac5b",
        "r": "0x5ffb3e95531e083181241b55ebc2b12753e00e41a3b7ae5df60366187c570456",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcf010ef8d7e0842964c519cdd3ca60e173061f0978589205a076ab8feae1551b",
      "signature": {
        "s": "0x3c0bbd7e7b1a9113dddfa471f256acc9d9d2fcce0fca15f42cfa68a05cf94422",
        "r": "0x539ccb5815fc1ddb3e442caae8ace85e83a7e87627418779582e58dde47bec25",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "20176",
    "total": "20176"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20176",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "56495755867"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "20"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MzNhM2RmYy0xNmE1LTU0N2MtOGRjMy02YjAzZDliMTkzZmUifQ==",
    "nonce": 7474,
    "balances": {
      "current": "12961166841684756",
      "previous": "12961166841704952"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6ce5aaf300c4f8ad22b56384e20836cd19723e7",
    "nonce": 6,
    "balances": {
      "current": "20176",
      "previous": "0"
    }
  },
  "blockNumber": "10114741",
  "created": "2020-05-22T08:57:07.915Z",
  "updated": "2020-05-22T08:57:07.979Z",
  "id": "5ec793e3e5756b00111b88ee"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000004ed0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `20176`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`