# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1c27e1fe3ed8fD2435157C160106CD99eD1c14F1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000cd56c00000000000000000000000000000000000000000000000000000000000cd56c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000cd56c00000000000000000000000000000000000000000000000000000000000cd56c175b19224f7f7b1e4455acb24ffaba72c8bb48f28346cd7dce87e4a68e5da96dbeddb4c77e18db23ec1f13079912b36e2d4ae6fe1d90c5a8b7f72df13989350a0d29e077edd5586a88c90a95f53700c90ae5d3dbfb80a2632a320c069e1b5bc2000000000000000000000000000000000000000000000000000000000000001b64b6c360a1602cb44c2b2e2d23a1742428baf61bdb1357452dcc6760424f6055f850a344c4a0765d8784c23561b1848afa83016151ad319a06be65977ff0843229924bad7faf62091a7c080cd974746bdeac6964819a9d05f5763d0e6f7e2165000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000038400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cab55021000000000000000000000000000000000000000000000000002386f2cac228d600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000003490000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000882dd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6d466a4e5459304d69316b4d4464694c545533596a6374595441354d6931695957566d4d6a466b5a444977596d496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000001c27e1fe3ed8fd2435157c160106cd99ed1c14f100000000000000000000000000000000000000000000000000000000000cd56c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x175b19224f7f7b1e4455acb24ffaba72c8bb48f28346cd7dce87e4a68e5da96d",
      "signature": {
        "s": "0x0d29e077edd5586a88c90a95f53700c90ae5d3dbfb80a2632a320c069e1b5bc2",
        "r": "0xbeddb4c77e18db23ec1f13079912b36e2d4ae6fe1d90c5a8b7f72df13989350a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x64b6c360a1602cb44c2b2e2d23a1742428baf61bdb1357452dcc6760424f6055",
      "signature": {
        "s": "0x29924bad7faf62091a7c080cd974746bdeac6964819a9d05f5763d0e6f7e2165",
        "r": "0xf850a344c4a0765d8784c23561b1848afa83016151ad319a06be65977ff08432",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "841068",
    "total": "841068"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "841068",
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
            "amount": "557789"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "841"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MmFjNTY0Mi1kMDdiLTU3YjctYTA5Mi1iYWVmMjFkZDIwYmIifQ==",
    "nonce": 900,
    "balances": {
      "current": "10000001525960737",
      "previous": "10000001526802646"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1c27e1fe3ed8fd2435157c160106cd99ed1c14f1",
    "nonce": 20,
    "balances": {
      "current": "841068",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:19.911Z",
  "updated": "2020-05-22T08:05:19.981Z",
  "id": "5ec787bfe5756b00111b8097"
}
```
* *stageAmount*: `841068`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000cd56c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000cd56c00000000000000000000000000000000000000000000000000000000000cd56c175b19224f7f7b1e4455acb24ffaba72c8bb48f28346cd7dce87e4a68e5da96dbeddb4c77e18db23ec1f13079912b36e2d4ae6fe1d90c5a8b7f72df13989350a0d29e077edd5586a88c90a95f53700c90ae5d3dbfb80a2632a320c069e1b5bc2000000000000000000000000000000000000000000000000000000000000001b64b6c360a1602cb44c2b2e2d23a1742428baf61bdb1357452dcc6760424f6055f850a344c4a0765d8784c23561b1848afa83016151ad319a06be65977ff0843229924bad7faf62091a7c080cd974746bdeac6964819a9d05f5763d0e6f7e2165000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000038400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cab55021000000000000000000000000000000000000000000000000002386f2cac228d600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000003490000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000882dd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6d466a4e5459304d69316b4d4464694c545533596a6374595441354d6931695957566d4d6a466b5a444977596d496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000001c27e1fe3ed8fd2435157c160106cd99ed1c14f100000000000000000000000000000000000000000000000000000000000cd56c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x175b19224f7f7b1e4455acb24ffaba72c8bb48f28346cd7dce87e4a68e5da96d",
      "signature": {
        "s": "0x0d29e077edd5586a88c90a95f53700c90ae5d3dbfb80a2632a320c069e1b5bc2",
        "r": "0xbeddb4c77e18db23ec1f13079912b36e2d4ae6fe1d90c5a8b7f72df13989350a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x64b6c360a1602cb44c2b2e2d23a1742428baf61bdb1357452dcc6760424f6055",
      "signature": {
        "s": "0x29924bad7faf62091a7c080cd974746bdeac6964819a9d05f5763d0e6f7e2165",
        "r": "0xf850a344c4a0765d8784c23561b1848afa83016151ad319a06be65977ff08432",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "841068",
    "total": "841068"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "841068",
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
            "amount": "557789"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "841"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MmFjNTY0Mi1kMDdiLTU3YjctYTA5Mi1iYWVmMjFkZDIwYmIifQ==",
    "nonce": 900,
    "balances": {
      "current": "10000001525960737",
      "previous": "10000001526802646"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1c27e1fe3ed8fd2435157c160106cd99ed1c14f1",
    "nonce": 20,
    "balances": {
      "current": "841068",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:19.911Z",
  "updated": "2020-05-22T08:05:19.981Z",
  "id": "5ec787bfe5756b00111b8097"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000cd56c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `841068`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``