# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFa68Bc1AA95e339e44F1c298e42EcF5e6276d49f`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000a8e97d7000000000000000000000000000000000000000000000000000000000a8e97d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000a8e97d7000000000000000000000000000000000000000000000000000000000a8e97d7040365adb2388609416abfa7c578223a1683a549b194c9b2cb0e73929f4028bf5d8d8751235310cd1ba9090cb2cfa8f6a228aa10cc64ea694b0105060429d77c15d246947f8f439ca3a81203da43dd7990d5b4044ae2d3b97a085f0d21f587e4000000000000000000000000000000000000000000000000000000000000001b91601f2cba41683a41d136e8b29a0ce0db4a7612ffe3c5ce889f31790d242595ac23f99cb64167d4d57ca75beb0ab3b0271b0d45e669c72b7964d8064edf6e7052f054b681c6aeea564d4c3994bd6c9fa43e0fcbe1ec1650cafa1122bb86c39d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019f300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e172aa9d40315000000000000000000000000000000000000000000000000002e172ab4654ec900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002b3dd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a53b15e38000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f546b314f4451314e69316c4e4467794c545577596a6b74596a63774d6930345a5464684d4749324e6d597959574d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fa68bc1aa95e339e44f1c298e42ecf5e6276d49f000000000000000000000000000000000000000000000000000000000a8e97d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x040365adb2388609416abfa7c578223a1683a549b194c9b2cb0e73929f4028bf",
      "signature": {
        "s": "0x15d246947f8f439ca3a81203da43dd7990d5b4044ae2d3b97a085f0d21f587e4",
        "r": "0x5d8d8751235310cd1ba9090cb2cfa8f6a228aa10cc64ea694b0105060429d77c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x91601f2cba41683a41d136e8b29a0ce0db4a7612ffe3c5ce889f31790d242595",
      "signature": {
        "s": "0x52f054b681c6aeea564d4c3994bd6c9fa43e0fcbe1ec1650cafa1122bb86c39d",
        "r": "0xac23f99cb64167d4d57ca75beb0ab3b0271b0d45e669c72b7964d8064edf6e70",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "177117143",
    "total": "177117143"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "177117143",
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
            "amount": "44353805880"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "177117"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0OTk1ODQ1Ni1lNDgyLTUwYjktYjcwMi04ZTdhMGI2NmYyYWMifQ==",
    "nonce": 6643,
    "balances": {
      "current": "12973320933999381",
      "previous": "12973321111293641"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfa68bc1aa95e339e44f1c298e42ecf5e6276d49f",
    "nonce": 22,
    "balances": {
      "current": "177117143",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:45.668Z",
  "updated": "2020-05-22T08:50:46.735Z",
  "id": "5ec79265b0c6090011d5b16f"
}
```
* *stageAmount*: `177117143`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000a8e97d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000a8e97d7000000000000000000000000000000000000000000000000000000000a8e97d7040365adb2388609416abfa7c578223a1683a549b194c9b2cb0e73929f4028bf5d8d8751235310cd1ba9090cb2cfa8f6a228aa10cc64ea694b0105060429d77c15d246947f8f439ca3a81203da43dd7990d5b4044ae2d3b97a085f0d21f587e4000000000000000000000000000000000000000000000000000000000000001b91601f2cba41683a41d136e8b29a0ce0db4a7612ffe3c5ce889f31790d242595ac23f99cb64167d4d57ca75beb0ab3b0271b0d45e669c72b7964d8064edf6e7052f054b681c6aeea564d4c3994bd6c9fa43e0fcbe1ec1650cafa1122bb86c39d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019f300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e172aa9d40315000000000000000000000000000000000000000000000000002e172ab4654ec900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002b3dd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a53b15e38000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f546b314f4451314e69316c4e4467794c545577596a6b74596a63774d6930345a5464684d4749324e6d597959574d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fa68bc1aa95e339e44f1c298e42ecf5e6276d49f000000000000000000000000000000000000000000000000000000000a8e97d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x040365adb2388609416abfa7c578223a1683a549b194c9b2cb0e73929f4028bf",
      "signature": {
        "s": "0x15d246947f8f439ca3a81203da43dd7990d5b4044ae2d3b97a085f0d21f587e4",
        "r": "0x5d8d8751235310cd1ba9090cb2cfa8f6a228aa10cc64ea694b0105060429d77c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x91601f2cba41683a41d136e8b29a0ce0db4a7612ffe3c5ce889f31790d242595",
      "signature": {
        "s": "0x52f054b681c6aeea564d4c3994bd6c9fa43e0fcbe1ec1650cafa1122bb86c39d",
        "r": "0xac23f99cb64167d4d57ca75beb0ab3b0271b0d45e669c72b7964d8064edf6e70",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "177117143",
    "total": "177117143"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "177117143",
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
            "amount": "44353805880"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "177117"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0OTk1ODQ1Ni1lNDgyLTUwYjktYjcwMi04ZTdhMGI2NmYyYWMifQ==",
    "nonce": 6643,
    "balances": {
      "current": "12973320933999381",
      "previous": "12973321111293641"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfa68bc1aa95e339e44f1c298e42ecf5e6276d49f",
    "nonce": 22,
    "balances": {
      "current": "177117143",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:45.668Z",
  "updated": "2020-05-22T08:50:46.735Z",
  "id": "5ec79265b0c6090011d5b16f"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000a8e97d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `177117143`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`