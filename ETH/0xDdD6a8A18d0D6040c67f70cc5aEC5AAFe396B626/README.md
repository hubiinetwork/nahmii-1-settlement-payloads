# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xDdD6a8A18d0D6040c67f70cc5aEC5AAFe396B626`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000048a000000000000000000000000000000000000000000000000000000000000048a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000048a000000000000000000000000000000000000000000000000000000000000048aadbd8c2b4d35f01c0c0554707fe90a5fc54a7f160f6d05e972a7e8b3e3ae511a63e407d4c40f9e7ecb3f42d4ffe16336fbaca47aef31d0283ff23e887f4a7e1c3125242f7564e87cc952388d9c9059c991344f22a1f8d1a239dfb50aaad4397e000000000000000000000000000000000000000000000000000000000000001b143bd841999de6fdfe6449e160b5664cd5c5421337bfb7383c6b9d7319ce8a2acbd8a511af97f688b64b6af8ddde2e9e45034c9ca0370265fa398da0915acab755a2e60857984a495e2b706ac0b195b35fb2b39738e29ceb6ede154c65292aa7000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007be00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3bd9b73000000000000000000000000000000000000000000000000002386f2c3bd9ffe00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a49cf00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e325a6859324e684e6930315a474a6b4c5456694f5751744f44517a5979316b4d7a4d345a6a466c4f57526c5a6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000ddd6a8a18d0d6040c67f70cc5aec5aafe396b626000000000000000000000000000000000000000000000000000000000000048a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xadbd8c2b4d35f01c0c0554707fe90a5fc54a7f160f6d05e972a7e8b3e3ae511a",
      "signature": {
        "s": "0x3125242f7564e87cc952388d9c9059c991344f22a1f8d1a239dfb50aaad4397e",
        "r": "0x63e407d4c40f9e7ecb3f42d4ffe16336fbaca47aef31d0283ff23e887f4a7e1c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x143bd841999de6fdfe6449e160b5664cd5c5421337bfb7383c6b9d7319ce8a2a",
      "signature": {
        "s": "0x55a2e60857984a495e2b706ac0b195b35fb2b39738e29ceb6ede154c65292aa7",
        "r": "0xcbd8a511af97f688b64b6af8ddde2e9e45034c9ca0370265fa398da0915acab7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1162",
    "total": "1162"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1162",
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
            "amount": "674255"
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
    "data": "eyJyZWYiOiI4N2ZhY2NhNi01ZGJkLTViOWQtODQzYy1kMzM4ZjFlOWRlZjkifQ==",
    "nonce": 1982,
    "balances": {
      "current": "10000001409063795",
      "previous": "10000001409064958"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xddd6a8a18d0d6040c67f70cc5aec5aafe396b626",
    "nonce": 20,
    "balances": {
      "current": "1162",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:33.551Z",
  "updated": "2020-05-22T08:13:33.620Z",
  "id": "5ec789ade5756b00111b81ee"
}
```
* *stageAmount*: `1162`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000048a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000048a000000000000000000000000000000000000000000000000000000000000048aadbd8c2b4d35f01c0c0554707fe90a5fc54a7f160f6d05e972a7e8b3e3ae511a63e407d4c40f9e7ecb3f42d4ffe16336fbaca47aef31d0283ff23e887f4a7e1c3125242f7564e87cc952388d9c9059c991344f22a1f8d1a239dfb50aaad4397e000000000000000000000000000000000000000000000000000000000000001b143bd841999de6fdfe6449e160b5664cd5c5421337bfb7383c6b9d7319ce8a2acbd8a511af97f688b64b6af8ddde2e9e45034c9ca0370265fa398da0915acab755a2e60857984a495e2b706ac0b195b35fb2b39738e29ceb6ede154c65292aa7000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007be00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3bd9b73000000000000000000000000000000000000000000000000002386f2c3bd9ffe00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a49cf00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e325a6859324e684e6930315a474a6b4c5456694f5751744f44517a5979316b4d7a4d345a6a466c4f57526c5a6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000ddd6a8a18d0d6040c67f70cc5aec5aafe396b626000000000000000000000000000000000000000000000000000000000000048a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xadbd8c2b4d35f01c0c0554707fe90a5fc54a7f160f6d05e972a7e8b3e3ae511a",
      "signature": {
        "s": "0x3125242f7564e87cc952388d9c9059c991344f22a1f8d1a239dfb50aaad4397e",
        "r": "0x63e407d4c40f9e7ecb3f42d4ffe16336fbaca47aef31d0283ff23e887f4a7e1c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x143bd841999de6fdfe6449e160b5664cd5c5421337bfb7383c6b9d7319ce8a2a",
      "signature": {
        "s": "0x55a2e60857984a495e2b706ac0b195b35fb2b39738e29ceb6ede154c65292aa7",
        "r": "0xcbd8a511af97f688b64b6af8ddde2e9e45034c9ca0370265fa398da0915acab7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1162",
    "total": "1162"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1162",
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
            "amount": "674255"
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
    "data": "eyJyZWYiOiI4N2ZhY2NhNi01ZGJkLTViOWQtODQzYy1kMzM4ZjFlOWRlZjkifQ==",
    "nonce": 1982,
    "balances": {
      "current": "10000001409063795",
      "previous": "10000001409064958"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xddd6a8a18d0d6040c67f70cc5aec5aafe396b626",
    "nonce": 20,
    "balances": {
      "current": "1162",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:33.551Z",
  "updated": "2020-05-22T08:13:33.620Z",
  "id": "5ec789ade5756b00111b81ee"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000048a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1162`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``