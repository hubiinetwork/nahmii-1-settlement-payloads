# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC2c8185cdED692896f01c5B23034C49A9e28e635`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000a243515c00000000000000000000000000000000000000000000000000000000a243515c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000a243515c00000000000000000000000000000000000000000000000000000000a243515c7e41edbc850c5c83ce54e29ea7534265e0dd6a25c8ec6483667b14f4f0dd3e6a9fd826b34f5b03bb1182f965ad83c581fde9779a8b7dc5fd4ecc489ba4e6a5f3260f4b1768101444b0e7bcc570960a62c1040654e2cdbbfdb61c2aa89289bd03000000000000000000000000000000000000000000000000000000000000001b1b131fe76422a6cc844bc59be6bb2cfe1cf3aa44f182dc4080f9e8f9d2e0237efe77fe73ccb25b5f759ce076020516e5a61ac7f07448554c1807acd88a58031f66c8cd4119e93ffccd984c7e850a1490c6d50bb7e4426b2823862fead32fb317000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56600000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000147100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e324067577bfa000000000000000000000000000000000000000000000000002e324109c4576600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000298a10000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003666dbaa1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e5455354e6a426d5979307a5a4441794c5455325a6a5974596d4532595330344f546b33596a51345a6a5930597a456966513d3d000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000c2c8185cded692896f01c5b23034c49a9e28e63500000000000000000000000000000000000000000000000000000000a243515c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7e41edbc850c5c83ce54e29ea7534265e0dd6a25c8ec6483667b14f4f0dd3e6a",
      "signature": {
        "s": "0x260f4b1768101444b0e7bcc570960a62c1040654e2cdbbfdb61c2aa89289bd03",
        "r": "0x9fd826b34f5b03bb1182f965ad83c581fde9779a8b7dc5fd4ecc489ba4e6a5f3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1b131fe76422a6cc844bc59be6bb2cfe1cf3aa44f182dc4080f9e8f9d2e0237e",
      "signature": {
        "s": "0x66c8cd4119e93ffccd984c7e850a1490c6d50bb7e4426b2823862fead32fb317",
        "r": "0xfe77fe73ccb25b5f759ce076020516e5a61ac7f07448554c1807acd88a58031f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2722320732",
    "total": "2722320732"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2722320732",
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
            "amount": "14603369121"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2722320"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1NTU5NjBmYy0zZDAyLTU2ZjYtYmE2YS04OTk3YjQ4ZjY0YzEifQ==",
    "nonce": 5233,
    "balances": {
      "current": "13003101121772538",
      "previous": "13003103846815590"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2c8185cded692896f01c5b23034c49a9e28e635",
    "nonce": 26,
    "balances": {
      "current": "2722320732",
      "previous": "0"
    }
  },
  "blockNumber": "10114656",
  "created": "2020-05-22T08:39:33.268Z",
  "updated": "2020-05-22T08:39:33.336Z",
  "id": "5ec78fc5005df800101bc90b"
}
```
* *stageAmount*: `2722320732`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000a243515c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000a243515c00000000000000000000000000000000000000000000000000000000a243515c7e41edbc850c5c83ce54e29ea7534265e0dd6a25c8ec6483667b14f4f0dd3e6a9fd826b34f5b03bb1182f965ad83c581fde9779a8b7dc5fd4ecc489ba4e6a5f3260f4b1768101444b0e7bcc570960a62c1040654e2cdbbfdb61c2aa89289bd03000000000000000000000000000000000000000000000000000000000000001b1b131fe76422a6cc844bc59be6bb2cfe1cf3aa44f182dc4080f9e8f9d2e0237efe77fe73ccb25b5f759ce076020516e5a61ac7f07448554c1807acd88a58031f66c8cd4119e93ffccd984c7e850a1490c6d50bb7e4426b2823862fead32fb317000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56600000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000147100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e324067577bfa000000000000000000000000000000000000000000000000002e324109c4576600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000298a10000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003666dbaa1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e5455354e6a426d5979307a5a4441794c5455325a6a5974596d4532595330344f546b33596a51345a6a5930597a456966513d3d000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000c2c8185cded692896f01c5b23034c49a9e28e63500000000000000000000000000000000000000000000000000000000a243515c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7e41edbc850c5c83ce54e29ea7534265e0dd6a25c8ec6483667b14f4f0dd3e6a",
      "signature": {
        "s": "0x260f4b1768101444b0e7bcc570960a62c1040654e2cdbbfdb61c2aa89289bd03",
        "r": "0x9fd826b34f5b03bb1182f965ad83c581fde9779a8b7dc5fd4ecc489ba4e6a5f3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1b131fe76422a6cc844bc59be6bb2cfe1cf3aa44f182dc4080f9e8f9d2e0237e",
      "signature": {
        "s": "0x66c8cd4119e93ffccd984c7e850a1490c6d50bb7e4426b2823862fead32fb317",
        "r": "0xfe77fe73ccb25b5f759ce076020516e5a61ac7f07448554c1807acd88a58031f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2722320732",
    "total": "2722320732"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2722320732",
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
            "amount": "14603369121"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2722320"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1NTU5NjBmYy0zZDAyLTU2ZjYtYmE2YS04OTk3YjQ4ZjY0YzEifQ==",
    "nonce": 5233,
    "balances": {
      "current": "13003101121772538",
      "previous": "13003103846815590"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2c8185cded692896f01c5b23034c49a9e28e635",
    "nonce": 26,
    "balances": {
      "current": "2722320732",
      "previous": "0"
    }
  },
  "blockNumber": "10114656",
  "created": "2020-05-22T08:39:33.268Z",
  "updated": "2020-05-22T08:39:33.336Z",
  "id": "5ec78fc5005df800101bc90b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000a243515c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2722320732`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`