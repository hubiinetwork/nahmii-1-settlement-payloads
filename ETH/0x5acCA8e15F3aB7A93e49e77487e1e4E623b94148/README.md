# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5acCA8e15F3aB7A93e49e77487e1e4E623b94148`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000289914d693f1c5faacb5be5f510c40197633ff12aa681d7efd2668c0026e1d6114bed142560afdaeaca57c6543ca959e1c2a6c61d1cc8ff00c1c9e296a7b6611a48f0769be91a86925fa21d2ee38c1fff59a56b9bef2aadb25c6082003619bb01000000000000000000000000000000000000000000000000000000000000001c550f214f1a70a32df5d8ab4a662fab6fd947eaf1040b6d74b2d28e88d41f3ed7156a647dbe1cafb9ecf55f1ede63f3bc0d3d8138c9d7cac23f27800c31f7c3ef15afec82b7131e9438ef27dbe35663a6f67458fe9a4b9843789c1e44e510b958000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000044600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c85e7a3c000000000000000000000000000000000000000000000000002386f2c85e7a3f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000091be700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f474e695a6d4d784e5330324e7a68694c5455354f4441744f544e6c5953316c4e7a5a684d3251774e6a49305954556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000005acca8e15f3ab7a93e49e77487e1e4e623b941480000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x89914d693f1c5faacb5be5f510c40197633ff12aa681d7efd2668c0026e1d611",
      "signature": {
        "s": "0x48f0769be91a86925fa21d2ee38c1fff59a56b9bef2aadb25c6082003619bb01",
        "r": "0x4bed142560afdaeaca57c6543ca959e1c2a6c61d1cc8ff00c1c9e296a7b6611a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x550f214f1a70a32df5d8ab4a662fab6fd947eaf1040b6d74b2d28e88d41f3ed7",
      "signature": {
        "s": "0x15afec82b7131e9438ef27dbe35663a6f67458fe9a4b9843789c1e44e510b958",
        "r": "0x156a647dbe1cafb9ecf55f1ede63f3bc0d3d8138c9d7cac23f27800c31f7c3ef",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2",
    "total": "2"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2",
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
            "amount": "596967"
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
    "data": "eyJyZWYiOiJhOGNiZmMxNS02NzhiLTU5ODAtOTNlYS1lNzZhM2QwNjI0YTUifQ==",
    "nonce": 1094,
    "balances": {
      "current": "10000001486715452",
      "previous": "10000001486715455"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5acca8e15f3ab7a93e49e77487e1e4e623b94148",
    "nonce": 20,
    "balances": {
      "current": "2",
      "previous": "0"
    }
  },
  "blockNumber": "10114518",
  "created": "2020-05-22T08:06:44.061Z",
  "updated": "2020-05-22T08:06:44.128Z",
  "id": "5ec78814005df800101bc38c"
}
```
* *stageAmount*: `2`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000289914d693f1c5faacb5be5f510c40197633ff12aa681d7efd2668c0026e1d6114bed142560afdaeaca57c6543ca959e1c2a6c61d1cc8ff00c1c9e296a7b6611a48f0769be91a86925fa21d2ee38c1fff59a56b9bef2aadb25c6082003619bb01000000000000000000000000000000000000000000000000000000000000001c550f214f1a70a32df5d8ab4a662fab6fd947eaf1040b6d74b2d28e88d41f3ed7156a647dbe1cafb9ecf55f1ede63f3bc0d3d8138c9d7cac23f27800c31f7c3ef15afec82b7131e9438ef27dbe35663a6f67458fe9a4b9843789c1e44e510b958000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000044600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c85e7a3c000000000000000000000000000000000000000000000000002386f2c85e7a3f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000091be700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f474e695a6d4d784e5330324e7a68694c5455354f4441744f544e6c5953316c4e7a5a684d3251774e6a49305954556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000005acca8e15f3ab7a93e49e77487e1e4e623b941480000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x89914d693f1c5faacb5be5f510c40197633ff12aa681d7efd2668c0026e1d611",
      "signature": {
        "s": "0x48f0769be91a86925fa21d2ee38c1fff59a56b9bef2aadb25c6082003619bb01",
        "r": "0x4bed142560afdaeaca57c6543ca959e1c2a6c61d1cc8ff00c1c9e296a7b6611a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x550f214f1a70a32df5d8ab4a662fab6fd947eaf1040b6d74b2d28e88d41f3ed7",
      "signature": {
        "s": "0x15afec82b7131e9438ef27dbe35663a6f67458fe9a4b9843789c1e44e510b958",
        "r": "0x156a647dbe1cafb9ecf55f1ede63f3bc0d3d8138c9d7cac23f27800c31f7c3ef",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2",
    "total": "2"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2",
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
            "amount": "596967"
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
    "data": "eyJyZWYiOiJhOGNiZmMxNS02NzhiLTU5ODAtOTNlYS1lNzZhM2QwNjI0YTUifQ==",
    "nonce": 1094,
    "balances": {
      "current": "10000001486715452",
      "previous": "10000001486715455"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5acca8e15f3ab7a93e49e77487e1e4e623b94148",
    "nonce": 20,
    "balances": {
      "current": "2",
      "previous": "0"
    }
  },
  "blockNumber": "10114518",
  "created": "2020-05-22T08:06:44.061Z",
  "updated": "2020-05-22T08:06:44.128Z",
  "id": "5ec78814005df800101bc38c"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``