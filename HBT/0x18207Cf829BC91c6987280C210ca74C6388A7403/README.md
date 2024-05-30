# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x18207Cf829BC91c6987280C210ca74C6388A7403`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000227d2ead50000000000000000000000000000000000000000000000000000000227d2ead5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000227d2ead50000000000000000000000000000000000000000000000000000000227d2ead530b71060916403eccc84a349e6645ffd81c2bc880e9317290a01692532779cbdcaf47cadee2be301b05b5e07649041fb130921d0af65c802c3ca0c9a07a431401429000ef1794ceacdd94f64860b64662d5f3c6efd320ffddac148105288ea5b000000000000000000000000000000000000000000000000000000000000001c0c117dcae7999a63afe6139a0ff25207bc8c1f26f23d4497299dab64e62920e46bfa4e982b8667a16c9bf23ee310f315664c80646da4f1c17cbc5c585305afff18a251a495204e991459a1d5032665958148573bfedd1107da132b843737bfbb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001cf800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12e280be07fb000000000000000000000000000000000000000000000000002e12e4a91e372400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000008d4454000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b6c07920a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d325a6d593255324d7930774e4745784c5455354d546774596a67794d69316d4d32466b4d7a4d795a4451324e7a516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000018207cf829bc91c6987280c210ca74c6388a74030000000000000000000000000000000000000000000000000000000227d2ead5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x30b71060916403eccc84a349e6645ffd81c2bc880e9317290a01692532779cbd",
      "signature": {
        "s": "0x1429000ef1794ceacdd94f64860b64662d5f3c6efd320ffddac148105288ea5b",
        "r": "0xcaf47cadee2be301b05b5e07649041fb130921d0af65c802c3ca0c9a07a43140",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0c117dcae7999a63afe6139a0ff25207bc8c1f26f23d4497299dab64e62920e4",
      "signature": {
        "s": "0x18a251a495204e991459a1d5032665958148573bfedd1107da132b843737bfbb",
        "r": "0x6bfa4e982b8667a16c9bf23ee310f315664c80646da4f1c17cbc5c585305afff",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9258068693",
    "total": "9258068693"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9258068693",
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
            "amount": "49057075722"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "9258068"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmM2ZmY2U2My0wNGExLTU5MTgtYjgyMi1mM2FkMzMyZDQ2NzQifQ==",
    "nonce": 7416,
    "balances": {
      "current": "12968612960536571",
      "previous": "12968622227863332"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x18207cf829bc91c6987280c210ca74c6388a7403",
    "nonce": 22,
    "balances": {
      "current": "9258068693",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:38.955Z",
  "updated": "2020-05-22T08:56:39.033Z",
  "id": "5ec793c6e5756b00111b88db"
}
```
* *stageAmount*: `9258068693`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000227d2ead5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000227d2ead50000000000000000000000000000000000000000000000000000000227d2ead530b71060916403eccc84a349e6645ffd81c2bc880e9317290a01692532779cbdcaf47cadee2be301b05b5e07649041fb130921d0af65c802c3ca0c9a07a431401429000ef1794ceacdd94f64860b64662d5f3c6efd320ffddac148105288ea5b000000000000000000000000000000000000000000000000000000000000001c0c117dcae7999a63afe6139a0ff25207bc8c1f26f23d4497299dab64e62920e46bfa4e982b8667a16c9bf23ee310f315664c80646da4f1c17cbc5c585305afff18a251a495204e991459a1d5032665958148573bfedd1107da132b843737bfbb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001cf800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12e280be07fb000000000000000000000000000000000000000000000000002e12e4a91e372400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000008d4454000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b6c07920a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d325a6d593255324d7930774e4745784c5455354d546774596a67794d69316d4d32466b4d7a4d795a4451324e7a516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000018207cf829bc91c6987280c210ca74c6388a74030000000000000000000000000000000000000000000000000000000227d2ead5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x30b71060916403eccc84a349e6645ffd81c2bc880e9317290a01692532779cbd",
      "signature": {
        "s": "0x1429000ef1794ceacdd94f64860b64662d5f3c6efd320ffddac148105288ea5b",
        "r": "0xcaf47cadee2be301b05b5e07649041fb130921d0af65c802c3ca0c9a07a43140",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0c117dcae7999a63afe6139a0ff25207bc8c1f26f23d4497299dab64e62920e4",
      "signature": {
        "s": "0x18a251a495204e991459a1d5032665958148573bfedd1107da132b843737bfbb",
        "r": "0x6bfa4e982b8667a16c9bf23ee310f315664c80646da4f1c17cbc5c585305afff",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9258068693",
    "total": "9258068693"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9258068693",
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
            "amount": "49057075722"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "9258068"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmM2ZmY2U2My0wNGExLTU5MTgtYjgyMi1mM2FkMzMyZDQ2NzQifQ==",
    "nonce": 7416,
    "balances": {
      "current": "12968612960536571",
      "previous": "12968622227863332"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x18207cf829bc91c6987280c210ca74c6388a7403",
    "nonce": 22,
    "balances": {
      "current": "9258068693",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:38.955Z",
  "updated": "2020-05-22T08:56:39.033Z",
  "id": "5ec793c6e5756b00111b88db"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000227d2ead5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9258068693`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`