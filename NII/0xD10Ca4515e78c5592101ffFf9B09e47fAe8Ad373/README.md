# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD10Ca4515e78c5592101ffFf9B09e47fAe8Ad373`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000003cf24e19484d4abab000000000000000000000000000000000000000000000000171e9bb1e18f880e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000171e9bb1e18f880e00000000000000000000000000000000000000000000000288c1e67583915896ea1e40e26c84443d65183eeb854f345f314f7efa704d0e3d4af1be002689faede2d1540c2e83032d89f1ec7cb2e2441b7b7325043bf3a8321ff3d01bf704fe161d88b1957a848387c4c960ac53526ec386c68ebb32f1d4e25c3abf5c961be8ff000000000000000000000000000000000000000000000000000000000000001c8f79d1472c2a2b15df37699c1719f1acbe4e0db611d715524230133359080aa0d85bfae6a8adadfce25fe668e7039d327b792595fc3af32c2ad5b46901fe9a1860281032a28ea18ebd336d43b9a078d6757190384c6ae3acdd694da42bc6596a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aee0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095d7e9b6f5d35aee8c540000000000000000000000000000000000000000000095d800db7caf2465e73400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005eb29e7e7d2d20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60faa43d526cc09510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e5759314e54457a4e6930354f574e6c4c5455794e325174595441784d79316c597a49784d4467794e5463304f44596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d10ca4515e78c5592101ffff9b09e47fae8ad373000000000000000000000000000000000000000000000003cf24e19484d4abab000000000000000000000000000000000000000000000003b80645e2a345239d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xea1e40e26c84443d65183eeb854f345f314f7efa704d0e3d4af1be002689faed",
      "signature": {
        "s": "0x1d88b1957a848387c4c960ac53526ec386c68ebb32f1d4e25c3abf5c961be8ff",
        "r": "0xe2d1540c2e83032d89f1ec7cb2e2441b7b7325043bf3a8321ff3d01bf704fe16",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8f79d1472c2a2b15df37699c1719f1acbe4e0db611d715524230133359080aa0",
      "signature": {
        "s": "0x60281032a28ea18ebd336d43b9a078d6757190384c6ae3acdd694da42bc6596a",
        "r": "0xd85bfae6a8adadfce25fe668e7039d327b792595fc3af32c2ad5b46901fe9a18",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1665940100469458958",
    "total": "46747898999475361942"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1665940100469458958",
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
            "amount": "27265416530182085019985"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1665940100469458"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlNWY1NTEzNi05OWNlLTUyN2QtYTAxMy1lYzIxMDgyNTc0ODYifQ==",
    "nonce": 110304,
    "balances": {
      "current": "707615496841569401474132",
      "previous": "707617164447609971402548"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd10ca4515e78c5592101ffff9b09e47fae8ad373",
    "nonce": 46,
    "balances": {
      "current": "70266535314141260715",
      "previous": "68600595213671801757"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:35.051Z",
  "updated": "2022-05-04T08:52:35.143Z",
  "id": "62723ed37832e20011830b86"
}
```
* *stageAmount*: `70266535314141260715`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000171e9bb1e18f880e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000171e9bb1e18f880e00000000000000000000000000000000000000000000000288c1e67583915896ea1e40e26c84443d65183eeb854f345f314f7efa704d0e3d4af1be002689faede2d1540c2e83032d89f1ec7cb2e2441b7b7325043bf3a8321ff3d01bf704fe161d88b1957a848387c4c960ac53526ec386c68ebb32f1d4e25c3abf5c961be8ff000000000000000000000000000000000000000000000000000000000000001c8f79d1472c2a2b15df37699c1719f1acbe4e0db611d715524230133359080aa0d85bfae6a8adadfce25fe668e7039d327b792595fc3af32c2ad5b46901fe9a1860281032a28ea18ebd336d43b9a078d6757190384c6ae3acdd694da42bc6596a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aee0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095d7e9b6f5d35aee8c540000000000000000000000000000000000000000000095d800db7caf2465e73400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005eb29e7e7d2d20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60faa43d526cc09510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e5759314e54457a4e6930354f574e6c4c5455794e325174595441784d79316c597a49784d4467794e5463304f44596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d10ca4515e78c5592101ffff9b09e47fae8ad373000000000000000000000000000000000000000000000003cf24e19484d4abab000000000000000000000000000000000000000000000003b80645e2a345239d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xea1e40e26c84443d65183eeb854f345f314f7efa704d0e3d4af1be002689faed",
      "signature": {
        "s": "0x1d88b1957a848387c4c960ac53526ec386c68ebb32f1d4e25c3abf5c961be8ff",
        "r": "0xe2d1540c2e83032d89f1ec7cb2e2441b7b7325043bf3a8321ff3d01bf704fe16",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8f79d1472c2a2b15df37699c1719f1acbe4e0db611d715524230133359080aa0",
      "signature": {
        "s": "0x60281032a28ea18ebd336d43b9a078d6757190384c6ae3acdd694da42bc6596a",
        "r": "0xd85bfae6a8adadfce25fe668e7039d327b792595fc3af32c2ad5b46901fe9a18",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1665940100469458958",
    "total": "46747898999475361942"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1665940100469458958",
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
            "amount": "27265416530182085019985"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1665940100469458"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlNWY1NTEzNi05OWNlLTUyN2QtYTAxMy1lYzIxMDgyNTc0ODYifQ==",
    "nonce": 110304,
    "balances": {
      "current": "707615496841569401474132",
      "previous": "707617164447609971402548"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd10ca4515e78c5592101ffff9b09e47fae8ad373",
    "nonce": 46,
    "balances": {
      "current": "70266535314141260715",
      "previous": "68600595213671801757"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:35.051Z",
  "updated": "2022-05-04T08:52:35.143Z",
  "id": "62723ed37832e20011830b86"
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
0x0f200f9b000000000000000000000000000000000000000000000003cf24e19484d4abab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `70266535314141260715`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`