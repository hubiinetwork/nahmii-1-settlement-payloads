# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8F5053b0dd4902EA9Ce86c8D6684E42eaE57E045`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000005df18000000000000000000000000000000000000000000000000000000000005df180000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000005df18000000000000000000000000000000000000000000000000000000000005df18db4aa0b36cece3de0e7093619cb6013211aa62d89128ee2f1f7ba41faafe67bf3337d0e3fc6a33fadb14bf4d83c8847a85ce29c078549f7fc67dcdac8c733c864a6707b01a364e34e897583ae1a8efd8255e94a31330ae366311ce868ec86e32000000000000000000000000000000000000000000000000000000000000001bd5150e73ec7de18951932b0c3e45a2ef02db8979d754effeca0ec977d5178bbb2a4ad0bf1a8c5cf048d0151d4d70a1f688814d956382d9fc6f2ed8bbfbfac79e4b2ec265c4d44bce2206451315197b8c0477562b7e92fc529186a7186ce0f59a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e2000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005d600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c672ccfa000000000000000000000000000000000000000000000000002386f2c678ad9200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000018000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009992e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d54646b4f5467304d5330344e4759774c54566b4d3249744f5446684d4331695a444d3359574d30597a49794d7a676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000008f5053b0dd4902ea9ce86c8d6684e42eae57e045000000000000000000000000000000000000000000000000000000000005df18000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdb4aa0b36cece3de0e7093619cb6013211aa62d89128ee2f1f7ba41faafe67bf",
      "signature": {
        "s": "0x4a6707b01a364e34e897583ae1a8efd8255e94a31330ae366311ce868ec86e32",
        "r": "0x3337d0e3fc6a33fadb14bf4d83c8847a85ce29c078549f7fc67dcdac8c733c86",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd5150e73ec7de18951932b0c3e45a2ef02db8979d754effeca0ec977d5178bbb",
      "signature": {
        "s": "0x4b2ec265c4d44bce2206451315197b8c0477562b7e92fc529186a7186ce0f59a",
        "r": "0x2a4ad0bf1a8c5cf048d0151d4d70a1f688814d956382d9fc6f2ed8bbfbfac79e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "384792",
    "total": "384792"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "384792",
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
            "amount": "629038"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "384"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMTdkOTg0MS04NGYwLTVkM2ItOTFhMC1iZDM3YWM0YzIyMzgifQ==",
    "nonce": 1494,
    "balances": {
      "current": "10000001454492922",
      "previous": "10000001454878098"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8f5053b0dd4902ea9ce86c8d6684e42eae57e045",
    "nonce": 20,
    "balances": {
      "current": "384792",
      "previous": "0"
    }
  },
  "blockNumber": "10114530",
  "created": "2020-05-22T08:09:57.930Z",
  "updated": "2020-05-22T08:09:57.997Z",
  "id": "5ec788d5005df800101bc41d"
}
```
* *stageAmount*: `384792`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000005df180000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000005df18000000000000000000000000000000000000000000000000000000000005df18db4aa0b36cece3de0e7093619cb6013211aa62d89128ee2f1f7ba41faafe67bf3337d0e3fc6a33fadb14bf4d83c8847a85ce29c078549f7fc67dcdac8c733c864a6707b01a364e34e897583ae1a8efd8255e94a31330ae366311ce868ec86e32000000000000000000000000000000000000000000000000000000000000001bd5150e73ec7de18951932b0c3e45a2ef02db8979d754effeca0ec977d5178bbb2a4ad0bf1a8c5cf048d0151d4d70a1f688814d956382d9fc6f2ed8bbfbfac79e4b2ec265c4d44bce2206451315197b8c0477562b7e92fc529186a7186ce0f59a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e2000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005d600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c672ccfa000000000000000000000000000000000000000000000000002386f2c678ad9200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000018000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009992e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d54646b4f5467304d5330344e4759774c54566b4d3249744f5446684d4331695a444d3359574d30597a49794d7a676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000008f5053b0dd4902ea9ce86c8d6684e42eae57e045000000000000000000000000000000000000000000000000000000000005df18000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdb4aa0b36cece3de0e7093619cb6013211aa62d89128ee2f1f7ba41faafe67bf",
      "signature": {
        "s": "0x4a6707b01a364e34e897583ae1a8efd8255e94a31330ae366311ce868ec86e32",
        "r": "0x3337d0e3fc6a33fadb14bf4d83c8847a85ce29c078549f7fc67dcdac8c733c86",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd5150e73ec7de18951932b0c3e45a2ef02db8979d754effeca0ec977d5178bbb",
      "signature": {
        "s": "0x4b2ec265c4d44bce2206451315197b8c0477562b7e92fc529186a7186ce0f59a",
        "r": "0x2a4ad0bf1a8c5cf048d0151d4d70a1f688814d956382d9fc6f2ed8bbfbfac79e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "384792",
    "total": "384792"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "384792",
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
            "amount": "629038"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "384"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMTdkOTg0MS04NGYwLTVkM2ItOTFhMC1iZDM3YWM0YzIyMzgifQ==",
    "nonce": 1494,
    "balances": {
      "current": "10000001454492922",
      "previous": "10000001454878098"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8f5053b0dd4902ea9ce86c8d6684e42eae57e045",
    "nonce": 20,
    "balances": {
      "current": "384792",
      "previous": "0"
    }
  },
  "blockNumber": "10114530",
  "created": "2020-05-22T08:09:57.930Z",
  "updated": "2020-05-22T08:09:57.997Z",
  "id": "5ec788d5005df800101bc41d"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000005df180000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `384792`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``