# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xfd23593bac5039abe164e1cd4Bf98e3Ec5fbF014`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000018a2aea60000000000000000000000000000000000000000000000000000000018a2aea60000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018a2aea60000000000000000000000000000000000000000000000000000000018a2aea603d5687612ef47cd0ebcf7344eff2faecf7a9177f26ed7565490d494a9d5913ab1333ae282601e8f9ee5a872cd6ddf34133a91754bb4bb2ed596a5874a0732b71013b72e3b270c328eabe253791329eccf587cbfbaf94b8f6727a3a4a6fcc4f8d000000000000000000000000000000000000000000000000000000000000001bf3e2c241b51266dc35531066074d5cd0c945e3f3e7b943c550efc34204269e9cba416d6f77dd9eb73eabdac179cf94a4241eec4fc607c77dc85de2e0277436696eb3ce101172373e8d09928382c604574de2030af8c88099a7df946df5344455000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b7d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e156eaba28cc9000000000000000000000000000000000000000000000000002e157036325f5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064e82b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ac53dd186000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f4459344d6a67344e53316d4f5463344c5456684f4745744f57466d4e53316d4e6d5a6c4f5745324d474a695a6a596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fd23593bac5039abe164e1cd4bf98e3ec5fbf014000000000000000000000000000000000000000000000000000000018a2aea60000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3d5687612ef47cd0ebcf7344eff2faecf7a9177f26ed7565490d494a9d5913ab",
      "signature": {
        "s": "0x013b72e3b270c328eabe253791329eccf587cbfbaf94b8f6727a3a4a6fcc4f8d",
        "r": "0x1333ae282601e8f9ee5a872cd6ddf34133a91754bb4bb2ed596a5874a0732b71",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf3e2c241b51266dc35531066074d5cd0c945e3f3e7b943c550efc34204269e9c",
      "signature": {
        "s": "0x6eb3ce101172373e8d09928382c604574de2030af8c88099a7df946df5344455",
        "r": "0xba416d6f77dd9eb73eabdac179cf94a4241eec4fc607c77dc85de2e027743669",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6613035616",
    "total": "6613035616"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6613035616",
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
            "amount": "46258835846"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6613035"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyODY4Mjg4NS1mOTc4LTVhOGEtOWFmNS1mNmZlOWE2MGJiZjYifQ==",
    "nonce": 7037,
    "balances": {
      "current": "12971413998832841",
      "previous": "12971420618481492"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfd23593bac5039abe164e1cd4bf98e3ec5fbf014",
    "nonce": 22,
    "balances": {
      "current": "6613035616",
      "previous": "0"
    }
  },
  "blockNumber": "10114727",
  "created": "2020-05-22T08:53:37.674Z",
  "updated": "2020-05-22T08:53:37.737Z",
  "id": "5ec79311005df800101bcb6b"
}
```
* *stageAmount*: `6613035616`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000018a2aea60000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018a2aea60000000000000000000000000000000000000000000000000000000018a2aea603d5687612ef47cd0ebcf7344eff2faecf7a9177f26ed7565490d494a9d5913ab1333ae282601e8f9ee5a872cd6ddf34133a91754bb4bb2ed596a5874a0732b71013b72e3b270c328eabe253791329eccf587cbfbaf94b8f6727a3a4a6fcc4f8d000000000000000000000000000000000000000000000000000000000000001bf3e2c241b51266dc35531066074d5cd0c945e3f3e7b943c550efc34204269e9cba416d6f77dd9eb73eabdac179cf94a4241eec4fc607c77dc85de2e0277436696eb3ce101172373e8d09928382c604574de2030af8c88099a7df946df5344455000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b7d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e156eaba28cc9000000000000000000000000000000000000000000000000002e157036325f5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064e82b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ac53dd186000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f4459344d6a67344e53316d4f5463344c5456684f4745744f57466d4e53316d4e6d5a6c4f5745324d474a695a6a596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fd23593bac5039abe164e1cd4bf98e3ec5fbf014000000000000000000000000000000000000000000000000000000018a2aea60000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3d5687612ef47cd0ebcf7344eff2faecf7a9177f26ed7565490d494a9d5913ab",
      "signature": {
        "s": "0x013b72e3b270c328eabe253791329eccf587cbfbaf94b8f6727a3a4a6fcc4f8d",
        "r": "0x1333ae282601e8f9ee5a872cd6ddf34133a91754bb4bb2ed596a5874a0732b71",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf3e2c241b51266dc35531066074d5cd0c945e3f3e7b943c550efc34204269e9c",
      "signature": {
        "s": "0x6eb3ce101172373e8d09928382c604574de2030af8c88099a7df946df5344455",
        "r": "0xba416d6f77dd9eb73eabdac179cf94a4241eec4fc607c77dc85de2e027743669",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6613035616",
    "total": "6613035616"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6613035616",
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
            "amount": "46258835846"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6613035"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyODY4Mjg4NS1mOTc4LTVhOGEtOWFmNS1mNmZlOWE2MGJiZjYifQ==",
    "nonce": 7037,
    "balances": {
      "current": "12971413998832841",
      "previous": "12971420618481492"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfd23593bac5039abe164e1cd4bf98e3ec5fbf014",
    "nonce": 22,
    "balances": {
      "current": "6613035616",
      "previous": "0"
    }
  },
  "blockNumber": "10114727",
  "created": "2020-05-22T08:53:37.674Z",
  "updated": "2020-05-22T08:53:37.737Z",
  "id": "5ec79311005df800101bcb6b"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000018a2aea60000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6613035616`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`