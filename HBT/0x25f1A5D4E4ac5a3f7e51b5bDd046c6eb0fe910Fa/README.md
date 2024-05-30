# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x25f1A5D4E4ac5a3f7e51b5bDd046c6eb0fe910Fa`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000002630000000000000000000000000000000000000000000000000000000000000263000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000026300000000000000000000000000000000000000000000000000000000000002636b08d525f8c5094b47bbfb2133f66f971ad2ed85f0165f99066d3463a547ac2904703cfb6c79e4de567dd06f0deebd59b790b811bef2598b76ddb6cd2de633447282b930a25b1307188075eb64fd670f60aed8352de2e77f9b66f6de2aa0976f000000000000000000000000000000000000000000000000000000000000001c63a600250aeee5c95d5c575010053f092e22048fd755d56933088ad1323b4b8adca26977bfeefab1871573e897590658c0a8895658e260101138e3ad19e1173e08137fdabbf1d09df0415210d9d4312d0e201b198cfe9d149a64ab51ecdb0b0d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000157e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d600da67529000000000000000000000000000000000000000000000000002e1d600da6778d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd372cc6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931597a49324e7a5a6d4e693032595442684c54566b595755745957517a4d4331695a6a56685a446b324e3246684e32496966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000025f1a5d4e4ac5a3f7e51b5bdd046c6eb0fe910fa0000000000000000000000000000000000000000000000000000000000000263000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6b08d525f8c5094b47bbfb2133f66f971ad2ed85f0165f99066d3463a547ac29",
      "signature": {
        "s": "0x7282b930a25b1307188075eb64fd670f60aed8352de2e77f9b66f6de2aa0976f",
        "r": "0x04703cfb6c79e4de567dd06f0deebd59b790b811bef2598b76ddb6cd2de63344",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x63a600250aeee5c95d5c575010053f092e22048fd755d56933088ad1323b4b8a",
      "signature": {
        "s": "0x08137fdabbf1d09df0415210d9d4312d0e201b198cfe9d149a64ab51ecdb0b0d",
        "r": "0xdca26977bfeefab1871573e897590658c0a8895658e260101138e3ad19e1173e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "611",
    "total": "611"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "611",
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
            "amount": "37534248134"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1YzI2NzZmNi02YTBhLTVkYWUtYWQzMC1iZjVhZDk2N2FhN2IifQ==",
    "nonce": 5502,
    "balances": {
      "current": "12980147311768873",
      "previous": "12980147311769485"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x25f1a5d4e4ac5a3f7e51b5bdd046c6eb0fe910fa",
    "nonce": 21,
    "balances": {
      "current": "611",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:37.553Z",
  "updated": "2020-05-22T08:41:39.650Z",
  "id": "5ec79041005df800101bc969"
}
```
* *stageAmount*: `611`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000263000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000026300000000000000000000000000000000000000000000000000000000000002636b08d525f8c5094b47bbfb2133f66f971ad2ed85f0165f99066d3463a547ac2904703cfb6c79e4de567dd06f0deebd59b790b811bef2598b76ddb6cd2de633447282b930a25b1307188075eb64fd670f60aed8352de2e77f9b66f6de2aa0976f000000000000000000000000000000000000000000000000000000000000001c63a600250aeee5c95d5c575010053f092e22048fd755d56933088ad1323b4b8adca26977bfeefab1871573e897590658c0a8895658e260101138e3ad19e1173e08137fdabbf1d09df0415210d9d4312d0e201b198cfe9d149a64ab51ecdb0b0d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000157e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d600da67529000000000000000000000000000000000000000000000000002e1d600da6778d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd372cc6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931597a49324e7a5a6d4e693032595442684c54566b595755745957517a4d4331695a6a56685a446b324e3246684e32496966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000025f1a5d4e4ac5a3f7e51b5bdd046c6eb0fe910fa0000000000000000000000000000000000000000000000000000000000000263000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6b08d525f8c5094b47bbfb2133f66f971ad2ed85f0165f99066d3463a547ac29",
      "signature": {
        "s": "0x7282b930a25b1307188075eb64fd670f60aed8352de2e77f9b66f6de2aa0976f",
        "r": "0x04703cfb6c79e4de567dd06f0deebd59b790b811bef2598b76ddb6cd2de63344",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x63a600250aeee5c95d5c575010053f092e22048fd755d56933088ad1323b4b8a",
      "signature": {
        "s": "0x08137fdabbf1d09df0415210d9d4312d0e201b198cfe9d149a64ab51ecdb0b0d",
        "r": "0xdca26977bfeefab1871573e897590658c0a8895658e260101138e3ad19e1173e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "611",
    "total": "611"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "611",
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
            "amount": "37534248134"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1YzI2NzZmNi02YTBhLTVkYWUtYWQzMC1iZjVhZDk2N2FhN2IifQ==",
    "nonce": 5502,
    "balances": {
      "current": "12980147311768873",
      "previous": "12980147311769485"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x25f1a5d4e4ac5a3f7e51b5bdd046c6eb0fe910fa",
    "nonce": 21,
    "balances": {
      "current": "611",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:37.553Z",
  "updated": "2020-05-22T08:41:39.650Z",
  "id": "5ec79041005df800101bc969"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000263000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `611`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`