# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xda5900d2ED980f59171571427158dd0238552b4e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000011d940000000000000000000000000000000000000000000000000000000000011d9400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000011d940000000000000000000000000000000000000000000000000000000000011d942a96ba7b55bf3a4bf9ae3fd49fc2816e9034131d7d2915007c45aff370f1b5eff2cb295e50de6d68da8824c5623ea3e8c1c9215b6114111d4a6f01339b88ae97328be5c5c3a2d9ae93302b336962db6b54627869e1364fc72a1024f869acaeda000000000000000000000000000000000000000000000000000000000000001b4de2942ba393248a8cc0a3a9d6ec82c2edf2d5b506319cd95f564b3458d0f30dc57054a8c358c0e0c48f68b2f12a8b4fc011357afee7cda859c8a67baeace2166d0ed552d2815bc15ac630e353c94b315e441385aa9ffbba7f774a6a8c746ad3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007bf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3bc7d96000000000000000000000000000000000000000000000000002386f2c3bd9b7300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000490000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4a1800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d4451304d4455325a4330774d4759344c5455314f4467744f4449794e4330335a6a4a6c4d6a63324f4759324d6a596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da5900d2ed980f59171571427158dd0238552b4e0000000000000000000000000000000000000000000000000000000000011d94000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2a96ba7b55bf3a4bf9ae3fd49fc2816e9034131d7d2915007c45aff370f1b5ef",
      "signature": {
        "s": "0x328be5c5c3a2d9ae93302b336962db6b54627869e1364fc72a1024f869acaeda",
        "r": "0xf2cb295e50de6d68da8824c5623ea3e8c1c9215b6114111d4a6f01339b88ae97",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4de2942ba393248a8cc0a3a9d6ec82c2edf2d5b506319cd95f564b3458d0f30d",
      "signature": {
        "s": "0x6d0ed552d2815bc15ac630e353c94b315e441385aa9ffbba7f774a6a8c746ad3",
        "r": "0xc57054a8c358c0e0c48f68b2f12a8b4fc011357afee7cda859c8a67baeace216",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "73108",
    "total": "73108"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "73108",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "674328"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "73"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMDQ0MDU2ZC0wMGY4LTU1ODgtODIyNC03ZjJlMjc2OGY2MjYifQ==",
    "nonce": 1983,
    "balances": {
      "current": "10000001408990614",
      "previous": "10000001409063795"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda5900d2ed980f59171571427158dd0238552b4e",
    "nonce": 20,
    "balances": {
      "current": "73108",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:33.727Z",
  "updated": "2020-05-22T08:13:33.792Z",
  "id": "5ec789adb0c6090011d5ab65"
}
```
* *stageAmount*: `73108`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000011d9400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000011d940000000000000000000000000000000000000000000000000000000000011d942a96ba7b55bf3a4bf9ae3fd49fc2816e9034131d7d2915007c45aff370f1b5eff2cb295e50de6d68da8824c5623ea3e8c1c9215b6114111d4a6f01339b88ae97328be5c5c3a2d9ae93302b336962db6b54627869e1364fc72a1024f869acaeda000000000000000000000000000000000000000000000000000000000000001b4de2942ba393248a8cc0a3a9d6ec82c2edf2d5b506319cd95f564b3458d0f30dc57054a8c358c0e0c48f68b2f12a8b4fc011357afee7cda859c8a67baeace2166d0ed552d2815bc15ac630e353c94b315e441385aa9ffbba7f774a6a8c746ad3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007bf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3bc7d96000000000000000000000000000000000000000000000000002386f2c3bd9b7300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000490000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4a1800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d4451304d4455325a4330774d4759344c5455314f4467744f4449794e4330335a6a4a6c4d6a63324f4759324d6a596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da5900d2ed980f59171571427158dd0238552b4e0000000000000000000000000000000000000000000000000000000000011d94000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2a96ba7b55bf3a4bf9ae3fd49fc2816e9034131d7d2915007c45aff370f1b5ef",
      "signature": {
        "s": "0x328be5c5c3a2d9ae93302b336962db6b54627869e1364fc72a1024f869acaeda",
        "r": "0xf2cb295e50de6d68da8824c5623ea3e8c1c9215b6114111d4a6f01339b88ae97",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4de2942ba393248a8cc0a3a9d6ec82c2edf2d5b506319cd95f564b3458d0f30d",
      "signature": {
        "s": "0x6d0ed552d2815bc15ac630e353c94b315e441385aa9ffbba7f774a6a8c746ad3",
        "r": "0xc57054a8c358c0e0c48f68b2f12a8b4fc011357afee7cda859c8a67baeace216",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "73108",
    "total": "73108"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "73108",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "674328"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "73"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMDQ0MDU2ZC0wMGY4LTU1ODgtODIyNC03ZjJlMjc2OGY2MjYifQ==",
    "nonce": 1983,
    "balances": {
      "current": "10000001408990614",
      "previous": "10000001409063795"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda5900d2ed980f59171571427158dd0238552b4e",
    "nonce": 20,
    "balances": {
      "current": "73108",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:33.727Z",
  "updated": "2020-05-22T08:13:33.792Z",
  "id": "5ec789adb0c6090011d5ab65"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000000000000011d940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `73108`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``