# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xaEC507e27BA58070618eE68813573904c00E32F2`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000b700000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000b700000000000000000000000000000000000000000000000000000000000000b760fc0cc005cf8aafd77bf9d42cdedf6887d3c2c05fa782f4af8821b2bc1c3f90c11c7622a90bb3d11276a3febda5e25fd110ee8fec0b41a930e61beadf798d1171f1c7aafefa2610b19af24b3beb35a0935b91a272db9bc3a280a59fa3600593000000000000000000000000000000000000000000000000000000000000001cd9b5ed6d7827e2d4d75e38042c980b6569e41b19ed38fe73b967e50e343b98219a9619bda3bc4a96224199fbcc5f96da24df873efbdcaa69e8820b882b37596b5a125bf6301d47d668b38527ba3240f5f18553c26bb9dca7c6da5ef0b07b254d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000040700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ca71a17d000000000000000000000000000000000000000000000000002386f2ca71a23500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008941d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d6a6c694e6a497a4e4330774d7a6b794c5455795a5749744f4441354d7930314d544a6c4f54497a4d7a51794f57556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000aec507e27ba58070618ee68813573904c00e32f200000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60fc0cc005cf8aafd77bf9d42cdedf6887d3c2c05fa782f4af8821b2bc1c3f90",
      "signature": {
        "s": "0x71f1c7aafefa2610b19af24b3beb35a0935b91a272db9bc3a280a59fa3600593",
        "r": "0xc11c7622a90bb3d11276a3febda5e25fd110ee8fec0b41a930e61beadf798d11",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd9b5ed6d7827e2d4d75e38042c980b6569e41b19ed38fe73b967e50e343b9821",
      "signature": {
        "s": "0x5a125bf6301d47d668b38527ba3240f5f18553c26bb9dca7c6da5ef0b07b254d",
        "r": "0x9a9619bda3bc4a96224199fbcc5f96da24df873efbdcaa69e8820b882b37596b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "183",
    "total": "183"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "183",
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
            "amount": "562205"
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
    "data": "eyJyZWYiOiI1MjliNjIzNC0wMzkyLTUyZWItODA5My01MTJlOTIzMzQyOWUifQ==",
    "nonce": 1031,
    "balances": {
      "current": "10000001521525117",
      "previous": "10000001521525301"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaec507e27ba58070618ee68813573904c00e32f2",
    "nonce": 20,
    "balances": {
      "current": "183",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:06:23.200Z",
  "updated": "2020-05-22T08:06:23.263Z",
  "id": "5ec787ff005df800101bc370"
}
```
* *stageAmount*: `183`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000b700000000000000000000000000000000000000000000000000000000000000b760fc0cc005cf8aafd77bf9d42cdedf6887d3c2c05fa782f4af8821b2bc1c3f90c11c7622a90bb3d11276a3febda5e25fd110ee8fec0b41a930e61beadf798d1171f1c7aafefa2610b19af24b3beb35a0935b91a272db9bc3a280a59fa3600593000000000000000000000000000000000000000000000000000000000000001cd9b5ed6d7827e2d4d75e38042c980b6569e41b19ed38fe73b967e50e343b98219a9619bda3bc4a96224199fbcc5f96da24df873efbdcaa69e8820b882b37596b5a125bf6301d47d668b38527ba3240f5f18553c26bb9dca7c6da5ef0b07b254d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000040700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ca71a17d000000000000000000000000000000000000000000000000002386f2ca71a23500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008941d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d6a6c694e6a497a4e4330774d7a6b794c5455795a5749744f4441354d7930314d544a6c4f54497a4d7a51794f57556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000aec507e27ba58070618ee68813573904c00e32f200000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60fc0cc005cf8aafd77bf9d42cdedf6887d3c2c05fa782f4af8821b2bc1c3f90",
      "signature": {
        "s": "0x71f1c7aafefa2610b19af24b3beb35a0935b91a272db9bc3a280a59fa3600593",
        "r": "0xc11c7622a90bb3d11276a3febda5e25fd110ee8fec0b41a930e61beadf798d11",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd9b5ed6d7827e2d4d75e38042c980b6569e41b19ed38fe73b967e50e343b9821",
      "signature": {
        "s": "0x5a125bf6301d47d668b38527ba3240f5f18553c26bb9dca7c6da5ef0b07b254d",
        "r": "0x9a9619bda3bc4a96224199fbcc5f96da24df873efbdcaa69e8820b882b37596b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "183",
    "total": "183"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "183",
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
            "amount": "562205"
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
    "data": "eyJyZWYiOiI1MjliNjIzNC0wMzkyLTUyZWItODA5My01MTJlOTIzMzQyOWUifQ==",
    "nonce": 1031,
    "balances": {
      "current": "10000001521525117",
      "previous": "10000001521525301"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaec507e27ba58070618ee68813573904c00e32f2",
    "nonce": 20,
    "balances": {
      "current": "183",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:06:23.200Z",
  "updated": "2020-05-22T08:06:23.263Z",
  "id": "5ec787ff005df800101bc370"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000b70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `183`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``