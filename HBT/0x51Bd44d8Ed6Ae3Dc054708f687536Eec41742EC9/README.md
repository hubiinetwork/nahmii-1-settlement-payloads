# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x51Bd44d8Ed6Ae3Dc054708f687536Eec41742EC9`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000000000000000000000000000000000000000000f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000000000000000000000000000000000000000000f03213559dcb5e7614434dbfd06624a3c32cca0aacc73a5c6e89ac81d2b73c4d2302babf41ac28b710a4ae900244753ee02b9a61e56195a48e9ebf1441edb17e412253957a3d9568ec2c0c1b8282fd7b25499a42726ce5e889e9976cbd82c09474000000000000000000000000000000000000000000000000000000000000001c00228b52e0eb9e1cee3ab550c4850bd44a702a763b41b4aaf24349f3709af77416edb12f757674c42e8113db45fd2aa1dca05ff951c5c4f2bd81556a3b6db4fe039e1526be06d4b4fb52df9877be80bdf411b00a9f88555a3e5c769b6d46515d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000162300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ceb9e87f1c4000000000000000000000000000000000000000000000000002e1ceb9e87f2b500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008dafe2c89000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f5751344d7a4d314d793078597a51354c54566b4d475974596d4a6b4d693077597a59794e6a67794d5451314f47556966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000051bd44d8ed6ae3dc054708f687536eec41742ec900000000000000000000000000000000000000000000000000000000000000f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3213559dcb5e7614434dbfd06624a3c32cca0aacc73a5c6e89ac81d2b73c4d23",
      "signature": {
        "s": "0x2253957a3d9568ec2c0c1b8282fd7b25499a42726ce5e889e9976cbd82c09474",
        "r": "0x02babf41ac28b710a4ae900244753ee02b9a61e56195a48e9ebf1441edb17e41",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x00228b52e0eb9e1cee3ab550c4850bd44a702a763b41b4aaf24349f3709af774",
      "signature": {
        "s": "0x039e1526be06d4b4fb52df9877be80bdf411b00a9f88555a3e5c769b6d46515d",
        "r": "0x16edb12f757674c42e8113db45fd2aa1dca05ff951c5c4f2bd81556a3b6db4fe",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "240",
    "total": "240"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "240",
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
            "amount": "38033829001"
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
    "data": "eyJyZWYiOiI0OWQ4MzM1My0xYzQ5LTVkMGYtYmJkMi0wYzYyNjgyMTQ1OGUifQ==",
    "nonce": 5667,
    "balances": {
      "current": "12979647231291844",
      "previous": "12979647231292085"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x51bd44d8ed6ae3dc054708f687536eec41742ec9",
    "nonce": 21,
    "balances": {
      "current": "240",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:42:57.808Z",
  "updated": "2020-05-22T08:42:57.870Z",
  "id": "5ec79091b0c6090011d5b029"
}
```
* *stageAmount*: `240`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000000000000000000000000000000000000000000f03213559dcb5e7614434dbfd06624a3c32cca0aacc73a5c6e89ac81d2b73c4d2302babf41ac28b710a4ae900244753ee02b9a61e56195a48e9ebf1441edb17e412253957a3d9568ec2c0c1b8282fd7b25499a42726ce5e889e9976cbd82c09474000000000000000000000000000000000000000000000000000000000000001c00228b52e0eb9e1cee3ab550c4850bd44a702a763b41b4aaf24349f3709af77416edb12f757674c42e8113db45fd2aa1dca05ff951c5c4f2bd81556a3b6db4fe039e1526be06d4b4fb52df9877be80bdf411b00a9f88555a3e5c769b6d46515d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000162300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ceb9e87f1c4000000000000000000000000000000000000000000000000002e1ceb9e87f2b500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008dafe2c89000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f5751344d7a4d314d793078597a51354c54566b4d475974596d4a6b4d693077597a59794e6a67794d5451314f47556966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000051bd44d8ed6ae3dc054708f687536eec41742ec900000000000000000000000000000000000000000000000000000000000000f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3213559dcb5e7614434dbfd06624a3c32cca0aacc73a5c6e89ac81d2b73c4d23",
      "signature": {
        "s": "0x2253957a3d9568ec2c0c1b8282fd7b25499a42726ce5e889e9976cbd82c09474",
        "r": "0x02babf41ac28b710a4ae900244753ee02b9a61e56195a48e9ebf1441edb17e41",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x00228b52e0eb9e1cee3ab550c4850bd44a702a763b41b4aaf24349f3709af774",
      "signature": {
        "s": "0x039e1526be06d4b4fb52df9877be80bdf411b00a9f88555a3e5c769b6d46515d",
        "r": "0x16edb12f757674c42e8113db45fd2aa1dca05ff951c5c4f2bd81556a3b6db4fe",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "240",
    "total": "240"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "240",
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
            "amount": "38033829001"
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
    "data": "eyJyZWYiOiI0OWQ4MzM1My0xYzQ5LTVkMGYtYmJkMi0wYzYyNjgyMTQ1OGUifQ==",
    "nonce": 5667,
    "balances": {
      "current": "12979647231291844",
      "previous": "12979647231292085"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x51bd44d8ed6ae3dc054708f687536eec41742ec9",
    "nonce": 21,
    "balances": {
      "current": "240",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:42:57.808Z",
  "updated": "2020-05-22T08:42:57.870Z",
  "id": "5ec79091b0c6090011d5b029"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `240`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`