# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x598e920Dd134708838306d1080bFB6e4f9457B50`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000d6ba000000000000000000000000000000000000000000000000000000000000d6ba0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000d6ba000000000000000000000000000000000000000000000000000000000000d6ba2a4cd216fd588ef6238776fa8ba295c06a3a28bb8615f776a2bded5e9410ff051688e57287a8c615387f8ca9d01c001894130a8b8ba3ceb1f12304d3b34c79a800836bc9f88c0b802840dea2ecaaeb1f825f4fe2fae779a3c21aa10ec972884b000000000000000000000000000000000000000000000000000000000000001b8d0585bfc288f2fc2bceaf3ffed7756efd641df63277de928da82149278a883d9826b079baff6fd25340c4630368460f9cfd4c321c340df89585dd42a73d156f7ec93a2f78059820bfb0671530594851194d66fe083acba93d306b28c8a1d93b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000058000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c70234f7000000000000000000000000000000000000000000000000002386f2c7030be700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009749b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d4463784d6a52694d7930795a4464694c5455784e3255744f47566b5a53316c4f57497a4e546b315a544d324e47596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000598e920dd134708838306d1080bfb6e4f9457b50000000000000000000000000000000000000000000000000000000000000d6ba000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2a4cd216fd588ef6238776fa8ba295c06a3a28bb8615f776a2bded5e9410ff05",
      "signature": {
        "s": "0x00836bc9f88c0b802840dea2ecaaeb1f825f4fe2fae779a3c21aa10ec972884b",
        "r": "0x1688e57287a8c615387f8ca9d01c001894130a8b8ba3ceb1f12304d3b34c79a8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8d0585bfc288f2fc2bceaf3ffed7756efd641df63277de928da82149278a883d",
      "signature": {
        "s": "0x7ec93a2f78059820bfb0671530594851194d66fe083acba93d306b28c8a1d93b",
        "r": "0x9826b079baff6fd25340c4630368460f9cfd4c321c340df89585dd42a73d156f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "54970",
    "total": "54970"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "54970",
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
            "amount": "619675"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "54"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMDcxMjRiMy0yZDdiLTUxN2UtOGVkZS1lOWIzNTk1ZTM2NGYifQ==",
    "nonce": 1408,
    "balances": {
      "current": "10000001463891191",
      "previous": "10000001463946215"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x598e920dd134708838306d1080bfb6e4f9457b50",
    "nonce": 20,
    "balances": {
      "current": "54970",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:12.484Z",
  "updated": "2020-05-22T08:09:12.557Z",
  "id": "5ec788a8b0c6090011d5aaa4"
}
```
* *stageAmount*: `54970`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000d6ba0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000d6ba000000000000000000000000000000000000000000000000000000000000d6ba2a4cd216fd588ef6238776fa8ba295c06a3a28bb8615f776a2bded5e9410ff051688e57287a8c615387f8ca9d01c001894130a8b8ba3ceb1f12304d3b34c79a800836bc9f88c0b802840dea2ecaaeb1f825f4fe2fae779a3c21aa10ec972884b000000000000000000000000000000000000000000000000000000000000001b8d0585bfc288f2fc2bceaf3ffed7756efd641df63277de928da82149278a883d9826b079baff6fd25340c4630368460f9cfd4c321c340df89585dd42a73d156f7ec93a2f78059820bfb0671530594851194d66fe083acba93d306b28c8a1d93b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000058000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c70234f7000000000000000000000000000000000000000000000000002386f2c7030be700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009749b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d4463784d6a52694d7930795a4464694c5455784e3255744f47566b5a53316c4f57497a4e546b315a544d324e47596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000598e920dd134708838306d1080bfb6e4f9457b50000000000000000000000000000000000000000000000000000000000000d6ba000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2a4cd216fd588ef6238776fa8ba295c06a3a28bb8615f776a2bded5e9410ff05",
      "signature": {
        "s": "0x00836bc9f88c0b802840dea2ecaaeb1f825f4fe2fae779a3c21aa10ec972884b",
        "r": "0x1688e57287a8c615387f8ca9d01c001894130a8b8ba3ceb1f12304d3b34c79a8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8d0585bfc288f2fc2bceaf3ffed7756efd641df63277de928da82149278a883d",
      "signature": {
        "s": "0x7ec93a2f78059820bfb0671530594851194d66fe083acba93d306b28c8a1d93b",
        "r": "0x9826b079baff6fd25340c4630368460f9cfd4c321c340df89585dd42a73d156f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "54970",
    "total": "54970"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "54970",
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
            "amount": "619675"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "54"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMDcxMjRiMy0yZDdiLTUxN2UtOGVkZS1lOWIzNTk1ZTM2NGYifQ==",
    "nonce": 1408,
    "balances": {
      "current": "10000001463891191",
      "previous": "10000001463946215"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x598e920dd134708838306d1080bfb6e4f9457b50",
    "nonce": 20,
    "balances": {
      "current": "54970",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:12.484Z",
  "updated": "2020-05-22T08:09:12.557Z",
  "id": "5ec788a8b0c6090011d5aaa4"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000d6ba0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `54970`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``