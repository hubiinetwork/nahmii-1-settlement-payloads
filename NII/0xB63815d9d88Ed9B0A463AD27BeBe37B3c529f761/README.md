# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB63815d9d88Ed9B0A463AD27BeBe37B3c529f761`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000028b4f209bae2b185360000000000000000000000000000000000000000000000014a478b9d6aa677ac0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000014a478b9d6aa677ac00000000000000000000000000000000000000000000002433f692870bc513e54fd75cae0a6964328be43d34023b845555cef608439da6eeb58615916159ed77871dfd6f5cbf5874ca673a4173a3bcbd6ac0e1f8e2c55a9339af84f4ac6704b3513ca154ba0281a980faeefe28910360d034721d01da0388b841aac782ec3238000000000000000000000000000000000000000000000000000000000000001c3b8bc23dbe24f4a8f48fb3ec26013b4464beca37c75f0758d6badd9eb957e40c2bd2ea864bd35001db08a0b1a64825410c3e210dfbae00a81831a6c4294d0ec430e3b3dd1fb3544cfa319b0dea752c51a6dfeb2c8a3fb456dedc812be75c86ef000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b462000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039af12d8257b6331c3690000000000000000000000000000000000000000000039b05d743e4ae1a9ce2500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000548d3213d193100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dda165f2b6ce4d1be60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e5451344f5745314d7931685a546c6b4c54566b4e446b745954597a4d69316d5a6d4d335932566b4e446b784e54556966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000b63815d9d88ed9b0a463ad27bebe37b3c529f761000000000000000000000000000000000000000000000028b4f209bae2b185360000000000000000000000000000000000000000000000276aaa7e1d780b0d8a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4fd75cae0a6964328be43d34023b845555cef608439da6eeb58615916159ed77",
      "signature": {
        "s": "0x513ca154ba0281a980faeefe28910360d034721d01da0388b841aac782ec3238",
        "r": "0x871dfd6f5cbf5874ca673a4173a3bcbd6ac0e1f8e2c55a9339af84f4ac6704b3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3b8bc23dbe24f4a8f48fb3ec26013b4464beca37c75f0758d6badd9eb957e40c",
      "signature": {
        "s": "0x30e3b3dd1fb3544cfa319b0dea752c51a6dfeb2c8a3fb456dedc812be75c86ef",
        "r": "0x2bd2ea864bd35001db08a0b1a64825410c3e210dfbae00a81831a6c4294d0ec4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "23799144264078096300",
    "total": "667827127902464709605"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23799144264078096300",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27700192823117750279142"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "23799144264078096"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NTQ4OWE1My1hZTlkLTVkNDktYTYzMi1mZmM3Y2VkNDkxNTUifQ==",
    "nonce": 111714,
    "balances": {
      "current": "272404427612968476328809",
      "previous": "272428250556376818503205"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb63815d9d88ed9b0a463ad27bebe37b3c529f761",
    "nonce": 36,
    "balances": {
      "current": "750908257517844923702",
      "previous": "727109113253766827402"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:46.496Z",
  "updated": "2022-05-04T08:59:46.683Z",
  "id": "627240827832e20011830d69"
}
```
* *stageAmount*: `750908257517844923702`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000014a478b9d6aa677ac0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000014a478b9d6aa677ac00000000000000000000000000000000000000000000002433f692870bc513e54fd75cae0a6964328be43d34023b845555cef608439da6eeb58615916159ed77871dfd6f5cbf5874ca673a4173a3bcbd6ac0e1f8e2c55a9339af84f4ac6704b3513ca154ba0281a980faeefe28910360d034721d01da0388b841aac782ec3238000000000000000000000000000000000000000000000000000000000000001c3b8bc23dbe24f4a8f48fb3ec26013b4464beca37c75f0758d6badd9eb957e40c2bd2ea864bd35001db08a0b1a64825410c3e210dfbae00a81831a6c4294d0ec430e3b3dd1fb3544cfa319b0dea752c51a6dfeb2c8a3fb456dedc812be75c86ef000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b462000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039af12d8257b6331c3690000000000000000000000000000000000000000000039b05d743e4ae1a9ce2500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000548d3213d193100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dda165f2b6ce4d1be60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e5451344f5745314d7931685a546c6b4c54566b4e446b745954597a4d69316d5a6d4d335932566b4e446b784e54556966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000b63815d9d88ed9b0a463ad27bebe37b3c529f761000000000000000000000000000000000000000000000028b4f209bae2b185360000000000000000000000000000000000000000000000276aaa7e1d780b0d8a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4fd75cae0a6964328be43d34023b845555cef608439da6eeb58615916159ed77",
      "signature": {
        "s": "0x513ca154ba0281a980faeefe28910360d034721d01da0388b841aac782ec3238",
        "r": "0x871dfd6f5cbf5874ca673a4173a3bcbd6ac0e1f8e2c55a9339af84f4ac6704b3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3b8bc23dbe24f4a8f48fb3ec26013b4464beca37c75f0758d6badd9eb957e40c",
      "signature": {
        "s": "0x30e3b3dd1fb3544cfa319b0dea752c51a6dfeb2c8a3fb456dedc812be75c86ef",
        "r": "0x2bd2ea864bd35001db08a0b1a64825410c3e210dfbae00a81831a6c4294d0ec4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "23799144264078096300",
    "total": "667827127902464709605"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23799144264078096300",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27700192823117750279142"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "23799144264078096"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NTQ4OWE1My1hZTlkLTVkNDktYTYzMi1mZmM3Y2VkNDkxNTUifQ==",
    "nonce": 111714,
    "balances": {
      "current": "272404427612968476328809",
      "previous": "272428250556376818503205"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb63815d9d88ed9b0a463ad27bebe37b3c529f761",
    "nonce": 36,
    "balances": {
      "current": "750908257517844923702",
      "previous": "727109113253766827402"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:46.496Z",
  "updated": "2022-05-04T08:59:46.683Z",
  "id": "627240827832e20011830d69"
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
0x0f200f9b000000000000000000000000000000000000000000000028b4f209bae2b185360000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `750908257517844923702`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`