# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x787e1433E96a9d291A7bc9AA76d29c5965a2B385`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b2800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b2877624c0f1f7a3a54cf91630a1f79f38f29a827cd3e7a1d3316778c95b33e20f28fc6a52a16d18a6853481c2867a29281c5230da5ed892a1ee9390356b6a2bc7e3f72d8061d0f9a131094a757533f2357de3377d09190fde86a556faee7f51c16000000000000000000000000000000000000000000000000000000000000001bd7db3858f2977e80a8299a14e09450e56fa99058cf744f0b7f2d46f029e0f6e67d903c877f0a5adfedc9042708fe63abfdb6225c8827450892fa01a105853a6161428d27cb5c2167c6c04e9832d904bef5daead5f0452bcaf4f205f21f4f9f96000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000029b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cafed414000000000000000000000000000000000000000000000000002386f2caff1f4f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008706b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e6a45354e3245344e5330304d6a59354c5455794e6a59744f44426c5a53316b5a6d45354f446b314e3249314f54416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000787e1433e96a9d291a7bc9aa76d29c5965a2b3850000000000000000000000000000000000000000000000000000000000004b28000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x77624c0f1f7a3a54cf91630a1f79f38f29a827cd3e7a1d3316778c95b33e20f2",
      "signature": {
        "s": "0x3f72d8061d0f9a131094a757533f2357de3377d09190fde86a556faee7f51c16",
        "r": "0x8fc6a52a16d18a6853481c2867a29281c5230da5ed892a1ee9390356b6a2bc7e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd7db3858f2977e80a8299a14e09450e56fa99058cf744f0b7f2d46f029e0f6e6",
      "signature": {
        "s": "0x61428d27cb5c2167c6c04e9832d904bef5daead5f0452bcaf4f205f21f4f9f96",
        "r": "0x7d903c877f0a5adfedc9042708fe63abfdb6225c8827450892fa01a105853a61",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19240",
    "total": "19240"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19240",
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
            "amount": "553067"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNjE5N2E4NS00MjY5LTUyNjYtODBlZS1kZmE5ODk1N2I1OTAifQ==",
    "nonce": 667,
    "balances": {
      "current": "10000001530778644",
      "previous": "10000001530797903"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x787e1433e96a9d291a7bc9aa76d29c5965a2b385",
    "nonce": 20,
    "balances": {
      "current": "19240",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:52.096Z",
  "updated": "2020-05-22T08:03:52.167Z",
  "id": "5ec78768b0c6090011d5a9ad"
}
```
* *stageAmount*: `19240`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004b2800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b2877624c0f1f7a3a54cf91630a1f79f38f29a827cd3e7a1d3316778c95b33e20f28fc6a52a16d18a6853481c2867a29281c5230da5ed892a1ee9390356b6a2bc7e3f72d8061d0f9a131094a757533f2357de3377d09190fde86a556faee7f51c16000000000000000000000000000000000000000000000000000000000000001bd7db3858f2977e80a8299a14e09450e56fa99058cf744f0b7f2d46f029e0f6e67d903c877f0a5adfedc9042708fe63abfdb6225c8827450892fa01a105853a6161428d27cb5c2167c6c04e9832d904bef5daead5f0452bcaf4f205f21f4f9f96000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000029b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cafed414000000000000000000000000000000000000000000000000002386f2caff1f4f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008706b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e6a45354e3245344e5330304d6a59354c5455794e6a59744f44426c5a53316b5a6d45354f446b314e3249314f54416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000787e1433e96a9d291a7bc9aa76d29c5965a2b3850000000000000000000000000000000000000000000000000000000000004b28000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x77624c0f1f7a3a54cf91630a1f79f38f29a827cd3e7a1d3316778c95b33e20f2",
      "signature": {
        "s": "0x3f72d8061d0f9a131094a757533f2357de3377d09190fde86a556faee7f51c16",
        "r": "0x8fc6a52a16d18a6853481c2867a29281c5230da5ed892a1ee9390356b6a2bc7e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd7db3858f2977e80a8299a14e09450e56fa99058cf744f0b7f2d46f029e0f6e6",
      "signature": {
        "s": "0x61428d27cb5c2167c6c04e9832d904bef5daead5f0452bcaf4f205f21f4f9f96",
        "r": "0x7d903c877f0a5adfedc9042708fe63abfdb6225c8827450892fa01a105853a61",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19240",
    "total": "19240"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19240",
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
            "amount": "553067"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNjE5N2E4NS00MjY5LTUyNjYtODBlZS1kZmE5ODk1N2I1OTAifQ==",
    "nonce": 667,
    "balances": {
      "current": "10000001530778644",
      "previous": "10000001530797903"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x787e1433e96a9d291a7bc9aa76d29c5965a2b385",
    "nonce": 20,
    "balances": {
      "current": "19240",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:52.096Z",
  "updated": "2020-05-22T08:03:52.167Z",
  "id": "5ec78768b0c6090011d5a9ad"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `19240`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``