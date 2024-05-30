# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x65d1451BC4d2D6E4D0c5F121D32BB3f0128f875a`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000024b9c829032445d528000000000000000000000000000000000000000000000000dee7d689b3c20dc20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dee7d689b3c20dc20000000000000000000000000000000000000000000000186ef2c7304b3e4f0c8f1d0c6cde4fa858a7272f364918000b30af46285fd1fcd22ad4faa1249c755d4a6fcf912c903b5ad52f0950a3dc76df862c0aaf9d172fc5e1966a64629eb0a41a89e51fcf2435c1e70788411b9833e46557de5e0c5d8c00d211ed4b3656cf2c000000000000000000000000000000000000000000000000000000000000001c30d08baebc5776b99a748c917b4c0694dcd288ff732ff54b2dd200be3eb0cc9fdcd8627368bfaef2f949f8b6a51255351b7b6c9aa48b85d855934e75434a72061cfaab82b6d0048e3483202a2d0726b07f83170c7155d588014e4dcd1193d48a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aeb1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096091b5075d90842ed2e000000000000000000000000000000000000000000009609fa715cba6c954d6200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000391057b09052720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c603158632bf8f15d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e3249345a475930595330344d4445784c545579596d4574596d52694f4330354f57466b4d7a4e694e324a6c4d32596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000065d1451bc4d2d6e4d0c5f121d32bb3f0128f875a000000000000000000000000000000000000000000000024b9c829032445d528000000000000000000000000000000000000000000000023dae052797083c76600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8f1d0c6cde4fa858a7272f364918000b30af46285fd1fcd22ad4faa1249c755d",
      "signature": {
        "s": "0x1a89e51fcf2435c1e70788411b9833e46557de5e0c5d8c00d211ed4b3656cf2c",
        "r": "0x4a6fcf912c903b5ad52f0950a3dc76df862c0aaf9d172fc5e1966a64629eb0a4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x30d08baebc5776b99a748c917b4c0694dcd288ff732ff54b2dd200be3eb0cc9f",
      "signature": {
        "s": "0x1cfaab82b6d0048e3483202a2d0726b07f83170c7155d588014e4dcd1193d48a",
        "r": "0xdcd8627368bfaef2f949f8b6a51255351b7b6c9aa48b85d855934e75434a7206",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16062042482954866114",
    "total": "450716529067800022796"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16062042482954866114",
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
            "amount": "27264509972251862308310"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16062042482954866"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0N2I4ZGY0YS04MDExLTUyYmEtYmRiOC05OWFkMzNiN2JlM2YifQ==",
    "nonce": 110257,
    "balances": {
      "current": "708522961329722335882542",
      "previous": "708539039434247773703522"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x65d1451bc4d2d6e4d0c5f121d32bb3f0128f875a",
    "nonce": 46,
    "balances": {
      "current": "677469781639372854568",
      "previous": "661407739156417988454"
    }
  },
  "blockNumber": "14709964",
  "created": "2022-05-04T08:52:20.794Z",
  "updated": "2022-05-04T08:52:20.893Z",
  "id": "62723ec47832e20011830b79"
}
```
* *stageAmount*: `677469781639372854568`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000dee7d689b3c20dc20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dee7d689b3c20dc20000000000000000000000000000000000000000000000186ef2c7304b3e4f0c8f1d0c6cde4fa858a7272f364918000b30af46285fd1fcd22ad4faa1249c755d4a6fcf912c903b5ad52f0950a3dc76df862c0aaf9d172fc5e1966a64629eb0a41a89e51fcf2435c1e70788411b9833e46557de5e0c5d8c00d211ed4b3656cf2c000000000000000000000000000000000000000000000000000000000000001c30d08baebc5776b99a748c917b4c0694dcd288ff732ff54b2dd200be3eb0cc9fdcd8627368bfaef2f949f8b6a51255351b7b6c9aa48b85d855934e75434a72061cfaab82b6d0048e3483202a2d0726b07f83170c7155d588014e4dcd1193d48a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aeb1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096091b5075d90842ed2e000000000000000000000000000000000000000000009609fa715cba6c954d6200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000391057b09052720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c603158632bf8f15d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e3249345a475930595330344d4445784c545579596d4574596d52694f4330354f57466b4d7a4e694e324a6c4d32596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000065d1451bc4d2d6e4d0c5f121d32bb3f0128f875a000000000000000000000000000000000000000000000024b9c829032445d528000000000000000000000000000000000000000000000023dae052797083c76600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8f1d0c6cde4fa858a7272f364918000b30af46285fd1fcd22ad4faa1249c755d",
      "signature": {
        "s": "0x1a89e51fcf2435c1e70788411b9833e46557de5e0c5d8c00d211ed4b3656cf2c",
        "r": "0x4a6fcf912c903b5ad52f0950a3dc76df862c0aaf9d172fc5e1966a64629eb0a4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x30d08baebc5776b99a748c917b4c0694dcd288ff732ff54b2dd200be3eb0cc9f",
      "signature": {
        "s": "0x1cfaab82b6d0048e3483202a2d0726b07f83170c7155d588014e4dcd1193d48a",
        "r": "0xdcd8627368bfaef2f949f8b6a51255351b7b6c9aa48b85d855934e75434a7206",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16062042482954866114",
    "total": "450716529067800022796"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16062042482954866114",
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
            "amount": "27264509972251862308310"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16062042482954866"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0N2I4ZGY0YS04MDExLTUyYmEtYmRiOC05OWFkMzNiN2JlM2YifQ==",
    "nonce": 110257,
    "balances": {
      "current": "708522961329722335882542",
      "previous": "708539039434247773703522"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x65d1451bc4d2d6e4d0c5f121d32bb3f0128f875a",
    "nonce": 46,
    "balances": {
      "current": "677469781639372854568",
      "previous": "661407739156417988454"
    }
  },
  "blockNumber": "14709964",
  "created": "2022-05-04T08:52:20.794Z",
  "updated": "2022-05-04T08:52:20.893Z",
  "id": "62723ec47832e20011830b79"
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
0x0f200f9b000000000000000000000000000000000000000000000024b9c829032445d5280000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `677469781639372854568`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`