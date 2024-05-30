# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD4f82cFae0112A579bCa7749Ee8799AAE12C1b81`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001838913734e01ef7a20000000000000000000000000000000000000000000000000000000d444a9c240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000d444a9c24000000000000000000000000000000000000000000000000000001359fb49fb233e4efb2e4844063748e7be850298ccaa12749b6e0c175e64ff49a844854ec66b525b3e5f94cb89c91574b4117525a6ff370b97c859058663b210a62c20c25194cc6c6331fc2306866c151c15d04bad42c57649e9e124aab4315cba272a945b1000000000000000000000000000000000000000000000000000000000000001b15a8f92436e1234c06b5c2a251b3499089662690ab4b29eac7490e931d1e02f2f81ae751232a9d02aa2f6e0ab07f7cbc24c4aeecd18029ceee5adbe074934996484f39b1813207334210c77c79c4e82f369b6cade04d6c58489beeb425adcd3d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac5f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a8c6dda31e8f5b27ba0000000000000000000000000000000000000000000009a8c6dda31f63d628b1f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000365735b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4db9df43c735d9ead0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d7a466c4e7a566d4f43307a5a6a42684c5455324e6d45744f544d774e7931694e44566c4d4449344e6a63355a6d496966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000d4f82cfae0112a579bca7749ee8799aae12c1b8100000000000000000000000000000000000000000000001838913734e01ef7a2000000000000000000000000000000000000000000000018389137279bd45b7e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x33e4efb2e4844063748e7be850298ccaa12749b6e0c175e64ff49a844854ec66",
      "signature": {
        "s": "0x4cc6c6331fc2306866c151c15d04bad42c57649e9e124aab4315cba272a945b1",
        "r": "0xb525b3e5f94cb89c91574b4117525a6ff370b97c859058663b210a62c20c2519",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x15a8f92436e1234c06b5c2a251b3499089662690ab4b29eac7490e931d1e02f2",
      "signature": {
        "s": "0x484f39b1813207334210c77c79c4e82f369b6cade04d6c58489beeb425adcd3d",
        "r": "0xf81ae751232a9d02aa2f6e0ab07f7cbc24c4aeecd18029ceee5adbe074934996",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "56980315172",
    "total": "1329824309170"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "56980315172",
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
            "amount": "27243219326001418706605"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "56980315"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MzFlNzVmOC0zZjBhLTU2NmEtOTMwNy1iNDVlMDI4Njc5ZmIifQ==",
    "nonce": 109663,
    "balances": {
      "current": "729834898226416381492128",
      "previous": "729834898226473418787615"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd4f82cfae0112a579bca7749ee8799aae12c1b81",
    "nonce": 36,
    "balances": {
      "current": "446797957607014201250",
      "previous": "446797957550033886078"
    }
  },
  "blockNumber": "14709945",
  "created": "2022-05-04T08:49:16.258Z",
  "updated": "2022-05-04T08:49:16.316Z",
  "id": "62723e0cbbd75600116d045b"
}
```
* *stageAmount*: `446797957607014201250`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000d444a9c240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000d444a9c24000000000000000000000000000000000000000000000000000001359fb49fb233e4efb2e4844063748e7be850298ccaa12749b6e0c175e64ff49a844854ec66b525b3e5f94cb89c91574b4117525a6ff370b97c859058663b210a62c20c25194cc6c6331fc2306866c151c15d04bad42c57649e9e124aab4315cba272a945b1000000000000000000000000000000000000000000000000000000000000001b15a8f92436e1234c06b5c2a251b3499089662690ab4b29eac7490e931d1e02f2f81ae751232a9d02aa2f6e0ab07f7cbc24c4aeecd18029ceee5adbe074934996484f39b1813207334210c77c79c4e82f369b6cade04d6c58489beeb425adcd3d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac5f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a8c6dda31e8f5b27ba0000000000000000000000000000000000000000000009a8c6dda31f63d628b1f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000365735b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4db9df43c735d9ead0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d7a466c4e7a566d4f43307a5a6a42684c5455324e6d45744f544d774e7931694e44566c4d4449344e6a63355a6d496966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000d4f82cfae0112a579bca7749ee8799aae12c1b8100000000000000000000000000000000000000000000001838913734e01ef7a2000000000000000000000000000000000000000000000018389137279bd45b7e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x33e4efb2e4844063748e7be850298ccaa12749b6e0c175e64ff49a844854ec66",
      "signature": {
        "s": "0x4cc6c6331fc2306866c151c15d04bad42c57649e9e124aab4315cba272a945b1",
        "r": "0xb525b3e5f94cb89c91574b4117525a6ff370b97c859058663b210a62c20c2519",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x15a8f92436e1234c06b5c2a251b3499089662690ab4b29eac7490e931d1e02f2",
      "signature": {
        "s": "0x484f39b1813207334210c77c79c4e82f369b6cade04d6c58489beeb425adcd3d",
        "r": "0xf81ae751232a9d02aa2f6e0ab07f7cbc24c4aeecd18029ceee5adbe074934996",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "56980315172",
    "total": "1329824309170"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "56980315172",
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
            "amount": "27243219326001418706605"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "56980315"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MzFlNzVmOC0zZjBhLTU2NmEtOTMwNy1iNDVlMDI4Njc5ZmIifQ==",
    "nonce": 109663,
    "balances": {
      "current": "729834898226416381492128",
      "previous": "729834898226473418787615"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd4f82cfae0112a579bca7749ee8799aae12c1b81",
    "nonce": 36,
    "balances": {
      "current": "446797957607014201250",
      "previous": "446797957550033886078"
    }
  },
  "blockNumber": "14709945",
  "created": "2022-05-04T08:49:16.258Z",
  "updated": "2022-05-04T08:49:16.316Z",
  "id": "62723e0cbbd75600116d045b"
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
0x0f200f9b00000000000000000000000000000000000000000000001838913734e01ef7a20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `446797957607014201250`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`