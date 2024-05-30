# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0fD07E2ba953b69d039CF101a093a01089765E88`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000007830000000000000000000000000000000000000000000000000000000000000783000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000007830000000000000000000000000000000000000000000000000000000000000783f545c5626e36d7c7dd15cc001a349358b8426a72851f82acfa4c1aa5b4c43889b67dee67cb4a3e909081fa24329d7f2e9acf5783274359e8223de7ea0eb6ab6f5d8adb8a5e8271a8c843ea73b775d6fac4a89f961c0a4435978ad22337f51229000000000000000000000000000000000000000000000000000000000000001cb76f36ccd77ae51905e679a78b42ddae9eb42846ed95582de53d895f1cae06414f523c980d4573a2c7c12397370b8a84844e8b48394b28c2fbbeaf7f2d4fd65a4233f29907ffc010989e6fa594a93ba482d9a634793614d3440f9ddffaa5019f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004f700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7ba7381000000000000000000000000000000000000000000000000002386f2c7ba7b0500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000945af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68596d4d304d44686959693035597a426d4c5455794e574d745954566c4e5331684e6a4d354d5463314e6d5a6b4d7a516966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000fd07e2ba953b69d039cf101a093a01089765e880000000000000000000000000000000000000000000000000000000000000783000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf545c5626e36d7c7dd15cc001a349358b8426a72851f82acfa4c1aa5b4c43889",
      "signature": {
        "s": "0x5d8adb8a5e8271a8c843ea73b775d6fac4a89f961c0a4435978ad22337f51229",
        "r": "0xb67dee67cb4a3e909081fa24329d7f2e9acf5783274359e8223de7ea0eb6ab6f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb76f36ccd77ae51905e679a78b42ddae9eb42846ed95582de53d895f1cae0641",
      "signature": {
        "s": "0x4233f29907ffc010989e6fa594a93ba482d9a634793614d3440f9ddffaa5019f",
        "r": "0x4f523c980d4573a2c7c12397370b8a84844e8b48394b28c2fbbeaf7f2d4fd65a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1923",
    "total": "1923"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1923",
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
            "amount": "607663"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhYmM0MDhiYi05YzBmLTUyNWMtYTVlNS1hNjM5MTc1NmZkMzQifQ==",
    "nonce": 1271,
    "balances": {
      "current": "10000001475965825",
      "previous": "10000001475967749"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fd07e2ba953b69d039cf101a093a01089765e88",
    "nonce": 20,
    "balances": {
      "current": "1923",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:07.976Z",
  "updated": "2020-05-22T08:08:08.038Z",
  "id": "5ec78867005df800101bc3cc"
}
```
* *stageAmount*: `1923`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000783000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000007830000000000000000000000000000000000000000000000000000000000000783f545c5626e36d7c7dd15cc001a349358b8426a72851f82acfa4c1aa5b4c43889b67dee67cb4a3e909081fa24329d7f2e9acf5783274359e8223de7ea0eb6ab6f5d8adb8a5e8271a8c843ea73b775d6fac4a89f961c0a4435978ad22337f51229000000000000000000000000000000000000000000000000000000000000001cb76f36ccd77ae51905e679a78b42ddae9eb42846ed95582de53d895f1cae06414f523c980d4573a2c7c12397370b8a84844e8b48394b28c2fbbeaf7f2d4fd65a4233f29907ffc010989e6fa594a93ba482d9a634793614d3440f9ddffaa5019f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004f700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7ba7381000000000000000000000000000000000000000000000000002386f2c7ba7b0500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000945af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68596d4d304d44686959693035597a426d4c5455794e574d745954566c4e5331684e6a4d354d5463314e6d5a6b4d7a516966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000fd07e2ba953b69d039cf101a093a01089765e880000000000000000000000000000000000000000000000000000000000000783000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf545c5626e36d7c7dd15cc001a349358b8426a72851f82acfa4c1aa5b4c43889",
      "signature": {
        "s": "0x5d8adb8a5e8271a8c843ea73b775d6fac4a89f961c0a4435978ad22337f51229",
        "r": "0xb67dee67cb4a3e909081fa24329d7f2e9acf5783274359e8223de7ea0eb6ab6f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb76f36ccd77ae51905e679a78b42ddae9eb42846ed95582de53d895f1cae0641",
      "signature": {
        "s": "0x4233f29907ffc010989e6fa594a93ba482d9a634793614d3440f9ddffaa5019f",
        "r": "0x4f523c980d4573a2c7c12397370b8a84844e8b48394b28c2fbbeaf7f2d4fd65a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1923",
    "total": "1923"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1923",
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
            "amount": "607663"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhYmM0MDhiYi05YzBmLTUyNWMtYTVlNS1hNjM5MTc1NmZkMzQifQ==",
    "nonce": 1271,
    "balances": {
      "current": "10000001475965825",
      "previous": "10000001475967749"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fd07e2ba953b69d039cf101a093a01089765e88",
    "nonce": 20,
    "balances": {
      "current": "1923",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:07.976Z",
  "updated": "2020-05-22T08:08:08.038Z",
  "id": "5ec78867005df800101bc3cc"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000007830000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1923`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``