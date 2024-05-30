# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x066D0A78D429228B54Da7A143cD86303b3C53d4F`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000018d5611d0000000000000000000000000000000000000000000000000000000018d5611d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000018d5611d0000000000000000000000000000000000000000000000000000000018d5611de0644f49d2546c20da31896c75230c06627273b09f1e8d3044882528a8f8fde1b434014d49252c05e9a84bc3cfc88da357276c4bff3dda4bd0bd9783c0bbb102432eb748bebcee8e5569d6e71e9e8c66811047b76f473ac99e95d4ad4802cff8000000000000000000000000000000000000000000000000000000000000001c5114b23c2bbc5124b1bc60dc4b7d4ad6498e0ff7f5ef1b71d074e99ba0e1ed9777c4974ba407d572a466fccf0367a6658bfdcffa790a700868558b69962dae517988d154c2da1cd3e120e82155cf4842b4958c32f8011207e777a870f47e111c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017c500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b116f9eb685000000000000000000000000000000000000000000000000002e1b11887a731f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000065b7d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009544332f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5954413159544a6a4e433032595759784c545535597a5974596a686b4e4330325a4459334e546869595751355932556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000066d0a78d429228b54da7a143cd86303b3c53d4f0000000000000000000000000000000000000000000000000000000018d5611d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe0644f49d2546c20da31896c75230c06627273b09f1e8d3044882528a8f8fde1",
      "signature": {
        "s": "0x432eb748bebcee8e5569d6e71e9e8c66811047b76f473ac99e95d4ad4802cff8",
        "r": "0xb434014d49252c05e9a84bc3cfc88da357276c4bff3dda4bd0bd9783c0bbb102",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5114b23c2bbc5124b1bc60dc4b7d4ad6498e0ff7f5ef1b71d074e99ba0e1ed97",
      "signature": {
        "s": "0x7988d154c2da1cd3e120e82155cf4842b4958c32f8011207e777a870f47e111c",
        "r": "0x77c4974ba407d572a466fccf0367a6658bfdcffa790a700868558b69962dae51",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "416637213",
    "total": "416637213"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "416637213",
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
            "amount": "40068395767"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "416637"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkYTA1YTJjNC02YWYxLTU5YzYtYjhkNC02ZDY3NThiYWQ5Y2UifQ==",
    "nonce": 6085,
    "balances": {
      "current": "12977610629756549",
      "previous": "12977611046810399"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x066d0a78d429228b54da7a143cd86303b3c53d4f",
    "nonce": 22,
    "balances": {
      "current": "416637213",
      "previous": "0"
    }
  },
  "blockNumber": "10114687",
  "created": "2020-05-22T08:46:18.941Z",
  "updated": "2020-05-22T08:46:19.009Z",
  "id": "5ec7915ae5756b00111b873b"
}
```
* *stageAmount*: `416637213`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000018d5611d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000018d5611d0000000000000000000000000000000000000000000000000000000018d5611de0644f49d2546c20da31896c75230c06627273b09f1e8d3044882528a8f8fde1b434014d49252c05e9a84bc3cfc88da357276c4bff3dda4bd0bd9783c0bbb102432eb748bebcee8e5569d6e71e9e8c66811047b76f473ac99e95d4ad4802cff8000000000000000000000000000000000000000000000000000000000000001c5114b23c2bbc5124b1bc60dc4b7d4ad6498e0ff7f5ef1b71d074e99ba0e1ed9777c4974ba407d572a466fccf0367a6658bfdcffa790a700868558b69962dae517988d154c2da1cd3e120e82155cf4842b4958c32f8011207e777a870f47e111c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017c500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b116f9eb685000000000000000000000000000000000000000000000000002e1b11887a731f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000065b7d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009544332f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5954413159544a6a4e433032595759784c545535597a5974596a686b4e4330325a4459334e546869595751355932556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000066d0a78d429228b54da7a143cd86303b3c53d4f0000000000000000000000000000000000000000000000000000000018d5611d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe0644f49d2546c20da31896c75230c06627273b09f1e8d3044882528a8f8fde1",
      "signature": {
        "s": "0x432eb748bebcee8e5569d6e71e9e8c66811047b76f473ac99e95d4ad4802cff8",
        "r": "0xb434014d49252c05e9a84bc3cfc88da357276c4bff3dda4bd0bd9783c0bbb102",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5114b23c2bbc5124b1bc60dc4b7d4ad6498e0ff7f5ef1b71d074e99ba0e1ed97",
      "signature": {
        "s": "0x7988d154c2da1cd3e120e82155cf4842b4958c32f8011207e777a870f47e111c",
        "r": "0x77c4974ba407d572a466fccf0367a6658bfdcffa790a700868558b69962dae51",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "416637213",
    "total": "416637213"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "416637213",
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
            "amount": "40068395767"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "416637"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkYTA1YTJjNC02YWYxLTU5YzYtYjhkNC02ZDY3NThiYWQ5Y2UifQ==",
    "nonce": 6085,
    "balances": {
      "current": "12977610629756549",
      "previous": "12977611046810399"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x066d0a78d429228b54da7a143cd86303b3c53d4f",
    "nonce": 22,
    "balances": {
      "current": "416637213",
      "previous": "0"
    }
  },
  "blockNumber": "10114687",
  "created": "2020-05-22T08:46:18.941Z",
  "updated": "2020-05-22T08:46:19.009Z",
  "id": "5ec7915ae5756b00111b873b"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000018d5611d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `416637213`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`