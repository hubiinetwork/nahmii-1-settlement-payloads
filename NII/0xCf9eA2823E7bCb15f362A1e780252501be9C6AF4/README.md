# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCf9eA2823E7bCb15f362A1e780252501be9C6AF4`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000007fef94482f21e0000000000000000000000000000000000000000000000000007fef94482f21e00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000007fef94482f21e0000000000000000000000000000000000000000000000000007fef94482f21e00000fcedce53664574b211c70c7ea3b32f2b5344cb9ddf86ecd1f63cf56242b3ec758ef1f8af359fa21ce276629230f499a7dc0e943f32d86a3d881e6421ae35eef2cac834c5a92732e5c9a7cc7b84636035ff310fa588215e4383ddaae22f36cad000000000000000000000000000000000000000000000000000000000000001ce231e0ee6169510984492916f2fc53ffa69d0cee750b382ee3e67a72c290e3e3b8a625011f50506ea780d2575acdef0534cecdaf977ea004ea22ab6b23d043ff0ed596e57f9f97572247457a06648440fd3ed0f7416ba886ae910fc942422ad5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000ba28b1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000210000000000000000000000000aadf828db22c00e179725f0d04ad127f8faac8400000000000000000000000000000000000000000000000011e744478a8992a600000000000000000000000000000000000000000000000812ec8f426d0652a600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000020c0677f05ec0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000020c0677f05ec0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e3245324d54417a4f4331684d6d466a4c5451314d7a45744f4745304e533035596a6b784e6d4978596a6b304d44516966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000cf9ea2823e7bcb15f362a1e780252501be9c6af4000000000000000000000000000000000000000000000007fef94482f21e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0fcedce53664574b211c70c7ea3b32f2b5344cb9ddf86ecd1f63cf56242b3ec7",
      "signature": {
        "s": "0x2cac834c5a92732e5c9a7cc7b84636035ff310fa588215e4383ddaae22f36cad",
        "r": "0x58ef1f8af359fa21ce276629230f499a7dc0e943f32d86a3d881e6421ae35eef",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe231e0ee6169510984492916f2fc53ffa69d0cee750b382ee3e67a72c290e3e3",
      "signature": {
        "s": "0x0ed596e57f9f97572247457a06648440fd3ed0f7416ba886ae910fc942422ad5",
        "r": "0xb8a625011f50506ea780d2575acdef0534cecdaf977ea004ea22ab6b23d043ff",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "147500000000000000000",
    "total": "147500000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "147500000000000000000",
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
            "amount": "147500000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "147500000000000000"
      }
    },
    "wallet": "0x0aadf828db22c00e179725f0d04ad127f8faac84",
    "data": "eyJyZWYiOiIwN2E2MTAzOC1hMmFjLTQ1MzEtOGE0NS05YjkxNmIxYjk0MDQifQ==",
    "nonce": 33,
    "balances": {
      "current": "1290074892322575014",
      "previous": "148937574892322575014"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcf9ea2823e7bcb15f362a1e780252501be9c6af4",
    "nonce": 1,
    "balances": {
      "current": "147500000000000000000",
      "previous": "0"
    }
  },
  "blockNumber": "12200113",
  "created": "2021-04-08T15:58:44.876Z",
  "updated": "2021-04-08T15:58:44.976Z",
  "id": "606f28341a03ef0010848e76"
}
```
* *stageAmount*: `147500000000000000000`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000007fef94482f21e00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000007fef94482f21e0000000000000000000000000000000000000000000000000007fef94482f21e00000fcedce53664574b211c70c7ea3b32f2b5344cb9ddf86ecd1f63cf56242b3ec758ef1f8af359fa21ce276629230f499a7dc0e943f32d86a3d881e6421ae35eef2cac834c5a92732e5c9a7cc7b84636035ff310fa588215e4383ddaae22f36cad000000000000000000000000000000000000000000000000000000000000001ce231e0ee6169510984492916f2fc53ffa69d0cee750b382ee3e67a72c290e3e3b8a625011f50506ea780d2575acdef0534cecdaf977ea004ea22ab6b23d043ff0ed596e57f9f97572247457a06648440fd3ed0f7416ba886ae910fc942422ad5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000ba28b1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000210000000000000000000000000aadf828db22c00e179725f0d04ad127f8faac8400000000000000000000000000000000000000000000000011e744478a8992a600000000000000000000000000000000000000000000000812ec8f426d0652a600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000020c0677f05ec0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000020c0677f05ec0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e3245324d54417a4f4331684d6d466a4c5451314d7a45744f4745304e533035596a6b784e6d4978596a6b304d44516966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000cf9ea2823e7bcb15f362a1e780252501be9c6af4000000000000000000000000000000000000000000000007fef94482f21e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0fcedce53664574b211c70c7ea3b32f2b5344cb9ddf86ecd1f63cf56242b3ec7",
      "signature": {
        "s": "0x2cac834c5a92732e5c9a7cc7b84636035ff310fa588215e4383ddaae22f36cad",
        "r": "0x58ef1f8af359fa21ce276629230f499a7dc0e943f32d86a3d881e6421ae35eef",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe231e0ee6169510984492916f2fc53ffa69d0cee750b382ee3e67a72c290e3e3",
      "signature": {
        "s": "0x0ed596e57f9f97572247457a06648440fd3ed0f7416ba886ae910fc942422ad5",
        "r": "0xb8a625011f50506ea780d2575acdef0534cecdaf977ea004ea22ab6b23d043ff",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "147500000000000000000",
    "total": "147500000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "147500000000000000000",
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
            "amount": "147500000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "147500000000000000"
      }
    },
    "wallet": "0x0aadf828db22c00e179725f0d04ad127f8faac84",
    "data": "eyJyZWYiOiIwN2E2MTAzOC1hMmFjLTQ1MzEtOGE0NS05YjkxNmIxYjk0MDQifQ==",
    "nonce": 33,
    "balances": {
      "current": "1290074892322575014",
      "previous": "148937574892322575014"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcf9ea2823e7bcb15f362a1e780252501be9c6af4",
    "nonce": 1,
    "balances": {
      "current": "147500000000000000000",
      "previous": "0"
    }
  },
  "blockNumber": "12200113",
  "created": "2021-04-08T15:58:44.876Z",
  "updated": "2021-04-08T15:58:44.976Z",
  "id": "606f28341a03ef0010848e76"
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
0x0f200f9b000000000000000000000000000000000000000000000007fef94482f21e00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `147500000000000000000`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`