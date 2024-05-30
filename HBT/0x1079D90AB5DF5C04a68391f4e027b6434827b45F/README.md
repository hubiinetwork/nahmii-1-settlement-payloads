# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1079D90AB5DF5C04a68391f4e027b6434827b45F`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000013f720000000000000000000000000000000000000000000000000000000000013f72000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000013f720000000000000000000000000000000000000000000000000000000000013f72ff2d8dd69278a46841527dc40f7742cd486ee2bd6966aab6f086a659733439a86ab48d6eadfe8722ba8ff53c0313c21c5cfa7c9456714532685ef23b116bde7056bd5206806437da345ab4334d1362e94f97318479abfb51b9b725b99e30f016000000000000000000000000000000000000000000000000000000000000001cf3636d844c2ab4ffca64b95d7a0e2998455419527ca02d3ca1b1258db6a61b52742e84b75e75e0481b4067ab37901b79b9e7120b988df36c81cc1b0463cf0d7633ed991074619f945374bd6df8dd42e86f7a46e0260e1d1ceb07a0a115c78178000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56c100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e7b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b04640870ff000000000000000000000000000000000000000000000000002e0b046409b0c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000051000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f208e67000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a5745345a6a4d34597930314d5467354c5455334d7a59744f474e6c5953316b4f47566b4f44686c4d6a55344d7a516966513d3d00000000000000000000000000000000000000000000000000000000000000070000000000000000000000001079d90ab5df5c04a68391f4e027b6434827b45f0000000000000000000000000000000000000000000000000000000000013f72000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xff2d8dd69278a46841527dc40f7742cd486ee2bd6966aab6f086a659733439a8",
      "signature": {
        "s": "0x56bd5206806437da345ab4334d1362e94f97318479abfb51b9b725b99e30f016",
        "r": "0x6ab48d6eadfe8722ba8ff53c0313c21c5cfa7c9456714532685ef23b116bde70",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf3636d844c2ab4ffca64b95d7a0e2998455419527ca02d3ca1b1258db6a61b52",
      "signature": {
        "s": "0x33ed991074619f945374bd6df8dd42e86f7a46e0260e1d1ceb07a0a115c78178",
        "r": "0x742e84b75e75e0481b4067ab37901b79b9e7120b988df36c81cc1b0463cf0d76",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "81778",
    "total": "81778"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "81778",
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
            "amount": "57698979431"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "81"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZWE4ZjM4Yy01MTg5LTU3MzYtOGNlYS1kOGVkODhlMjU4MzQifQ==",
    "nonce": 7803,
    "balances": {
      "current": "12959962414739711",
      "previous": "12959962414821570"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1079d90ab5df5c04a68391f4e027b6434827b45f",
    "nonce": 7,
    "balances": {
      "current": "81778",
      "previous": "0"
    }
  },
  "blockNumber": "10114753",
  "created": "2020-05-22T08:59:41.976Z",
  "updated": "2020-05-22T08:59:43.051Z",
  "id": "5ec7947de5756b00111b895a"
}
```
* *stageAmount*: `81778`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000013f72000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000013f720000000000000000000000000000000000000000000000000000000000013f72ff2d8dd69278a46841527dc40f7742cd486ee2bd6966aab6f086a659733439a86ab48d6eadfe8722ba8ff53c0313c21c5cfa7c9456714532685ef23b116bde7056bd5206806437da345ab4334d1362e94f97318479abfb51b9b725b99e30f016000000000000000000000000000000000000000000000000000000000000001cf3636d844c2ab4ffca64b95d7a0e2998455419527ca02d3ca1b1258db6a61b52742e84b75e75e0481b4067ab37901b79b9e7120b988df36c81cc1b0463cf0d7633ed991074619f945374bd6df8dd42e86f7a46e0260e1d1ceb07a0a115c78178000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56c100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e7b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b04640870ff000000000000000000000000000000000000000000000000002e0b046409b0c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000051000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f208e67000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a5745345a6a4d34597930314d5467354c5455334d7a59744f474e6c5953316b4f47566b4f44686c4d6a55344d7a516966513d3d00000000000000000000000000000000000000000000000000000000000000070000000000000000000000001079d90ab5df5c04a68391f4e027b6434827b45f0000000000000000000000000000000000000000000000000000000000013f72000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xff2d8dd69278a46841527dc40f7742cd486ee2bd6966aab6f086a659733439a8",
      "signature": {
        "s": "0x56bd5206806437da345ab4334d1362e94f97318479abfb51b9b725b99e30f016",
        "r": "0x6ab48d6eadfe8722ba8ff53c0313c21c5cfa7c9456714532685ef23b116bde70",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf3636d844c2ab4ffca64b95d7a0e2998455419527ca02d3ca1b1258db6a61b52",
      "signature": {
        "s": "0x33ed991074619f945374bd6df8dd42e86f7a46e0260e1d1ceb07a0a115c78178",
        "r": "0x742e84b75e75e0481b4067ab37901b79b9e7120b988df36c81cc1b0463cf0d76",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "81778",
    "total": "81778"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "81778",
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
            "amount": "57698979431"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "81"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZWE4ZjM4Yy01MTg5LTU3MzYtOGNlYS1kOGVkODhlMjU4MzQifQ==",
    "nonce": 7803,
    "balances": {
      "current": "12959962414739711",
      "previous": "12959962414821570"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1079d90ab5df5c04a68391f4e027b6434827b45f",
    "nonce": 7,
    "balances": {
      "current": "81778",
      "previous": "0"
    }
  },
  "blockNumber": "10114753",
  "created": "2020-05-22T08:59:41.976Z",
  "updated": "2020-05-22T08:59:43.051Z",
  "id": "5ec7947de5756b00111b895a"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000013f72000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `81778`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`