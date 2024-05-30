# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x98270824ed7a713fEE18032BC514C17F6E63e651`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001a055690d9db80000000000000000000000000000000000000000000000000001a055690d9db800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001a055690d9db80000000000000000000000000000000000000000000000000001a055690d9db80000d51722f68a7ab6149154d5d13cea8049d5e26a9d0de6a282b76e0b933540ffac712a290db4904653f2798cab110d0ab996793bb15889e68a66d676d1eb6dd89708a2e15d9b246d4442ca8b90ff81c2aa8f759ca5ca219a8f1abffa474a62dca6000000000000000000000000000000000000000000000000000000000000001bf5004bdc6e18fa36d3b4a273b21731721d04f40ab72b5989c6c6eccac1c28bfbed5f4750a8b8991ef4885ca1721d571aa921d7466769670bc6c92be34d2e12f313eec19de905e33c4f1bcdbf1a6a40cc6a457579be3cb6089b89bdc490efc4ab000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000caaa7200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000029000000000000000000000000243a01797aa7e527f44588098ac219d2d7d846bb00000000000000000000000000000000000000000000001b1c9e0b8e6de557de00000000000000000000000000000000000000000000001cbd5e09735ae057de00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000006a94d74f4300000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ad7c71fdac00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d545132597a6c6c4d5330304e6d566d4c5452694d6d457459544a6a5a69316a4e474d334e5749304f4445325a54416966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000098270824ed7a713fee18032bc514c17f6e63e651000000000000000000000000000000000000000000000001a055690d9db80000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd51722f68a7ab6149154d5d13cea8049d5e26a9d0de6a282b76e0b933540ffac",
      "signature": {
        "s": "0x08a2e15d9b246d4442ca8b90ff81c2aa8f759ca5ca219a8f1abffa474a62dca6",
        "r": "0x712a290db4904653f2798cab110d0ab996793bb15889e68a66d676d1eb6dd897",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf5004bdc6e18fa36d3b4a273b21731721d04f40ab72b5989c6c6eccac1c28bfb",
      "signature": {
        "s": "0x13eec19de905e33c4f1bcdbf1a6a40cc6a457579be3cb6089b89bdc490efc4ab",
        "r": "0xed5f4750a8b8991ef4885ca1721d571aa921d7466769670bc6c92be34d2e12f3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "30000000000000000000",
    "total": "30000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "30000000000000000000",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "48832000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "30000000000000000"
      }
    },
    "wallet": "0x243a01797aa7e527f44588098ac219d2d7d846bb",
    "data": "eyJyZWYiOiI2MTQ2YzllMS00NmVmLTRiMmEtYTJjZi1jNGM3NWI0ODE2ZTAifQ==",
    "nonce": 41,
    "balances": {
      "current": "500124188375897167838",
      "previous": "530154188375897167838"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98270824ed7a713fee18032bc514c17f6e63e651",
    "nonce": 1,
    "balances": {
      "current": "30000000000000000000",
      "previous": "0"
    }
  },
  "blockNumber": "13281906",
  "created": "2021-09-23T12:12:54.158Z",
  "updated": "2021-09-23T12:12:54.367Z",
  "id": "614c6f46a2be2100101cc965"
}
```
* *stageAmount*: `30000000000000000000`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001a055690d9db800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001a055690d9db80000000000000000000000000000000000000000000000000001a055690d9db80000d51722f68a7ab6149154d5d13cea8049d5e26a9d0de6a282b76e0b933540ffac712a290db4904653f2798cab110d0ab996793bb15889e68a66d676d1eb6dd89708a2e15d9b246d4442ca8b90ff81c2aa8f759ca5ca219a8f1abffa474a62dca6000000000000000000000000000000000000000000000000000000000000001bf5004bdc6e18fa36d3b4a273b21731721d04f40ab72b5989c6c6eccac1c28bfbed5f4750a8b8991ef4885ca1721d571aa921d7466769670bc6c92be34d2e12f313eec19de905e33c4f1bcdbf1a6a40cc6a457579be3cb6089b89bdc490efc4ab000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000caaa7200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000029000000000000000000000000243a01797aa7e527f44588098ac219d2d7d846bb00000000000000000000000000000000000000000000001b1c9e0b8e6de557de00000000000000000000000000000000000000000000001cbd5e09735ae057de00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000006a94d74f4300000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ad7c71fdac00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d545132597a6c6c4d5330304e6d566d4c5452694d6d457459544a6a5a69316a4e474d334e5749304f4445325a54416966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000098270824ed7a713fee18032bc514c17f6e63e651000000000000000000000000000000000000000000000001a055690d9db80000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd51722f68a7ab6149154d5d13cea8049d5e26a9d0de6a282b76e0b933540ffac",
      "signature": {
        "s": "0x08a2e15d9b246d4442ca8b90ff81c2aa8f759ca5ca219a8f1abffa474a62dca6",
        "r": "0x712a290db4904653f2798cab110d0ab996793bb15889e68a66d676d1eb6dd897",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf5004bdc6e18fa36d3b4a273b21731721d04f40ab72b5989c6c6eccac1c28bfb",
      "signature": {
        "s": "0x13eec19de905e33c4f1bcdbf1a6a40cc6a457579be3cb6089b89bdc490efc4ab",
        "r": "0xed5f4750a8b8991ef4885ca1721d571aa921d7466769670bc6c92be34d2e12f3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "30000000000000000000",
    "total": "30000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "30000000000000000000",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "48832000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "30000000000000000"
      }
    },
    "wallet": "0x243a01797aa7e527f44588098ac219d2d7d846bb",
    "data": "eyJyZWYiOiI2MTQ2YzllMS00NmVmLTRiMmEtYTJjZi1jNGM3NWI0ODE2ZTAifQ==",
    "nonce": 41,
    "balances": {
      "current": "500124188375897167838",
      "previous": "530154188375897167838"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98270824ed7a713fee18032bc514c17f6e63e651",
    "nonce": 1,
    "balances": {
      "current": "30000000000000000000",
      "previous": "0"
    }
  },
  "blockNumber": "13281906",
  "created": "2021-09-23T12:12:54.158Z",
  "updated": "2021-09-23T12:12:54.367Z",
  "id": "614c6f46a2be2100101cc965"
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
0x0f200f9b000000000000000000000000000000000000000000000001a055690d9db800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `30000000000000000000`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`