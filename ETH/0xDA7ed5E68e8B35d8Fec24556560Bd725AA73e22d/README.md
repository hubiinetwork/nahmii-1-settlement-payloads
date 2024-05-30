# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xDA7ed5E68e8B35d8Fec24556560Bd725AA73e22d`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000004e48d000000000000000000000000000000000000000000000000000000000004e48d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000004e48d000000000000000000000000000000000000000000000000000000000004e48db6910da06b238a06fc48ee1adb4cd47e1b417d4f960d69aeeec54b2a6e09d4298d01e03010defaf17588c4c0b162858bb0ea2f2de991a661708f88021649a62d32607f5bdb67fd2a6a05b852748997bdc37d04bb7170de8e21023c64aadb4a8d000000000000000000000000000000000000000000000000000000000000001b4423bd0a1a698967837e004fcce8eb10b7f9204e898f901ac8b5c5e16a8f2c1af4243d4bae0d457f0bc716848b8d6e5260e1bc73d68653d7644e95452e1a9bd236c356e24fb664c75fa2d13055d301f37381262c99edc1b2bf9cb825d6669428000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000074400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c41668ae000000000000000000000000000000000000000000000000002386f2c41b4e7b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000001400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a334700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e44686c596d56684d4330314e6a63344c54557a4d4751744f446b324d7930304e54566a597a63784d6d466b4d32496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da7ed5e68e8b35d8fec24556560bd725aa73e22d000000000000000000000000000000000000000000000000000000000004e48d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb6910da06b238a06fc48ee1adb4cd47e1b417d4f960d69aeeec54b2a6e09d429",
      "signature": {
        "s": "0x32607f5bdb67fd2a6a05b852748997bdc37d04bb7170de8e21023c64aadb4a8d",
        "r": "0x8d01e03010defaf17588c4c0b162858bb0ea2f2de991a661708f88021649a62d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4423bd0a1a698967837e004fcce8eb10b7f9204e898f901ac8b5c5e16a8f2c1a",
      "signature": {
        "s": "0x36c356e24fb664c75fa2d13055d301f37381262c99edc1b2bf9cb825d6669428",
        "r": "0xf4243d4bae0d457f0bc716848b8d6e5260e1bc73d68653d7644e95452e1a9bd2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "320653",
    "total": "320653"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "320653",
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
            "amount": "668487"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "320"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNDhlYmVhMC01Njc4LTUzMGQtODk2My00NTVjYzcxMmFkM2IifQ==",
    "nonce": 1860,
    "balances": {
      "current": "10000001414883502",
      "previous": "10000001415204475"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda7ed5e68e8b35d8fec24556560bd725aa73e22d",
    "nonce": 20,
    "balances": {
      "current": "320653",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:39.086Z",
  "updated": "2020-05-22T08:12:39.151Z",
  "id": "5ec78977005df800101bc492"
}
```
* *stageAmount*: `320653`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000004e48d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000004e48d000000000000000000000000000000000000000000000000000000000004e48db6910da06b238a06fc48ee1adb4cd47e1b417d4f960d69aeeec54b2a6e09d4298d01e03010defaf17588c4c0b162858bb0ea2f2de991a661708f88021649a62d32607f5bdb67fd2a6a05b852748997bdc37d04bb7170de8e21023c64aadb4a8d000000000000000000000000000000000000000000000000000000000000001b4423bd0a1a698967837e004fcce8eb10b7f9204e898f901ac8b5c5e16a8f2c1af4243d4bae0d457f0bc716848b8d6e5260e1bc73d68653d7644e95452e1a9bd236c356e24fb664c75fa2d13055d301f37381262c99edc1b2bf9cb825d6669428000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000074400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c41668ae000000000000000000000000000000000000000000000000002386f2c41b4e7b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000001400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a334700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e44686c596d56684d4330314e6a63344c54557a4d4751744f446b324d7930304e54566a597a63784d6d466b4d32496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da7ed5e68e8b35d8fec24556560bd725aa73e22d000000000000000000000000000000000000000000000000000000000004e48d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb6910da06b238a06fc48ee1adb4cd47e1b417d4f960d69aeeec54b2a6e09d429",
      "signature": {
        "s": "0x32607f5bdb67fd2a6a05b852748997bdc37d04bb7170de8e21023c64aadb4a8d",
        "r": "0x8d01e03010defaf17588c4c0b162858bb0ea2f2de991a661708f88021649a62d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4423bd0a1a698967837e004fcce8eb10b7f9204e898f901ac8b5c5e16a8f2c1a",
      "signature": {
        "s": "0x36c356e24fb664c75fa2d13055d301f37381262c99edc1b2bf9cb825d6669428",
        "r": "0xf4243d4bae0d457f0bc716848b8d6e5260e1bc73d68653d7644e95452e1a9bd2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "320653",
    "total": "320653"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "320653",
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
            "amount": "668487"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "320"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNDhlYmVhMC01Njc4LTUzMGQtODk2My00NTVjYzcxMmFkM2IifQ==",
    "nonce": 1860,
    "balances": {
      "current": "10000001414883502",
      "previous": "10000001415204475"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda7ed5e68e8b35d8fec24556560bd725aa73e22d",
    "nonce": 20,
    "balances": {
      "current": "320653",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:39.086Z",
  "updated": "2020-05-22T08:12:39.151Z",
  "id": "5ec78977005df800101bc492"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000004e48d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `320653`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``