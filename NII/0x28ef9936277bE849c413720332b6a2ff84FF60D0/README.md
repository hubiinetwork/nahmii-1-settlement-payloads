# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x28ef9936277bE849c413720332b6a2ff84FF60D0`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000358ad9b256c591f5b00000000000000000000000000000000000000000000000000000002125c4a890000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002125c4a890000000000000000000000000000000000000000000000000000003059a1577a9a17f7c8cce23558ccab744aac6ff4d88ee7d86d147c04f934330b8c43edebd127d2aa0bb8c233b0cf22155e1a301edbe2e042d2c3f2026eb1c99fcca64a9fcd08e3161c2de9007d18d1f3de6bf321ecaef5e2a77e919eff36edfe3963e9a4aa000000000000000000000000000000000000000000000000000000000000001b5ce25fe69b80069a61011671ab8c6e54d5789de52db8bdb6200b3f61ea10d4364b18a8652f62d5cae9c0437ead8546c0ab6ea8de46c77b592535c02c7e604ad91a1b48119f52ac55d151aaa077ea9e8c0d7de819679a26f795abe8f1b6ea8a9f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af94000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000005384783569fa270c1fd9000000000000000000000000000000000000000000005384783569fc39f0301600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000087c5b40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7060f69d28e2b65dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6d45784d6d4d784e7930305954466b4c5456695a6d4d74595451774e7930325a6a51794e3251334d6d5a694e32556966513d3d000000000000000000000000000000000000000000000000000000000000002100000000000000000000000028ef9936277be849c413720332b6a2ff84ff60d000000000000000000000000000000000000000000000000358ad9b256c591f5b00000000000000000000000000000000000000000000000358ad9b2359fcd4d200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9a17f7c8cce23558ccab744aac6ff4d88ee7d86d147c04f934330b8c43edebd1",
      "signature": {
        "s": "0x08e3161c2de9007d18d1f3de6bf321ecaef5e2a77e919eff36edfe3963e9a4aa",
        "r": "0x27d2aa0bb8c233b0cf22155e1a301edbe2e042d2c3f2026eb1c99fcca64a9fcd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5ce25fe69b80069a61011671ab8c6e54d5789de52db8bdb6200b3f61ea10d436",
      "signature": {
        "s": "0x1a1b48119f52ac55d151aaa077ea9e8c0d7de819679a26f795abe8f1b6ea8a9f",
        "r": "0x4b18a8652f62d5cae9c0437ead8546c0ab6ea8de46c77b592535c02c7e604ad9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8897972873",
    "total": "207662176122"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8897972873",
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
            "amount": "27578319074237707150813"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8897972"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZmExMmMxNy00YTFkLTViZmMtYTQwNy02ZjQyN2Q3MmZiN2UifQ==",
    "nonce": 110484,
    "balances": {
      "current": "394400050241891648413657",
      "previous": "394400050241900555284502"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x28ef9936277be849c413720332b6a2ff84ff60d0",
    "nonce": 33,
    "balances": {
      "current": "61730166252471131995",
      "previous": "61730166243573159122"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:31.494Z",
  "updated": "2022-05-04T08:53:31.580Z",
  "id": "62723f0bbbd75600116d0578"
}
```
* *stageAmount*: `61730166252471131995`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000002125c4a890000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002125c4a890000000000000000000000000000000000000000000000000000003059a1577a9a17f7c8cce23558ccab744aac6ff4d88ee7d86d147c04f934330b8c43edebd127d2aa0bb8c233b0cf22155e1a301edbe2e042d2c3f2026eb1c99fcca64a9fcd08e3161c2de9007d18d1f3de6bf321ecaef5e2a77e919eff36edfe3963e9a4aa000000000000000000000000000000000000000000000000000000000000001b5ce25fe69b80069a61011671ab8c6e54d5789de52db8bdb6200b3f61ea10d4364b18a8652f62d5cae9c0437ead8546c0ab6ea8de46c77b592535c02c7e604ad91a1b48119f52ac55d151aaa077ea9e8c0d7de819679a26f795abe8f1b6ea8a9f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af94000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000005384783569fa270c1fd9000000000000000000000000000000000000000000005384783569fc39f0301600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000087c5b40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7060f69d28e2b65dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6d45784d6d4d784e7930305954466b4c5456695a6d4d74595451774e7930325a6a51794e3251334d6d5a694e32556966513d3d000000000000000000000000000000000000000000000000000000000000002100000000000000000000000028ef9936277be849c413720332b6a2ff84ff60d000000000000000000000000000000000000000000000000358ad9b256c591f5b00000000000000000000000000000000000000000000000358ad9b2359fcd4d200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9a17f7c8cce23558ccab744aac6ff4d88ee7d86d147c04f934330b8c43edebd1",
      "signature": {
        "s": "0x08e3161c2de9007d18d1f3de6bf321ecaef5e2a77e919eff36edfe3963e9a4aa",
        "r": "0x27d2aa0bb8c233b0cf22155e1a301edbe2e042d2c3f2026eb1c99fcca64a9fcd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5ce25fe69b80069a61011671ab8c6e54d5789de52db8bdb6200b3f61ea10d436",
      "signature": {
        "s": "0x1a1b48119f52ac55d151aaa077ea9e8c0d7de819679a26f795abe8f1b6ea8a9f",
        "r": "0x4b18a8652f62d5cae9c0437ead8546c0ab6ea8de46c77b592535c02c7e604ad9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8897972873",
    "total": "207662176122"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8897972873",
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
            "amount": "27578319074237707150813"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8897972"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZmExMmMxNy00YTFkLTViZmMtYTQwNy02ZjQyN2Q3MmZiN2UifQ==",
    "nonce": 110484,
    "balances": {
      "current": "394400050241891648413657",
      "previous": "394400050241900555284502"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x28ef9936277be849c413720332b6a2ff84ff60d0",
    "nonce": 33,
    "balances": {
      "current": "61730166252471131995",
      "previous": "61730166243573159122"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:31.494Z",
  "updated": "2022-05-04T08:53:31.580Z",
  "id": "62723f0bbbd75600116d0578"
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
0x0f200f9b00000000000000000000000000000000000000000000000358ad9b256c591f5b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `61730166252471131995`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`