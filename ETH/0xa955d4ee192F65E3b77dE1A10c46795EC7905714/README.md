# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa955d4ee192F65E3b77dE1A10c46795EC7905714`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000004793811f65a9ec4ec9e9483f081f680ecf56581b6f65bb40328e90d4dca7a2843f74325c908eab61ccd18f54ff53f091bf5a17a30bb8be8381ea4a57f66a2b5882214d56d506ad6cc2181721c634dce80d4915ec74a0dd142aebb7d88ccf8b239e83000000000000000000000000000000000000000000000000000000000000001b10518c8b4de351efdc43f3a30ca2492581e814ace24a50a866c775fbbe669369caf2e79151ab2ea0937a13bd4d0aceb01f9630bf26fef47799597b8590872497102f937df84cb47552becbc1f6a33f48fd7358f37b97b4077e340048c87c70a3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000073900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c42076d3000000000000000000000000000000000000000000000000002386f2c420be7800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a30ba00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e324d3259574e684e53307a4d44637a4c5456695a6d51744f4749345953316a596a51314e7a41304f54597a4d54496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a955d4ee192f65e3b77de1a10c46795ec79057140000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x811f65a9ec4ec9e9483f081f680ecf56581b6f65bb40328e90d4dca7a2843f74",
      "signature": {
        "s": "0x4d56d506ad6cc2181721c634dce80d4915ec74a0dd142aebb7d88ccf8b239e83",
        "r": "0x325c908eab61ccd18f54ff53f091bf5a17a30bb8be8381ea4a57f66a2b588221",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x10518c8b4de351efdc43f3a30ca2492581e814ace24a50a866c775fbbe669369",
      "signature": {
        "s": "0x102f937df84cb47552becbc1f6a33f48fd7358f37b97b4077e340048c87c70a3",
        "r": "0xcaf2e79151ab2ea0937a13bd4d0aceb01f9630bf26fef47799597b8590872497",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
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
            "amount": "667834"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxN2M2YWNhNS0zMDczLTViZmQtOGI4YS1jYjQ1NzA0OTYzMTIifQ==",
    "nonce": 1849,
    "balances": {
      "current": "10000001415542483",
      "previous": "10000001415560824"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa955d4ee192f65e3b77de1a10c46795ec7905714",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:32.049Z",
  "updated": "2020-05-22T08:12:35.160Z",
  "id": "5ec78970005df800101bc48f"
}
```
* *stageAmount*: `18323`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000004793811f65a9ec4ec9e9483f081f680ecf56581b6f65bb40328e90d4dca7a2843f74325c908eab61ccd18f54ff53f091bf5a17a30bb8be8381ea4a57f66a2b5882214d56d506ad6cc2181721c634dce80d4915ec74a0dd142aebb7d88ccf8b239e83000000000000000000000000000000000000000000000000000000000000001b10518c8b4de351efdc43f3a30ca2492581e814ace24a50a866c775fbbe669369caf2e79151ab2ea0937a13bd4d0aceb01f9630bf26fef47799597b8590872497102f937df84cb47552becbc1f6a33f48fd7358f37b97b4077e340048c87c70a3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000073900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c42076d3000000000000000000000000000000000000000000000000002386f2c420be7800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a30ba00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e324d3259574e684e53307a4d44637a4c5456695a6d51744f4749345953316a596a51314e7a41304f54597a4d54496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a955d4ee192f65e3b77de1a10c46795ec79057140000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x811f65a9ec4ec9e9483f081f680ecf56581b6f65bb40328e90d4dca7a2843f74",
      "signature": {
        "s": "0x4d56d506ad6cc2181721c634dce80d4915ec74a0dd142aebb7d88ccf8b239e83",
        "r": "0x325c908eab61ccd18f54ff53f091bf5a17a30bb8be8381ea4a57f66a2b588221",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x10518c8b4de351efdc43f3a30ca2492581e814ace24a50a866c775fbbe669369",
      "signature": {
        "s": "0x102f937df84cb47552becbc1f6a33f48fd7358f37b97b4077e340048c87c70a3",
        "r": "0xcaf2e79151ab2ea0937a13bd4d0aceb01f9630bf26fef47799597b8590872497",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
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
            "amount": "667834"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxN2M2YWNhNS0zMDczLTViZmQtOGI4YS1jYjQ1NzA0OTYzMTIifQ==",
    "nonce": 1849,
    "balances": {
      "current": "10000001415542483",
      "previous": "10000001415560824"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa955d4ee192f65e3b77de1a10c46795ec7905714",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:32.049Z",
  "updated": "2020-05-22T08:12:35.160Z",
  "id": "5ec78970005df800101bc48f"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18323`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``