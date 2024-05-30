# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5f0780e7FBdF887631D7aF3DFCb35CbbE5602B98`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000009c000000000000000000000000000000000000000000000000000000000000009c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000009c000000000000000000000000000000000000000000000000000000000000009c0c84c2e78609a0b356251e4a6628d32cc8184b14c40420572217fd336dce39ee033f7743b73eec932fecac38cdf93e27f7d6ebcee4d35721b3fe1f413583af430b7e8fb8e02bb603fdcceca4dd668ac12b00db849c7fafff9e2a176cf04b183e000000000000000000000000000000000000000000000000000000000000001b612bd4683f9f004f846b38a2cef56ea1080105ed0c8485a291f9b11d0c909f9964ff121f4da70501f62ac2298d56ca8622da4c94b74571ce38972203aa76fd6d40a091fb06eba680da39400d1a830e762d7efb5a6f44c1dc219019e3bf03cd01000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000094500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc506a88000000000000000000000000000000000000000000000000002386f2bc506b2500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2fc700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a6332597a49334d53307a593245314c545579597a4d7459574a694d69307a4e32466c4e4445324f5467784f57516966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000005f0780e7fbdf887631d7af3dfcb35cbbe5602b98000000000000000000000000000000000000000000000000000000000000009c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c84c2e78609a0b356251e4a6628d32cc8184b14c40420572217fd336dce39ee",
      "signature": {
        "s": "0x0b7e8fb8e02bb603fdcceca4dd668ac12b00db849c7fafff9e2a176cf04b183e",
        "r": "0x033f7743b73eec932fecac38cdf93e27f7d6ebcee4d35721b3fe1f413583af43",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x612bd4683f9f004f846b38a2cef56ea1080105ed0c8485a291f9b11d0c909f99",
      "signature": {
        "s": "0x40a091fb06eba680da39400d1a830e762d7efb5a6f44c1dc219019e3bf03cd01",
        "r": "0x64ff121f4da70501f62ac2298d56ca8622da4c94b74571ce38972203aa76fd6d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "156",
    "total": "156"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "156",
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
            "amount": "798663"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0Yzc2YzI3MS0zY2E1LTUyYzMtYWJiMi0zN2FlNDE2OTgxOWQifQ==",
    "nonce": 2373,
    "balances": {
      "current": "10000001284467336",
      "previous": "10000001284467493"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5f0780e7fbdf887631d7af3dfcb35cbbe5602b98",
    "nonce": 6,
    "balances": {
      "current": "156",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:08.011Z",
  "updated": "2020-05-22T08:16:09.079Z",
  "id": "5ec78a48005df800101bc540"
}
```
* *stageAmount*: `156`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000009c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000009c000000000000000000000000000000000000000000000000000000000000009c0c84c2e78609a0b356251e4a6628d32cc8184b14c40420572217fd336dce39ee033f7743b73eec932fecac38cdf93e27f7d6ebcee4d35721b3fe1f413583af430b7e8fb8e02bb603fdcceca4dd668ac12b00db849c7fafff9e2a176cf04b183e000000000000000000000000000000000000000000000000000000000000001b612bd4683f9f004f846b38a2cef56ea1080105ed0c8485a291f9b11d0c909f9964ff121f4da70501f62ac2298d56ca8622da4c94b74571ce38972203aa76fd6d40a091fb06eba680da39400d1a830e762d7efb5a6f44c1dc219019e3bf03cd01000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000094500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc506a88000000000000000000000000000000000000000000000000002386f2bc506b2500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2fc700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a6332597a49334d53307a593245314c545579597a4d7459574a694d69307a4e32466c4e4445324f5467784f57516966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000005f0780e7fbdf887631d7af3dfcb35cbbe5602b98000000000000000000000000000000000000000000000000000000000000009c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c84c2e78609a0b356251e4a6628d32cc8184b14c40420572217fd336dce39ee",
      "signature": {
        "s": "0x0b7e8fb8e02bb603fdcceca4dd668ac12b00db849c7fafff9e2a176cf04b183e",
        "r": "0x033f7743b73eec932fecac38cdf93e27f7d6ebcee4d35721b3fe1f413583af43",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x612bd4683f9f004f846b38a2cef56ea1080105ed0c8485a291f9b11d0c909f99",
      "signature": {
        "s": "0x40a091fb06eba680da39400d1a830e762d7efb5a6f44c1dc219019e3bf03cd01",
        "r": "0x64ff121f4da70501f62ac2298d56ca8622da4c94b74571ce38972203aa76fd6d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "156",
    "total": "156"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "156",
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
            "amount": "798663"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0Yzc2YzI3MS0zY2E1LTUyYzMtYWJiMi0zN2FlNDE2OTgxOWQifQ==",
    "nonce": 2373,
    "balances": {
      "current": "10000001284467336",
      "previous": "10000001284467493"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5f0780e7fbdf887631d7af3dfcb35cbbe5602b98",
    "nonce": 6,
    "balances": {
      "current": "156",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:08.011Z",
  "updated": "2020-05-22T08:16:09.079Z",
  "id": "5ec78a48005df800101bc540"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000009c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `156`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``