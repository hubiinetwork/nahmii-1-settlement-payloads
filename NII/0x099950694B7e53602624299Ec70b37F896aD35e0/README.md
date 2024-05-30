# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x099950694B7e53602624299Ec70b37F896aD35e0`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000b5636e4fc0084a3a6e8000000000000000000000000000000000000000000000044cee7c22b7b433b440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000044cee7c22b7b433b4400000000000000000000000000000000000000000000078ad35ea6e26fa4fc69abf60c7908b229d341a49f17cd39db4bf1bc5c6f4a3e18ebc07373c4073298f67e60458d0ec92d92b6bee4acfeadeecc117891ec8a6f3c882a8067569b98a03404bd6f3907a21a0a9168332d9dba024f878f6549a42edab5650f83bad8e5addd000000000000000000000000000000000000000000000000000000000000001c1146b3ce06bd5dea7094cd2a6b946eab413f88b3185d4b925b39b3a2c01c9decbce11f6df7a177fceb34edb1731f834cc9ef3c1b3d4d0fc1f2496263b4ef51f204b8d3998c0e92a14f3c90062e388da5bae995ade22d0a9c52ad7f347caeb61e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b72a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002edc065d69272f1290f4000000000000000000000000000000000000000000002f20e6e295c1d017251c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000119d6a6f25c158e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e06613fa10250cf1630000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f5451314f444e6c4e79316d59544d354c5455794e6d4974596a67774e5331694f5449334e6a41795a6d49314d7a676966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000099950694b7e53602624299ec70b37f896ad35e0000000000000000000000000000000000000000000000b5636e4fc0084a3a6e8000000000000000000000000000000000000000000000b1167fd39d509606ba400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xabf60c7908b229d341a49f17cd39db4bf1bc5c6f4a3e18ebc07373c4073298f6",
      "signature": {
        "s": "0x04bd6f3907a21a0a9168332d9dba024f878f6549a42edab5650f83bad8e5addd",
        "r": "0x7e60458d0ec92d92b6bee4acfeadeecc117891ec8a6f3c882a8067569b98a034",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1146b3ce06bd5dea7094cd2a6b946eab413f88b3185d4b925b39b3a2c01c9dec",
      "signature": {
        "s": "0x04b8d3998c0e92a14f3c90062e388da5bae995ade22d0a9c52ad7f347caeb61e",
        "r": "0xbce11f6df7a177fceb34edb1731f834cc9ef3c1b3d4d0fc1f2496263b4ef51f2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1269287695595690212164",
    "total": "35617446856740714118249"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1269287695595690212164",
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
            "amount": "27751258584422839808355"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1269287695595690212"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2OTQ1ODNlNy1mYTM5LTUyNmItYjgwNS1iOTI3NjAyZmI1MzgifQ==",
    "nonce": 112426,
    "balances": {
      "current": "221287600546573857231092",
      "previous": "222558157529865143133468"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x099950694b7e53602624299ec70b37f896ad35e0",
    "nonce": 46,
    "balances": {
      "current": "53536406865357012444904",
      "previous": "52267119169761322232740"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:44.139Z",
  "updated": "2022-05-04T09:03:44.226Z",
  "id": "62724170bbd75600116d07e9"
}
```
* *stageAmount*: `53536406865357012444904`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000044cee7c22b7b433b440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000044cee7c22b7b433b4400000000000000000000000000000000000000000000078ad35ea6e26fa4fc69abf60c7908b229d341a49f17cd39db4bf1bc5c6f4a3e18ebc07373c4073298f67e60458d0ec92d92b6bee4acfeadeecc117891ec8a6f3c882a8067569b98a03404bd6f3907a21a0a9168332d9dba024f878f6549a42edab5650f83bad8e5addd000000000000000000000000000000000000000000000000000000000000001c1146b3ce06bd5dea7094cd2a6b946eab413f88b3185d4b925b39b3a2c01c9decbce11f6df7a177fceb34edb1731f834cc9ef3c1b3d4d0fc1f2496263b4ef51f204b8d3998c0e92a14f3c90062e388da5bae995ade22d0a9c52ad7f347caeb61e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b72a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002edc065d69272f1290f4000000000000000000000000000000000000000000002f20e6e295c1d017251c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000119d6a6f25c158e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e06613fa10250cf1630000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f5451314f444e6c4e79316d59544d354c5455794e6d4974596a67774e5331694f5449334e6a41795a6d49314d7a676966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000099950694b7e53602624299ec70b37f896ad35e0000000000000000000000000000000000000000000000b5636e4fc0084a3a6e8000000000000000000000000000000000000000000000b1167fd39d509606ba400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xabf60c7908b229d341a49f17cd39db4bf1bc5c6f4a3e18ebc07373c4073298f6",
      "signature": {
        "s": "0x04bd6f3907a21a0a9168332d9dba024f878f6549a42edab5650f83bad8e5addd",
        "r": "0x7e60458d0ec92d92b6bee4acfeadeecc117891ec8a6f3c882a8067569b98a034",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1146b3ce06bd5dea7094cd2a6b946eab413f88b3185d4b925b39b3a2c01c9dec",
      "signature": {
        "s": "0x04b8d3998c0e92a14f3c90062e388da5bae995ade22d0a9c52ad7f347caeb61e",
        "r": "0xbce11f6df7a177fceb34edb1731f834cc9ef3c1b3d4d0fc1f2496263b4ef51f2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1269287695595690212164",
    "total": "35617446856740714118249"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1269287695595690212164",
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
            "amount": "27751258584422839808355"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1269287695595690212"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2OTQ1ODNlNy1mYTM5LTUyNmItYjgwNS1iOTI3NjAyZmI1MzgifQ==",
    "nonce": 112426,
    "balances": {
      "current": "221287600546573857231092",
      "previous": "222558157529865143133468"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x099950694b7e53602624299ec70b37f896ad35e0",
    "nonce": 46,
    "balances": {
      "current": "53536406865357012444904",
      "previous": "52267119169761322232740"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:44.139Z",
  "updated": "2022-05-04T09:03:44.226Z",
  "id": "62724170bbd75600116d07e9"
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
0x0f200f9b000000000000000000000000000000000000000000000b5636e4fc0084a3a6e80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `53536406865357012444904`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`