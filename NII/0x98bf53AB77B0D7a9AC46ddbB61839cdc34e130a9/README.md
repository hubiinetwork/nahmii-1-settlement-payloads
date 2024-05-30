# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x98bf53AB77B0D7a9AC46ddbB61839cdc34e130a9`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001cdc6cc25e81744b86000000000000000000000000000000000000000000000000af2bd3c0737ff9130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000af2bd3c0737ff9130000000000000000000000000000000000000000000000133379642a92ae2b431fb5047a21aed4cfab0b4c3ccd2fa14f6752d88b40a51a106c7e2c364e9bd756f1873660c830a1df390a2491337ea6b7d689b6343a8b5f4dcd4b057e62c8378b31b20e684d45bb5b45bcc3b20b72230694785b285f9af9bb63fd0b4f496789c3000000000000000000000000000000000000000000000000000000000000001c4fdb9bd6205d52ab456834a046e21959fa34833614d35d0074ccfd5f0a3162fbf27a0f31b2e3ef3ee10d936a631a4d1172bec854b220235947c668690a1810c55ad94fd4d68fff3737b3744034d763c92f478c43e8fd428767da7d0643282b6e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0b5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bc3471805efd368243c000000000000000000000000000000000000000000004bc3f670b1b5555bb2ce00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000002cd8050e73957f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d901c2f9a693e1234a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a55794e444d77595330774d4455784c5455344f446374595745334e4331695a6a5534597a59794d4451355932596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000098bf53ab77b0d7a9ac46ddbb61839cdc34e130a900000000000000000000000000000000000000000000001cdc6cc25e81744b8600000000000000000000000000000000000000000000001c2d40ee9e0df4527300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1fb5047a21aed4cfab0b4c3ccd2fa14f6752d88b40a51a106c7e2c364e9bd756",
      "signature": {
        "s": "0x31b20e684d45bb5b45bcc3b20b72230694785b285f9af9bb63fd0b4f496789c3",
        "r": "0xf1873660c830a1df390a2491337ea6b7d689b6343a8b5f4dcd4b057e62c8378b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4fdb9bd6205d52ab456834a046e21959fa34833614d35d0074ccfd5f0a3162fb",
      "signature": {
        "s": "0x5ad94fd4d68fff3737b3744034d763c92f478c43e8fd428767da7d0643282b6e",
        "r": "0xf27a0f31b2e3ef3ee10d936a631a4d1172bec854b220235947c668690a1810c5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "12622415204160895251",
    "total": "354197243302610086723"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12622415204160895251",
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
            "amount": "27614902816576559457098"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12622415204160895"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMzUyNDMwYS0wMDUxLTU4ODctYWE3NC1iZjU4YzYyMDQ5Y2YifQ==",
    "nonce": 110773,
    "balances": {
      "current": "357779724160700489671740",
      "previous": "357792359198319854727886"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98bf53ab77b0d7a9ac46ddbb61839cdc34e130a9",
    "nonce": 46,
    "balances": {
      "current": "532392117760850938758",
      "previous": "519769702556690043507"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:54:56.680Z",
  "updated": "2022-05-04T08:54:56.736Z",
  "id": "62723f60bbd75600116d05da"
}
```
* *stageAmount*: `532392117760850938758`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000af2bd3c0737ff9130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000af2bd3c0737ff9130000000000000000000000000000000000000000000000133379642a92ae2b431fb5047a21aed4cfab0b4c3ccd2fa14f6752d88b40a51a106c7e2c364e9bd756f1873660c830a1df390a2491337ea6b7d689b6343a8b5f4dcd4b057e62c8378b31b20e684d45bb5b45bcc3b20b72230694785b285f9af9bb63fd0b4f496789c3000000000000000000000000000000000000000000000000000000000000001c4fdb9bd6205d52ab456834a046e21959fa34833614d35d0074ccfd5f0a3162fbf27a0f31b2e3ef3ee10d936a631a4d1172bec854b220235947c668690a1810c55ad94fd4d68fff3737b3744034d763c92f478c43e8fd428767da7d0643282b6e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0b5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bc3471805efd368243c000000000000000000000000000000000000000000004bc3f670b1b5555bb2ce00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000002cd8050e73957f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d901c2f9a693e1234a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a55794e444d77595330774d4455784c5455344f446374595745334e4331695a6a5534597a59794d4451355932596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000098bf53ab77b0d7a9ac46ddbb61839cdc34e130a900000000000000000000000000000000000000000000001cdc6cc25e81744b8600000000000000000000000000000000000000000000001c2d40ee9e0df4527300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1fb5047a21aed4cfab0b4c3ccd2fa14f6752d88b40a51a106c7e2c364e9bd756",
      "signature": {
        "s": "0x31b20e684d45bb5b45bcc3b20b72230694785b285f9af9bb63fd0b4f496789c3",
        "r": "0xf1873660c830a1df390a2491337ea6b7d689b6343a8b5f4dcd4b057e62c8378b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4fdb9bd6205d52ab456834a046e21959fa34833614d35d0074ccfd5f0a3162fb",
      "signature": {
        "s": "0x5ad94fd4d68fff3737b3744034d763c92f478c43e8fd428767da7d0643282b6e",
        "r": "0xf27a0f31b2e3ef3ee10d936a631a4d1172bec854b220235947c668690a1810c5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "12622415204160895251",
    "total": "354197243302610086723"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12622415204160895251",
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
            "amount": "27614902816576559457098"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12622415204160895"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMzUyNDMwYS0wMDUxLTU4ODctYWE3NC1iZjU4YzYyMDQ5Y2YifQ==",
    "nonce": 110773,
    "balances": {
      "current": "357779724160700489671740",
      "previous": "357792359198319854727886"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98bf53ab77b0d7a9ac46ddbb61839cdc34e130a9",
    "nonce": 46,
    "balances": {
      "current": "532392117760850938758",
      "previous": "519769702556690043507"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:54:56.680Z",
  "updated": "2022-05-04T08:54:56.736Z",
  "id": "62723f60bbd75600116d05da"
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
0x0f200f9b00000000000000000000000000000000000000000000001cdc6cc25e81744b860000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `532392117760850938758`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`