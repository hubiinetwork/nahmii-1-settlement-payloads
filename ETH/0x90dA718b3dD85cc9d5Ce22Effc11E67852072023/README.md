# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x90dA718b3dD85cc9d5Ce22Effc11E67852072023`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000007604800000000000000000000000000000000000000000000000000000000000760480000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000007604800000000000000000000000000000000000000000000000000000000000760482eb9080932d4ff8ec07d8bf32bd05c5f951da5af91bd4d8d5cd5465c9089136391d4a4028965984ac721541987c846771ecbe7d38d8efde1f550615d3ab07b1d1ad3b6048f8fbab0924b1cdff5892538790078457f4176296fe41812f2969f0e000000000000000000000000000000000000000000000000000000000000001b7d37cde2b99bc6f27c18e9a1b3c31416ac5935048ab52245ebf8dfb96f0c764a5cbaaab6f7f3c1909221feb2abdd8d89640bca07bdf277b324978b1393ff86673136581fff081e022d2606fab78a8d1cd1c43f15af14c5e6de3efa7a00a314d1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001e500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb7df4c3000000000000000000000000000000000000000000000000002386f2cb8556ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000001e300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008503300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d6a56694d5441775a69316a4e445a684c545535593245744f54466b596931684f5451305a6a55794e6d59314d6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000090da718b3dd85cc9d5ce22effc11e678520720230000000000000000000000000000000000000000000000000000000000076048000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2eb9080932d4ff8ec07d8bf32bd05c5f951da5af91bd4d8d5cd5465c90891363",
      "signature": {
        "s": "0x1ad3b6048f8fbab0924b1cdff5892538790078457f4176296fe41812f2969f0e",
        "r": "0x91d4a4028965984ac721541987c846771ecbe7d38d8efde1f550615d3ab07b1d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7d37cde2b99bc6f27c18e9a1b3c31416ac5935048ab52245ebf8dfb96f0c764a",
      "signature": {
        "s": "0x3136581fff081e022d2606fab78a8d1cd1c43f15af14c5e6de3efa7a00a314d1",
        "r": "0x5cbaaab6f7f3c1909221feb2abdd8d89640bca07bdf277b324978b1393ff8667",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "483400",
    "total": "483400"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "483400",
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
            "amount": "544819"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "483"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMjViMTAwZi1jNDZhLTU5Y2EtOTFkYi1hOTQ0ZjUyNmY1MmMifQ==",
    "nonce": 485,
    "balances": {
      "current": "10000001539110083",
      "previous": "10000001539593966"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x90da718b3dd85cc9d5ce22effc11e67852072023",
    "nonce": 20,
    "balances": {
      "current": "483400",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:20.037Z",
  "updated": "2020-05-22T08:02:20.114Z",
  "id": "5ec7870cb0c6090011d5a96f"
}
```
* *stageAmount*: `483400`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000760480000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000007604800000000000000000000000000000000000000000000000000000000000760482eb9080932d4ff8ec07d8bf32bd05c5f951da5af91bd4d8d5cd5465c9089136391d4a4028965984ac721541987c846771ecbe7d38d8efde1f550615d3ab07b1d1ad3b6048f8fbab0924b1cdff5892538790078457f4176296fe41812f2969f0e000000000000000000000000000000000000000000000000000000000000001b7d37cde2b99bc6f27c18e9a1b3c31416ac5935048ab52245ebf8dfb96f0c764a5cbaaab6f7f3c1909221feb2abdd8d89640bca07bdf277b324978b1393ff86673136581fff081e022d2606fab78a8d1cd1c43f15af14c5e6de3efa7a00a314d1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001e500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb7df4c3000000000000000000000000000000000000000000000000002386f2cb8556ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000001e300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008503300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d6a56694d5441775a69316a4e445a684c545535593245744f54466b596931684f5451305a6a55794e6d59314d6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000090da718b3dd85cc9d5ce22effc11e678520720230000000000000000000000000000000000000000000000000000000000076048000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2eb9080932d4ff8ec07d8bf32bd05c5f951da5af91bd4d8d5cd5465c90891363",
      "signature": {
        "s": "0x1ad3b6048f8fbab0924b1cdff5892538790078457f4176296fe41812f2969f0e",
        "r": "0x91d4a4028965984ac721541987c846771ecbe7d38d8efde1f550615d3ab07b1d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7d37cde2b99bc6f27c18e9a1b3c31416ac5935048ab52245ebf8dfb96f0c764a",
      "signature": {
        "s": "0x3136581fff081e022d2606fab78a8d1cd1c43f15af14c5e6de3efa7a00a314d1",
        "r": "0x5cbaaab6f7f3c1909221feb2abdd8d89640bca07bdf277b324978b1393ff8667",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "483400",
    "total": "483400"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "483400",
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
            "amount": "544819"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "483"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMjViMTAwZi1jNDZhLTU5Y2EtOTFkYi1hOTQ0ZjUyNmY1MmMifQ==",
    "nonce": 485,
    "balances": {
      "current": "10000001539110083",
      "previous": "10000001539593966"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x90da718b3dd85cc9d5ce22effc11e67852072023",
    "nonce": 20,
    "balances": {
      "current": "483400",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:20.037Z",
  "updated": "2020-05-22T08:02:20.114Z",
  "id": "5ec7870cb0c6090011d5a96f"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000760480000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `483400`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``