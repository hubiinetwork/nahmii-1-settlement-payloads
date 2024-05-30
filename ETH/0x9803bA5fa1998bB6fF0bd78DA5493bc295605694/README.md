# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9803bA5fa1998bB6fF0bd78DA5493bc295605694`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000010c71f45aff710a798bce3898a533fc2f68ce748b34bfc6019d143a3c19166ee1d7257bedc6000c1f78b8682da30efec1a8ab0cf2b9f321cad62cc2467cfac2c310dc22df0d44a364eb2346f49222a9aa3d2a3b756db665fc5bf9d4eede43fcbab000000000000000000000000000000000000000000000000000000000000001c164cfb001f52f082ea2ce8fbef20e074958a4cedc8c57f918f7026fc7b4ef2e8873429af693cf6ba8d9ba99f000507f20e2ae43a8777c6201bf0710c6f7f2d75144418ebf85033e2a858bb422ff623b42f6336341ac665c043eaaa9f2354f90d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000012b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ccfa82a5000000000000000000000000000000000000000000000000002386f2ccfa82b600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007eef700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f5441795a4446684f53316c4e546c684c54566a4e574d744f4451334e6930334e6a41304f445133597a67785a6d596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000009803ba5fa1998bb6ff0bd78da5493bc2956056940000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc71f45aff710a798bce3898a533fc2f68ce748b34bfc6019d143a3c19166ee1d",
      "signature": {
        "s": "0x0dc22df0d44a364eb2346f49222a9aa3d2a3b756db665fc5bf9d4eede43fcbab",
        "r": "0x7257bedc6000c1f78b8682da30efec1a8ab0cf2b9f321cad62cc2467cfac2c31",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x164cfb001f52f082ea2ce8fbef20e074958a4cedc8c57f918f7026fc7b4ef2e8",
      "signature": {
        "s": "0x144418ebf85033e2a858bb422ff623b42f6336341ac665c043eaaa9f2354f90d",
        "r": "0x873429af693cf6ba8d9ba99f000507f20e2ae43a8777c6201bf0710c6f7f2d75",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16",
    "total": "16"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16",
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
            "amount": "519927"
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
    "data": "eyJyZWYiOiJlOTAyZDFhOS1lNTlhLTVjNWMtODQ3Ni03NjA0ODQ3YzgxZmYifQ==",
    "nonce": 299,
    "balances": {
      "current": "10000001564050085",
      "previous": "10000001564050102"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9803ba5fa1998bb6ff0bd78da5493bc295605694",
    "nonce": 20,
    "balances": {
      "current": "16",
      "previous": "0"
    }
  },
  "blockNumber": "10114495",
  "created": "2020-05-22T08:00:57.079Z",
  "updated": "2020-05-22T08:00:57.149Z",
  "id": "5ec786b9b0c6090011d5a931"
}
```
* *stageAmount*: `16`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000010c71f45aff710a798bce3898a533fc2f68ce748b34bfc6019d143a3c19166ee1d7257bedc6000c1f78b8682da30efec1a8ab0cf2b9f321cad62cc2467cfac2c310dc22df0d44a364eb2346f49222a9aa3d2a3b756db665fc5bf9d4eede43fcbab000000000000000000000000000000000000000000000000000000000000001c164cfb001f52f082ea2ce8fbef20e074958a4cedc8c57f918f7026fc7b4ef2e8873429af693cf6ba8d9ba99f000507f20e2ae43a8777c6201bf0710c6f7f2d75144418ebf85033e2a858bb422ff623b42f6336341ac665c043eaaa9f2354f90d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000012b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ccfa82a5000000000000000000000000000000000000000000000000002386f2ccfa82b600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007eef700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f5441795a4446684f53316c4e546c684c54566a4e574d744f4451334e6930334e6a41304f445133597a67785a6d596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000009803ba5fa1998bb6ff0bd78da5493bc2956056940000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc71f45aff710a798bce3898a533fc2f68ce748b34bfc6019d143a3c19166ee1d",
      "signature": {
        "s": "0x0dc22df0d44a364eb2346f49222a9aa3d2a3b756db665fc5bf9d4eede43fcbab",
        "r": "0x7257bedc6000c1f78b8682da30efec1a8ab0cf2b9f321cad62cc2467cfac2c31",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x164cfb001f52f082ea2ce8fbef20e074958a4cedc8c57f918f7026fc7b4ef2e8",
      "signature": {
        "s": "0x144418ebf85033e2a858bb422ff623b42f6336341ac665c043eaaa9f2354f90d",
        "r": "0x873429af693cf6ba8d9ba99f000507f20e2ae43a8777c6201bf0710c6f7f2d75",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16",
    "total": "16"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16",
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
            "amount": "519927"
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
    "data": "eyJyZWYiOiJlOTAyZDFhOS1lNTlhLTVjNWMtODQ3Ni03NjA0ODQ3YzgxZmYifQ==",
    "nonce": 299,
    "balances": {
      "current": "10000001564050085",
      "previous": "10000001564050102"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9803ba5fa1998bb6ff0bd78da5493bc295605694",
    "nonce": 20,
    "balances": {
      "current": "16",
      "previous": "0"
    }
  },
  "blockNumber": "10114495",
  "created": "2020-05-22T08:00:57.079Z",
  "updated": "2020-05-22T08:00:57.149Z",
  "id": "5ec786b9b0c6090011d5a931"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `16`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``