# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6A67C614506d4526D45AacAe121c4944AC35eC0B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000001138e900000000000000000000000000000000000000000000000000000000001138e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000001138e900000000000000000000000000000000000000000000000000000000001138e9c5bc713229330bab5e366a61ee1513fd778a376a8cf5502333265242c62d1ff77f536be528064f5749cf42037e801a221a26e1f3233fb2195b9a888fc7f14f27099131d47d65d35b2d005e6cb05b6b9d5b82098e63f70127cea9f4d2abe50f6b000000000000000000000000000000000000000000000000000000000000001c86d9567ccb49d586083c4a0ad1268610778ec0769ca7e8f5990ce4ed834f3a95cc63f01f83fa49f73208230baccb2662f812a3f711bf3edf97f53feeb46aff8a1e7c77d4325b197bd211a86fa9ace57bbe86bc3acb1af4e17e226f2ca6325fcc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000189200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ab902e655e6000000000000000000000000000000000000000000000000002e1ab902f7933700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000468000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096ae068a7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f4467784f4751314d43316a596a4d7a4c54566a4e7a63744f446b345a5331694f4446694d4746684d574e6b4d54456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006a67c614506d4526d45aacae121c4944ac35ec0b00000000000000000000000000000000000000000000000000000000001138e9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc5bc713229330bab5e366a61ee1513fd778a376a8cf5502333265242c62d1ff7",
      "signature": {
        "s": "0x099131d47d65d35b2d005e6cb05b6b9d5b82098e63f70127cea9f4d2abe50f6b",
        "r": "0x7f536be528064f5749cf42037e801a221a26e1f3233fb2195b9a888fc7f14f27",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x86d9567ccb49d586083c4a0ad1268610778ec0769ca7e8f5990ce4ed834f3a95",
      "signature": {
        "s": "0x1e7c77d4325b197bd211a86fa9ace57bbe86bc3acb1af4e17e226f2ca6325fcc",
        "r": "0xcc63f01f83fa49f73208230baccb2662f812a3f711bf3edf97f53feeb46aff8a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1128681",
    "total": "1128681"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1128681",
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
            "amount": "40447797415"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1128"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkODgxOGQ1MC1jYjMzLTVjNzctODk4ZS1iODFiMGFhMWNkMTEifQ==",
    "nonce": 6290,
    "balances": {
      "current": "12977230848611814",
      "previous": "12977230849741623"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6a67c614506d4526d45aacae121c4944ac35ec0b",
    "nonce": 22,
    "balances": {
      "current": "1128681",
      "previous": "0"
    }
  },
  "blockNumber": "10114698",
  "created": "2020-05-22T08:47:56.151Z",
  "updated": "2020-05-22T08:47:56.218Z",
  "id": "5ec791bce5756b00111b8782"
}
```
* *stageAmount*: `1128681`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000001138e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000001138e900000000000000000000000000000000000000000000000000000000001138e9c5bc713229330bab5e366a61ee1513fd778a376a8cf5502333265242c62d1ff77f536be528064f5749cf42037e801a221a26e1f3233fb2195b9a888fc7f14f27099131d47d65d35b2d005e6cb05b6b9d5b82098e63f70127cea9f4d2abe50f6b000000000000000000000000000000000000000000000000000000000000001c86d9567ccb49d586083c4a0ad1268610778ec0769ca7e8f5990ce4ed834f3a95cc63f01f83fa49f73208230baccb2662f812a3f711bf3edf97f53feeb46aff8a1e7c77d4325b197bd211a86fa9ace57bbe86bc3acb1af4e17e226f2ca6325fcc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000189200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ab902e655e6000000000000000000000000000000000000000000000000002e1ab902f7933700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000468000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096ae068a7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f4467784f4751314d43316a596a4d7a4c54566a4e7a63744f446b345a5331694f4446694d4746684d574e6b4d54456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006a67c614506d4526d45aacae121c4944ac35ec0b00000000000000000000000000000000000000000000000000000000001138e9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc5bc713229330bab5e366a61ee1513fd778a376a8cf5502333265242c62d1ff7",
      "signature": {
        "s": "0x099131d47d65d35b2d005e6cb05b6b9d5b82098e63f70127cea9f4d2abe50f6b",
        "r": "0x7f536be528064f5749cf42037e801a221a26e1f3233fb2195b9a888fc7f14f27",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x86d9567ccb49d586083c4a0ad1268610778ec0769ca7e8f5990ce4ed834f3a95",
      "signature": {
        "s": "0x1e7c77d4325b197bd211a86fa9ace57bbe86bc3acb1af4e17e226f2ca6325fcc",
        "r": "0xcc63f01f83fa49f73208230baccb2662f812a3f711bf3edf97f53feeb46aff8a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1128681",
    "total": "1128681"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1128681",
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
            "amount": "40447797415"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1128"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkODgxOGQ1MC1jYjMzLTVjNzctODk4ZS1iODFiMGFhMWNkMTEifQ==",
    "nonce": 6290,
    "balances": {
      "current": "12977230848611814",
      "previous": "12977230849741623"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6a67c614506d4526d45aacae121c4944ac35ec0b",
    "nonce": 22,
    "balances": {
      "current": "1128681",
      "previous": "0"
    }
  },
  "blockNumber": "10114698",
  "created": "2020-05-22T08:47:56.151Z",
  "updated": "2020-05-22T08:47:56.218Z",
  "id": "5ec791bce5756b00111b8782"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000001138e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1128681`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`