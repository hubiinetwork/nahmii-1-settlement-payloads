# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x4c230D8d11f1E494216f1ad79a0Ab50756709CA7`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001c452bcf88999a3aa90000000000000000000000000000000000000000000000020467b3a2a1fcdc6f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000020467b3a2a1fcdc6f0000000000000000000000000000000000000000000000389ad42a9b1a21d080690fa33576ac2d1c838e7a6be81320e744b11e2f9975fba31d6ce85dc556836daead097d7232f76c50166172659c2d6fccc18f5749ff13cf71a622921aba2daf21d5870cb22beabdecdffe9f468ec9bb126fad7b74cc04a91c3a6ebf3a963608000000000000000000000000000000000000000000000000000000000000001baab2f783e92a6f0a1373917afa53728aa3890a4c3801023011e7d1ed93f6f331a10c5b4611b0d53e9e397510db8e83c30651cc1bae738b00d1e9195cf7ca9c1321e2f5faedd782250ceb383d345b61bc4f27a0de0d85bd18b40bf0a9b1beb174000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b103000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004b96d0d10cff7d514c9f000000000000000000000000000000000000000000004b98d5bcf3c1c5de077b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000084331fa68fde6d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d90d21ed5e2fb6b4df0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d5755355a546b334e53316a4d545a694c5455324d6a49744f44466d5969307a4d3252684e54526b4f445a684e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004c230d8d11f1e494216f1ad79a0ab50756709ca700000000000000000000000000000000000000000000001c452bcf88999a3aa900000000000000000000000000000000000000000000001a40c41be5f79d5e3a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x690fa33576ac2d1c838e7a6be81320e744b11e2f9975fba31d6ce85dc556836d",
      "signature": {
        "s": "0x21d5870cb22beabdecdffe9f468ec9bb126fad7b74cc04a91c3a6ebf3a963608",
        "r": "0xaead097d7232f76c50166172659c2d6fccc18f5749ff13cf71a622921aba2daf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaab2f783e92a6f0a1373917afa53728aa3890a4c3801023011e7d1ed93f6f331",
      "signature": {
        "s": "0x21e2f5faedd782250ceb383d345b61bc4f27a0de0d85bd18b40bf0a9b1beb174",
        "r": "0xa10c5b4611b0d53e9e397510db8e83c30651cc1bae738b00d1e9195cf7ca9c13",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "37210907957255789679",
    "total": "1044174257150285172864"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "37210907957255789679",
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
            "amount": "27615722176728706495711"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "37210907957255789"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MWU5ZTk3NS1jMTZiLTU2MjItODFmYi0zM2RhNTRkODZhNzkifQ==",
    "nonce": 110851,
    "balances": {
      "current": "356959544648401303981215",
      "previous": "356996792767266517026683"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4c230d8d11f1e494216f1ad79a0ab50756709ca7",
    "nonce": 46,
    "balances": {
      "current": "521493139662082554537",
      "previous": "484282231704826764858"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:21.150Z",
  "updated": "2022-05-04T08:55:21.243Z",
  "id": "62723f79bbd75600116d05f7"
}
```
* *stageAmount*: `521493139662082554537`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000020467b3a2a1fcdc6f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000020467b3a2a1fcdc6f0000000000000000000000000000000000000000000000389ad42a9b1a21d080690fa33576ac2d1c838e7a6be81320e744b11e2f9975fba31d6ce85dc556836daead097d7232f76c50166172659c2d6fccc18f5749ff13cf71a622921aba2daf21d5870cb22beabdecdffe9f468ec9bb126fad7b74cc04a91c3a6ebf3a963608000000000000000000000000000000000000000000000000000000000000001baab2f783e92a6f0a1373917afa53728aa3890a4c3801023011e7d1ed93f6f331a10c5b4611b0d53e9e397510db8e83c30651cc1bae738b00d1e9195cf7ca9c1321e2f5faedd782250ceb383d345b61bc4f27a0de0d85bd18b40bf0a9b1beb174000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b103000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004b96d0d10cff7d514c9f000000000000000000000000000000000000000000004b98d5bcf3c1c5de077b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000084331fa68fde6d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d90d21ed5e2fb6b4df0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d5755355a546b334e53316a4d545a694c5455324d6a49744f44466d5969307a4d3252684e54526b4f445a684e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004c230d8d11f1e494216f1ad79a0ab50756709ca700000000000000000000000000000000000000000000001c452bcf88999a3aa900000000000000000000000000000000000000000000001a40c41be5f79d5e3a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x690fa33576ac2d1c838e7a6be81320e744b11e2f9975fba31d6ce85dc556836d",
      "signature": {
        "s": "0x21d5870cb22beabdecdffe9f468ec9bb126fad7b74cc04a91c3a6ebf3a963608",
        "r": "0xaead097d7232f76c50166172659c2d6fccc18f5749ff13cf71a622921aba2daf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaab2f783e92a6f0a1373917afa53728aa3890a4c3801023011e7d1ed93f6f331",
      "signature": {
        "s": "0x21e2f5faedd782250ceb383d345b61bc4f27a0de0d85bd18b40bf0a9b1beb174",
        "r": "0xa10c5b4611b0d53e9e397510db8e83c30651cc1bae738b00d1e9195cf7ca9c13",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "37210907957255789679",
    "total": "1044174257150285172864"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "37210907957255789679",
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
            "amount": "27615722176728706495711"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "37210907957255789"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MWU5ZTk3NS1jMTZiLTU2MjItODFmYi0zM2RhNTRkODZhNzkifQ==",
    "nonce": 110851,
    "balances": {
      "current": "356959544648401303981215",
      "previous": "356996792767266517026683"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4c230d8d11f1e494216f1ad79a0ab50756709ca7",
    "nonce": 46,
    "balances": {
      "current": "521493139662082554537",
      "previous": "484282231704826764858"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:21.150Z",
  "updated": "2022-05-04T08:55:21.243Z",
  "id": "62723f79bbd75600116d05f7"
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
0x0f200f9b00000000000000000000000000000000000000000000001c452bcf88999a3aa90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `521493139662082554537`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`