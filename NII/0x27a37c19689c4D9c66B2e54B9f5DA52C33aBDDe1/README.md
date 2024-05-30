# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x27a37c19689c4D9c66B2e54B9f5DA52C33aBDDe1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000a491792db0e4ea3bb00000000000000000000000000000000000000000000000309c9f042b58147c00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000309c9f042b58147c000000000000000000000000000000000000000000000000a491792db0e4ea3bbd1a097111e4d8fe50692067a30a5f88192ceb64ab3b566fdf5462269be910e536143716cb9eead381a54a40958f28df303821dce08691008478f2f1ac28e512059b8fa9100a99f4a80b26f851b395fe93d7929bf281d0393fa9e1408c53e5fe3000000000000000000000000000000000000000000000000000000000000001cb1afc9ee5295a8d8be297f8447c7f3829b8ff45a39c27a798e300652bb8da48db4dd3a3e848c55ae0d8754f46d4cf4abea957214bd54f75154e18af60da080b772318ea3f413d799e94123f7723f95e7e460e0e341d4dc7ff6618998dfae5ce0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000d7741400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000015f19000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002a1bd74f061376994fb8000000000000000000000000000000000000000000002a1ee1e013813f3ab89000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000c71d2b132021180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000046685a49332d18117580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e44526a596a593259533030593245774c54557a596d45744f44526a4d79316d596a63784e5755344e6d4a6b5932556966513d3d000000000000000000000000000000000000000000000000000000000000000200000000000000000000000027a37c19689c4d9c66b2e54b9f5da52c33abdde100000000000000000000000000000000000000000000000a491792db0e4ea3bb0000000000000000000000000000000000000000000000073f4da29858cd5bfb00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd1a097111e4d8fe50692067a30a5f88192ceb64ab3b566fdf5462269be910e53",
      "signature": {
        "s": "0x59b8fa9100a99f4a80b26f851b395fe93d7929bf281d0393fa9e1408c53e5fe3",
        "r": "0x6143716cb9eead381a54a40958f28df303821dce08691008478f2f1ac28e5120",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb1afc9ee5295a8d8be297f8447c7f3829b8ff45a39c27a798e300652bb8da48d",
      "signature": {
        "s": "0x72318ea3f413d799e94123f7723f95e7e460e0e341d4dc7ff6618998dfae5ce0",
        "r": "0xb4dd3a3e848c55ae0d8754f46d4cf4abea957214bd54f75154e18af60da080b7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "56045591207092504512",
    "total": "189734280495864128443"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "56045591207092504512",
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
            "amount": "20780663810746652628824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "56045591207092504"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NDRjYjY2YS00Y2EwLTUzYmEtODRjMy1mYjcxNWU4NmJkY2UifQ==",
    "nonce": 89881,
    "balances": {
      "current": "198852968996437235421112",
      "previous": "198909070633235535018128"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x27a37c19689c4d9c66b2e54b9f5da52c33abdde1",
    "nonce": 2,
    "balances": {
      "current": "189734280495864128443",
      "previous": "133688689288771623931"
    }
  },
  "blockNumber": "14119956",
  "created": "2022-02-01T11:58:28.038Z",
  "updated": "2022-02-01T11:58:28.187Z",
  "id": "61f92064b7e258001221f326"
}
```
* *stageAmount*: `189734280495864128443`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000309c9f042b58147c00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000309c9f042b58147c000000000000000000000000000000000000000000000000a491792db0e4ea3bbd1a097111e4d8fe50692067a30a5f88192ceb64ab3b566fdf5462269be910e536143716cb9eead381a54a40958f28df303821dce08691008478f2f1ac28e512059b8fa9100a99f4a80b26f851b395fe93d7929bf281d0393fa9e1408c53e5fe3000000000000000000000000000000000000000000000000000000000000001cb1afc9ee5295a8d8be297f8447c7f3829b8ff45a39c27a798e300652bb8da48db4dd3a3e848c55ae0d8754f46d4cf4abea957214bd54f75154e18af60da080b772318ea3f413d799e94123f7723f95e7e460e0e341d4dc7ff6618998dfae5ce0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000d7741400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000015f19000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002a1bd74f061376994fb8000000000000000000000000000000000000000000002a1ee1e013813f3ab89000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000c71d2b132021180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000046685a49332d18117580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e44526a596a593259533030593245774c54557a596d45744f44526a4d79316d596a63784e5755344e6d4a6b5932556966513d3d000000000000000000000000000000000000000000000000000000000000000200000000000000000000000027a37c19689c4d9c66b2e54b9f5da52c33abdde100000000000000000000000000000000000000000000000a491792db0e4ea3bb0000000000000000000000000000000000000000000000073f4da29858cd5bfb00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd1a097111e4d8fe50692067a30a5f88192ceb64ab3b566fdf5462269be910e53",
      "signature": {
        "s": "0x59b8fa9100a99f4a80b26f851b395fe93d7929bf281d0393fa9e1408c53e5fe3",
        "r": "0x6143716cb9eead381a54a40958f28df303821dce08691008478f2f1ac28e5120",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb1afc9ee5295a8d8be297f8447c7f3829b8ff45a39c27a798e300652bb8da48d",
      "signature": {
        "s": "0x72318ea3f413d799e94123f7723f95e7e460e0e341d4dc7ff6618998dfae5ce0",
        "r": "0xb4dd3a3e848c55ae0d8754f46d4cf4abea957214bd54f75154e18af60da080b7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "56045591207092504512",
    "total": "189734280495864128443"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "56045591207092504512",
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
            "amount": "20780663810746652628824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "56045591207092504"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NDRjYjY2YS00Y2EwLTUzYmEtODRjMy1mYjcxNWU4NmJkY2UifQ==",
    "nonce": 89881,
    "balances": {
      "current": "198852968996437235421112",
      "previous": "198909070633235535018128"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x27a37c19689c4d9c66b2e54b9f5da52c33abdde1",
    "nonce": 2,
    "balances": {
      "current": "189734280495864128443",
      "previous": "133688689288771623931"
    }
  },
  "blockNumber": "14119956",
  "created": "2022-02-01T11:58:28.038Z",
  "updated": "2022-02-01T11:58:28.187Z",
  "id": "61f92064b7e258001221f326"
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
0x0f200f9b00000000000000000000000000000000000000000000000a491792db0e4ea3bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `189734280495864128443`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`