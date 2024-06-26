# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x74c2c94916349b5707FB91fa2137De21cD318959`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002030f000000000000000000000000000000000000000000000000000000000002030f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002030f000000000000000000000000000000000000000000000000000000000002030ff747dcd79e9a199bccd3195cf3ea9b50e1314972cee0b16721776ac3555429fced3ab499fc80d2d3863a3b3a16269af55c8fe08a566920e7e59ed9165f920fe047d5b91506a504ea4b9d960c87e2bbfbe5a92739495d91f9b15bd0f0ffa638bf000000000000000000000000000000000000000000000000000000000000001b2e81d8ab9beba393b3c1f978b16d2ee1f0c3a102500d74845ef18a93719dd48373def84f4e664e6c2c22741d4f548167ebf33164c0f8374a84473db204703cbf19bf991fc7f524b88c89b12b9a35c14772b4acc1651e74e887c1ee96813f74b5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568f0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000190100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1845b74ab3cb000000000000000000000000000000000000000000000000002e1845b74cb75d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000083000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0b4dc43d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a4459784d6d4a6b4e43316d4f446b344c5455354d54497459574d794e693078595449314f5445305a5445344f57516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000074c2c94916349b5707fb91fa2137de21cd318959000000000000000000000000000000000000000000000000000000000002030f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf747dcd79e9a199bccd3195cf3ea9b50e1314972cee0b16721776ac3555429fc",
      "signature": {
        "s": "0x47d5b91506a504ea4b9d960c87e2bbfbe5a92739495d91f9b15bd0f0ffa638bf",
        "r": "0xed3ab499fc80d2d3863a3b3a16269af55c8fe08a566920e7e59ed9165f920fe0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2e81d8ab9beba393b3c1f978b16d2ee1f0c3a102500d74845ef18a93719dd483",
      "signature": {
        "s": "0x19bf991fc7f524b88c89b12b9a35c14772b4acc1651e74e887c1ee96813f74b5",
        "r": "0x73def84f4e664e6c2c22741d4f548167ebf33164c0f8374a84473db204703cbf",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "131855",
    "total": "131855"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "131855",
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
            "amount": "43139318845"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "131"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZDYxMmJkNC1mODk4LTU5MTItYWMyNi0xYTI1OTE0ZTE4OWQifQ==",
    "nonce": 6401,
    "balances": {
      "current": "12974536635626443",
      "previous": "12974536635758429"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x74c2c94916349b5707fb91fa2137de21cd318959",
    "nonce": 22,
    "balances": {
      "current": "131855",
      "previous": "0"
    }
  },
  "blockNumber": "10114703",
  "created": "2020-05-22T08:48:46.611Z",
  "updated": "2020-05-22T08:48:46.687Z",
  "id": "5ec791ee005df800101bca96"
}
```
* *stageAmount*: `131855`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002030f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002030f000000000000000000000000000000000000000000000000000000000002030ff747dcd79e9a199bccd3195cf3ea9b50e1314972cee0b16721776ac3555429fced3ab499fc80d2d3863a3b3a16269af55c8fe08a566920e7e59ed9165f920fe047d5b91506a504ea4b9d960c87e2bbfbe5a92739495d91f9b15bd0f0ffa638bf000000000000000000000000000000000000000000000000000000000000001b2e81d8ab9beba393b3c1f978b16d2ee1f0c3a102500d74845ef18a93719dd48373def84f4e664e6c2c22741d4f548167ebf33164c0f8374a84473db204703cbf19bf991fc7f524b88c89b12b9a35c14772b4acc1651e74e887c1ee96813f74b5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568f0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000190100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1845b74ab3cb000000000000000000000000000000000000000000000000002e1845b74cb75d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000083000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0b4dc43d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a4459784d6d4a6b4e43316d4f446b344c5455354d54497459574d794e693078595449314f5445305a5445344f57516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000074c2c94916349b5707fb91fa2137de21cd318959000000000000000000000000000000000000000000000000000000000002030f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf747dcd79e9a199bccd3195cf3ea9b50e1314972cee0b16721776ac3555429fc",
      "signature": {
        "s": "0x47d5b91506a504ea4b9d960c87e2bbfbe5a92739495d91f9b15bd0f0ffa638bf",
        "r": "0xed3ab499fc80d2d3863a3b3a16269af55c8fe08a566920e7e59ed9165f920fe0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2e81d8ab9beba393b3c1f978b16d2ee1f0c3a102500d74845ef18a93719dd483",
      "signature": {
        "s": "0x19bf991fc7f524b88c89b12b9a35c14772b4acc1651e74e887c1ee96813f74b5",
        "r": "0x73def84f4e664e6c2c22741d4f548167ebf33164c0f8374a84473db204703cbf",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "131855",
    "total": "131855"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "131855",
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
            "amount": "43139318845"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "131"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZDYxMmJkNC1mODk4LTU5MTItYWMyNi0xYTI1OTE0ZTE4OWQifQ==",
    "nonce": 6401,
    "balances": {
      "current": "12974536635626443",
      "previous": "12974536635758429"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x74c2c94916349b5707fb91fa2137de21cd318959",
    "nonce": 22,
    "balances": {
      "current": "131855",
      "previous": "0"
    }
  },
  "blockNumber": "10114703",
  "created": "2020-05-22T08:48:46.611Z",
  "updated": "2020-05-22T08:48:46.687Z",
  "id": "5ec791ee005df800101bca96"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000002030f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `131855`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`
