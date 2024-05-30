# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x60f34088BaEccab9a350fb3d7780acB213Fe2B76`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000020baba030000000000000000000000000000000000000000000000000000000020baba03000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000020baba030000000000000000000000000000000000000000000000000000000020baba03c1dc7a183da9d1d8b7df8fc6dc688a8c802b62e185d0ba72bb5f2ebc09509ffe5f6560fc1ca72b903cddc38616a4423c16f2655e66d9b563ef240903f5c5577500203fd66ce5277ae77c0dc1168ab77b2aa8b65f47338ee558190d901514e685000000000000000000000000000000000000000000000000000000000000001ca8750e102c082fe8346740aa3e91d88a9463e501a93d2a6ed7b31c3dcec4d454f565fb23b7a30a371f68396d5d47a528c5152d20c083207b81ca26f8f4e4af26035fd2742b12566b424fa08809a2713d8ec5acdd893db237b9491f8b86a72bc1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d6c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b664a0e2e8a000000000000000000000000000000000000000000000000002e0b666ad1498100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000860f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d56171707000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d47597a4e6d4d334e43316c596d566c4c54566b4d6a5574596a56684d69316d4e474e6b4d6d566a596a45784d44676966513d3d000000000000000000000000000000000000000000000000000000000000001000000000000000000000000060f34088baeccab9a350fb3d7780acb213fe2b760000000000000000000000000000000000000000000000000000000020baba03000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc1dc7a183da9d1d8b7df8fc6dc688a8c802b62e185d0ba72bb5f2ebc09509ffe",
      "signature": {
        "s": "0x00203fd66ce5277ae77c0dc1168ab77b2aa8b65f47338ee558190d901514e685",
        "r": "0x5f6560fc1ca72b903cddc38616a4423c16f2655e66d9b563ef240903f5c55775",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa8750e102c082fe8346740aa3e91d88a9463e501a93d2a6ed7b31c3dcec4d454",
      "signature": {
        "s": "0x035fd2742b12566b424fa08809a2713d8ec5acdd893db237b9491f8b86a72bc1",
        "r": "0xf565fb23b7a30a371f68396d5d47a528c5152d20c083207b81ca26f8f4e4af26",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "549108227",
    "total": "549108227"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "549108227",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "57278928647"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "549108"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMGYzNmM3NC1lYmVlLTVkMjUtYjVhMi1mNGNkMmVjYjExMDgifQ==",
    "nonce": 7532,
    "balances": {
      "current": "12960382885703306",
      "previous": "12960383435360641"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x60f34088baeccab9a350fb3d7780acb213fe2b76",
    "nonce": 16,
    "balances": {
      "current": "549108227",
      "previous": "0"
    }
  },
  "blockNumber": "10114742",
  "created": "2020-05-22T08:57:27.850Z",
  "updated": "2020-05-22T08:57:27.914Z",
  "id": "5ec793f7005df800101bcc17"
}
```
* *stageAmount*: `549108227`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000020baba03000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000020baba030000000000000000000000000000000000000000000000000000000020baba03c1dc7a183da9d1d8b7df8fc6dc688a8c802b62e185d0ba72bb5f2ebc09509ffe5f6560fc1ca72b903cddc38616a4423c16f2655e66d9b563ef240903f5c5577500203fd66ce5277ae77c0dc1168ab77b2aa8b65f47338ee558190d901514e685000000000000000000000000000000000000000000000000000000000000001ca8750e102c082fe8346740aa3e91d88a9463e501a93d2a6ed7b31c3dcec4d454f565fb23b7a30a371f68396d5d47a528c5152d20c083207b81ca26f8f4e4af26035fd2742b12566b424fa08809a2713d8ec5acdd893db237b9491f8b86a72bc1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d6c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b664a0e2e8a000000000000000000000000000000000000000000000000002e0b666ad1498100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000860f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d56171707000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d47597a4e6d4d334e43316c596d566c4c54566b4d6a5574596a56684d69316d4e474e6b4d6d566a596a45784d44676966513d3d000000000000000000000000000000000000000000000000000000000000001000000000000000000000000060f34088baeccab9a350fb3d7780acb213fe2b760000000000000000000000000000000000000000000000000000000020baba03000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc1dc7a183da9d1d8b7df8fc6dc688a8c802b62e185d0ba72bb5f2ebc09509ffe",
      "signature": {
        "s": "0x00203fd66ce5277ae77c0dc1168ab77b2aa8b65f47338ee558190d901514e685",
        "r": "0x5f6560fc1ca72b903cddc38616a4423c16f2655e66d9b563ef240903f5c55775",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa8750e102c082fe8346740aa3e91d88a9463e501a93d2a6ed7b31c3dcec4d454",
      "signature": {
        "s": "0x035fd2742b12566b424fa08809a2713d8ec5acdd893db237b9491f8b86a72bc1",
        "r": "0xf565fb23b7a30a371f68396d5d47a528c5152d20c083207b81ca26f8f4e4af26",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "549108227",
    "total": "549108227"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "549108227",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "57278928647"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "549108"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMGYzNmM3NC1lYmVlLTVkMjUtYjVhMi1mNGNkMmVjYjExMDgifQ==",
    "nonce": 7532,
    "balances": {
      "current": "12960382885703306",
      "previous": "12960383435360641"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x60f34088baeccab9a350fb3d7780acb213fe2b76",
    "nonce": 16,
    "balances": {
      "current": "549108227",
      "previous": "0"
    }
  },
  "blockNumber": "10114742",
  "created": "2020-05-22T08:57:27.850Z",
  "updated": "2020-05-22T08:57:27.914Z",
  "id": "5ec793f7005df800101bcc17"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000020baba03000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `549108227`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`