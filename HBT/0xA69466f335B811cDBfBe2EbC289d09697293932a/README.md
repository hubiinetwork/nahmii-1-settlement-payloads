# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA69466f335B811cDBfBe2EbC289d09697293932a`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000141d6e3500000000000000000000000000000000000000000000000000000000141d6e35000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000141d6e3500000000000000000000000000000000000000000000000000000000141d6e350124f728c661e68c7be7a9ccd1993e5836e88ede6debefc7a1b8a18c6b9bd7d7f9c1e1125ff4da20af8aff8e1ec46e975a43f8f14bcc8de3ffd0bc9a66cd8bcd071323f27facc8b80bb1b039720cce98bac5aba48cf82f2d857045357e567754000000000000000000000000000000000000000000000000000000000000001bc57d78761034de4744aded2085d9f4fe07484956bd2f94614254886cf3c52fa5000c4f8e52f6b9b992b1c88b3d056ebe7b6532e7dfd3a5f74ac6209d63922050100a37143851814099f9858285db0ba81ef3a90767e85c3ad088ac9aabf4693f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018b200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a0e0e8eedc9000000000000000000000000000000000000000000000000002e1a0e22b1823f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000052641000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099698e338000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5954466b4e6a5a694d5330354d6d597a4c54566d4e3249744f44566a4d6930304d4467334e6a677a597a55324f47496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a69466f335b811cdbfbe2ebc289d09697293932a00000000000000000000000000000000000000000000000000000000141d6e35000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0124f728c661e68c7be7a9ccd1993e5836e88ede6debefc7a1b8a18c6b9bd7d7",
      "signature": {
        "s": "0x071323f27facc8b80bb1b039720cce98bac5aba48cf82f2d857045357e567754",
        "r": "0xf9c1e1125ff4da20af8aff8e1ec46e975a43f8f14bcc8de3ffd0bc9a66cd8bcd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc57d78761034de4744aded2085d9f4fe07484956bd2f94614254886cf3c52fa5",
      "signature": {
        "s": "0x100a37143851814099f9858285db0ba81ef3a90767e85c3ad088ac9aabf4693f",
        "r": "0x000c4f8e52f6b9b992b1c88b3d056ebe7b6532e7dfd3a5f74ac6209d63922050",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "337473077",
    "total": "337473077"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "337473077",
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
            "amount": "41181307704"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "337473"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzYTFkNjZiMS05MmYzLTVmN2ItODVjMi00MDg3NjgzYzU2OGIifQ==",
    "nonce": 6322,
    "balances": {
      "current": "12976496604802505",
      "previous": "12976496942613055"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa69466f335b811cdbfbe2ebc289d09697293932a",
    "nonce": 22,
    "balances": {
      "current": "337473077",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:12.295Z",
  "updated": "2020-05-22T08:48:12.370Z",
  "id": "5ec791cce5756b00111b878b"
}
```
* *stageAmount*: `337473077`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000141d6e35000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000141d6e3500000000000000000000000000000000000000000000000000000000141d6e350124f728c661e68c7be7a9ccd1993e5836e88ede6debefc7a1b8a18c6b9bd7d7f9c1e1125ff4da20af8aff8e1ec46e975a43f8f14bcc8de3ffd0bc9a66cd8bcd071323f27facc8b80bb1b039720cce98bac5aba48cf82f2d857045357e567754000000000000000000000000000000000000000000000000000000000000001bc57d78761034de4744aded2085d9f4fe07484956bd2f94614254886cf3c52fa5000c4f8e52f6b9b992b1c88b3d056ebe7b6532e7dfd3a5f74ac6209d63922050100a37143851814099f9858285db0ba81ef3a90767e85c3ad088ac9aabf4693f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018b200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a0e0e8eedc9000000000000000000000000000000000000000000000000002e1a0e22b1823f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000052641000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099698e338000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5954466b4e6a5a694d5330354d6d597a4c54566d4e3249744f44566a4d6930304d4467334e6a677a597a55324f47496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a69466f335b811cdbfbe2ebc289d09697293932a00000000000000000000000000000000000000000000000000000000141d6e35000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0124f728c661e68c7be7a9ccd1993e5836e88ede6debefc7a1b8a18c6b9bd7d7",
      "signature": {
        "s": "0x071323f27facc8b80bb1b039720cce98bac5aba48cf82f2d857045357e567754",
        "r": "0xf9c1e1125ff4da20af8aff8e1ec46e975a43f8f14bcc8de3ffd0bc9a66cd8bcd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc57d78761034de4744aded2085d9f4fe07484956bd2f94614254886cf3c52fa5",
      "signature": {
        "s": "0x100a37143851814099f9858285db0ba81ef3a90767e85c3ad088ac9aabf4693f",
        "r": "0x000c4f8e52f6b9b992b1c88b3d056ebe7b6532e7dfd3a5f74ac6209d63922050",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "337473077",
    "total": "337473077"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "337473077",
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
            "amount": "41181307704"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "337473"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzYTFkNjZiMS05MmYzLTVmN2ItODVjMi00MDg3NjgzYzU2OGIifQ==",
    "nonce": 6322,
    "balances": {
      "current": "12976496604802505",
      "previous": "12976496942613055"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa69466f335b811cdbfbe2ebc289d09697293932a",
    "nonce": 22,
    "balances": {
      "current": "337473077",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:12.295Z",
  "updated": "2020-05-22T08:48:12.370Z",
  "id": "5ec791cce5756b00111b878b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000141d6e35000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `337473077`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`