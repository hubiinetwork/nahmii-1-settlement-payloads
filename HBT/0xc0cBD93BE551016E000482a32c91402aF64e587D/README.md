# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc0cBD93BE551016E000482a32c91402aF64e587D`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000002834c94c000000000000000000000000000000000000000000000000000000002834c94c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002834c94c000000000000000000000000000000000000000000000000000000002834c94c1fdea2f909ac73edcf2f839d8c80bb08a87e8e253810199f1bbfefed8e634a5477ce3fdc1c325d783061558d7acad83b33ee9c33a71a6fd460a38ccb39de9fa02e97c45ea60b794c73aedac39f2323f8444a15d4499f96e0835c9b52820078df000000000000000000000000000000000000000000000000000000000000001b87abca65c61274c2779adb0999d40ca10b28c4d00ef7d6bc94b8bf7938e4149eba1cbdae25eb7b624eb27d9d69f3be044164cc71ea6e5a6e1407120509508c662fe72f38f351cd3153854d84479989396379ab15cd186239c0f10521a92463dd000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568d000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018d600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e191f6ea56cc0000000000000000000000000000000000000000000000000002e191f96e4810000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000a4af4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009d39fc51e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a44517a597a46694e433168596a426d4c54566c4d324d744f5468695953307a4e6a45354d5746684d6a4a6b5a54516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c0cbd93be551016e000482a32c91402af64e587d000000000000000000000000000000000000000000000000000000002834c94c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1fdea2f909ac73edcf2f839d8c80bb08a87e8e253810199f1bbfefed8e634a54",
      "signature": {
        "s": "0x2e97c45ea60b794c73aedac39f2323f8444a15d4499f96e0835c9b52820078df",
        "r": "0x77ce3fdc1c325d783061558d7acad83b33ee9c33a71a6fd460a38ccb39de9fa0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x87abca65c61274c2779adb0999d40ca10b28c4d00ef7d6bc94b8bf7938e4149e",
      "signature": {
        "s": "0x2fe72f38f351cd3153854d84479989396379ab15cd186239c0f10521a92463dd",
        "r": "0xba1cbdae25eb7b624eb27d9d69f3be044164cc71ea6e5a6e1407120509508c66",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "674548044",
    "total": "674548044"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "674548044",
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
            "amount": "42205168926"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "674548"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZDQzYzFiNC1hYjBmLTVlM2MtOThiYS0zNjE5MWFhMjJkZTQifQ==",
    "nonce": 6358,
    "balances": {
      "current": "12975471719705792",
      "previous": "12975472394928384"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc0cbd93be551016e000482a32c91402af64e587d",
    "nonce": 22,
    "balances": {
      "current": "674548044",
      "previous": "0"
    }
  },
  "blockNumber": "10114701",
  "created": "2020-05-22T08:48:25.431Z",
  "updated": "2020-05-22T08:48:25.494Z",
  "id": "5ec791d9e5756b00111b8795"
}
```
* *stageAmount*: `674548044`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000002834c94c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002834c94c000000000000000000000000000000000000000000000000000000002834c94c1fdea2f909ac73edcf2f839d8c80bb08a87e8e253810199f1bbfefed8e634a5477ce3fdc1c325d783061558d7acad83b33ee9c33a71a6fd460a38ccb39de9fa02e97c45ea60b794c73aedac39f2323f8444a15d4499f96e0835c9b52820078df000000000000000000000000000000000000000000000000000000000000001b87abca65c61274c2779adb0999d40ca10b28c4d00ef7d6bc94b8bf7938e4149eba1cbdae25eb7b624eb27d9d69f3be044164cc71ea6e5a6e1407120509508c662fe72f38f351cd3153854d84479989396379ab15cd186239c0f10521a92463dd000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568d000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018d600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e191f6ea56cc0000000000000000000000000000000000000000000000000002e191f96e4810000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000a4af4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009d39fc51e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a44517a597a46694e433168596a426d4c54566c4d324d744f5468695953307a4e6a45354d5746684d6a4a6b5a54516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c0cbd93be551016e000482a32c91402af64e587d000000000000000000000000000000000000000000000000000000002834c94c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1fdea2f909ac73edcf2f839d8c80bb08a87e8e253810199f1bbfefed8e634a54",
      "signature": {
        "s": "0x2e97c45ea60b794c73aedac39f2323f8444a15d4499f96e0835c9b52820078df",
        "r": "0x77ce3fdc1c325d783061558d7acad83b33ee9c33a71a6fd460a38ccb39de9fa0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x87abca65c61274c2779adb0999d40ca10b28c4d00ef7d6bc94b8bf7938e4149e",
      "signature": {
        "s": "0x2fe72f38f351cd3153854d84479989396379ab15cd186239c0f10521a92463dd",
        "r": "0xba1cbdae25eb7b624eb27d9d69f3be044164cc71ea6e5a6e1407120509508c66",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "674548044",
    "total": "674548044"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "674548044",
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
            "amount": "42205168926"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "674548"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZDQzYzFiNC1hYjBmLTVlM2MtOThiYS0zNjE5MWFhMjJkZTQifQ==",
    "nonce": 6358,
    "balances": {
      "current": "12975471719705792",
      "previous": "12975472394928384"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc0cbd93be551016e000482a32c91402af64e587d",
    "nonce": 22,
    "balances": {
      "current": "674548044",
      "previous": "0"
    }
  },
  "blockNumber": "10114701",
  "created": "2020-05-22T08:48:25.431Z",
  "updated": "2020-05-22T08:48:25.494Z",
  "id": "5ec791d9e5756b00111b8795"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000002834c94c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `674548044`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`