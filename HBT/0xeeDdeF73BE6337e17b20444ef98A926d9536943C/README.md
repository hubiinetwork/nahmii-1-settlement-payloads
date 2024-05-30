# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xeeDdeF73BE6337e17b20444ef98A926d9536943C`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000013c15b6c8000000000000000000000000000000000000000000000000000000013c15b6c8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000013c15b6c8000000000000000000000000000000000000000000000000000000013c15b6c8a97ed5a718db23d40ca78e51de4a4a8f2c988c7be854cba3805017efe2f1b699be2f027969ef85bd3785a3177bd973cddb7d72685e08add82dda391ef925f4d853c8a154df8c7356bab14f9a6433b07db05e363c00155d2ee94cbdc444c05457000000000000000000000000000000000000000000000000000000000000001b2d7ae05c8d34e183fb24a7326a39c50944a456491edbf6506f95da8df4519545898fa418ad63eb37dc79cbbbdd991a7a1c9c5a994e648eb5462b20eaabd7d3e529f1735ec7de8a5ccd1e4d712f99b174919c3dec2c5bf1951056fe1ff8c9bab0000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b6800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15844c3f68c8000000000000000000000000000000000000000000000000002e158588a60a7f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000050eaef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000abfb5dc98000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a444d355a444a6d595330324f5441354c5455774e6a4d744f44566b596930794f574e684e474d354d47466a4d7a636966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000eeddef73be6337e17b20444ef98a926d9536943c000000000000000000000000000000000000000000000000000000013c15b6c8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa97ed5a718db23d40ca78e51de4a4a8f2c988c7be854cba3805017efe2f1b699",
      "signature": {
        "s": "0x53c8a154df8c7356bab14f9a6433b07db05e363c00155d2ee94cbdc444c05457",
        "r": "0xbe2f027969ef85bd3785a3177bd973cddb7d72685e08add82dda391ef925f4d8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2d7ae05c8d34e183fb24a7326a39c50944a456491edbf6506f95da8df4519545",
      "signature": {
        "s": "0x29f1735ec7de8a5ccd1e4d712f99b174919c3dec2c5bf1951056fe1ff8c9bab0",
        "r": "0x898fa418ad63eb37dc79cbbbdd991a7a1c9c5a994e648eb5462b20eaabd7d3e5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5303023304",
    "total": "5303023304"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5303023304",
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
            "amount": "46166039704"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5303023"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZDM5ZDJmYS02OTA5LTUwNjMtODVkYi0yOWNhNGM5MGFjMzcifQ==",
    "nonce": 7016,
    "balances": {
      "current": "12971506887780552",
      "previous": "12971512196106879"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeeddef73be6337e17b20444ef98a926d9536943c",
    "nonce": 13,
    "balances": {
      "current": "5303023304",
      "previous": "0"
    }
  },
  "blockNumber": "10114726",
  "created": "2020-05-22T08:53:27.584Z",
  "updated": "2020-05-22T08:53:27.643Z",
  "id": "5ec79307005df800101bcb63"
}
```
* *stageAmount*: `5303023304`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000013c15b6c8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000013c15b6c8000000000000000000000000000000000000000000000000000000013c15b6c8a97ed5a718db23d40ca78e51de4a4a8f2c988c7be854cba3805017efe2f1b699be2f027969ef85bd3785a3177bd973cddb7d72685e08add82dda391ef925f4d853c8a154df8c7356bab14f9a6433b07db05e363c00155d2ee94cbdc444c05457000000000000000000000000000000000000000000000000000000000000001b2d7ae05c8d34e183fb24a7326a39c50944a456491edbf6506f95da8df4519545898fa418ad63eb37dc79cbbbdd991a7a1c9c5a994e648eb5462b20eaabd7d3e529f1735ec7de8a5ccd1e4d712f99b174919c3dec2c5bf1951056fe1ff8c9bab0000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b6800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15844c3f68c8000000000000000000000000000000000000000000000000002e158588a60a7f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000050eaef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000abfb5dc98000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a444d355a444a6d595330324f5441354c5455774e6a4d744f44566b596930794f574e684e474d354d47466a4d7a636966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000eeddef73be6337e17b20444ef98a926d9536943c000000000000000000000000000000000000000000000000000000013c15b6c8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa97ed5a718db23d40ca78e51de4a4a8f2c988c7be854cba3805017efe2f1b699",
      "signature": {
        "s": "0x53c8a154df8c7356bab14f9a6433b07db05e363c00155d2ee94cbdc444c05457",
        "r": "0xbe2f027969ef85bd3785a3177bd973cddb7d72685e08add82dda391ef925f4d8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2d7ae05c8d34e183fb24a7326a39c50944a456491edbf6506f95da8df4519545",
      "signature": {
        "s": "0x29f1735ec7de8a5ccd1e4d712f99b174919c3dec2c5bf1951056fe1ff8c9bab0",
        "r": "0x898fa418ad63eb37dc79cbbbdd991a7a1c9c5a994e648eb5462b20eaabd7d3e5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5303023304",
    "total": "5303023304"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5303023304",
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
            "amount": "46166039704"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5303023"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZDM5ZDJmYS02OTA5LTUwNjMtODVkYi0yOWNhNGM5MGFjMzcifQ==",
    "nonce": 7016,
    "balances": {
      "current": "12971506887780552",
      "previous": "12971512196106879"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeeddef73be6337e17b20444ef98a926d9536943c",
    "nonce": 13,
    "balances": {
      "current": "5303023304",
      "previous": "0"
    }
  },
  "blockNumber": "10114726",
  "created": "2020-05-22T08:53:27.584Z",
  "updated": "2020-05-22T08:53:27.643Z",
  "id": "5ec79307005df800101bcb63"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000013c15b6c8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5303023304`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`