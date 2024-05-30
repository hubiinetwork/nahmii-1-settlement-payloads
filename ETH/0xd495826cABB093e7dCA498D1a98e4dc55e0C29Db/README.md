# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd495826cABB093e7dCA498D1a98e4dc55e0C29Db`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000675e800000000000000000000000000000000000000000000000000000000000675e8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000675e800000000000000000000000000000000000000000000000000000000000675e87548c2e9bb2a0bef07dd16731c66e81bda02ae6ca8820d774945be81cfbf7bbe0ecc11cbfe65f3dcdca1f8f72afd1dd1f02923e76c3e24e384617c2a24182f51094fb6c4214b81d5f3dd3bb87b9b12fe038a1255cca6de778c81d3a73191b90a000000000000000000000000000000000000000000000000000000000000001cc98db084f3aa3bbb535eb30c6f657fa264ac39c0d69888e1d2ec9f259a91b14986a7a3714250649e3cbdaa473437155b2d20c5ca00d0ec316bba4416fa7c6cf940e4f1227c0fc1e0ae5cdf44aaa7ff22b4616070506b6ec78a06060e0046b555000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000007a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d3369c1c000000000000000000000000000000000000000000000000002386f2d33d13ab00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000001a70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000656fc00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6a63344e5459335a69316d4d444a6c4c54566c4e574974596a51314d79307a596d597a596a55305a44526d5957516966513d3d000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000d495826cabb093e7dca498d1a98e4dc55e0c29db00000000000000000000000000000000000000000000000000000000000675e8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7548c2e9bb2a0bef07dd16731c66e81bda02ae6ca8820d774945be81cfbf7bbe",
      "signature": {
        "s": "0x094fb6c4214b81d5f3dd3bb87b9b12fe038a1255cca6de778c81d3a73191b90a",
        "r": "0x0ecc11cbfe65f3dcdca1f8f72afd1dd1f02923e76c3e24e384617c2a24182f51",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc98db084f3aa3bbb535eb30c6f657fa264ac39c0d69888e1d2ec9f259a91b149",
      "signature": {
        "s": "0x40e4f1227c0fc1e0ae5cdf44aaa7ff22b4616070506b6ec78a06060e0046b555",
        "r": "0x86a7a3714250649e3cbdaa473437155b2d20c5ca00d0ec316bba4416fa7c6cf9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "423400",
    "total": "423400"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "423400",
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
            "amount": "415484"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "423"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5Zjc4NTY3Zi1mMDJlLTVlNWItYjQ1My0zYmYzYjU0ZDRmYWQifQ==",
    "nonce": 122,
    "balances": {
      "current": "10000001668652060",
      "previous": "10000001669075883"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd495826cabb093e7dca498d1a98e4dc55e0c29db",
    "nonce": 27,
    "balances": {
      "current": "423400",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:43.436Z",
  "updated": "2020-05-22T07:59:43.501Z",
  "id": "5ec7866f005df800101bc237"
}
```
* *stageAmount*: `423400`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000675e8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000675e800000000000000000000000000000000000000000000000000000000000675e87548c2e9bb2a0bef07dd16731c66e81bda02ae6ca8820d774945be81cfbf7bbe0ecc11cbfe65f3dcdca1f8f72afd1dd1f02923e76c3e24e384617c2a24182f51094fb6c4214b81d5f3dd3bb87b9b12fe038a1255cca6de778c81d3a73191b90a000000000000000000000000000000000000000000000000000000000000001cc98db084f3aa3bbb535eb30c6f657fa264ac39c0d69888e1d2ec9f259a91b14986a7a3714250649e3cbdaa473437155b2d20c5ca00d0ec316bba4416fa7c6cf940e4f1227c0fc1e0ae5cdf44aaa7ff22b4616070506b6ec78a06060e0046b555000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000007a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d3369c1c000000000000000000000000000000000000000000000000002386f2d33d13ab00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000001a70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000656fc00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6a63344e5459335a69316d4d444a6c4c54566c4e574974596a51314d79307a596d597a596a55305a44526d5957516966513d3d000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000d495826cabb093e7dca498d1a98e4dc55e0c29db00000000000000000000000000000000000000000000000000000000000675e8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7548c2e9bb2a0bef07dd16731c66e81bda02ae6ca8820d774945be81cfbf7bbe",
      "signature": {
        "s": "0x094fb6c4214b81d5f3dd3bb87b9b12fe038a1255cca6de778c81d3a73191b90a",
        "r": "0x0ecc11cbfe65f3dcdca1f8f72afd1dd1f02923e76c3e24e384617c2a24182f51",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc98db084f3aa3bbb535eb30c6f657fa264ac39c0d69888e1d2ec9f259a91b149",
      "signature": {
        "s": "0x40e4f1227c0fc1e0ae5cdf44aaa7ff22b4616070506b6ec78a06060e0046b555",
        "r": "0x86a7a3714250649e3cbdaa473437155b2d20c5ca00d0ec316bba4416fa7c6cf9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "423400",
    "total": "423400"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "423400",
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
            "amount": "415484"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "423"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5Zjc4NTY3Zi1mMDJlLTVlNWItYjQ1My0zYmYzYjU0ZDRmYWQifQ==",
    "nonce": 122,
    "balances": {
      "current": "10000001668652060",
      "previous": "10000001669075883"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd495826cabb093e7dca498d1a98e4dc55e0c29db",
    "nonce": 27,
    "balances": {
      "current": "423400",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:43.436Z",
  "updated": "2020-05-22T07:59:43.501Z",
  "id": "5ec7866f005df800101bc237"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000675e80000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `423400`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``