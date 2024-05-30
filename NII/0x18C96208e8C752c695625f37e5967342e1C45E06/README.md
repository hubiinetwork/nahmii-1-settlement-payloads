# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x18C96208e8C752c695625f37e5967342e1C45E06`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000002494ab834a7e7aead0000000000000000000000000000000000000000000000007bfb519b4036d72e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000007bfb519b4036d72e000000000000000000000000000000000000000000000002494ab834a7e7aeadac49f6d9979c66d25b0f2dc4f70e1d9002a8fa1216e99f3116ac9ddcc4b04e45a673244395ac8d760a7503b8083e230b9ac0858cf8f7dd9ad3039a960622e1df55bfb398a83683bb1aa6bce7c6da4a6d3042ac413ca7d38b4f906a9aacd511e1000000000000000000000000000000000000000000000000000000000000001be555caf386853e78c6ec63f211dcbf11a8b67040e1dd5e2d9dfa0955ce98fad878aab4bd02443180ca014315aa46e9820c8602149920ad429d2482b803a0e4f55a24edcd189e383eb41b21e592a04d7cd96885c5e06d6233a46dcbfefe341f73000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000139a3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026c418f53341d6414d5f0000000000000000000000000000000000000000000026c4951042211540e6d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001fbd43fec8c2430000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c4e8b90416f373b28e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e324e694d4446684e6930354e6a64684c54557a4e3245744f544a6c4e433077596a4a694e6d593059574d324e6d496966513d3d000000000000000000000000000000000000000000000000000000000000000500000000000000000000000018c96208e8c752c695625f37e5967342e1c45e06000000000000000000000000000000000000000000000002494ab834a7e7aead000000000000000000000000000000000000000000000001cd4f669967b0d77f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xac49f6d9979c66d25b0f2dc4f70e1d9002a8fa1216e99f3116ac9ddcc4b04e45",
      "signature": {
        "s": "0x55bfb398a83683bb1aa6bce7c6da4a6d3042ac413ca7d38b4f906a9aacd511e1",
        "r": "0xa673244395ac8d760a7503b8083e230b9ac0858cf8f7dd9ad3039a960622e1df",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe555caf386853e78c6ec63f211dcbf11a8b67040e1dd5e2d9dfa0955ce98fad8",
      "signature": {
        "s": "0x5a24edcd189e383eb41b21e592a04d7cd96885c5e06d6233a46dcbfefe341f73",
        "r": "0x78aab4bd02443180ca014315aa46e9820c8602149920ad429d2482b803a0e4f5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8933824013058627374",
    "total": "42174724196759219885"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8933824013058627374",
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
            "amount": "17799430726240118747790"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8933824013058627"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmN2NiMDFhNi05NjdhLTUzN2EtOTJlNC0wYjJiNmY0YWM2NmIifQ==",
    "nonce": 80291,
    "balances": {
      "current": "183067286587477655113055",
      "previous": "183076229345314726799056"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x18c96208e8c752c695625f37e5967342e1c45e06",
    "nonce": 5,
    "balances": {
      "current": "42174724196759219885",
      "previous": "33240900183700592511"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:44.115Z",
  "updated": "2021-07-05T11:14:44.195Z",
  "id": "60e2e9a4cc369000105e3026"
}
```
* *stageAmount*: `42174724196759219885`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000007bfb519b4036d72e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000007bfb519b4036d72e000000000000000000000000000000000000000000000002494ab834a7e7aeadac49f6d9979c66d25b0f2dc4f70e1d9002a8fa1216e99f3116ac9ddcc4b04e45a673244395ac8d760a7503b8083e230b9ac0858cf8f7dd9ad3039a960622e1df55bfb398a83683bb1aa6bce7c6da4a6d3042ac413ca7d38b4f906a9aacd511e1000000000000000000000000000000000000000000000000000000000000001be555caf386853e78c6ec63f211dcbf11a8b67040e1dd5e2d9dfa0955ce98fad878aab4bd02443180ca014315aa46e9820c8602149920ad429d2482b803a0e4f55a24edcd189e383eb41b21e592a04d7cd96885c5e06d6233a46dcbfefe341f73000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000139a3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026c418f53341d6414d5f0000000000000000000000000000000000000000000026c4951042211540e6d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001fbd43fec8c2430000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c4e8b90416f373b28e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e324e694d4446684e6930354e6a64684c54557a4e3245744f544a6c4e433077596a4a694e6d593059574d324e6d496966513d3d000000000000000000000000000000000000000000000000000000000000000500000000000000000000000018c96208e8c752c695625f37e5967342e1c45e06000000000000000000000000000000000000000000000002494ab834a7e7aead000000000000000000000000000000000000000000000001cd4f669967b0d77f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xac49f6d9979c66d25b0f2dc4f70e1d9002a8fa1216e99f3116ac9ddcc4b04e45",
      "signature": {
        "s": "0x55bfb398a83683bb1aa6bce7c6da4a6d3042ac413ca7d38b4f906a9aacd511e1",
        "r": "0xa673244395ac8d760a7503b8083e230b9ac0858cf8f7dd9ad3039a960622e1df",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe555caf386853e78c6ec63f211dcbf11a8b67040e1dd5e2d9dfa0955ce98fad8",
      "signature": {
        "s": "0x5a24edcd189e383eb41b21e592a04d7cd96885c5e06d6233a46dcbfefe341f73",
        "r": "0x78aab4bd02443180ca014315aa46e9820c8602149920ad429d2482b803a0e4f5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8933824013058627374",
    "total": "42174724196759219885"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8933824013058627374",
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
            "amount": "17799430726240118747790"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8933824013058627"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmN2NiMDFhNi05NjdhLTUzN2EtOTJlNC0wYjJiNmY0YWM2NmIifQ==",
    "nonce": 80291,
    "balances": {
      "current": "183067286587477655113055",
      "previous": "183076229345314726799056"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x18c96208e8c752c695625f37e5967342e1c45e06",
    "nonce": 5,
    "balances": {
      "current": "42174724196759219885",
      "previous": "33240900183700592511"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:44.115Z",
  "updated": "2021-07-05T11:14:44.195Z",
  "id": "60e2e9a4cc369000105e3026"
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
0x0f200f9b000000000000000000000000000000000000000000000002494ab834a7e7aead0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `42174724196759219885`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`