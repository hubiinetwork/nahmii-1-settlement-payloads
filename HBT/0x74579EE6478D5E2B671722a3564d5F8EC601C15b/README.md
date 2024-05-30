# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x74579EE6478D5E2B671722a3564d5F8EC601C15b`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000249552a800000000000000000000000000000000000000000000000000000000249552a8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000249552a800000000000000000000000000000000000000000000000000000000249552a89fa7129d947b5682bdf776ea89a05519fe453a025ca5ea801aa73a5698e98f72c7690ea5118d270df9da888ea1cb2efe0acbe89551cc473d85326de01014f4041118a62de689989a8492dd73cab472583675659c4d057c21c351f79e58d47ea5000000000000000000000000000000000000000000000000000000000000001c2e4cbfab5bf347628162b92f7cb923fffabda5b0e59bc91d7538592099918f71c28201fc83ce98d242c738eae84d68eb064603f8e4dd8ffaf1595f9fd4cd46053d7d3746204a506e2cbcea217b030a7f4b40ea7cb5f865779846cac7f0e00528000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a0e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1720300638a8000000000000000000000000000000000000000000000000002e172054a4e8d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000095d85000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a565f394b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6d5a684f444e6c5a69316a59546b344c5455324d544174596a457a4d79307a4d7a45355a4445774f546b334f47456966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000074579ee6478d5e2b671722a3564d5f8ec601c15b00000000000000000000000000000000000000000000000000000000249552a8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9fa7129d947b5682bdf776ea89a05519fe453a025ca5ea801aa73a5698e98f72",
      "signature": {
        "s": "0x1118a62de689989a8492dd73cab472583675659c4d057c21c351f79e58d47ea5",
        "r": "0xc7690ea5118d270df9da888ea1cb2efe0acbe89551cc473d85326de01014f404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2e4cbfab5bf347628162b92f7cb923fffabda5b0e59bc91d7538592099918f71",
      "signature": {
        "s": "0x3d7d3746204a506e2cbcea217b030a7f4b40ea7cb5f865779846cac7f0e00528",
        "r": "0xc28201fc83ce98d242c738eae84d68eb064603f8e4dd8ffaf1595f9fd4cd4605",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "613765800",
    "total": "613765800"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "613765800",
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
            "amount": "44398754123"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "613765"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MmZhODNlZi1jYTk4LTU2MTAtYjEzMy0zMzE5ZDEwOTk3OGEifQ==",
    "nonce": 6670,
    "balances": {
      "current": "12973275940796584",
      "previous": "12973276555176149"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x74579ee6478d5e2b671722a3564d5f8ec601c15b",
    "nonce": 22,
    "balances": {
      "current": "613765800",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:50:54.058Z",
  "updated": "2020-05-22T08:50:54.126Z",
  "id": "5ec7926e005df800101bcaf5"
}
```
* *stageAmount*: `613765800`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000249552a8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000249552a800000000000000000000000000000000000000000000000000000000249552a89fa7129d947b5682bdf776ea89a05519fe453a025ca5ea801aa73a5698e98f72c7690ea5118d270df9da888ea1cb2efe0acbe89551cc473d85326de01014f4041118a62de689989a8492dd73cab472583675659c4d057c21c351f79e58d47ea5000000000000000000000000000000000000000000000000000000000000001c2e4cbfab5bf347628162b92f7cb923fffabda5b0e59bc91d7538592099918f71c28201fc83ce98d242c738eae84d68eb064603f8e4dd8ffaf1595f9fd4cd46053d7d3746204a506e2cbcea217b030a7f4b40ea7cb5f865779846cac7f0e00528000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a0e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1720300638a8000000000000000000000000000000000000000000000000002e172054a4e8d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000095d85000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a565f394b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6d5a684f444e6c5a69316a59546b344c5455324d544174596a457a4d79307a4d7a45355a4445774f546b334f47456966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000074579ee6478d5e2b671722a3564d5f8ec601c15b00000000000000000000000000000000000000000000000000000000249552a8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9fa7129d947b5682bdf776ea89a05519fe453a025ca5ea801aa73a5698e98f72",
      "signature": {
        "s": "0x1118a62de689989a8492dd73cab472583675659c4d057c21c351f79e58d47ea5",
        "r": "0xc7690ea5118d270df9da888ea1cb2efe0acbe89551cc473d85326de01014f404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2e4cbfab5bf347628162b92f7cb923fffabda5b0e59bc91d7538592099918f71",
      "signature": {
        "s": "0x3d7d3746204a506e2cbcea217b030a7f4b40ea7cb5f865779846cac7f0e00528",
        "r": "0xc28201fc83ce98d242c738eae84d68eb064603f8e4dd8ffaf1595f9fd4cd4605",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "613765800",
    "total": "613765800"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "613765800",
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
            "amount": "44398754123"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "613765"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MmZhODNlZi1jYTk4LTU2MTAtYjEzMy0zMzE5ZDEwOTk3OGEifQ==",
    "nonce": 6670,
    "balances": {
      "current": "12973275940796584",
      "previous": "12973276555176149"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x74579ee6478d5e2b671722a3564d5f8ec601c15b",
    "nonce": 22,
    "balances": {
      "current": "613765800",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:50:54.058Z",
  "updated": "2020-05-22T08:50:54.126Z",
  "id": "5ec7926e005df800101bcaf5"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000249552a8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `613765800`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`