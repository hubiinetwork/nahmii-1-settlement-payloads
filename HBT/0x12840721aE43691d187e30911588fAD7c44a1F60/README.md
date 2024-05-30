# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x12840721aE43691d187e30911588fAD7c44a1F60`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000007e23fc00000000000000000000000000000000000000000000000000000000007e23fc0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000007e23fc00000000000000000000000000000000000000000000000000000000007e23fc0ed3f4a6efbabbd93b9ce90cfa889e86667398cfe4baa1afbf5324aaab5f8213ab1f9814577638cab50de14932400c8f821ffd77427e38a053d0f9c3b8864819e5b3623a1bf17617e93502d5b3a502feaeb250e98f9ec02c1e6494c6021ad9707000000000000000000000000000000000000000000000000000000000000001cc1ccbfb969bdfccb27819e0e2669d60780b795270e7e4062100df2391974b41a81d9246d05f45af34a3a592d5a1625e66de019c10c1182c7e1b101dd18185a47557a563776c65ff728b029ba9657dbca0d2fc8c521b8388e15a8bd7c8e82aaf1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000163500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1cdbf4cc020a000000000000000000000000000000000000000000000000002e1cdbfcb0467500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000204ab000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008deffa3ef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e324934596d517a4e7930775a4449774c5455325a445974596a6b795a43307a4e446732596d4e6c5a6d51794e6d456966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000012840721ae43691d187e30911588fad7c44a1f600000000000000000000000000000000000000000000000000000000007e23fc0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xed3f4a6efbabbd93b9ce90cfa889e86667398cfe4baa1afbf5324aaab5f8213a",
      "signature": {
        "s": "0x5b3623a1bf17617e93502d5b3a502feaeb250e98f9ec02c1e6494c6021ad9707",
        "r": "0xb1f9814577638cab50de14932400c8f821ffd77427e38a053d0f9c3b8864819e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc1ccbfb969bdfccb27819e0e2669d60780b795270e7e4062100df2391974b41a",
      "signature": {
        "s": "0x557a563776c65ff728b029ba9657dbca0d2fc8c521b8388e15a8bd7c8e82aaf1",
        "r": "0x81d9246d05f45af34a3a592d5a1625e66de019c10c1182c7e1b101dd18185a47",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "132267968",
    "total": "132267968"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "132267968",
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
            "amount": "38101033967"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "132267"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjN2I4YmQzNy0wZDIwLTU2ZDYtYjkyZC0zNDg2YmNlZmQyNmEifQ==",
    "nonce": 5685,
    "balances": {
      "current": "12979579959116298",
      "previous": "12979580091516533"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x12840721ae43691d187e30911588fad7c44a1f60",
    "nonce": 22,
    "balances": {
      "current": "132267968",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:43:03.258Z",
  "updated": "2020-05-22T08:43:03.351Z",
  "id": "5ec79097b0c6090011d5b02f"
}
```
* *stageAmount*: `132267968`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000007e23fc0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000007e23fc00000000000000000000000000000000000000000000000000000000007e23fc0ed3f4a6efbabbd93b9ce90cfa889e86667398cfe4baa1afbf5324aaab5f8213ab1f9814577638cab50de14932400c8f821ffd77427e38a053d0f9c3b8864819e5b3623a1bf17617e93502d5b3a502feaeb250e98f9ec02c1e6494c6021ad9707000000000000000000000000000000000000000000000000000000000000001cc1ccbfb969bdfccb27819e0e2669d60780b795270e7e4062100df2391974b41a81d9246d05f45af34a3a592d5a1625e66de019c10c1182c7e1b101dd18185a47557a563776c65ff728b029ba9657dbca0d2fc8c521b8388e15a8bd7c8e82aaf1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000163500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1cdbf4cc020a000000000000000000000000000000000000000000000000002e1cdbfcb0467500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000204ab000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008deffa3ef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e324934596d517a4e7930775a4449774c5455325a445974596a6b795a43307a4e446732596d4e6c5a6d51794e6d456966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000012840721ae43691d187e30911588fad7c44a1f600000000000000000000000000000000000000000000000000000000007e23fc0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xed3f4a6efbabbd93b9ce90cfa889e86667398cfe4baa1afbf5324aaab5f8213a",
      "signature": {
        "s": "0x5b3623a1bf17617e93502d5b3a502feaeb250e98f9ec02c1e6494c6021ad9707",
        "r": "0xb1f9814577638cab50de14932400c8f821ffd77427e38a053d0f9c3b8864819e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc1ccbfb969bdfccb27819e0e2669d60780b795270e7e4062100df2391974b41a",
      "signature": {
        "s": "0x557a563776c65ff728b029ba9657dbca0d2fc8c521b8388e15a8bd7c8e82aaf1",
        "r": "0x81d9246d05f45af34a3a592d5a1625e66de019c10c1182c7e1b101dd18185a47",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "132267968",
    "total": "132267968"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "132267968",
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
            "amount": "38101033967"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "132267"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjN2I4YmQzNy0wZDIwLTU2ZDYtYjkyZC0zNDg2YmNlZmQyNmEifQ==",
    "nonce": 5685,
    "balances": {
      "current": "12979579959116298",
      "previous": "12979580091516533"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x12840721ae43691d187e30911588fad7c44a1f60",
    "nonce": 22,
    "balances": {
      "current": "132267968",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:43:03.258Z",
  "updated": "2020-05-22T08:43:03.351Z",
  "id": "5ec79097b0c6090011d5b02f"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000007e23fc0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `132267968`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`