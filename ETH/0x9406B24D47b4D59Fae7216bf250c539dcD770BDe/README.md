# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9406B24D47b4D59Fae7216bf250c539dcD770BDe`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000012ca10000000000000000000000000000000000000000000000000000000000012ca100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000012ca10000000000000000000000000000000000000000000000000000000000012ca1f1f6a58b245887730ad3057f94fd791760919a64ea175846bf9c50023916de2ec93f23ce489ffa8f4112a78f2d40bb46b52b8a097668cddce40fd33d87f2cec902f50bd736b12c001e466ad43ac7197f8dcde000143d851ad5a7ec363082faa5000000000000000000000000000000000000000000000000000000000000001bd24c5d5391cd9efc3271ceb41eaec56c2863794542aeffddea2b1448691e33fe46a375a623e46bc70c676b8ba5912a05ef65ed4579950b398b1e7a64b863b1205fc42955bdedee0a28646e73bf94de190a1029a17a2df4d35fd85c64ba804bb1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000020900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb4c35b0000000000000000000000000000000000000000000000000002386f2cb4d629d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000004c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000085cdd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979595755314d4755345a53307a4f5751304c545579596d51744f474e6a4e79316a4d6d45325a6d4e684e6d4e6a4d574d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000009406b24d47b4d59fae7216bf250c539dcd770bde0000000000000000000000000000000000000000000000000000000000012ca1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf1f6a58b245887730ad3057f94fd791760919a64ea175846bf9c50023916de2e",
      "signature": {
        "s": "0x02f50bd736b12c001e466ad43ac7197f8dcde000143d851ad5a7ec363082faa5",
        "r": "0xc93f23ce489ffa8f4112a78f2d40bb46b52b8a097668cddce40fd33d87f2cec9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd24c5d5391cd9efc3271ceb41eaec56c2863794542aeffddea2b1448691e33fe",
      "signature": {
        "s": "0x5fc42955bdedee0a28646e73bf94de190a1029a17a2df4d35fd85c64ba804bb1",
        "r": "0x46a375a623e46bc70c676b8ba5912a05ef65ed4579950b398b1e7a64b863b120",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "76961",
    "total": "76961"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76961",
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
            "amount": "548061"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "76"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYWU1MGU4ZS0zOWQ0LTUyYmQtOGNjNy1jMmE2ZmNhNmNjMWMifQ==",
    "nonce": 521,
    "balances": {
      "current": "10000001535849904",
      "previous": "10000001535926941"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9406b24d47b4d59fae7216bf250c539dcd770bde",
    "nonce": 20,
    "balances": {
      "current": "76961",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:38.101Z",
  "updated": "2020-05-22T08:02:38.175Z",
  "id": "5ec7871ee5756b00111b801e"
}
```
* *stageAmount*: `76961`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000012ca100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000012ca10000000000000000000000000000000000000000000000000000000000012ca1f1f6a58b245887730ad3057f94fd791760919a64ea175846bf9c50023916de2ec93f23ce489ffa8f4112a78f2d40bb46b52b8a097668cddce40fd33d87f2cec902f50bd736b12c001e466ad43ac7197f8dcde000143d851ad5a7ec363082faa5000000000000000000000000000000000000000000000000000000000000001bd24c5d5391cd9efc3271ceb41eaec56c2863794542aeffddea2b1448691e33fe46a375a623e46bc70c676b8ba5912a05ef65ed4579950b398b1e7a64b863b1205fc42955bdedee0a28646e73bf94de190a1029a17a2df4d35fd85c64ba804bb1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000020900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb4c35b0000000000000000000000000000000000000000000000000002386f2cb4d629d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000004c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000085cdd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979595755314d4755345a53307a4f5751304c545579596d51744f474e6a4e79316a4d6d45325a6d4e684e6d4e6a4d574d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000009406b24d47b4d59fae7216bf250c539dcd770bde0000000000000000000000000000000000000000000000000000000000012ca1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf1f6a58b245887730ad3057f94fd791760919a64ea175846bf9c50023916de2e",
      "signature": {
        "s": "0x02f50bd736b12c001e466ad43ac7197f8dcde000143d851ad5a7ec363082faa5",
        "r": "0xc93f23ce489ffa8f4112a78f2d40bb46b52b8a097668cddce40fd33d87f2cec9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd24c5d5391cd9efc3271ceb41eaec56c2863794542aeffddea2b1448691e33fe",
      "signature": {
        "s": "0x5fc42955bdedee0a28646e73bf94de190a1029a17a2df4d35fd85c64ba804bb1",
        "r": "0x46a375a623e46bc70c676b8ba5912a05ef65ed4579950b398b1e7a64b863b120",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "76961",
    "total": "76961"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76961",
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
            "amount": "548061"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "76"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYWU1MGU4ZS0zOWQ0LTUyYmQtOGNjNy1jMmE2ZmNhNmNjMWMifQ==",
    "nonce": 521,
    "balances": {
      "current": "10000001535849904",
      "previous": "10000001535926941"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9406b24d47b4d59fae7216bf250c539dcd770bde",
    "nonce": 20,
    "balances": {
      "current": "76961",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:38.101Z",
  "updated": "2020-05-22T08:02:38.175Z",
  "id": "5ec7871ee5756b00111b801e"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000012ca10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `76961`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``