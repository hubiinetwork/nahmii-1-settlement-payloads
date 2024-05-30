# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7B1f8FD5bC25D1D389085d9b7065d609C3E621c1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb60000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb60000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb62430248df1bd205b3a814c5e1191cb0cd5bd4a7609cc28bd5c30670b833dd6a05b40fd75dcb877e73d457ff81a75375c05a6b5b6540b9ca87eb3b1fd79df5953242c6f91d76f479771e009cacd732a81de12119656a723153c5f3de4649d58e0000000000000000000000000000000000000000000000000000000000000001bf889fc47db081a454ca7c48b3b611a7f95f6c718176815b9048dd3cb481155caa084aa0857a5833c8dcc6ae9d2f5e0e0d060377ba12c28c4e7c3c29e912a9daa75df892c85b8d3d32ffd1caf0f61bcf8e4307bcf48c4a541124881e59e5978c0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c6eb430000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001487b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000000105eb1c6ddaa15c9c8000000000000000000000000000000000000000000000010a90fe9f10dc62b2f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001304e4e91525b10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000404f67db39664b21d270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e6d4e6b4e4749774f533078596a45314c5455315a445574596d4e685953307a4d4449344f446b7a4d446c6b4e44676966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000007b1f8fd5bc25d1d389085d9b7065d609c3e621c10000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2430248df1bd205b3a814c5e1191cb0cd5bd4a7609cc28bd5c30670b833dd6a0",
      "signature": {
        "s": "0x242c6f91d76f479771e009cacd732a81de12119656a723153c5f3de4649d58e0",
        "r": "0x5b40fd75dcb877e73d457ff81a75375c05a6b5b6540b9ca87eb3b1fd79df5953",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf889fc47db081a454ca7c48b3b611a7f95f6c718176815b9048dd3cb481155ca",
      "signature": {
        "s": "0x75df892c85b8d3d32ffd1caf0f61bcf8e4307bcf48c4a541124881e59e5978c0",
        "r": "0xa084aa0857a5833c8dcc6ae9d2f5e0e0d060377ba12c28c4e7c3c29e912a9daa",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5353405767034289078",
    "total": "5353405767034289078"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5353405767034289078",
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
            "amount": "18981014457737354026279"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5353405767034289"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NmNkNGIwOS0xYjE1LTU1ZDUtYmNhYS0zMDI4ODkzMDlkNDgifQ==",
    "nonce": 84091,
    "balances": {
      "current": "301971358745139464648",
      "previous": "307330117917940788015"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7b1f8fd5bc25d1d389085d9b7065d609c3e621c1",
    "nonce": 1,
    "balances": {
      "current": "5353405767034289078",
      "previous": "0"
    }
  },
  "blockNumber": "13036355",
  "created": "2021-08-16T12:46:42.970Z",
  "updated": "2021-08-16T12:46:43.076Z",
  "id": "611a5e324b9bda00102879d4"
}
```
* *stageAmount*: `5353405767034289078`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb60000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb62430248df1bd205b3a814c5e1191cb0cd5bd4a7609cc28bd5c30670b833dd6a05b40fd75dcb877e73d457ff81a75375c05a6b5b6540b9ca87eb3b1fd79df5953242c6f91d76f479771e009cacd732a81de12119656a723153c5f3de4649d58e0000000000000000000000000000000000000000000000000000000000000001bf889fc47db081a454ca7c48b3b611a7f95f6c718176815b9048dd3cb481155caa084aa0857a5833c8dcc6ae9d2f5e0e0d060377ba12c28c4e7c3c29e912a9daa75df892c85b8d3d32ffd1caf0f61bcf8e4307bcf48c4a541124881e59e5978c0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c6eb430000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001487b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000000105eb1c6ddaa15c9c8000000000000000000000000000000000000000000000010a90fe9f10dc62b2f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001304e4e91525b10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000404f67db39664b21d270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e6d4e6b4e4749774f533078596a45314c5455315a445574596d4e685953307a4d4449344f446b7a4d446c6b4e44676966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000007b1f8fd5bc25d1d389085d9b7065d609c3e621c10000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2430248df1bd205b3a814c5e1191cb0cd5bd4a7609cc28bd5c30670b833dd6a0",
      "signature": {
        "s": "0x242c6f91d76f479771e009cacd732a81de12119656a723153c5f3de4649d58e0",
        "r": "0x5b40fd75dcb877e73d457ff81a75375c05a6b5b6540b9ca87eb3b1fd79df5953",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf889fc47db081a454ca7c48b3b611a7f95f6c718176815b9048dd3cb481155ca",
      "signature": {
        "s": "0x75df892c85b8d3d32ffd1caf0f61bcf8e4307bcf48c4a541124881e59e5978c0",
        "r": "0xa084aa0857a5833c8dcc6ae9d2f5e0e0d060377ba12c28c4e7c3c29e912a9daa",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5353405767034289078",
    "total": "5353405767034289078"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5353405767034289078",
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
            "amount": "18981014457737354026279"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5353405767034289"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NmNkNGIwOS0xYjE1LTU1ZDUtYmNhYS0zMDI4ODkzMDlkNDgifQ==",
    "nonce": 84091,
    "balances": {
      "current": "301971358745139464648",
      "previous": "307330117917940788015"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7b1f8fd5bc25d1d389085d9b7065d609c3e621c1",
    "nonce": 1,
    "balances": {
      "current": "5353405767034289078",
      "previous": "0"
    }
  },
  "blockNumber": "13036355",
  "created": "2021-08-16T12:46:42.970Z",
  "updated": "2021-08-16T12:46:43.076Z",
  "id": "611a5e324b9bda00102879d4"
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
0x0f200f9b0000000000000000000000000000000000000000000000004a4b1e2e7a9b3bb60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5353405767034289078`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`