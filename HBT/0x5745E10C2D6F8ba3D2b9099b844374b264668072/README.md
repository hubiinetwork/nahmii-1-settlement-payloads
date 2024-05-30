# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5745E10C2D6F8ba3D2b9099b844374b264668072`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001b975909000000000000000000000000000000000000000000000000000000001b975909000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001b975909000000000000000000000000000000000000000000000000000000001b975909b48c3da109fdbc1e496a78c714ca66fa746a56cbae3cb6a8c7386564b92181a9dfc1753ef7ffba90cd909bb3883e9ad3869f2d40df58fb7da63df859bbbac837183ffd51531fdef2c3df316ed2d9fceb1042c7940f7d545cf5ccfa55096e9eca000000000000000000000000000000000000000000000000000000000000001cf0bb85d177df6f13c27cdece6e44580a60eaef4ff1a12daa9592c3568416c2468ac827dd0987d92a7ba19e72eb10033e95c79c972c7af1381532f972e0b3e5e240e50faadacc1bc41175ed789d8cc3292b1785c8d2a535abeb6ccdb8ad42f067000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001cf100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12e7676c9af8000000000000000000000000000000000000000000000000002e12e7830b043800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000071037000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b6ac6b15c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e32457a4f5463304f53316b4e7a49314c54566d595749744f4449324d6930324d4449304d324d354e6a41785a6a4d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005745e10c2d6f8ba3d2b9099b844374b264668072000000000000000000000000000000000000000000000000000000001b975909000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb48c3da109fdbc1e496a78c714ca66fa746a56cbae3cb6a8c7386564b92181a9",
      "signature": {
        "s": "0x183ffd51531fdef2c3df316ed2d9fceb1042c7940f7d545cf5ccfa55096e9eca",
        "r": "0xdfc1753ef7ffba90cd909bb3883e9ad3869f2d40df58fb7da63df859bbbac837",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf0bb85d177df6f13c27cdece6e44580a60eaef4ff1a12daa9592c3568416c246",
      "signature": {
        "s": "0x40e50faadacc1bc41175ed789d8cc3292b1785c8d2a535abeb6ccdb8ad42f067",
        "r": "0x8ac827dd0987d92a7ba19e72eb10033e95c79c972c7af1381532f972e0b3e5e2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "462903561",
    "total": "462903561"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "462903561",
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
            "amount": "49036046684"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "462903"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmN2EzOTc0OS1kNzI1LTVmYWItODI2Mi02MDI0M2M5NjAxZjMifQ==",
    "nonce": 7409,
    "balances": {
      "current": "12968634010606328",
      "previous": "12968634473972792"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5745e10c2d6f8ba3d2b9099b844374b264668072",
    "nonce": 22,
    "balances": {
      "current": "462903561",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:37.584Z",
  "updated": "2020-05-22T08:56:37.666Z",
  "id": "5ec793c5b0c6090011d5b279"
}
```
* *stageAmount*: `462903561`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001b975909000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001b975909000000000000000000000000000000000000000000000000000000001b975909b48c3da109fdbc1e496a78c714ca66fa746a56cbae3cb6a8c7386564b92181a9dfc1753ef7ffba90cd909bb3883e9ad3869f2d40df58fb7da63df859bbbac837183ffd51531fdef2c3df316ed2d9fceb1042c7940f7d545cf5ccfa55096e9eca000000000000000000000000000000000000000000000000000000000000001cf0bb85d177df6f13c27cdece6e44580a60eaef4ff1a12daa9592c3568416c2468ac827dd0987d92a7ba19e72eb10033e95c79c972c7af1381532f972e0b3e5e240e50faadacc1bc41175ed789d8cc3292b1785c8d2a535abeb6ccdb8ad42f067000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001cf100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12e7676c9af8000000000000000000000000000000000000000000000000002e12e7830b043800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000071037000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b6ac6b15c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e32457a4f5463304f53316b4e7a49314c54566d595749744f4449324d6930324d4449304d324d354e6a41785a6a4d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005745e10c2d6f8ba3d2b9099b844374b264668072000000000000000000000000000000000000000000000000000000001b975909000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb48c3da109fdbc1e496a78c714ca66fa746a56cbae3cb6a8c7386564b92181a9",
      "signature": {
        "s": "0x183ffd51531fdef2c3df316ed2d9fceb1042c7940f7d545cf5ccfa55096e9eca",
        "r": "0xdfc1753ef7ffba90cd909bb3883e9ad3869f2d40df58fb7da63df859bbbac837",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf0bb85d177df6f13c27cdece6e44580a60eaef4ff1a12daa9592c3568416c246",
      "signature": {
        "s": "0x40e50faadacc1bc41175ed789d8cc3292b1785c8d2a535abeb6ccdb8ad42f067",
        "r": "0x8ac827dd0987d92a7ba19e72eb10033e95c79c972c7af1381532f972e0b3e5e2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "462903561",
    "total": "462903561"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "462903561",
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
            "amount": "49036046684"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "462903"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmN2EzOTc0OS1kNzI1LTVmYWItODI2Mi02MDI0M2M5NjAxZjMifQ==",
    "nonce": 7409,
    "balances": {
      "current": "12968634010606328",
      "previous": "12968634473972792"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5745e10c2d6f8ba3d2b9099b844374b264668072",
    "nonce": 22,
    "balances": {
      "current": "462903561",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:37.584Z",
  "updated": "2020-05-22T08:56:37.666Z",
  "id": "5ec793c5b0c6090011d5b279"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000001b975909000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `462903561`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`