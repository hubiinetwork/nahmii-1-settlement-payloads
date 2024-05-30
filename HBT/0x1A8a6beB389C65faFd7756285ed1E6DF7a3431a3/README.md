# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1A8a6beB389C65faFd7756285ed1E6DF7a3431a3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000046a32f000000000000000000000000000000000000000000000000000000000046a32f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000046a32f000000000000000000000000000000000000000000000000000000000046a32fd0a61419bc0a2a4fdefd0b4be2c9319a69b34317da4f83e7589cccb713a8c82e50ccd844be7665ca339034b408c90d95aec0e8a522abd8fc80d9de40c9d4d1c02bcc0e5c37dc4cff7de9dee906c7b9a9f59b86fc31241d1207c05ab2b185393c000000000000000000000000000000000000000000000000000000000000001cc2e36e9d8c7179b15db66725b759fd8fb31e5b18777d0750ffba5161cd47eb0a8062628a81a38305d2259350c2f26b162d7e579368af32801d787e3cd2902df45a1ec7f2a9f021ce453d532d8699b7b337f7836e80d1df51441371576bd5bf0e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000180600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0381a76d91000000000000000000000000000000000000000000000000002e1b0381ee22d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000001215000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000957d32c86000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e574a6c596a4a6b4e6930355a5449354c54566d5a6d517459546b354d5330304d6a466c4f54557a595463314e7a556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000001a8a6beb389c65fafd7756285ed1e6df7a3431a3000000000000000000000000000000000000000000000000000000000046a32f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd0a61419bc0a2a4fdefd0b4be2c9319a69b34317da4f83e7589cccb713a8c82e",
      "signature": {
        "s": "0x2bcc0e5c37dc4cff7de9dee906c7b9a9f59b86fc31241d1207c05ab2b185393c",
        "r": "0x50ccd844be7665ca339034b408c90d95aec0e8a522abd8fc80d9de40c9d4d1c0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc2e36e9d8c7179b15db66725b759fd8fb31e5b18777d0750ffba5161cd47eb0a",
      "signature": {
        "s": "0x5a1ec7f2a9f021ce453d532d8699b7b337f7836e80d1df51441371576bd5bf0e",
        "r": "0x8062628a81a38305d2259350c2f26b162d7e579368af32801d787e3cd2902df4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4629295",
    "total": "4629295"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4629295",
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
            "amount": "40128162950"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4629"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNWJlYjJkNi05ZTI5LTVmZmQtYTk5MS00MjFlOTUzYTc1NzUifQ==",
    "nonce": 6150,
    "balances": {
      "current": "12977550802775441",
      "previous": "12977550807409365"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1a8a6beb389c65fafd7756285ed1e6df7a3431a3",
    "nonce": 22,
    "balances": {
      "current": "4629295",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:46:59.468Z",
  "updated": "2020-05-22T08:46:59.528Z",
  "id": "5ec79183005df800101bca3e"
}
```
* *stageAmount*: `4629295`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000046a32f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000046a32f000000000000000000000000000000000000000000000000000000000046a32fd0a61419bc0a2a4fdefd0b4be2c9319a69b34317da4f83e7589cccb713a8c82e50ccd844be7665ca339034b408c90d95aec0e8a522abd8fc80d9de40c9d4d1c02bcc0e5c37dc4cff7de9dee906c7b9a9f59b86fc31241d1207c05ab2b185393c000000000000000000000000000000000000000000000000000000000000001cc2e36e9d8c7179b15db66725b759fd8fb31e5b18777d0750ffba5161cd47eb0a8062628a81a38305d2259350c2f26b162d7e579368af32801d787e3cd2902df45a1ec7f2a9f021ce453d532d8699b7b337f7836e80d1df51441371576bd5bf0e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000180600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0381a76d91000000000000000000000000000000000000000000000000002e1b0381ee22d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000001215000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000957d32c86000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e574a6c596a4a6b4e6930355a5449354c54566d5a6d517459546b354d5330304d6a466c4f54557a595463314e7a556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000001a8a6beb389c65fafd7756285ed1e6df7a3431a3000000000000000000000000000000000000000000000000000000000046a32f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd0a61419bc0a2a4fdefd0b4be2c9319a69b34317da4f83e7589cccb713a8c82e",
      "signature": {
        "s": "0x2bcc0e5c37dc4cff7de9dee906c7b9a9f59b86fc31241d1207c05ab2b185393c",
        "r": "0x50ccd844be7665ca339034b408c90d95aec0e8a522abd8fc80d9de40c9d4d1c0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc2e36e9d8c7179b15db66725b759fd8fb31e5b18777d0750ffba5161cd47eb0a",
      "signature": {
        "s": "0x5a1ec7f2a9f021ce453d532d8699b7b337f7836e80d1df51441371576bd5bf0e",
        "r": "0x8062628a81a38305d2259350c2f26b162d7e579368af32801d787e3cd2902df4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4629295",
    "total": "4629295"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4629295",
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
            "amount": "40128162950"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4629"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNWJlYjJkNi05ZTI5LTVmZmQtYTk5MS00MjFlOTUzYTc1NzUifQ==",
    "nonce": 6150,
    "balances": {
      "current": "12977550802775441",
      "previous": "12977550807409365"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1a8a6beb389c65fafd7756285ed1e6df7a3431a3",
    "nonce": 22,
    "balances": {
      "current": "4629295",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:46:59.468Z",
  "updated": "2020-05-22T08:46:59.528Z",
  "id": "5ec79183005df800101bca3e"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000046a32f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4629295`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`