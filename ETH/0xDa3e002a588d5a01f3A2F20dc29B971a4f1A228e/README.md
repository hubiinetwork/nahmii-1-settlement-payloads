# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xDa3e002a588d5a01f3A2F20dc29B971a4f1A228e`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006b100000000000000000000000000000000000000000000000000000000000006b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000006b100000000000000000000000000000000000000000000000000000000000006b1b8a3c89ef12fc37d8fea8c58425b8ed39fdc35ea632bd78cb2049861feee7eb7581beb3203630451826d74981efb29efa9d42dfaa14b5625316e40b703c6012a1063b57ce3810399344872299a6b0a0df8701ce10d660645c61d26f924385ce1000000000000000000000000000000000000000000000000000000000000001b7d287850cfc75aa54b717325764153ccaa17dbb103230d46b9c5ca2c587dfb428c53738944eccc4dd1ab5d056640cc5a05fe4858405cba1f3d6a7cb43ec302c70cf452d4d93cd887e09bc7bedaf07a73e25239ba512c5b943896cd4a7b850436000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003bb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caabd60a000000000000000000000000000000000000000000000000002386f2caabdcbc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008853600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493459575132596d51314d79316b4e4749304c5456694f4459744f546c6c5a69316a4f54417a4e7a41324d3251304d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da3e002a588d5a01f3a2f20dc29b971a4f1a228e00000000000000000000000000000000000000000000000000000000000006b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb8a3c89ef12fc37d8fea8c58425b8ed39fdc35ea632bd78cb2049861feee7eb7",
      "signature": {
        "s": "0x1063b57ce3810399344872299a6b0a0df8701ce10d660645c61d26f924385ce1",
        "r": "0x581beb3203630451826d74981efb29efa9d42dfaa14b5625316e40b703c6012a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7d287850cfc75aa54b717325764153ccaa17dbb103230d46b9c5ca2c587dfb42",
      "signature": {
        "s": "0x0cf452d4d93cd887e09bc7bedaf07a73e25239ba512c5b943896cd4a7b850436",
        "r": "0x8c53738944eccc4dd1ab5d056640cc5a05fe4858405cba1f3d6a7cb43ec302c7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1713",
    "total": "1713"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1713",
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
            "amount": "558390"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YWQ2YmQ1My1kNGI0LTViODYtOTllZi1jOTAzNzA2M2Q0MmUifQ==",
    "nonce": 955,
    "balances": {
      "current": "10000001525339658",
      "previous": "10000001525341372"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda3e002a588d5a01f3a2f20dc29b971a4f1a228e",
    "nonce": 20,
    "balances": {
      "current": "1713",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:45.676Z",
  "updated": "2020-05-22T08:05:45.748Z",
  "id": "5ec787d9b0c6090011d5aa0f"
}
```
* *stageAmount*: `1713`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000006b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000006b100000000000000000000000000000000000000000000000000000000000006b1b8a3c89ef12fc37d8fea8c58425b8ed39fdc35ea632bd78cb2049861feee7eb7581beb3203630451826d74981efb29efa9d42dfaa14b5625316e40b703c6012a1063b57ce3810399344872299a6b0a0df8701ce10d660645c61d26f924385ce1000000000000000000000000000000000000000000000000000000000000001b7d287850cfc75aa54b717325764153ccaa17dbb103230d46b9c5ca2c587dfb428c53738944eccc4dd1ab5d056640cc5a05fe4858405cba1f3d6a7cb43ec302c70cf452d4d93cd887e09bc7bedaf07a73e25239ba512c5b943896cd4a7b850436000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003bb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caabd60a000000000000000000000000000000000000000000000000002386f2caabdcbc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008853600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493459575132596d51314d79316b4e4749304c5456694f4459744f546c6c5a69316a4f54417a4e7a41324d3251304d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da3e002a588d5a01f3a2f20dc29b971a4f1a228e00000000000000000000000000000000000000000000000000000000000006b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb8a3c89ef12fc37d8fea8c58425b8ed39fdc35ea632bd78cb2049861feee7eb7",
      "signature": {
        "s": "0x1063b57ce3810399344872299a6b0a0df8701ce10d660645c61d26f924385ce1",
        "r": "0x581beb3203630451826d74981efb29efa9d42dfaa14b5625316e40b703c6012a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7d287850cfc75aa54b717325764153ccaa17dbb103230d46b9c5ca2c587dfb42",
      "signature": {
        "s": "0x0cf452d4d93cd887e09bc7bedaf07a73e25239ba512c5b943896cd4a7b850436",
        "r": "0x8c53738944eccc4dd1ab5d056640cc5a05fe4858405cba1f3d6a7cb43ec302c7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1713",
    "total": "1713"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1713",
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
            "amount": "558390"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YWQ2YmQ1My1kNGI0LTViODYtOTllZi1jOTAzNzA2M2Q0MmUifQ==",
    "nonce": 955,
    "balances": {
      "current": "10000001525339658",
      "previous": "10000001525341372"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda3e002a588d5a01f3a2f20dc29b971a4f1a228e",
    "nonce": 20,
    "balances": {
      "current": "1713",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:45.676Z",
  "updated": "2020-05-22T08:05:45.748Z",
  "id": "5ec787d9b0c6090011d5aa0f"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000006b10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1713`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``