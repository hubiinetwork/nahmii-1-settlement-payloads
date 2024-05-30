# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0CA87DEf88161442F874AcB8acb7E5D5e0FC5916`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000005a300000000000000000000000000000000000000000000000000000000000005a3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000005a300000000000000000000000000000000000000000000000000000000000005a3055b5fcbd7c9972c46063f3c6b0f887bd8bb469cd8b859be816a07937f45864aaea1dd345b6904626c837352ddd6b7d7398050d02ec8dbcb9d0a2d2b5366251a628d9ed89dbbac2bbe217e318cc8aeaf3ad8d43e04f4c6ed846964fc9f3b6b474000000000000000000000000000000000000000000000000000000000000001c83a8ea2b25d3bd2458b656c79020e131aef896777b46f97683f3593f0bb15c1a92b867bfb8c0a1a07e8e9888229dd8a2d12341b361212a5705cda826377f8038387b0512a09da1382a18290f499d518d3e9748456c368b8e24255fe6138e68d7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000028700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb05813b000000000000000000000000000000000000000000000000002386f2cb05db8200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000017000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086ebd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6d4e6d5a4755345a69316a4e4759354c54557a4f5751744f474a6d5a43316c4e6a51334f4759334d7a63784f47496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000ca87def88161442f874acb8acb7e5d5e0fc59160000000000000000000000000000000000000000000000000000000000005a30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x55b5fcbd7c9972c46063f3c6b0f887bd8bb469cd8b859be816a07937f45864aa",
      "signature": {
        "s": "0x28d9ed89dbbac2bbe217e318cc8aeaf3ad8d43e04f4c6ed846964fc9f3b6b474",
        "r": "0xea1dd345b6904626c837352ddd6b7d7398050d02ec8dbcb9d0a2d2b5366251a6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x83a8ea2b25d3bd2458b656c79020e131aef896777b46f97683f3593f0bb15c1a",
      "signature": {
        "s": "0x387b0512a09da1382a18290f499d518d3e9748456c368b8e24255fe6138e68d7",
        "r": "0x92b867bfb8c0a1a07e8e9888229dd8a2d12341b361212a5705cda826377f8038",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "23088",
    "total": "23088"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23088",
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
            "amount": "552637"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "23"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NmNmZGU4Zi1jNGY5LTUzOWQtOGJmZC1lNjQ3OGY3MzcxOGIifQ==",
    "nonce": 647,
    "balances": {
      "current": "10000001531216187",
      "previous": "10000001531239298"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0ca87def88161442f874acb8acb7e5d5e0fc5916",
    "nonce": 20,
    "balances": {
      "current": "23088",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:40.331Z",
  "updated": "2020-05-22T08:03:40.405Z",
  "id": "5ec7875ce5756b00111b8045"
}
```
* *stageAmount*: `23088`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000005a3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000005a300000000000000000000000000000000000000000000000000000000000005a3055b5fcbd7c9972c46063f3c6b0f887bd8bb469cd8b859be816a07937f45864aaea1dd345b6904626c837352ddd6b7d7398050d02ec8dbcb9d0a2d2b5366251a628d9ed89dbbac2bbe217e318cc8aeaf3ad8d43e04f4c6ed846964fc9f3b6b474000000000000000000000000000000000000000000000000000000000000001c83a8ea2b25d3bd2458b656c79020e131aef896777b46f97683f3593f0bb15c1a92b867bfb8c0a1a07e8e9888229dd8a2d12341b361212a5705cda826377f8038387b0512a09da1382a18290f499d518d3e9748456c368b8e24255fe6138e68d7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000028700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb05813b000000000000000000000000000000000000000000000000002386f2cb05db8200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000017000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086ebd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6d4e6d5a4755345a69316a4e4759354c54557a4f5751744f474a6d5a43316c4e6a51334f4759334d7a63784f47496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000ca87def88161442f874acb8acb7e5d5e0fc59160000000000000000000000000000000000000000000000000000000000005a30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x55b5fcbd7c9972c46063f3c6b0f887bd8bb469cd8b859be816a07937f45864aa",
      "signature": {
        "s": "0x28d9ed89dbbac2bbe217e318cc8aeaf3ad8d43e04f4c6ed846964fc9f3b6b474",
        "r": "0xea1dd345b6904626c837352ddd6b7d7398050d02ec8dbcb9d0a2d2b5366251a6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x83a8ea2b25d3bd2458b656c79020e131aef896777b46f97683f3593f0bb15c1a",
      "signature": {
        "s": "0x387b0512a09da1382a18290f499d518d3e9748456c368b8e24255fe6138e68d7",
        "r": "0x92b867bfb8c0a1a07e8e9888229dd8a2d12341b361212a5705cda826377f8038",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "23088",
    "total": "23088"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23088",
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
            "amount": "552637"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "23"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NmNmZGU4Zi1jNGY5LTUzOWQtOGJmZC1lNjQ3OGY3MzcxOGIifQ==",
    "nonce": 647,
    "balances": {
      "current": "10000001531216187",
      "previous": "10000001531239298"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0ca87def88161442f874acb8acb7e5d5e0fc5916",
    "nonce": 20,
    "balances": {
      "current": "23088",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:40.331Z",
  "updated": "2020-05-22T08:03:40.405Z",
  "id": "5ec7875ce5756b00111b8045"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000005a300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `23088`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``