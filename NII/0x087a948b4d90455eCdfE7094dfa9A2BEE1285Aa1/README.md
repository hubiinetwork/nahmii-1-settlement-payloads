# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x087a948b4d90455eCdfE7094dfa9A2BEE1285Aa1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000002c8b32dde7e830de000000000000000000000000000000000000000000000000010e5b60fd8dadc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000010e5b60fd8dadc10000000000000000000000000000000000000000000000001da27a95b12d24c3fc215b786deeb2ca80b13a4be8a00d57456c2a1a4ef75a0202293b97b605a7074812c6c7c1b341d3f8c330d032750c5e547c202ca317df8e13c4f284dea434626ff955f1467cb3453a77b5ecdae8e24429d8b92d01f1ff36490118e8bfa966fd000000000000000000000000000000000000000000000000000000000000001bd1a8a2ad557e1917af11aac6653e0d0bdeec7e5f2ffdf7efd8a08fd67f31f8e44801021dab44aa4a265cb59548f65c4f910193837728934969d5f935c1d3c08c7e305cc8cfe00770a736510da048aa31b05ccf168dadda7445389518bfbdf19a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b05f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004efb5f46290e22b6f925000000000000000000000000000000000000000000004efb6054c9a53d3197f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000045361cecf1110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d82f011330a636bbec0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d324d305a4459335a53307a4d544d774c5455315a5751744f4441314e69316b4d5745305a57526d4d545a6a596a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000087a948b4d90455ecdfe7094dfa9a2bee1285aa10000000000000000000000000000000000000000000000002c8b32dde7e830de0000000000000000000000000000000000000000000000002b7cd77cea5a831d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfc215b786deeb2ca80b13a4be8a00d57456c2a1a4ef75a0202293b97b605a707",
      "signature": {
        "s": "0x6ff955f1467cb3453a77b5ecdae8e24429d8b92d01f1ff36490118e8bfa966fd",
        "r": "0x4812c6c7c1b341d3f8c330d032750c5e547c202ca317df8e13c4f284dea43462",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd1a8a2ad557e1917af11aac6653e0d0bdeec7e5f2ffdf7efd8a08fd67f31f8e4",
      "signature": {
        "s": "0x7e305cc8cfe00770a736510da048aa31b05ccf168dadda7445389518bfbdf19a",
        "r": "0x4801021dab44aa4a265cb59548f65c4f910193837728934969d5f935c1d3c08c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "76098715840785857",
    "total": "2135403956668277955"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76098715840785857",
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
            "amount": "27599716143763916504044"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "76098715840785"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkM2M0ZDY3ZS0zMTMwLTU1ZWQtODA1Ni1kMWE0ZWRmMTZjYjcifQ==",
    "nonce": 110687,
    "balances": {
      "current": "372981583646156085721381",
      "previous": "372981659820970642348023"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x087a948b4d90455ecdfe7094dfa9a2bee1285aa1",
    "nonce": 46,
    "balances": {
      "current": "3209715088091525342",
      "previous": "3133616372250739485"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:31.547Z",
  "updated": "2022-05-04T08:54:31.644Z",
  "id": "62723f473592fd001130b52a"
}
```
* *stageAmount*: `3209715088091525342`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000010e5b60fd8dadc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000010e5b60fd8dadc10000000000000000000000000000000000000000000000001da27a95b12d24c3fc215b786deeb2ca80b13a4be8a00d57456c2a1a4ef75a0202293b97b605a7074812c6c7c1b341d3f8c330d032750c5e547c202ca317df8e13c4f284dea434626ff955f1467cb3453a77b5ecdae8e24429d8b92d01f1ff36490118e8bfa966fd000000000000000000000000000000000000000000000000000000000000001bd1a8a2ad557e1917af11aac6653e0d0bdeec7e5f2ffdf7efd8a08fd67f31f8e44801021dab44aa4a265cb59548f65c4f910193837728934969d5f935c1d3c08c7e305cc8cfe00770a736510da048aa31b05ccf168dadda7445389518bfbdf19a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b05f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004efb5f46290e22b6f925000000000000000000000000000000000000000000004efb6054c9a53d3197f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000045361cecf1110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d82f011330a636bbec0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d324d305a4459335a53307a4d544d774c5455315a5751744f4441314e69316b4d5745305a57526d4d545a6a596a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000087a948b4d90455ecdfe7094dfa9a2bee1285aa10000000000000000000000000000000000000000000000002c8b32dde7e830de0000000000000000000000000000000000000000000000002b7cd77cea5a831d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfc215b786deeb2ca80b13a4be8a00d57456c2a1a4ef75a0202293b97b605a707",
      "signature": {
        "s": "0x6ff955f1467cb3453a77b5ecdae8e24429d8b92d01f1ff36490118e8bfa966fd",
        "r": "0x4812c6c7c1b341d3f8c330d032750c5e547c202ca317df8e13c4f284dea43462",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd1a8a2ad557e1917af11aac6653e0d0bdeec7e5f2ffdf7efd8a08fd67f31f8e4",
      "signature": {
        "s": "0x7e305cc8cfe00770a736510da048aa31b05ccf168dadda7445389518bfbdf19a",
        "r": "0x4801021dab44aa4a265cb59548f65c4f910193837728934969d5f935c1d3c08c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "76098715840785857",
    "total": "2135403956668277955"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76098715840785857",
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
            "amount": "27599716143763916504044"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "76098715840785"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkM2M0ZDY3ZS0zMTMwLTU1ZWQtODA1Ni1kMWE0ZWRmMTZjYjcifQ==",
    "nonce": 110687,
    "balances": {
      "current": "372981583646156085721381",
      "previous": "372981659820970642348023"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x087a948b4d90455ecdfe7094dfa9a2bee1285aa1",
    "nonce": 46,
    "balances": {
      "current": "3209715088091525342",
      "previous": "3133616372250739485"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:31.547Z",
  "updated": "2022-05-04T08:54:31.644Z",
  "id": "62723f473592fd001130b52a"
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
0x0f200f9b0000000000000000000000000000000000000000000000002c8b32dde7e830de0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3209715088091525342`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`