# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA3910b7904B0c1B2ca6997713498D040b306548C`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000009cae59f9500000000000000000000000000000000000000000000000000000009cae59f95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000009cae59f9500000000000000000000000000000000000000000000000000000009cae59f9597b25fe14f4f1e415fc162541a246441dc8e54d2cc3eac4c758f1fba1a4eb891752321faba28c1ad004f04acbb064017ee4f4a26ef54d6267ba27347d2f9364747859661080a10b9b2e792aa5c98c63c92dd7c3fa946b4e8956e8a7710987765000000000000000000000000000000000000000000000000000000000000001caa6292a5b54c4cebe3e37f4eb884837f73719149a855e9ac25e30e79a0b5cf487906496fa531e7bb35de2060158835ed3f481bf38ea028b103c6105a3bb7f03f0bfea79d771029b9480bed054e26a2baab0b86d976a8c4bab2efd58e078a4414000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bc100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e14dd26c82ebe000000000000000000000000000000000000000000000000002e14e6f42f925200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000281c3ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aea750567000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6a4d7a5a6a49324d79316b4d5745324c54566c596d5974596a56694e6930344d5755304e32513059325978596a636966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a3910b7904b0c1b2ca6997713498d040b306548c00000000000000000000000000000000000000000000000000000009cae59f95000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x97b25fe14f4f1e415fc162541a246441dc8e54d2cc3eac4c758f1fba1a4eb891",
      "signature": {
        "s": "0x47859661080a10b9b2e792aa5c98c63c92dd7c3fa946b4e8956e8a7710987765",
        "r": "0x752321faba28c1ad004f04acbb064017ee4f4a26ef54d6267ba27347d2f93647",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xaa6292a5b54c4cebe3e37f4eb884837f73719149a855e9ac25e30e79a0b5cf48",
      "signature": {
        "s": "0x0bfea79d771029b9480bed054e26a2baab0b86d976a8c4bab2efd58e078a4414",
        "r": "0x7906496fa531e7bb35de2060158835ed3f481bf38ea028b103c6105a3bb7f03f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "42058751893",
    "total": "42058751893"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "42058751893",
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
            "amount": "46883210599"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "42058751"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNjMzZjI2My1kMWE2LTVlYmYtYjViNi04MWU0N2Q0Y2YxYjcifQ==",
    "nonce": 7105,
    "balances": {
      "current": "12970788999671486",
      "previous": "12970831100482130"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa3910b7904b0c1b2ca6997713498d040b306548c",
    "nonce": 22,
    "balances": {
      "current": "42058751893",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:17.781Z",
  "updated": "2020-05-22T08:54:18.866Z",
  "id": "5ec79339e5756b00111b8879"
}
```
* *stageAmount*: `42058751893`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000009cae59f95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000009cae59f9500000000000000000000000000000000000000000000000000000009cae59f9597b25fe14f4f1e415fc162541a246441dc8e54d2cc3eac4c758f1fba1a4eb891752321faba28c1ad004f04acbb064017ee4f4a26ef54d6267ba27347d2f9364747859661080a10b9b2e792aa5c98c63c92dd7c3fa946b4e8956e8a7710987765000000000000000000000000000000000000000000000000000000000000001caa6292a5b54c4cebe3e37f4eb884837f73719149a855e9ac25e30e79a0b5cf487906496fa531e7bb35de2060158835ed3f481bf38ea028b103c6105a3bb7f03f0bfea79d771029b9480bed054e26a2baab0b86d976a8c4bab2efd58e078a4414000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bc100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e14dd26c82ebe000000000000000000000000000000000000000000000000002e14e6f42f925200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000281c3ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aea750567000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6a4d7a5a6a49324d79316b4d5745324c54566c596d5974596a56694e6930344d5755304e32513059325978596a636966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a3910b7904b0c1b2ca6997713498d040b306548c00000000000000000000000000000000000000000000000000000009cae59f95000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x97b25fe14f4f1e415fc162541a246441dc8e54d2cc3eac4c758f1fba1a4eb891",
      "signature": {
        "s": "0x47859661080a10b9b2e792aa5c98c63c92dd7c3fa946b4e8956e8a7710987765",
        "r": "0x752321faba28c1ad004f04acbb064017ee4f4a26ef54d6267ba27347d2f93647",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xaa6292a5b54c4cebe3e37f4eb884837f73719149a855e9ac25e30e79a0b5cf48",
      "signature": {
        "s": "0x0bfea79d771029b9480bed054e26a2baab0b86d976a8c4bab2efd58e078a4414",
        "r": "0x7906496fa531e7bb35de2060158835ed3f481bf38ea028b103c6105a3bb7f03f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "42058751893",
    "total": "42058751893"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "42058751893",
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
            "amount": "46883210599"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "42058751"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNjMzZjI2My1kMWE2LTVlYmYtYjViNi04MWU0N2Q0Y2YxYjcifQ==",
    "nonce": 7105,
    "balances": {
      "current": "12970788999671486",
      "previous": "12970831100482130"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa3910b7904b0c1b2ca6997713498d040b306548c",
    "nonce": 22,
    "balances": {
      "current": "42058751893",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:17.781Z",
  "updated": "2020-05-22T08:54:18.866Z",
  "id": "5ec79339e5756b00111b8879"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000009cae59f95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `42058751893`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`