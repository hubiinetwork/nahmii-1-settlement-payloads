# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x38291B8A510161b890Af154e81c88a98C4505Ae6`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000209b99d13d100000000000000000000000000000000000000000000000000000209b99d13d1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000209b99d13d100000000000000000000000000000000000000000000000000000209b99d13d1502d1e788d1a3d54fd63aef7acadbeff1cc95b7efb9d761c3e9d48c95c4b0f26085a9a52595e66249a888861617a1e93884749041dbee1629d1e0b2dd24b9c9c5f1668d9fb4b5b0f1cb86557afc96ad30c92598288679e96982c180d7de3e61e000000000000000000000000000000000000000000000000000000000000001bd17ccca166448e56099d3de26d9f7e4603344840d20f9cf05447627041e4aa53e8347f836edb07e6ebb5316b96cbbe35bd7c5b2bffb895d5095315d2af79d9c2709cd667aa49d59e16d154af508f99fab296c368609adc79807b3149bcefaf55000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000149500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2c76185efa21000000000000000000000000000000000000000000000000002e2e80578bd3da00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000858fc5e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004e1853feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d4445794f475530595330354e5459784c545530596d45744f475668596930334e4455324d6a6b33596a59325a54516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000038291b8a510161b890af154e81c88a98c4505ae600000000000000000000000000000000000000000000000000000209b99d13d1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x502d1e788d1a3d54fd63aef7acadbeff1cc95b7efb9d761c3e9d48c95c4b0f26",
      "signature": {
        "s": "0x5f1668d9fb4b5b0f1cb86557afc96ad30c92598288679e96982c180d7de3e61e",
        "r": "0x085a9a52595e66249a888861617a1e93884749041dbee1629d1e0b2dd24b9c9c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd17ccca166448e56099d3de26d9f7e4603344840d20f9cf05447627041e4aa53",
      "signature": {
        "s": "0x709cd667aa49d59e16d154af508f99fab296c368609adc79807b3149bcefaf55",
        "r": "0xe8347f836edb07e6ebb5316b96cbbe35bd7c5b2bffb895d5095315d2af79d9c2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2240792040401",
    "total": "2240792040401"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2240792040401",
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
            "amount": "20963475435"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2240792040"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMDEyOGU0YS05NTYxLTU0YmEtOGVhYi03NDU2Mjk3YjY2ZTQifQ==",
    "nonce": 5269,
    "balances": {
      "current": "12996734655330849",
      "previous": "12998977688163290"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x38291b8a510161b890af154e81c88a98c4505ae6",
    "nonce": 22,
    "balances": {
      "current": "2240792040401",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:47.487Z",
  "updated": "2020-05-22T08:39:47.555Z",
  "id": "5ec78fd3b0c6090011d5af9b"
}
```
* *stageAmount*: `2240792040401`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000209b99d13d1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000209b99d13d100000000000000000000000000000000000000000000000000000209b99d13d1502d1e788d1a3d54fd63aef7acadbeff1cc95b7efb9d761c3e9d48c95c4b0f26085a9a52595e66249a888861617a1e93884749041dbee1629d1e0b2dd24b9c9c5f1668d9fb4b5b0f1cb86557afc96ad30c92598288679e96982c180d7de3e61e000000000000000000000000000000000000000000000000000000000000001bd17ccca166448e56099d3de26d9f7e4603344840d20f9cf05447627041e4aa53e8347f836edb07e6ebb5316b96cbbe35bd7c5b2bffb895d5095315d2af79d9c2709cd667aa49d59e16d154af508f99fab296c368609adc79807b3149bcefaf55000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000149500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2c76185efa21000000000000000000000000000000000000000000000000002e2e80578bd3da00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000858fc5e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004e1853feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d4445794f475530595330354e5459784c545530596d45744f475668596930334e4455324d6a6b33596a59325a54516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000038291b8a510161b890af154e81c88a98c4505ae600000000000000000000000000000000000000000000000000000209b99d13d1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x502d1e788d1a3d54fd63aef7acadbeff1cc95b7efb9d761c3e9d48c95c4b0f26",
      "signature": {
        "s": "0x5f1668d9fb4b5b0f1cb86557afc96ad30c92598288679e96982c180d7de3e61e",
        "r": "0x085a9a52595e66249a888861617a1e93884749041dbee1629d1e0b2dd24b9c9c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd17ccca166448e56099d3de26d9f7e4603344840d20f9cf05447627041e4aa53",
      "signature": {
        "s": "0x709cd667aa49d59e16d154af508f99fab296c368609adc79807b3149bcefaf55",
        "r": "0xe8347f836edb07e6ebb5316b96cbbe35bd7c5b2bffb895d5095315d2af79d9c2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2240792040401",
    "total": "2240792040401"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2240792040401",
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
            "amount": "20963475435"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2240792040"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMDEyOGU0YS05NTYxLTU0YmEtOGVhYi03NDU2Mjk3YjY2ZTQifQ==",
    "nonce": 5269,
    "balances": {
      "current": "12996734655330849",
      "previous": "12998977688163290"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x38291b8a510161b890af154e81c88a98c4505ae6",
    "nonce": 22,
    "balances": {
      "current": "2240792040401",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:47.487Z",
  "updated": "2020-05-22T08:39:47.555Z",
  "id": "5ec78fd3b0c6090011d5af9b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000209b99d13d1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2240792040401`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`