# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x00d97D7f128D251Cfd3Bd638FE300Abf3037C736`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000042b000000000000000000000000000000000000000000000000000000000000042b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000042b000000000000000000000000000000000000000000000000000000000000042b5b5c69bbc86f133a4acdead2fd5f4d43f3f6ecc89328efed94e44df44ac7081432db35a196aa500d41927abd188b9a4db2adc972d4f79bf15bdd8dcc3f66c3c608c6e0ce9f0c02e4eefd79cc36d0eca0947dd22b8b485a76fe3e735f116a2487000000000000000000000000000000000000000000000000000000000000001c3f47134fce602818f8178393c2aa592e03b91ee2da5359ca2ad6647e37e99e577762e1173353d0a18af8d085a629a2ed85df58fe25b8d107bc0654e879bf6e8603473f04b2fbff4cebdfca58dd350d94449661b58cd14a10c76972b4198da618000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56660000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000153100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d717775f48c000000000000000000000000000000000000000000000000002e1d717775f8b800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008b8c31da3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e7a6c6b4e445a6d4d7930334f4446694c54553259324574595467344f5330355a6a63324d3245325a6a41794d57496966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000000d97d7f128d251cfd3bd638fe300abf3037c736000000000000000000000000000000000000000000000000000000000000042b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5b5c69bbc86f133a4acdead2fd5f4d43f3f6ecc89328efed94e44df44ac70814",
      "signature": {
        "s": "0x08c6e0ce9f0c02e4eefd79cc36d0eca0947dd22b8b485a76fe3e735f116a2487",
        "r": "0x32db35a196aa500d41927abd188b9a4db2adc972d4f79bf15bdd8dcc3f66c3c6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3f47134fce602818f8178393c2aa592e03b91ee2da5359ca2ad6647e37e99e57",
      "signature": {
        "s": "0x03473f04b2fbff4cebdfca58dd350d94449661b58cd14a10c76972b4198da618",
        "r": "0x7762e1173353d0a18af8d085a629a2ed85df58fe25b8d107bc0654e879bf6e86",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1067",
    "total": "1067"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1067",
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
            "amount": "37459533219"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NzlkNDZmMy03ODFiLTU2Y2EtYTg4OS05Zjc2M2E2ZjAyMWIifQ==",
    "nonce": 5425,
    "balances": {
      "current": "12980222101419148",
      "previous": "12980222101420216"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x00d97d7f128d251cfd3bd638fe300abf3037c736",
    "nonce": 21,
    "balances": {
      "current": "1067",
      "previous": "0"
    }
  },
  "blockNumber": "10114662",
  "created": "2020-05-22T08:41:00.611Z",
  "updated": "2020-05-22T08:41:00.858Z",
  "id": "5ec7901c005df800101bc94f"
}
```
* *stageAmount*: `1067`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000042b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000042b000000000000000000000000000000000000000000000000000000000000042b5b5c69bbc86f133a4acdead2fd5f4d43f3f6ecc89328efed94e44df44ac7081432db35a196aa500d41927abd188b9a4db2adc972d4f79bf15bdd8dcc3f66c3c608c6e0ce9f0c02e4eefd79cc36d0eca0947dd22b8b485a76fe3e735f116a2487000000000000000000000000000000000000000000000000000000000000001c3f47134fce602818f8178393c2aa592e03b91ee2da5359ca2ad6647e37e99e577762e1173353d0a18af8d085a629a2ed85df58fe25b8d107bc0654e879bf6e8603473f04b2fbff4cebdfca58dd350d94449661b58cd14a10c76972b4198da618000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56660000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000153100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d717775f48c000000000000000000000000000000000000000000000000002e1d717775f8b800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008b8c31da3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e7a6c6b4e445a6d4d7930334f4446694c54553259324574595467344f5330355a6a63324d3245325a6a41794d57496966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000000d97d7f128d251cfd3bd638fe300abf3037c736000000000000000000000000000000000000000000000000000000000000042b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5b5c69bbc86f133a4acdead2fd5f4d43f3f6ecc89328efed94e44df44ac70814",
      "signature": {
        "s": "0x08c6e0ce9f0c02e4eefd79cc36d0eca0947dd22b8b485a76fe3e735f116a2487",
        "r": "0x32db35a196aa500d41927abd188b9a4db2adc972d4f79bf15bdd8dcc3f66c3c6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3f47134fce602818f8178393c2aa592e03b91ee2da5359ca2ad6647e37e99e57",
      "signature": {
        "s": "0x03473f04b2fbff4cebdfca58dd350d94449661b58cd14a10c76972b4198da618",
        "r": "0x7762e1173353d0a18af8d085a629a2ed85df58fe25b8d107bc0654e879bf6e86",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1067",
    "total": "1067"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1067",
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
            "amount": "37459533219"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NzlkNDZmMy03ODFiLTU2Y2EtYTg4OS05Zjc2M2E2ZjAyMWIifQ==",
    "nonce": 5425,
    "balances": {
      "current": "12980222101419148",
      "previous": "12980222101420216"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x00d97d7f128d251cfd3bd638fe300abf3037c736",
    "nonce": 21,
    "balances": {
      "current": "1067",
      "previous": "0"
    }
  },
  "blockNumber": "10114662",
  "created": "2020-05-22T08:41:00.611Z",
  "updated": "2020-05-22T08:41:00.858Z",
  "id": "5ec7901c005df800101bc94f"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000042b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1067`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`