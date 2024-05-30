# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc2657Fd11e6d3aAfBf0706dD954F0833c0616E1B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000004792a485a18f2ad3d9b64432cd4789937ba950cf3b8671260f41c8c58cb37ce0d46284dfc584f17a263a02f64fa7f4927852177623ba2d21e806515875eeacade8ad447e2bb302fe2637501ca194a53de07f340b87071d7ddf0ac24afc58f64cd5a3000000000000000000000000000000000000000000000000000000000000001c667bb416747e9782e1e0f3e94ae8f626b6d8dde85ecfbbb350c830affb6a154d4a7856cdb15e5c78dfbe0198e65a5febde3cce85b2e7dabf1d3cf0cbeaaae25b480e3f52eb9fb9fdc553e5b2e44e7f3793d06808b9f2cc617c3f9d5e8a962d08000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007cc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3b91e19000000000000000000000000000000000000000000000000002386f2c3b965bd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4af100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a4d324d6d45795a53316a595441354c5455784e574d745954646b5a69316d4d7a566c4d3249345a4759334d32516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000c2657fd11e6d3aafbf0706dd954f0833c0616e1b0000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa485a18f2ad3d9b64432cd4789937ba950cf3b8671260f41c8c58cb37ce0d462",
      "signature": {
        "s": "0x447e2bb302fe2637501ca194a53de07f340b87071d7ddf0ac24afc58f64cd5a3",
        "r": "0x84dfc584f17a263a02f64fa7f4927852177623ba2d21e806515875eeacade8ad",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x667bb416747e9782e1e0f3e94ae8f626b6d8dde85ecfbbb350c830affb6a154d",
      "signature": {
        "s": "0x480e3f52eb9fb9fdc553e5b2e44e7f3793d06808b9f2cc617c3f9d5e8a962d08",
        "r": "0x4a7856cdb15e5c78dfbe0198e65a5febde3cce85b2e7dabf1d3cf0cbeaaae25b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18322",
    "total": "18322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18322",
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
            "amount": "674545"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMzM2MmEyZS1jYTA5LTUxNWMtYTdkZi1mMzVlM2I4ZGY3M2QifQ==",
    "nonce": 1996,
    "balances": {
      "current": "10000001408769561",
      "previous": "10000001408787901"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2657fd11e6d3aafbf0706dd954f0833c0616e1b",
    "nonce": 20,
    "balances": {
      "current": "18322",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:36.385Z",
  "updated": "2020-05-22T08:13:36.458Z",
  "id": "5ec789b0005df800101bc4c1"
}
```
* *stageAmount*: `18322`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000004792a485a18f2ad3d9b64432cd4789937ba950cf3b8671260f41c8c58cb37ce0d46284dfc584f17a263a02f64fa7f4927852177623ba2d21e806515875eeacade8ad447e2bb302fe2637501ca194a53de07f340b87071d7ddf0ac24afc58f64cd5a3000000000000000000000000000000000000000000000000000000000000001c667bb416747e9782e1e0f3e94ae8f626b6d8dde85ecfbbb350c830affb6a154d4a7856cdb15e5c78dfbe0198e65a5febde3cce85b2e7dabf1d3cf0cbeaaae25b480e3f52eb9fb9fdc553e5b2e44e7f3793d06808b9f2cc617c3f9d5e8a962d08000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007cc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3b91e19000000000000000000000000000000000000000000000000002386f2c3b965bd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4af100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a4d324d6d45795a53316a595441354c5455784e574d745954646b5a69316d4d7a566c4d3249345a4759334d32516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000c2657fd11e6d3aafbf0706dd954f0833c0616e1b0000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa485a18f2ad3d9b64432cd4789937ba950cf3b8671260f41c8c58cb37ce0d462",
      "signature": {
        "s": "0x447e2bb302fe2637501ca194a53de07f340b87071d7ddf0ac24afc58f64cd5a3",
        "r": "0x84dfc584f17a263a02f64fa7f4927852177623ba2d21e806515875eeacade8ad",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x667bb416747e9782e1e0f3e94ae8f626b6d8dde85ecfbbb350c830affb6a154d",
      "signature": {
        "s": "0x480e3f52eb9fb9fdc553e5b2e44e7f3793d06808b9f2cc617c3f9d5e8a962d08",
        "r": "0x4a7856cdb15e5c78dfbe0198e65a5febde3cce85b2e7dabf1d3cf0cbeaaae25b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18322",
    "total": "18322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18322",
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
            "amount": "674545"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMzM2MmEyZS1jYTA5LTUxNWMtYTdkZi1mMzVlM2I4ZGY3M2QifQ==",
    "nonce": 1996,
    "balances": {
      "current": "10000001408769561",
      "previous": "10000001408787901"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2657fd11e6d3aafbf0706dd954f0833c0616e1b",
    "nonce": 20,
    "balances": {
      "current": "18322",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:36.385Z",
  "updated": "2020-05-22T08:13:36.458Z",
  "id": "5ec789b0005df800101bc4c1"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18322`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``