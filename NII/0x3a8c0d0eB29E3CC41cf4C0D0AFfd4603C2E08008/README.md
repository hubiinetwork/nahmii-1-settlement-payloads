# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x3a8c0d0eB29E3CC41cf4C0D0AFfd4603C2E08008`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002eef7273b27b1b50bc0000000000000000000000000000000000000000000000053679300dd709050e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000053679300dd709050e000000000000000000000000000000000000000000000092469eed784701ccd1d0aa107b8272d565cf3f9f6f5c2bda2d294b762714978724b61d149fa4636d7d1a45611c6d1099f8d61b87343680ce71de76c4ef1219bd4a8f4f65cc7b6d01432f74cb9bd724764758c53605493c6166c343a301e3b3fafdf01ff5cda00991c5000000000000000000000000000000000000000000000000000000000000001b3f374b530ade3329e5eb4bb31b3e1cee8ae7f813908d47972545b1792a5da5351c4b0fcbf3206ecc1d82a6749d1fec1686de79f1825c85f4e90d85e85151aad27f1e97b1f7f3cf3d5631ea100efa7978c81e3cc7146bde2a52fcd65f7951424f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d700000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b29f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004745e236c15e9d89f69a00000000000000000000000000000000000000000000474b1a059178c1d85e3800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000155a00c4d4562900000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da27b669bc348a67240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b597a5a685a6a6c684f5330304d444d324c5455354d4441744f444a6a4e793035596a526b4d3255304d324d344f44636966513d3d00000000000000000000000000000000000000000000000000000000000000310000000000000000000000003a8c0d0eb29e3cc41cf4c0d0affd4603c2e0800800000000000000000000000000000000000000000000002eef7273b27b1b50bc000000000000000000000000000000000000000000000029b8f943a4a4124bae00000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000047d5fb9d5bc0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xd0aa107b8272d565cf3f9f6f5c2bda2d294b762714978724b61d149fa4636d7d",
      "signature": {
        "s": "0x2f74cb9bd724764758c53605493c6166c343a301e3b3fafdf01ff5cda00991c5",
        "r": "0x1a45611c6d1099f8d61b87343680ce71de76c4ef1219bd4a8f4f65cc7b6d0143",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3f374b530ade3329e5eb4bb31b3e1cee8ae7f813908d47972545b1792a5da535",
      "signature": {
        "s": "0x7f1e97b1f7f3cf3d5631ea100efa7978c81e3cc7146bde2a52fcd65f7951424f",
        "r": "0x1c4b0fcbf3206ecc1d82a6749d1fec1686de79f1825c85f4e90d85e85151aad2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "96158941754778256654",
    "total": "2698313400491412933841"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "96158941754778256654",
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
            "amount": "27636084213287205103396"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "96158941754778256"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkYzZhZjlhOS00MDM2LTU5MDAtODJjNy05YjRkM2U0M2M4ODcifQ==",
    "nonce": 111263,
    "balances": {
      "current": "336577146053344197473946",
      "previous": "336673401154040730508856"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "20220000000000000"
          }
        }
      ]
    },
    "wallet": "0x3a8c0d0eb29e3cc41cf4c0d0affd4603c2e08008",
    "nonce": 49,
    "balances": {
      "current": "865804207723455926460",
      "previous": "769645265968677669806"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:23.773Z",
  "updated": "2022-05-04T08:57:23.861Z",
  "id": "62723ff33592fd001130b5ef"
}
```
* *stageAmount*: `865804207723455926460`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006800000000000000000000000000000000000000000000000053679300dd709050e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000053679300dd709050e000000000000000000000000000000000000000000000092469eed784701ccd1d0aa107b8272d565cf3f9f6f5c2bda2d294b762714978724b61d149fa4636d7d1a45611c6d1099f8d61b87343680ce71de76c4ef1219bd4a8f4f65cc7b6d01432f74cb9bd724764758c53605493c6166c343a301e3b3fafdf01ff5cda00991c5000000000000000000000000000000000000000000000000000000000000001b3f374b530ade3329e5eb4bb31b3e1cee8ae7f813908d47972545b1792a5da5351c4b0fcbf3206ecc1d82a6749d1fec1686de79f1825c85f4e90d85e85151aad27f1e97b1f7f3cf3d5631ea100efa7978c81e3cc7146bde2a52fcd65f7951424f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d700000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b29f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004745e236c15e9d89f69a00000000000000000000000000000000000000000000474b1a059178c1d85e3800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000155a00c4d4562900000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da27b669bc348a67240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b597a5a685a6a6c684f5330304d444d324c5455354d4441744f444a6a4e793035596a526b4d3255304d324d344f44636966513d3d00000000000000000000000000000000000000000000000000000000000000310000000000000000000000003a8c0d0eb29e3cc41cf4c0d0affd4603c2e0800800000000000000000000000000000000000000000000002eef7273b27b1b50bc000000000000000000000000000000000000000000000029b8f943a4a4124bae00000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000047d5fb9d5bc0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xd0aa107b8272d565cf3f9f6f5c2bda2d294b762714978724b61d149fa4636d7d",
      "signature": {
        "s": "0x2f74cb9bd724764758c53605493c6166c343a301e3b3fafdf01ff5cda00991c5",
        "r": "0x1a45611c6d1099f8d61b87343680ce71de76c4ef1219bd4a8f4f65cc7b6d0143",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3f374b530ade3329e5eb4bb31b3e1cee8ae7f813908d47972545b1792a5da535",
      "signature": {
        "s": "0x7f1e97b1f7f3cf3d5631ea100efa7978c81e3cc7146bde2a52fcd65f7951424f",
        "r": "0x1c4b0fcbf3206ecc1d82a6749d1fec1686de79f1825c85f4e90d85e85151aad2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "96158941754778256654",
    "total": "2698313400491412933841"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "96158941754778256654",
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
            "amount": "27636084213287205103396"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "96158941754778256"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkYzZhZjlhOS00MDM2LTU5MDAtODJjNy05YjRkM2U0M2M4ODcifQ==",
    "nonce": 111263,
    "balances": {
      "current": "336577146053344197473946",
      "previous": "336673401154040730508856"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "20220000000000000"
          }
        }
      ]
    },
    "wallet": "0x3a8c0d0eb29e3cc41cf4c0d0affd4603c2e08008",
    "nonce": 49,
    "balances": {
      "current": "865804207723455926460",
      "previous": "769645265968677669806"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:23.773Z",
  "updated": "2022-05-04T08:57:23.861Z",
  "id": "62723ff33592fd001130b5ef"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000002eef7273b27b1b50bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `865804207723455926460`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`