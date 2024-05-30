# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8F9F610D0BD4CDa3B6afD02701AD2E2C231059F8`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000018a29f422000000000000000000000000000000000000000000000000000000018a29f422000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018a29f422000000000000000000000000000000000000000000000000000000018a29f42278040bb8b853e0f81a67883d5b93a62d15749c04c7038f628e17ac7b92faf2d050c6ffa89b30803c02b9c9904ecb7063957de0603dcf2221647fb7637eb042631369c7aa2cda1b10fc74bab54e9a7fa058653dec7470562d4196f91739155c39000000000000000000000000000000000000000000000000000000000000001c8259db508391e6680cd032082ace011579965873a7ef817cc17842c3e2d678ca093a234dfe7491c6ee5e607650ecd733db0194e4801d14b3acc05e702b99f5bb1fc7f89d6310116f3da5760dfa30af75f55b64f3a837839c12615afabf2d59dc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bff00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13c04bf91ecd000000000000000000000000000000000000000000000000002e13c1d687fadb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064e7ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b334e9c34000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d574e6b597a63304e5330304f4455344c54566c4d6a4974595455324d693168593249324d6d4577596a59784d44456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000008f9f610d0bd4cda3b6afd02701ad2e2c231059f8000000000000000000000000000000000000000000000000000000018a29f422000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x78040bb8b853e0f81a67883d5b93a62d15749c04c7038f628e17ac7b92faf2d0",
      "signature": {
        "s": "0x1369c7aa2cda1b10fc74bab54e9a7fa058653dec7470562d4196f91739155c39",
        "r": "0x50c6ffa89b30803c02b9c9904ecb7063957de0603dcf2221647fb7637eb04263",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8259db508391e6680cd032082ace011579965873a7ef817cc17842c3e2d678ca",
      "signature": {
        "s": "0x1fc7f89d6310116f3da5760dfa30af75f55b64f3a837839c12615afabf2d59dc",
        "r": "0x093a234dfe7491c6ee5e607650ecd733db0194e4801d14b3acc05e702b99f5bb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6612972578",
    "total": "6612972578"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6612972578",
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
            "amount": "48105430068"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6612972"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMWNkYzc0NS00ODU4LTVlMjItYTU2Mi1hY2I2MmEwYjYxMDEifQ==",
    "nonce": 7167,
    "balances": {
      "current": "12969565557956301",
      "previous": "12969572177541851"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8f9f610d0bd4cda3b6afd02701ad2e2c231059f8",
    "nonce": 22,
    "balances": {
      "current": "6612972578",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:44.402Z",
  "updated": "2020-05-22T08:54:44.474Z",
  "id": "5ec79354b0c6090011d5b228"
}
```
* *stageAmount*: `6612972578`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000018a29f422000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018a29f422000000000000000000000000000000000000000000000000000000018a29f42278040bb8b853e0f81a67883d5b93a62d15749c04c7038f628e17ac7b92faf2d050c6ffa89b30803c02b9c9904ecb7063957de0603dcf2221647fb7637eb042631369c7aa2cda1b10fc74bab54e9a7fa058653dec7470562d4196f91739155c39000000000000000000000000000000000000000000000000000000000000001c8259db508391e6680cd032082ace011579965873a7ef817cc17842c3e2d678ca093a234dfe7491c6ee5e607650ecd733db0194e4801d14b3acc05e702b99f5bb1fc7f89d6310116f3da5760dfa30af75f55b64f3a837839c12615afabf2d59dc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bff00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13c04bf91ecd000000000000000000000000000000000000000000000000002e13c1d687fadb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064e7ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b334e9c34000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d574e6b597a63304e5330304f4455344c54566c4d6a4974595455324d693168593249324d6d4577596a59784d44456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000008f9f610d0bd4cda3b6afd02701ad2e2c231059f8000000000000000000000000000000000000000000000000000000018a29f422000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x78040bb8b853e0f81a67883d5b93a62d15749c04c7038f628e17ac7b92faf2d0",
      "signature": {
        "s": "0x1369c7aa2cda1b10fc74bab54e9a7fa058653dec7470562d4196f91739155c39",
        "r": "0x50c6ffa89b30803c02b9c9904ecb7063957de0603dcf2221647fb7637eb04263",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8259db508391e6680cd032082ace011579965873a7ef817cc17842c3e2d678ca",
      "signature": {
        "s": "0x1fc7f89d6310116f3da5760dfa30af75f55b64f3a837839c12615afabf2d59dc",
        "r": "0x093a234dfe7491c6ee5e607650ecd733db0194e4801d14b3acc05e702b99f5bb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6612972578",
    "total": "6612972578"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6612972578",
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
            "amount": "48105430068"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6612972"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMWNkYzc0NS00ODU4LTVlMjItYTU2Mi1hY2I2MmEwYjYxMDEifQ==",
    "nonce": 7167,
    "balances": {
      "current": "12969565557956301",
      "previous": "12969572177541851"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8f9f610d0bd4cda3b6afd02701ad2e2c231059f8",
    "nonce": 22,
    "balances": {
      "current": "6612972578",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:44.402Z",
  "updated": "2020-05-22T08:54:44.474Z",
  "id": "5ec79354b0c6090011d5b228"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000018a29f422000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6612972578`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`