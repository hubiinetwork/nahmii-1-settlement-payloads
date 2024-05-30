# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7a8044Be44e114EE073b384733252255871a5f06`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000035bdf8b40000000000000000000000000000000000000000000000000000000035bdf8b4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000035bdf8b40000000000000000000000000000000000000000000000000000000035bdf8b4014766027ccda2b9a80caee44f54df7da6d9e4ee4523c7117a0928fc7fb0881be134a2a35e6ac36ee4d89873f782a945c393d17deac42cae2d85ae960f63afad1bf576355cc499c2de0a418db84430b464ffd42ac86bc4ed786c300c79dcdd50000000000000000000000000000000000000000000000000000000000000001bc7936b810d2110df85cad97c81bd64baa2489a26ae9b539c87b6f4603200d67d6a2c4dc85889103d27b14bcbf77759ac5e1d0cd4b9c393c6148b2d2e5e1af39c224c4ba37763ae260b4ce925df64612be60ac67a2e9eae2ce168781b6ecbae18000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d9100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b2a777d4578000000000000000000000000000000000000000000000000002e0b2aad49003600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000dc20a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6563b3b6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5463354d6a55794d7930794f446b304c5455344d6d4d744f4442694e53307959546b345a6d56694e6d5531596d516966513d3d000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000007a8044be44e114ee073b384733252255871a5f060000000000000000000000000000000000000000000000000000000035bdf8b4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x014766027ccda2b9a80caee44f54df7da6d9e4ee4523c7117a0928fc7fb0881b",
      "signature": {
        "s": "0x1bf576355cc499c2de0a418db84430b464ffd42ac86bc4ed786c300c79dcdd50",
        "r": "0xe134a2a35e6ac36ee4d89873f782a945c393d17deac42cae2d85ae960f63afad",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc7936b810d2110df85cad97c81bd64baa2489a26ae9b539c87b6f4603200d67d",
      "signature": {
        "s": "0x224c4ba37763ae260b4ce925df64612be60ac67a2e9eae2ce168781b6ecbae18",
        "r": "0x6a2c4dc85889103d27b14bcbf77759ac5e1d0cd4b9c393c6148b2d2e5e1af39c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "901642420",
    "total": "901642420"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "901642420",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "57535607734"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "901642"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiZTc5MjUyMy0yODk0LTU4MmMtODBiNS0yYTk4ZmViNmU1YmQifQ==",
    "nonce": 7569,
    "balances": {
      "current": "12960125949920632",
      "previous": "12960126852464694"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7a8044be44e114ee073b384733252255871a5f06",
    "nonce": 12,
    "balances": {
      "current": "901642420",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:45.124Z",
  "updated": "2020-05-22T08:57:46.180Z",
  "id": "5ec79409e5756b00111b890d"
}
```
* *stageAmount*: `901642420`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000035bdf8b4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000035bdf8b40000000000000000000000000000000000000000000000000000000035bdf8b4014766027ccda2b9a80caee44f54df7da6d9e4ee4523c7117a0928fc7fb0881be134a2a35e6ac36ee4d89873f782a945c393d17deac42cae2d85ae960f63afad1bf576355cc499c2de0a418db84430b464ffd42ac86bc4ed786c300c79dcdd50000000000000000000000000000000000000000000000000000000000000001bc7936b810d2110df85cad97c81bd64baa2489a26ae9b539c87b6f4603200d67d6a2c4dc85889103d27b14bcbf77759ac5e1d0cd4b9c393c6148b2d2e5e1af39c224c4ba37763ae260b4ce925df64612be60ac67a2e9eae2ce168781b6ecbae18000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d9100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b2a777d4578000000000000000000000000000000000000000000000000002e0b2aad49003600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000dc20a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6563b3b6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5463354d6a55794d7930794f446b304c5455344d6d4d744f4442694e53307959546b345a6d56694e6d5531596d516966513d3d000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000007a8044be44e114ee073b384733252255871a5f060000000000000000000000000000000000000000000000000000000035bdf8b4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x014766027ccda2b9a80caee44f54df7da6d9e4ee4523c7117a0928fc7fb0881b",
      "signature": {
        "s": "0x1bf576355cc499c2de0a418db84430b464ffd42ac86bc4ed786c300c79dcdd50",
        "r": "0xe134a2a35e6ac36ee4d89873f782a945c393d17deac42cae2d85ae960f63afad",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc7936b810d2110df85cad97c81bd64baa2489a26ae9b539c87b6f4603200d67d",
      "signature": {
        "s": "0x224c4ba37763ae260b4ce925df64612be60ac67a2e9eae2ce168781b6ecbae18",
        "r": "0x6a2c4dc85889103d27b14bcbf77759ac5e1d0cd4b9c393c6148b2d2e5e1af39c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "901642420",
    "total": "901642420"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "901642420",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "57535607734"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "901642"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiZTc5MjUyMy0yODk0LTU4MmMtODBiNS0yYTk4ZmViNmU1YmQifQ==",
    "nonce": 7569,
    "balances": {
      "current": "12960125949920632",
      "previous": "12960126852464694"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7a8044be44e114ee073b384733252255871a5f06",
    "nonce": 12,
    "balances": {
      "current": "901642420",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:45.124Z",
  "updated": "2020-05-22T08:57:46.180Z",
  "id": "5ec79409e5756b00111b890d"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000035bdf8b4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `901642420`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`