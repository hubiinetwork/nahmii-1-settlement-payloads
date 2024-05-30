# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x811a3B3f5B2E8F52731F7E6649Cf673149574828`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000007d6e36498e6ff8890000000000000000000000000000000000000000000000000dc2fb268752f14440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb268752f1444000000000000000000000000000000000000000000000007d6e36498e6ff8890e078fb75b1185a28821ae64965b484df3e6b1e9c1199e1581c7c3d605a8cae6e42703123627146c129932742893dfdd4974dfe8c17415ffc9b02587282bae0364cc905105963ba0843214281357e88e2f364b097a1394f8970738b84739be166000000000000000000000000000000000000000000000000000000000000001baff1365eca3f35428e8dbf8580458233916a6dd49010a14a0b6fb0f8b8fdea90add530d450a922f608884da615177cea7374332b06546a873bb13e8d36ba4eba6c2e4a41428874b0fc0227e631434b6bd381e109db0d3b3b2e50ffc56fab8b08000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5f2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000032827fd741ed949aee4e0000000000000000000000000000000000000000000032835c3f52776c35d54700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e21626bd2b50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df77176f7d263a54e10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979595446685a446b324f53316c5a5759784c54557a5a446374596a55785979307a5a6a5933596a45354f44646b5a6a556966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000811a3b3f5b2e8f52731f7e6649cf673149574828000000000000000000000000000000000000000000000007d6e36498e6ff8890000000000000000000000000000000000000000000000006fab3b23071d0744c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe078fb75b1185a28821ae64965b484df3e6b1e9c1199e1581c7c3d605a8cae6e",
      "signature": {
        "s": "0x4cc905105963ba0843214281357e88e2f364b097a1394f8970738b84739be166",
        "r": "0x42703123627146c129932742893dfdd4974dfe8c17415ffc9b02587282bae036",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaff1365eca3f35428e8dbf8580458233916a6dd49010a14a0b6fb0f8b8fdea90",
      "signature": {
        "s": "0x6c2e4a41428874b0fc0227e631434b6bd381e109db0d3b3b2e50ffc56fab8b08",
        "r": "0xadd530d450a922f608884da615177cea7374332b06546a873bb13e8d36ba4eba",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096173961909316",
    "total": "144611539067670071440"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096173961909316",
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
            "amount": "27734037792983736800481"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096173961909"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyYTFhZDk2OS1lZWYxLTUzZDctYjUxYy0zZjY3YjE5ODdkZjUifQ==",
    "nonce": 112114,
    "balances": {
      "current": "238525612777115968269902",
      "previous": "238541494739386104141127"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x811a3b3f5b2e8f52731f7e6649cf673149574828",
    "nonce": 10,
    "balances": {
      "current": "144611539067670071440",
      "previous": "128745442893708162124"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:06.286Z",
  "updated": "2022-05-04T09:02:06.362Z",
  "id": "6272410e3592fd001130b717"
}
```
* *stageAmount*: `144611539067670071440`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000dc2fb268752f14440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb268752f1444000000000000000000000000000000000000000000000007d6e36498e6ff8890e078fb75b1185a28821ae64965b484df3e6b1e9c1199e1581c7c3d605a8cae6e42703123627146c129932742893dfdd4974dfe8c17415ffc9b02587282bae0364cc905105963ba0843214281357e88e2f364b097a1394f8970738b84739be166000000000000000000000000000000000000000000000000000000000000001baff1365eca3f35428e8dbf8580458233916a6dd49010a14a0b6fb0f8b8fdea90add530d450a922f608884da615177cea7374332b06546a873bb13e8d36ba4eba6c2e4a41428874b0fc0227e631434b6bd381e109db0d3b3b2e50ffc56fab8b08000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5f2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000032827fd741ed949aee4e0000000000000000000000000000000000000000000032835c3f52776c35d54700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e21626bd2b50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df77176f7d263a54e10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979595446685a446b324f53316c5a5759784c54557a5a446374596a55785979307a5a6a5933596a45354f44646b5a6a556966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000811a3b3f5b2e8f52731f7e6649cf673149574828000000000000000000000000000000000000000000000007d6e36498e6ff8890000000000000000000000000000000000000000000000006fab3b23071d0744c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe078fb75b1185a28821ae64965b484df3e6b1e9c1199e1581c7c3d605a8cae6e",
      "signature": {
        "s": "0x4cc905105963ba0843214281357e88e2f364b097a1394f8970738b84739be166",
        "r": "0x42703123627146c129932742893dfdd4974dfe8c17415ffc9b02587282bae036",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaff1365eca3f35428e8dbf8580458233916a6dd49010a14a0b6fb0f8b8fdea90",
      "signature": {
        "s": "0x6c2e4a41428874b0fc0227e631434b6bd381e109db0d3b3b2e50ffc56fab8b08",
        "r": "0xadd530d450a922f608884da615177cea7374332b06546a873bb13e8d36ba4eba",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096173961909316",
    "total": "144611539067670071440"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096173961909316",
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
            "amount": "27734037792983736800481"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096173961909"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyYTFhZDk2OS1lZWYxLTUzZDctYjUxYy0zZjY3YjE5ODdkZjUifQ==",
    "nonce": 112114,
    "balances": {
      "current": "238525612777115968269902",
      "previous": "238541494739386104141127"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x811a3b3f5b2e8f52731f7e6649cf673149574828",
    "nonce": 10,
    "balances": {
      "current": "144611539067670071440",
      "previous": "128745442893708162124"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:06.286Z",
  "updated": "2022-05-04T09:02:06.362Z",
  "id": "6272410e3592fd001130b717"
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
0x0f200f9b000000000000000000000000000000000000000000000007d6e36498e6ff88900000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `144611539067670071440`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`