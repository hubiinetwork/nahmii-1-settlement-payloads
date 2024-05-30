# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF025281457fCaE8C6bE5272e7B06F128939E68Fa`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000e8c0000000000000000000000000000000000000000000000000000000000000e8c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000e8c0000000000000000000000000000000000000000000000000000000000000e8cc0f48c909395c7ad4cea1f6ae8be6885017ecca34c831cc6340f9fda137c8421d2ca25bd9029631b3819b3703c1817f39e84d27a4ea9d789abbc10391884ccbc19f6a63230053249d5844777d501d012c494c6a094d19bb9a76cd47accc1d30f000000000000000000000000000000000000000000000000000000000000001c78d4c1e5dc5c1489f46d64de56f83e7ceb32ca7055e60519370821259f925afff9cc9c53bf120a1ef0bf1a50b6f52e8bd046ade5556aa055df9624231f4186ce71c069dbb8647f4cb147bcea79017726c3fa3c2eb1f6c2eeb12cdfa015220e54000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000083e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bd9ab72d000000000000000000000000000000000000000000000000002386f2bd9ac5bc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000bdb5100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e6a67354f4464694e6930774f5751354c5455775a44597459546b325a53316c4d575135595459794e3252694d57496966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000f025281457fcae8c6be5272e7b06f128939e68fa0000000000000000000000000000000000000000000000000000000000000e8c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc0f48c909395c7ad4cea1f6ae8be6885017ecca34c831cc6340f9fda137c8421",
      "signature": {
        "s": "0x19f6a63230053249d5844777d501d012c494c6a094d19bb9a76cd47accc1d30f",
        "r": "0xd2ca25bd9029631b3819b3703c1817f39e84d27a4ea9d789abbc10391884ccbc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x78d4c1e5dc5c1489f46d64de56f83e7ceb32ca7055e60519370821259f925aff",
      "signature": {
        "s": "0x71c069dbb8647f4cb147bcea79017726c3fa3c2eb1f6c2eeb12cdfa015220e54",
        "r": "0xf9cc9c53bf120a1ef0bf1a50b6f52e8bd046ade5556aa055df9624231f4186ce",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3724",
    "total": "3724"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3724",
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
            "amount": "777041"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3Njg5ODdiNi0wOWQ5LTUwZDYtYTk2ZS1lMWQ5YTYyN2RiMWIifQ==",
    "nonce": 2110,
    "balances": {
      "current": "10000001306113837",
      "previous": "10000001306117564"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf025281457fcae8c6be5272e7b06f128939e68fa",
    "nonce": 6,
    "balances": {
      "current": "3724",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:28.553Z",
  "updated": "2020-05-22T08:14:28.670Z",
  "id": "5ec789e4e5756b00111b8222"
}
```
* *stageAmount*: `3724`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000e8c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000e8c0000000000000000000000000000000000000000000000000000000000000e8cc0f48c909395c7ad4cea1f6ae8be6885017ecca34c831cc6340f9fda137c8421d2ca25bd9029631b3819b3703c1817f39e84d27a4ea9d789abbc10391884ccbc19f6a63230053249d5844777d501d012c494c6a094d19bb9a76cd47accc1d30f000000000000000000000000000000000000000000000000000000000000001c78d4c1e5dc5c1489f46d64de56f83e7ceb32ca7055e60519370821259f925afff9cc9c53bf120a1ef0bf1a50b6f52e8bd046ade5556aa055df9624231f4186ce71c069dbb8647f4cb147bcea79017726c3fa3c2eb1f6c2eeb12cdfa015220e54000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000083e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bd9ab72d000000000000000000000000000000000000000000000000002386f2bd9ac5bc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000bdb5100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e6a67354f4464694e6930774f5751354c5455775a44597459546b325a53316c4d575135595459794e3252694d57496966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000f025281457fcae8c6be5272e7b06f128939e68fa0000000000000000000000000000000000000000000000000000000000000e8c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc0f48c909395c7ad4cea1f6ae8be6885017ecca34c831cc6340f9fda137c8421",
      "signature": {
        "s": "0x19f6a63230053249d5844777d501d012c494c6a094d19bb9a76cd47accc1d30f",
        "r": "0xd2ca25bd9029631b3819b3703c1817f39e84d27a4ea9d789abbc10391884ccbc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x78d4c1e5dc5c1489f46d64de56f83e7ceb32ca7055e60519370821259f925aff",
      "signature": {
        "s": "0x71c069dbb8647f4cb147bcea79017726c3fa3c2eb1f6c2eeb12cdfa015220e54",
        "r": "0xf9cc9c53bf120a1ef0bf1a50b6f52e8bd046ade5556aa055df9624231f4186ce",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3724",
    "total": "3724"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3724",
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
            "amount": "777041"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3Njg5ODdiNi0wOWQ5LTUwZDYtYTk2ZS1lMWQ5YTYyN2RiMWIifQ==",
    "nonce": 2110,
    "balances": {
      "current": "10000001306113837",
      "previous": "10000001306117564"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf025281457fcae8c6be5272e7b06f128939e68fa",
    "nonce": 6,
    "balances": {
      "current": "3724",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:28.553Z",
  "updated": "2020-05-22T08:14:28.670Z",
  "id": "5ec789e4e5756b00111b8222"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000e8c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3724`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``