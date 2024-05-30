# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5fD045502157bE5D4548d676cB9d530d9a32ce10`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000029c67ced0000000000000000000000000000000000000000000000000000000029c67ced000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000029c67ced0000000000000000000000000000000000000000000000000000000029c67cedce01384f3938d1e4c6743da0cd80e7b97bdca1efc52b683cf67ffe81a732ff015fd53338343649a86954920c8962d3ca7db1b03f08ce5ab54e90f82664b7d3be1875eba41136ff9cc85c9d99bdc73cf2513358bc8b5614981f9417b46547afb6000000000000000000000000000000000000000000000000000000000000001b23bd32433376ad2a002169e4eae6075bf28994b156feac5b3f3f780a53189ffa1e0aaeb2f4648458ae0b51e386ac9c8a597436b3507d7d146b6bb09519d33fe21c1f161ae0c0deaf5549301920ffc72b504a45fa3b482ac3e9018178639da54b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b0f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15c4ebd48bf2000000000000000000000000000000000000000000000000002e15c515a5baa800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000ab1c9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aaf2eefa9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e3249784f44566b4e4331684d7a51794c5455784d6d5574596d4d774d4330795a4441795a4449355a54466c4f446b6966513d3d000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000005fd045502157be5d4548d676cb9d530d9a32ce100000000000000000000000000000000000000000000000000000000029c67ced000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xce01384f3938d1e4c6743da0cd80e7b97bdca1efc52b683cf67ffe81a732ff01",
      "signature": {
        "s": "0x1875eba41136ff9cc85c9d99bdc73cf2513358bc8b5614981f9417b46547afb6",
        "r": "0x5fd53338343649a86954920c8962d3ca7db1b03f08ce5ab54e90f82664b7d3be",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x23bd32433376ad2a002169e4eae6075bf28994b156feac5b3f3f780a53189ffa",
      "signature": {
        "s": "0x1c1f161ae0c0deaf5549301920ffc72b504a45fa3b482ac3e9018178639da54b",
        "r": "0x1e0aaeb2f4648458ae0b51e386ac9c8a597436b3507d7d146b6bb09519d33fe2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "700873965",
    "total": "700873965"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "700873965",
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
            "amount": "45888761769"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "700873"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlN2IxODVkNC1hMzQyLTUxMmUtYmMwMC0yZDAyZDI5ZTFlODkifQ==",
    "nonce": 6927,
    "balances": {
      "current": "12971784443038706",
      "previous": "12971785144613544"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5fd045502157be5d4548d676cb9d530d9a32ce10",
    "nonce": 11,
    "balances": {
      "current": "700873965",
      "previous": "0"
    }
  },
  "blockNumber": "10114721",
  "created": "2020-05-22T08:52:47.754Z",
  "updated": "2020-05-22T08:52:48.862Z",
  "id": "5ec792dfb0c6090011d5b1d5"
}
```
* *stageAmount*: `700873965`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000029c67ced000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000029c67ced0000000000000000000000000000000000000000000000000000000029c67cedce01384f3938d1e4c6743da0cd80e7b97bdca1efc52b683cf67ffe81a732ff015fd53338343649a86954920c8962d3ca7db1b03f08ce5ab54e90f82664b7d3be1875eba41136ff9cc85c9d99bdc73cf2513358bc8b5614981f9417b46547afb6000000000000000000000000000000000000000000000000000000000000001b23bd32433376ad2a002169e4eae6075bf28994b156feac5b3f3f780a53189ffa1e0aaeb2f4648458ae0b51e386ac9c8a597436b3507d7d146b6bb09519d33fe21c1f161ae0c0deaf5549301920ffc72b504a45fa3b482ac3e9018178639da54b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b0f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15c4ebd48bf2000000000000000000000000000000000000000000000000002e15c515a5baa800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000ab1c9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aaf2eefa9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e3249784f44566b4e4331684d7a51794c5455784d6d5574596d4d774d4330795a4441795a4449355a54466c4f446b6966513d3d000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000005fd045502157be5d4548d676cb9d530d9a32ce100000000000000000000000000000000000000000000000000000000029c67ced000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xce01384f3938d1e4c6743da0cd80e7b97bdca1efc52b683cf67ffe81a732ff01",
      "signature": {
        "s": "0x1875eba41136ff9cc85c9d99bdc73cf2513358bc8b5614981f9417b46547afb6",
        "r": "0x5fd53338343649a86954920c8962d3ca7db1b03f08ce5ab54e90f82664b7d3be",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x23bd32433376ad2a002169e4eae6075bf28994b156feac5b3f3f780a53189ffa",
      "signature": {
        "s": "0x1c1f161ae0c0deaf5549301920ffc72b504a45fa3b482ac3e9018178639da54b",
        "r": "0x1e0aaeb2f4648458ae0b51e386ac9c8a597436b3507d7d146b6bb09519d33fe2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "700873965",
    "total": "700873965"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "700873965",
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
            "amount": "45888761769"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "700873"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlN2IxODVkNC1hMzQyLTUxMmUtYmMwMC0yZDAyZDI5ZTFlODkifQ==",
    "nonce": 6927,
    "balances": {
      "current": "12971784443038706",
      "previous": "12971785144613544"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5fd045502157be5d4548d676cb9d530d9a32ce10",
    "nonce": 11,
    "balances": {
      "current": "700873965",
      "previous": "0"
    }
  },
  "blockNumber": "10114721",
  "created": "2020-05-22T08:52:47.754Z",
  "updated": "2020-05-22T08:52:48.862Z",
  "id": "5ec792dfb0c6090011d5b1d5"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000029c67ced000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `700873965`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`