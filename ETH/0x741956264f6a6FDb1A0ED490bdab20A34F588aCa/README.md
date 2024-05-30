# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x741956264f6a6FDb1A0ED490bdab20A34F588aCa`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000fbf0000000000000000000000000000000000000000000000000000000000000fbf00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000fbf0000000000000000000000000000000000000000000000000000000000000fbf1214e49077479d5cf2eb9b07f878abe460e650a62f5c6b3593ec42d8837c97618e2aad4665e3fef65b816e7383d663b41e433da8b057c5cc875fea6a82c1e651728875065a86eb6bd987d514572086137bf628f50e4d91e5a570e56942b3ac4c000000000000000000000000000000000000000000000000000000000000001bcea9086d64f23018e74c00f0a9ed6872f375fadc073dcd6e2e1c758a04c213084bf40e9645a713d09cf97c85c64090b7b13a005effb2a620891738a8776dc0eb0ed79617158b5aad3400d89cb5f9c0c772b07715390ec60b83cff10142281bf3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007c600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3bad6dd000000000000000000000000000000000000000000000000002386f2c3bae6a000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4a8300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e544e6c4e574e6c4e6930794d6a557a4c5455325a4451744f44417a597931694d7a49324d7a4d32596a4d324e6a556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000741956264f6a6fdb1a0ed490bdab20a34f588aca0000000000000000000000000000000000000000000000000000000000000fbf000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1214e49077479d5cf2eb9b07f878abe460e650a62f5c6b3593ec42d8837c9761",
      "signature": {
        "s": "0x728875065a86eb6bd987d514572086137bf628f50e4d91e5a570e56942b3ac4c",
        "r": "0x8e2aad4665e3fef65b816e7383d663b41e433da8b057c5cc875fea6a82c1e651",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcea9086d64f23018e74c00f0a9ed6872f375fadc073dcd6e2e1c758a04c21308",
      "signature": {
        "s": "0x0ed79617158b5aad3400d89cb5f9c0c772b07715390ec60b83cff10142281bf3",
        "r": "0x4bf40e9645a713d09cf97c85c64090b7b13a005effb2a620891738a8776dc0eb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4031",
    "total": "4031"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4031",
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
            "amount": "674435"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNTNlNWNlNi0yMjUzLTU2ZDQtODAzYy1iMzI2MzM2YjM2NjUifQ==",
    "nonce": 1990,
    "balances": {
      "current": "10000001408882397",
      "previous": "10000001408886432"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x741956264f6a6fdb1a0ed490bdab20a34f588aca",
    "nonce": 20,
    "balances": {
      "current": "4031",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:35.175Z",
  "updated": "2020-05-22T08:13:35.241Z",
  "id": "5ec789afe5756b00111b81f2"
}
```
* *stageAmount*: `4031`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000fbf00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000fbf0000000000000000000000000000000000000000000000000000000000000fbf1214e49077479d5cf2eb9b07f878abe460e650a62f5c6b3593ec42d8837c97618e2aad4665e3fef65b816e7383d663b41e433da8b057c5cc875fea6a82c1e651728875065a86eb6bd987d514572086137bf628f50e4d91e5a570e56942b3ac4c000000000000000000000000000000000000000000000000000000000000001bcea9086d64f23018e74c00f0a9ed6872f375fadc073dcd6e2e1c758a04c213084bf40e9645a713d09cf97c85c64090b7b13a005effb2a620891738a8776dc0eb0ed79617158b5aad3400d89cb5f9c0c772b07715390ec60b83cff10142281bf3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007c600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3bad6dd000000000000000000000000000000000000000000000000002386f2c3bae6a000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4a8300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e544e6c4e574e6c4e6930794d6a557a4c5455325a4451744f44417a597931694d7a49324d7a4d32596a4d324e6a556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000741956264f6a6fdb1a0ed490bdab20a34f588aca0000000000000000000000000000000000000000000000000000000000000fbf000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1214e49077479d5cf2eb9b07f878abe460e650a62f5c6b3593ec42d8837c9761",
      "signature": {
        "s": "0x728875065a86eb6bd987d514572086137bf628f50e4d91e5a570e56942b3ac4c",
        "r": "0x8e2aad4665e3fef65b816e7383d663b41e433da8b057c5cc875fea6a82c1e651",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcea9086d64f23018e74c00f0a9ed6872f375fadc073dcd6e2e1c758a04c21308",
      "signature": {
        "s": "0x0ed79617158b5aad3400d89cb5f9c0c772b07715390ec60b83cff10142281bf3",
        "r": "0x4bf40e9645a713d09cf97c85c64090b7b13a005effb2a620891738a8776dc0eb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4031",
    "total": "4031"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4031",
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
            "amount": "674435"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNTNlNWNlNi0yMjUzLTU2ZDQtODAzYy1iMzI2MzM2YjM2NjUifQ==",
    "nonce": 1990,
    "balances": {
      "current": "10000001408882397",
      "previous": "10000001408886432"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x741956264f6a6fdb1a0ed490bdab20a34f588aca",
    "nonce": 20,
    "balances": {
      "current": "4031",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:35.175Z",
  "updated": "2020-05-22T08:13:35.241Z",
  "id": "5ec789afe5756b00111b81f2"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000fbf0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4031`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``