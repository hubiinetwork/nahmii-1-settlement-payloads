# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xaaFA153278D151b0D464fd5dda56AEE92429AAa7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001bee423de2a772014e000000000000000000000000000000000000000000000000000000052161193a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000052161193a00000000000000000000000000000000000000000000000f2e646bf99daeee13f9a8aceb5532c87ae3357af39a42029e2db6c5d0339de28ec34a1be97326e13e55e6d081f1368e52ccf9c90149666dc98f224f580850b5eccc0f53f537c5aba950465bc6aeda321625c4fe93ab40f0518df2596e014bb4ff09bba2a14ce9bd5a000000000000000000000000000000000000000000000000000000000000001bc2658d31aa2ee3f0a70841da4d5a1667c35abf4ac43d326d57b025bc4d65843af6a1d712dec02e096b00965fb316d278d93d3c7b9ac86d1afa93f9d10e6290222f9fbc59d51a9e05d345fbc8fc88e687130bbac22368a64972b7cb14d3415995000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adbb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009662469ad89604e9d9a7000000000000000000000000000000000000000000009662469ad89b279b2c8100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000015039a00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ec479365f6cd93ec0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f5756694d5452684d7931694d6a4a6b4c54557a4d6d4d744f54526d4f4331685a4446694e6a6c6c4f446c68597a596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000aafa153278d151b0d464fd5dda56aee92429aaa700000000000000000000000000000000000000000000001bee423de2a772014e00000000000000000000000000000000000000000000001bee423ddd8610e81400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf9a8aceb5532c87ae3357af39a42029e2db6c5d0339de28ec34a1be97326e13e",
      "signature": {
        "s": "0x50465bc6aeda321625c4fe93ab40f0518df2596e014bb4ff09bba2a14ce9bd5a",
        "r": "0x55e6d081f1368e52ccf9c90149666dc98f224f580850b5eccc0f53f537c5aba9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc2658d31aa2ee3f0a70841da4d5a1667c35abf4ac43d326d57b025bc4d65843a",
      "signature": {
        "s": "0x2f9fbc59d51a9e05d345fbc8fc88e687130bbac22368a64972b7cb14d3415995",
        "r": "0xf6a1d712dec02e096b00965fb316d278d93d3c7b9ac86d1afa93f9d10e629022",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "22034848058",
    "total": "280044076648895540755"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "22034848058",
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
            "amount": "27262866735851446834156"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "22034848"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyOWViMTRhMy1iMjJkLTUzMmMtOTRmOC1hZDFiNjllODlhYzYifQ==",
    "nonce": 110011,
    "balances": {
      "current": "710167840966538225637799",
      "previous": "710167840966560282520705"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaafa153278d151b0d464fd5dda56aee92429aaa7",
    "nonce": 46,
    "balances": {
      "current": "515230442763328815438",
      "previous": "515230442741293967380"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:51:05.334Z",
  "updated": "2022-05-04T08:51:05.408Z",
  "id": "62723e79bbd75600116d04d5"
}
```
* *stageAmount*: `515230442763328815438`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000052161193a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000052161193a00000000000000000000000000000000000000000000000f2e646bf99daeee13f9a8aceb5532c87ae3357af39a42029e2db6c5d0339de28ec34a1be97326e13e55e6d081f1368e52ccf9c90149666dc98f224f580850b5eccc0f53f537c5aba950465bc6aeda321625c4fe93ab40f0518df2596e014bb4ff09bba2a14ce9bd5a000000000000000000000000000000000000000000000000000000000000001bc2658d31aa2ee3f0a70841da4d5a1667c35abf4ac43d326d57b025bc4d65843af6a1d712dec02e096b00965fb316d278d93d3c7b9ac86d1afa93f9d10e6290222f9fbc59d51a9e05d345fbc8fc88e687130bbac22368a64972b7cb14d3415995000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adbb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009662469ad89604e9d9a7000000000000000000000000000000000000000000009662469ad89b279b2c8100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000015039a00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ec479365f6cd93ec0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f5756694d5452684d7931694d6a4a6b4c54557a4d6d4d744f54526d4f4331685a4446694e6a6c6c4f446c68597a596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000aafa153278d151b0d464fd5dda56aee92429aaa700000000000000000000000000000000000000000000001bee423de2a772014e00000000000000000000000000000000000000000000001bee423ddd8610e81400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf9a8aceb5532c87ae3357af39a42029e2db6c5d0339de28ec34a1be97326e13e",
      "signature": {
        "s": "0x50465bc6aeda321625c4fe93ab40f0518df2596e014bb4ff09bba2a14ce9bd5a",
        "r": "0x55e6d081f1368e52ccf9c90149666dc98f224f580850b5eccc0f53f537c5aba9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc2658d31aa2ee3f0a70841da4d5a1667c35abf4ac43d326d57b025bc4d65843a",
      "signature": {
        "s": "0x2f9fbc59d51a9e05d345fbc8fc88e687130bbac22368a64972b7cb14d3415995",
        "r": "0xf6a1d712dec02e096b00965fb316d278d93d3c7b9ac86d1afa93f9d10e629022",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "22034848058",
    "total": "280044076648895540755"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "22034848058",
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
            "amount": "27262866735851446834156"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "22034848"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyOWViMTRhMy1iMjJkLTUzMmMtOTRmOC1hZDFiNjllODlhYzYifQ==",
    "nonce": 110011,
    "balances": {
      "current": "710167840966538225637799",
      "previous": "710167840966560282520705"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaafa153278d151b0d464fd5dda56aee92429aaa7",
    "nonce": 46,
    "balances": {
      "current": "515230442763328815438",
      "previous": "515230442741293967380"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:51:05.334Z",
  "updated": "2022-05-04T08:51:05.408Z",
  "id": "62723e79bbd75600116d04d5"
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
0x0f200f9b00000000000000000000000000000000000000000000001bee423de2a772014e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `515230442763328815438`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`