# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x99B8BEc899495102c1D47C5F9636787a71a4b45A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000007ad083ad600000000000000000000000000000000000000000000000000000007ad083ad6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000007ad083ad600000000000000000000000000000000000000000000000000000007ad083ad6692b26cb649f9403652bdbe7cab8fca2d02527f7f6ffeea50d56decbd6913b46c7af234fd1da1d5593de40337ebe7c5f2333c98dee929c5e19601fdcbb3028f0012f9657be60f5ae5b312c3e67ad893c987ca06c267e523dd56dfe608b07eab1000000000000000000000000000000000000000000000000000000000000001cae8e387636613d30b2da284ae52b1aa97ffbf9c89b303f0652defb93129bd0b55e3d1986418a48c922b011c183b6fb7b6517c107c026aa0a3496da5da9c503d650fb49f25a2092945a0aca9043a7ec6999c0b72768a98315d7ee31a93cba5223000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018b800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a0572d132c0000000000000000000000000000000000000000000000000002e1a0d21d079ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001f70c58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000998cc7b51000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a57466b4e4456694f43307a4e47557a4c5455774e7a49744f4752694f43307a4e54566a5a574579596d4d345a54596966513d3d000000000000000000000000000000000000000000000000000000000000001300000000000000000000000099b8bec899495102c1d47c5f9636787a71a4b45a00000000000000000000000000000000000000000000000000000007ad083ad6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x692b26cb649f9403652bdbe7cab8fca2d02527f7f6ffeea50d56decbd6913b46",
      "signature": {
        "s": "0x012f9657be60f5ae5b312c3e67ad893c987ca06c267e523dd56dfe608b07eab1",
        "r": "0xc7af234fd1da1d5593de40337ebe7c5f2333c98dee929c5e19601fdcbb3028f0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xae8e387636613d30b2da284ae52b1aa97ffbf9c89b303f0652defb93129bd0b5",
      "signature": {
        "s": "0x50fb49f25a2092945a0aca9043a7ec6999c0b72768a98315d7ee31a93cba5223",
        "r": "0x5e3d1986418a48c922b011c183b6fb7b6517c107c026aa0a3496da5da9c503d6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "32967768790",
    "total": "32967768790"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "32967768790",
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
            "amount": "41218243409"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "32967768"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZWFkNDViOC0zNGUzLTUwNzItOGRiOC0zNTVjZWEyYmM4ZTYifQ==",
    "nonce": 6328,
    "balances": {
      "current": "12976459632161472",
      "previous": "12976492632898030"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x99b8bec899495102c1d47c5f9636787a71a4b45a",
    "nonce": 19,
    "balances": {
      "current": "32967768790",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:15.429Z",
  "updated": "2020-05-22T08:48:15.488Z",
  "id": "5ec791cf005df800101bca7b"
}
```
* *stageAmount*: `32967768790`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000007ad083ad6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000007ad083ad600000000000000000000000000000000000000000000000000000007ad083ad6692b26cb649f9403652bdbe7cab8fca2d02527f7f6ffeea50d56decbd6913b46c7af234fd1da1d5593de40337ebe7c5f2333c98dee929c5e19601fdcbb3028f0012f9657be60f5ae5b312c3e67ad893c987ca06c267e523dd56dfe608b07eab1000000000000000000000000000000000000000000000000000000000000001cae8e387636613d30b2da284ae52b1aa97ffbf9c89b303f0652defb93129bd0b55e3d1986418a48c922b011c183b6fb7b6517c107c026aa0a3496da5da9c503d650fb49f25a2092945a0aca9043a7ec6999c0b72768a98315d7ee31a93cba5223000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018b800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a0572d132c0000000000000000000000000000000000000000000000000002e1a0d21d079ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001f70c58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000998cc7b51000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a57466b4e4456694f43307a4e47557a4c5455774e7a49744f4752694f43307a4e54566a5a574579596d4d345a54596966513d3d000000000000000000000000000000000000000000000000000000000000001300000000000000000000000099b8bec899495102c1d47c5f9636787a71a4b45a00000000000000000000000000000000000000000000000000000007ad083ad6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x692b26cb649f9403652bdbe7cab8fca2d02527f7f6ffeea50d56decbd6913b46",
      "signature": {
        "s": "0x012f9657be60f5ae5b312c3e67ad893c987ca06c267e523dd56dfe608b07eab1",
        "r": "0xc7af234fd1da1d5593de40337ebe7c5f2333c98dee929c5e19601fdcbb3028f0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xae8e387636613d30b2da284ae52b1aa97ffbf9c89b303f0652defb93129bd0b5",
      "signature": {
        "s": "0x50fb49f25a2092945a0aca9043a7ec6999c0b72768a98315d7ee31a93cba5223",
        "r": "0x5e3d1986418a48c922b011c183b6fb7b6517c107c026aa0a3496da5da9c503d6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "32967768790",
    "total": "32967768790"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "32967768790",
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
            "amount": "41218243409"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "32967768"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZWFkNDViOC0zNGUzLTUwNzItOGRiOC0zNTVjZWEyYmM4ZTYifQ==",
    "nonce": 6328,
    "balances": {
      "current": "12976459632161472",
      "previous": "12976492632898030"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x99b8bec899495102c1d47c5f9636787a71a4b45a",
    "nonce": 19,
    "balances": {
      "current": "32967768790",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:15.429Z",
  "updated": "2020-05-22T08:48:15.488Z",
  "id": "5ec791cf005df800101bca7b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000007ad083ad6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `32967768790`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`