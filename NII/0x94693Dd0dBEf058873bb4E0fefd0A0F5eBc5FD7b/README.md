# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x94693Dd0dBEf058873bb4E0fefd0A0F5eBc5FD7b`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000028533cf16633146600000000000000000000000000000000000000000000000005280d4341fc411080000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005280d4341fc411080000000000000000000000000000000000000000000000028533cf16633146601ea8b46c54480e53bfc0534098d2a19da7d5dd0113d516f4a5a1f5ad677be70d4c12996761119a9d40127fd2daded28382b5c83d900e4b12ed2c6cfb81605a2d00e7543d091583e7326a0e076b7e3ed02ed0a53fb6a1a9b7fde227dffcd8ca44000000000000000000000000000000000000000000000000000000000000001cbce1a620d357dc162174c7d1556c76b8d1f409b192dba9a30c8b9577054391b7254cbbc99a3f7822f5ee800b5e96bce04284314489e6aec595107bf42d1447f768da12e646136a0d252419759c0012b724e0128b1f7b7284d32b996c071d3966000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000b3cb030000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000fe24000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000236f1e633f664a43acde00000000000000000000000000000000000000000000236f70f932890eed0ecf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000151eeea4e550e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002b6fb3f6ae2d5a219ed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e44646b5a6d59795a4330304e5751784c5455304f5441744f4441344e7931695a4756694d7a6b314e4749344d44636966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000094693dd0dbef058873bb4e0fefd0a0f5ebc5fd7b0000000000000000000000000000000000000000000000028533cf166331466000000000000000000000000000000000000000000000000232b2fae2436d355800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1ea8b46c54480e53bfc0534098d2a19da7d5dd0113d516f4a5a1f5ad677be70d",
      "signature": {
        "s": "0x00e7543d091583e7326a0e076b7e3ed02ed0a53fb6a1a9b7fde227dffcd8ca44",
        "r": "0x4c12996761119a9d40127fd2daded28382b5c83d900e4b12ed2c6cfb81605a2d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbce1a620d357dc162174c7d1556c76b8d1f409b192dba9a30c8b9577054391b7",
      "signature": {
        "s": "0x68da12e646136a0d252419759c0012b724e0128b1f7b7284d32b996c071d3966",
        "r": "0x254cbbc99a3f7822f5ee800b5e96bce04284314489e6aec595107bf42d1447f7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5944984828465385736",
    "total": "46491731073336165984"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5944984828465385736",
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
            "amount": "12820144693703960828397"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5944984828465385"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NDdkZmYyZC00NWQxLTU0OTAtODA4Ny1iZGViMzk1NGI4MDcifQ==",
    "nonce": 65060,
    "balances": {
      "current": "167332605156171740064990",
      "previous": "167338556085985033916111"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x94693dd0dbef058873bb4e0fefd0a0f5ebc5fd7b",
    "nonce": 3,
    "balances": {
      "current": "46491731073336165984",
      "previous": "40546746244870780248"
    }
  },
  "blockNumber": "11782915",
  "created": "2021-02-03T11:09:04.115Z",
  "updated": "2021-02-03T11:09:04.208Z",
  "id": "601a845078236f0011162604"
}
```
* *stageAmount*: `46491731073336165984`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000005280d4341fc411080000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005280d4341fc411080000000000000000000000000000000000000000000000028533cf16633146601ea8b46c54480e53bfc0534098d2a19da7d5dd0113d516f4a5a1f5ad677be70d4c12996761119a9d40127fd2daded28382b5c83d900e4b12ed2c6cfb81605a2d00e7543d091583e7326a0e076b7e3ed02ed0a53fb6a1a9b7fde227dffcd8ca44000000000000000000000000000000000000000000000000000000000000001cbce1a620d357dc162174c7d1556c76b8d1f409b192dba9a30c8b9577054391b7254cbbc99a3f7822f5ee800b5e96bce04284314489e6aec595107bf42d1447f768da12e646136a0d252419759c0012b724e0128b1f7b7284d32b996c071d3966000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000b3cb030000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000fe24000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000236f1e633f664a43acde00000000000000000000000000000000000000000000236f70f932890eed0ecf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000151eeea4e550e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002b6fb3f6ae2d5a219ed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e44646b5a6d59795a4330304e5751784c5455304f5441744f4441344e7931695a4756694d7a6b314e4749344d44636966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000094693dd0dbef058873bb4e0fefd0a0f5ebc5fd7b0000000000000000000000000000000000000000000000028533cf166331466000000000000000000000000000000000000000000000000232b2fae2436d355800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1ea8b46c54480e53bfc0534098d2a19da7d5dd0113d516f4a5a1f5ad677be70d",
      "signature": {
        "s": "0x00e7543d091583e7326a0e076b7e3ed02ed0a53fb6a1a9b7fde227dffcd8ca44",
        "r": "0x4c12996761119a9d40127fd2daded28382b5c83d900e4b12ed2c6cfb81605a2d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbce1a620d357dc162174c7d1556c76b8d1f409b192dba9a30c8b9577054391b7",
      "signature": {
        "s": "0x68da12e646136a0d252419759c0012b724e0128b1f7b7284d32b996c071d3966",
        "r": "0x254cbbc99a3f7822f5ee800b5e96bce04284314489e6aec595107bf42d1447f7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5944984828465385736",
    "total": "46491731073336165984"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5944984828465385736",
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
            "amount": "12820144693703960828397"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5944984828465385"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NDdkZmYyZC00NWQxLTU0OTAtODA4Ny1iZGViMzk1NGI4MDcifQ==",
    "nonce": 65060,
    "balances": {
      "current": "167332605156171740064990",
      "previous": "167338556085985033916111"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x94693dd0dbef058873bb4e0fefd0a0f5ebc5fd7b",
    "nonce": 3,
    "balances": {
      "current": "46491731073336165984",
      "previous": "40546746244870780248"
    }
  },
  "blockNumber": "11782915",
  "created": "2021-02-03T11:09:04.115Z",
  "updated": "2021-02-03T11:09:04.208Z",
  "id": "601a845078236f0011162604"
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
0x0f200f9b0000000000000000000000000000000000000000000000028533cf16633146600000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `46491731073336165984`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`