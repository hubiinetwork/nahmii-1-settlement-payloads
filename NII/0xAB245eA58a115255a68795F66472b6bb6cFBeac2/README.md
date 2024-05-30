# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAB245eA58a115255a68795F66472b6bb6cFBeac2`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000e77725c6358cacb0000000000000000000000000000000000000000000004806bdb138ef05880000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000004806bdb138ef05880000000000000000000000000000000000000000000000004806bdb138ef0588000d4b4d4ae71c56aa295c2e0ea1c9f68224f22c197ce2f11eff61d476878d79e4918bbba7655f34a2292457113745d8c73492c4a51403aee3e6fd998456b84c5684a3745424fdee4dc1047884dd42907c93b8d846f477f0699bf356408fcb97b52000000000000000000000000000000000000000000000000000000000000001ba42c6cadeb1bffb089e873669e5524a9ff01e962aff1ae4680809c874887dd99f513693f27f36193a51b40ae0478b31bd8620552fd1928bffdb1707e1e76e89736433617c919bdda48e34f4bd4022381b37553237d4aa18a26d8b4f217ff82f0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e304b50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000ab245ea58a115255a68795f66472b6bb6cfbeac20000000000000000000000000000000000000000000000000e77725c6358cacb000000000000000000000000000000000000000000000481a1579b2fd2659acb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000001270515447eb450000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001270515447eb450000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a546b324e5745324d5330304d5759324c545131596a45744f544d794f533079596a646c4e6d4e684e44646d4e47496966513d3d00000000000000000000000000000000000000000000000000000000000000e5000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000ca52bc1a741a7d390a5f00000000000000000000000000000000000000000000c5d2503f608b8ce08a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd4b4d4ae71c56aa295c2e0ea1c9f68224f22c197ce2f11eff61d476878d79e49",
      "signature": {
        "s": "0x4a3745424fdee4dc1047884dd42907c93b8d846f477f0699bf356408fcb97b52",
        "r": "0x18bbba7655f34a2292457113745d8c73492c4a51403aee3e6fd998456b84c568",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa42c6cadeb1bffb089e873669e5524a9ff01e962aff1ae4680809c874887dd99",
      "signature": {
        "s": "0x36433617c919bdda48e34f4bd4022381b37553237d4aa18a26d8b4f217ff82f0",
        "r": "0xf513693f27f36193a51b40ae0478b31bd8620552fd1928bffdb1707e1e76e897",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21258421000000000000000",
    "total": "21258421000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21258421000000000000000",
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
            "amount": "21258421000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21258421000000000000"
      }
    },
    "wallet": "0xab245ea58a115255a68795f66472b6bb6cfbeac2",
    "data": "eyJyZWYiOiJiZTk2NWE2MS00MWY2LTQ1YjEtOTMyOS0yYjdlNmNhNDdmNGIifQ==",
    "nonce": 47,
    "balances": {
      "current": "1042427579888880331",
      "previous": "21280721848579888880331"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 229,
    "balances": {
      "current": "955444216827398160190047",
      "previous": "934185795827398160190047"
    }
  },
  "blockNumber": "14877877",
  "created": "2022-05-31T09:14:55.317Z",
  "updated": "2022-05-31T09:14:55.452Z",
  "id": "6295dc8f7832e20011830f68"
}
```
* *stageAmount*: `1042427579888880331`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000004806bdb138ef05880000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000004806bdb138ef05880000000000000000000000000000000000000000000000004806bdb138ef0588000d4b4d4ae71c56aa295c2e0ea1c9f68224f22c197ce2f11eff61d476878d79e4918bbba7655f34a2292457113745d8c73492c4a51403aee3e6fd998456b84c5684a3745424fdee4dc1047884dd42907c93b8d846f477f0699bf356408fcb97b52000000000000000000000000000000000000000000000000000000000000001ba42c6cadeb1bffb089e873669e5524a9ff01e962aff1ae4680809c874887dd99f513693f27f36193a51b40ae0478b31bd8620552fd1928bffdb1707e1e76e89736433617c919bdda48e34f4bd4022381b37553237d4aa18a26d8b4f217ff82f0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e304b50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000ab245ea58a115255a68795f66472b6bb6cfbeac20000000000000000000000000000000000000000000000000e77725c6358cacb000000000000000000000000000000000000000000000481a1579b2fd2659acb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000001270515447eb450000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001270515447eb450000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a546b324e5745324d5330304d5759324c545131596a45744f544d794f533079596a646c4e6d4e684e44646d4e47496966513d3d00000000000000000000000000000000000000000000000000000000000000e5000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000ca52bc1a741a7d390a5f00000000000000000000000000000000000000000000c5d2503f608b8ce08a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd4b4d4ae71c56aa295c2e0ea1c9f68224f22c197ce2f11eff61d476878d79e49",
      "signature": {
        "s": "0x4a3745424fdee4dc1047884dd42907c93b8d846f477f0699bf356408fcb97b52",
        "r": "0x18bbba7655f34a2292457113745d8c73492c4a51403aee3e6fd998456b84c568",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa42c6cadeb1bffb089e873669e5524a9ff01e962aff1ae4680809c874887dd99",
      "signature": {
        "s": "0x36433617c919bdda48e34f4bd4022381b37553237d4aa18a26d8b4f217ff82f0",
        "r": "0xf513693f27f36193a51b40ae0478b31bd8620552fd1928bffdb1707e1e76e897",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21258421000000000000000",
    "total": "21258421000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21258421000000000000000",
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
            "amount": "21258421000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21258421000000000000"
      }
    },
    "wallet": "0xab245ea58a115255a68795f66472b6bb6cfbeac2",
    "data": "eyJyZWYiOiJiZTk2NWE2MS00MWY2LTQ1YjEtOTMyOS0yYjdlNmNhNDdmNGIifQ==",
    "nonce": 47,
    "balances": {
      "current": "1042427579888880331",
      "previous": "21280721848579888880331"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 229,
    "balances": {
      "current": "955444216827398160190047",
      "previous": "934185795827398160190047"
    }
  },
  "blockNumber": "14877877",
  "created": "2022-05-31T09:14:55.317Z",
  "updated": "2022-05-31T09:14:55.452Z",
  "id": "6295dc8f7832e20011830f68"
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
0x0f200f9b0000000000000000000000000000000000000000000000000e77725c6358cacb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1042427579888880331`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`