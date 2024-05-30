# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x91977D46d97E342C758f467f479d3cd6036f6A65`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000001243618efe7c4f9c7340000000000000000000000000000000000000000000000057318f9ec4f4c42580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000057318f9ec4f4c42580000000000000000000000000000000000000000000001243618efe7c4f9c7342afa7ef6955520c2916665f5fbe74b7064d27cf0b8497fd21e5edcff68385c69a9fac545d3029334a35ebbffc4feaa88a7c7668717772166d7edbf22caca041359717619e4faf8112efc9ddb4276b13b5749ec13d9d4eb630df2899c4d1f0f28000000000000000000000000000000000000000000000000000000000000001c724ed6b2e293c96ff0dc0196ce640bf92c3bd336d33d85911a83c68fdb56de3ce22da351b88d2b7d8ba3dd6deaec81d57073ba7944a825ea75c9dafc2c2e101a10a3468c885935aa3150b1e55e18084f229848c723b5d8958fb47beb8a88c21d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b62e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003190c7bd3a771fb73a980000000000000000000000000000000000000000000031963c3b59809913b13a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000165251d2a10344a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfb4e8ea8261eedbb90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a6b774d5759344e6930774e32597a4c5455794f544574596a46694d69316b4f54646a595455304f54426d4d54596966513d3d000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000091977d46d97e342c758f467f479d3cd6036f6a650000000000000000000000000000000000000000000001243618efe7c4f9c73400000000000000000000000000000000000000000000011ec2fff5fb75ad84dc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2afa7ef6955520c2916665f5fbe74b7064d27cf0b8497fd21e5edcff68385c69",
      "signature": {
        "s": "0x59717619e4faf8112efc9ddb4276b13b5749ec13d9d4eb630df2899c4d1f0f28",
        "r": "0xa9fac545d3029334a35ebbffc4feaa88a7c7668717772166d7edbf22caca0413",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x724ed6b2e293c96ff0dc0196ce640bf92c3bd336d33d85911a83c68fdb56de3c",
      "signature": {
        "s": "0x10a3468c885935aa3150b1e55e18084f229848c723b5d8958fb47beb8a88c21d",
        "r": "0xe22da351b88d2b7d8ba3dd6deaec81d57073ba7944a825ea75c9dafc2c2e101a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "100527373875688522328",
    "total": "5390347398779399423796"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "100527373875688522328",
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
            "amount": "27738492269752589671353"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "100527373875688522"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YjkwMWY4Ni0wN2YzLTUyOTEtYjFiMi1kOTdjYTU0OTBmMTYifQ==",
    "nonce": 112174,
    "balances": {
      "current": "234066681531494244498072",
      "previous": "234167309432743808708922"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x91977d46d97e342c758f467f479d3cd6036f6a65",
    "nonce": 12,
    "balances": {
      "current": "5390347398779399423796",
      "previous": "5289820024903710901468"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:23.754Z",
  "updated": "2022-05-04T09:02:23.817Z",
  "id": "6272411fbbd75600116d0796"
}
```
* *stageAmount*: `5390347398779399423796`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000057318f9ec4f4c42580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000057318f9ec4f4c42580000000000000000000000000000000000000000000001243618efe7c4f9c7342afa7ef6955520c2916665f5fbe74b7064d27cf0b8497fd21e5edcff68385c69a9fac545d3029334a35ebbffc4feaa88a7c7668717772166d7edbf22caca041359717619e4faf8112efc9ddb4276b13b5749ec13d9d4eb630df2899c4d1f0f28000000000000000000000000000000000000000000000000000000000000001c724ed6b2e293c96ff0dc0196ce640bf92c3bd336d33d85911a83c68fdb56de3ce22da351b88d2b7d8ba3dd6deaec81d57073ba7944a825ea75c9dafc2c2e101a10a3468c885935aa3150b1e55e18084f229848c723b5d8958fb47beb8a88c21d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b62e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003190c7bd3a771fb73a980000000000000000000000000000000000000000000031963c3b59809913b13a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000165251d2a10344a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfb4e8ea8261eedbb90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a6b774d5759344e6930774e32597a4c5455794f544574596a46694d69316b4f54646a595455304f54426d4d54596966513d3d000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000091977d46d97e342c758f467f479d3cd6036f6a650000000000000000000000000000000000000000000001243618efe7c4f9c73400000000000000000000000000000000000000000000011ec2fff5fb75ad84dc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2afa7ef6955520c2916665f5fbe74b7064d27cf0b8497fd21e5edcff68385c69",
      "signature": {
        "s": "0x59717619e4faf8112efc9ddb4276b13b5749ec13d9d4eb630df2899c4d1f0f28",
        "r": "0xa9fac545d3029334a35ebbffc4feaa88a7c7668717772166d7edbf22caca0413",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x724ed6b2e293c96ff0dc0196ce640bf92c3bd336d33d85911a83c68fdb56de3c",
      "signature": {
        "s": "0x10a3468c885935aa3150b1e55e18084f229848c723b5d8958fb47beb8a88c21d",
        "r": "0xe22da351b88d2b7d8ba3dd6deaec81d57073ba7944a825ea75c9dafc2c2e101a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "100527373875688522328",
    "total": "5390347398779399423796"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "100527373875688522328",
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
            "amount": "27738492269752589671353"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "100527373875688522"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YjkwMWY4Ni0wN2YzLTUyOTEtYjFiMi1kOTdjYTU0OTBmMTYifQ==",
    "nonce": 112174,
    "balances": {
      "current": "234066681531494244498072",
      "previous": "234167309432743808708922"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x91977d46d97e342c758f467f479d3cd6036f6a65",
    "nonce": 12,
    "balances": {
      "current": "5390347398779399423796",
      "previous": "5289820024903710901468"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:23.754Z",
  "updated": "2022-05-04T09:02:23.817Z",
  "id": "6272411fbbd75600116d0796"
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
0x0f200f9b0000000000000000000000000000000000000000000001243618efe7c4f9c7340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5390347398779399423796`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`