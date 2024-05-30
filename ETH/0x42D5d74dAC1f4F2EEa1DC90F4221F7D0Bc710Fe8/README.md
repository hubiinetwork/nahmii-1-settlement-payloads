# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x42D5d74dAC1f4F2EEa1DC90F4221F7D0Bc710Fe8`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001bea0000000000000000000000000000000000000000000000000000000000001bea00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001bea0000000000000000000000000000000000000000000000000000000000001bea3dbf65180e969e93481a9c7d57dc00e826a82082c4abe517ef704fb6e0ee9d78ef0d52c9238d946f8974c68b18f4b45fe331ea011f3ecbba31f58e8e2651db921f8d1be0416c7ccb58fd2c4c7ec082e230316b4dd2a59021af292be3ad6fed2e000000000000000000000000000000000000000000000000000000000000001c0cca2a0f7412fa1dea82ca1e2b3b384c846be686be2eae75aedbf7eb1bfb49f86286bd3c60e4ffa01279d3ed80caf29cda7aa18b4a98d611af3f540b21d331c1162397344b9c2faf9e9ca49fdf63d3c477dd1b39041473b6138374e9e2fba6a3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000064300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c60faacb000000000000000000000000000000000000000000000000002386f2c60fc6bc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009b27200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a6a5930595759775953316b5a475a694c54566d4e324d744f5749334e793077595745774e7a41304e5451794e7a636966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000042d5d74dac1f4f2eea1dc90f4221f7d0bc710fe80000000000000000000000000000000000000000000000000000000000001bea000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3dbf65180e969e93481a9c7d57dc00e826a82082c4abe517ef704fb6e0ee9d78",
      "signature": {
        "s": "0x1f8d1be0416c7ccb58fd2c4c7ec082e230316b4dd2a59021af292be3ad6fed2e",
        "r": "0xef0d52c9238d946f8974c68b18f4b45fe331ea011f3ecbba31f58e8e2651db92",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0cca2a0f7412fa1dea82ca1e2b3b384c846be686be2eae75aedbf7eb1bfb49f8",
      "signature": {
        "s": "0x162397344b9c2faf9e9ca49fdf63d3c477dd1b39041473b6138374e9e2fba6a3",
        "r": "0x6286bd3c60e4ffa01279d3ed80caf29cda7aa18b4a98d611af3f540b21d331c1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7146",
    "total": "7146"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7146",
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
            "amount": "635506"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "7"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZjY0YWYwYS1kZGZiLTVmN2MtOWI3Ny0wYWEwNzA0NTQyNzcifQ==",
    "nonce": 1603,
    "balances": {
      "current": "10000001447996107",
      "previous": "10000001448003260"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x42d5d74dac1f4f2eea1dc90f4221f7d0bc710fe8",
    "nonce": 20,
    "balances": {
      "current": "7146",
      "previous": "0"
    }
  },
  "blockNumber": "10114535",
  "created": "2020-05-22T08:10:47.328Z",
  "updated": "2020-05-22T08:10:47.393Z",
  "id": "5ec78907b0c6090011d5aae5"
}
```
* *stageAmount*: `7146`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000001bea00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001bea0000000000000000000000000000000000000000000000000000000000001bea3dbf65180e969e93481a9c7d57dc00e826a82082c4abe517ef704fb6e0ee9d78ef0d52c9238d946f8974c68b18f4b45fe331ea011f3ecbba31f58e8e2651db921f8d1be0416c7ccb58fd2c4c7ec082e230316b4dd2a59021af292be3ad6fed2e000000000000000000000000000000000000000000000000000000000000001c0cca2a0f7412fa1dea82ca1e2b3b384c846be686be2eae75aedbf7eb1bfb49f86286bd3c60e4ffa01279d3ed80caf29cda7aa18b4a98d611af3f540b21d331c1162397344b9c2faf9e9ca49fdf63d3c477dd1b39041473b6138374e9e2fba6a3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000064300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c60faacb000000000000000000000000000000000000000000000000002386f2c60fc6bc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009b27200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a6a5930595759775953316b5a475a694c54566d4e324d744f5749334e793077595745774e7a41304e5451794e7a636966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000042d5d74dac1f4f2eea1dc90f4221f7d0bc710fe80000000000000000000000000000000000000000000000000000000000001bea000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3dbf65180e969e93481a9c7d57dc00e826a82082c4abe517ef704fb6e0ee9d78",
      "signature": {
        "s": "0x1f8d1be0416c7ccb58fd2c4c7ec082e230316b4dd2a59021af292be3ad6fed2e",
        "r": "0xef0d52c9238d946f8974c68b18f4b45fe331ea011f3ecbba31f58e8e2651db92",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0cca2a0f7412fa1dea82ca1e2b3b384c846be686be2eae75aedbf7eb1bfb49f8",
      "signature": {
        "s": "0x162397344b9c2faf9e9ca49fdf63d3c477dd1b39041473b6138374e9e2fba6a3",
        "r": "0x6286bd3c60e4ffa01279d3ed80caf29cda7aa18b4a98d611af3f540b21d331c1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7146",
    "total": "7146"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7146",
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
            "amount": "635506"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "7"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZjY0YWYwYS1kZGZiLTVmN2MtOWI3Ny0wYWEwNzA0NTQyNzcifQ==",
    "nonce": 1603,
    "balances": {
      "current": "10000001447996107",
      "previous": "10000001448003260"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x42d5d74dac1f4f2eea1dc90f4221f7d0bc710fe8",
    "nonce": 20,
    "balances": {
      "current": "7146",
      "previous": "0"
    }
  },
  "blockNumber": "10114535",
  "created": "2020-05-22T08:10:47.328Z",
  "updated": "2020-05-22T08:10:47.393Z",
  "id": "5ec78907b0c6090011d5aae5"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000001bea0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7146`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``