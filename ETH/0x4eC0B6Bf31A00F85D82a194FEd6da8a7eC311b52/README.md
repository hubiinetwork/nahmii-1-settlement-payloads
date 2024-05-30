# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4eC0B6Bf31A00F85D82a194FEd6da8a7eC311b52`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000a630000000000000000000000000000000000000000000000000000000000000a6300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000a630000000000000000000000000000000000000000000000000000000000000a63933ad892e67aa4d052106fd49af412ea1ef2cef2bc864100fa81ddd9d4281d1f7842c821570cdcba978a5969836a24769ffc6af6abb1cefd047ea6dcc23793132baa70377660cfbcfc93a165f1dae6f745a9264e99ea975d440125bbd5e948bf000000000000000000000000000000000000000000000000000000000000001c2a2913c1440818e1828fff3b1cf79e4b3b209e1c827a1527ba9c48f5609751672b31e45f47bcd86fcacea9f823068852a3985eb4ef01a9def49e461856062cc437755f2b549dcb4be7ff376f39476a1b4db2f33e8e02b56e5fc8a9ae35d357ee000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008fe00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc55d729000000000000000000000000000000000000000000000000002386f2bc55e18e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e5100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f5441774e3259344e43316c5a6a426d4c54566a5a446374595746684e433034596d45305a5459784e44677a59546b6966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000004ec0b6bf31a00f85d82a194fed6da8a7ec311b520000000000000000000000000000000000000000000000000000000000000a63000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x933ad892e67aa4d052106fd49af412ea1ef2cef2bc864100fa81ddd9d4281d1f",
      "signature": {
        "s": "0x2baa70377660cfbcfc93a165f1dae6f745a9264e99ea975d440125bbd5e948bf",
        "r": "0x7842c821570cdcba978a5969836a24769ffc6af6abb1cefd047ea6dcc2379313",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2a2913c1440818e1828fff3b1cf79e4b3b209e1c827a1527ba9c48f560975167",
      "signature": {
        "s": "0x37755f2b549dcb4be7ff376f39476a1b4db2f33e8e02b56e5fc8a9ae35d357ee",
        "r": "0x2b31e45f47bcd86fcacea9f823068852a3985eb4ef01a9def49e461856062cc4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2659",
    "total": "2659"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2659",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "798289"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOTAwN2Y4NC1lZjBmLTVjZDctYWFhNC04YmE0ZTYxNDgzYTkifQ==",
    "nonce": 2302,
    "balances": {
      "current": "10000001284822825",
      "previous": "10000001284825486"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4ec0b6bf31a00f85d82a194fed6da8a7ec311b52",
    "nonce": 3,
    "balances": {
      "current": "2659",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:37.002Z",
  "updated": "2020-05-22T08:15:37.081Z",
  "id": "5ec78a28b0c6090011d5abcc"
}
```
* *stageAmount*: `2659`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000a6300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000a630000000000000000000000000000000000000000000000000000000000000a63933ad892e67aa4d052106fd49af412ea1ef2cef2bc864100fa81ddd9d4281d1f7842c821570cdcba978a5969836a24769ffc6af6abb1cefd047ea6dcc23793132baa70377660cfbcfc93a165f1dae6f745a9264e99ea975d440125bbd5e948bf000000000000000000000000000000000000000000000000000000000000001c2a2913c1440818e1828fff3b1cf79e4b3b209e1c827a1527ba9c48f5609751672b31e45f47bcd86fcacea9f823068852a3985eb4ef01a9def49e461856062cc437755f2b549dcb4be7ff376f39476a1b4db2f33e8e02b56e5fc8a9ae35d357ee000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008fe00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc55d729000000000000000000000000000000000000000000000000002386f2bc55e18e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e5100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f5441774e3259344e43316c5a6a426d4c54566a5a446374595746684e433034596d45305a5459784e44677a59546b6966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000004ec0b6bf31a00f85d82a194fed6da8a7ec311b520000000000000000000000000000000000000000000000000000000000000a63000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x933ad892e67aa4d052106fd49af412ea1ef2cef2bc864100fa81ddd9d4281d1f",
      "signature": {
        "s": "0x2baa70377660cfbcfc93a165f1dae6f745a9264e99ea975d440125bbd5e948bf",
        "r": "0x7842c821570cdcba978a5969836a24769ffc6af6abb1cefd047ea6dcc2379313",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2a2913c1440818e1828fff3b1cf79e4b3b209e1c827a1527ba9c48f560975167",
      "signature": {
        "s": "0x37755f2b549dcb4be7ff376f39476a1b4db2f33e8e02b56e5fc8a9ae35d357ee",
        "r": "0x2b31e45f47bcd86fcacea9f823068852a3985eb4ef01a9def49e461856062cc4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2659",
    "total": "2659"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2659",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "798289"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOTAwN2Y4NC1lZjBmLTVjZDctYWFhNC04YmE0ZTYxNDgzYTkifQ==",
    "nonce": 2302,
    "balances": {
      "current": "10000001284822825",
      "previous": "10000001284825486"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4ec0b6bf31a00f85d82a194fed6da8a7ec311b52",
    "nonce": 3,
    "balances": {
      "current": "2659",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:37.002Z",
  "updated": "2020-05-22T08:15:37.081Z",
  "id": "5ec78a28b0c6090011d5abcc"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000a630000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2659`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``