# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xaB7FF788aeBBF9338feb34eDd56451B2C8dfBA57`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000c890000000000000000000000000000000000000000000000000000000000000c89000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000c890000000000000000000000000000000000000000000000000000000000000c89300960b3ba9a362bdd878d505f3e5525acc095b7c8b4237ba7da22c44423cea50b72d0ab72388e652a4e65389bc90315210a95f6c8d0028c27dc6641a4577fee2d2963768ebcb66d22e6438b685534d51d1715babe2a7096edb1febcff2cdf9b000000000000000000000000000000000000000000000000000000000000001b066a2ee0f2eaa1b43c9b655cac9ba328089786954213eb05d5c5c98e6d4af824679a1f4a36dba729268cbc8e3cc3077297c5a28e790e41e733d18396e7e0a31f7f915151299e535aeb1541c3107f7a3ede32a44a657aa984145657b99a360d37000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e9d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b02a638c316000000000000000000000000000000000000000000000000002e0b02a638cfa200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000003000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f9291d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930595459784d474a6d4e7931685a474a6c4c5455325a5441744f544d334e7930354f4759325a47466b4f4463354d6a556966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000ab7ff788aebbf9338feb34edd56451b2c8dfba570000000000000000000000000000000000000000000000000000000000000c89000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x300960b3ba9a362bdd878d505f3e5525acc095b7c8b4237ba7da22c44423cea5",
      "signature": {
        "s": "0x2d2963768ebcb66d22e6438b685534d51d1715babe2a7096edb1febcff2cdf9b",
        "r": "0x0b72d0ab72388e652a4e65389bc90315210a95f6c8d0028c27dc6641a4577fee",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x066a2ee0f2eaa1b43c9b655cac9ba328089786954213eb05d5c5c98e6d4af824",
      "signature": {
        "s": "0x7f915151299e535aeb1541c3107f7a3ede32a44a657aa984145657b99a360d37",
        "r": "0x679a1f4a36dba729268cbc8e3cc3077297c5a28e790e41e733d18396e7e0a31f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3209",
    "total": "3209"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3209",
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
            "amount": "57706451415"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YTYxMGJmNy1hZGJlLTU2ZTAtOTM3Ny05OGY2ZGFkODc5MjUifQ==",
    "nonce": 7837,
    "balances": {
      "current": "12959954935268118",
      "previous": "12959954935271330"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xab7ff788aebbf9338feb34edd56451b2c8dfba57",
    "nonce": 4,
    "balances": {
      "current": "3209",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:55.700Z",
  "updated": "2020-05-22T08:59:55.772Z",
  "id": "5ec7948b005df800101bcc7f"
}
```
* *stageAmount*: `3209`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000c89000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000c890000000000000000000000000000000000000000000000000000000000000c89300960b3ba9a362bdd878d505f3e5525acc095b7c8b4237ba7da22c44423cea50b72d0ab72388e652a4e65389bc90315210a95f6c8d0028c27dc6641a4577fee2d2963768ebcb66d22e6438b685534d51d1715babe2a7096edb1febcff2cdf9b000000000000000000000000000000000000000000000000000000000000001b066a2ee0f2eaa1b43c9b655cac9ba328089786954213eb05d5c5c98e6d4af824679a1f4a36dba729268cbc8e3cc3077297c5a28e790e41e733d18396e7e0a31f7f915151299e535aeb1541c3107f7a3ede32a44a657aa984145657b99a360d37000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e9d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b02a638c316000000000000000000000000000000000000000000000000002e0b02a638cfa200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000003000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f9291d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930595459784d474a6d4e7931685a474a6c4c5455325a5441744f544d334e7930354f4759325a47466b4f4463354d6a556966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000ab7ff788aebbf9338feb34edd56451b2c8dfba570000000000000000000000000000000000000000000000000000000000000c89000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x300960b3ba9a362bdd878d505f3e5525acc095b7c8b4237ba7da22c44423cea5",
      "signature": {
        "s": "0x2d2963768ebcb66d22e6438b685534d51d1715babe2a7096edb1febcff2cdf9b",
        "r": "0x0b72d0ab72388e652a4e65389bc90315210a95f6c8d0028c27dc6641a4577fee",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x066a2ee0f2eaa1b43c9b655cac9ba328089786954213eb05d5c5c98e6d4af824",
      "signature": {
        "s": "0x7f915151299e535aeb1541c3107f7a3ede32a44a657aa984145657b99a360d37",
        "r": "0x679a1f4a36dba729268cbc8e3cc3077297c5a28e790e41e733d18396e7e0a31f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3209",
    "total": "3209"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3209",
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
            "amount": "57706451415"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YTYxMGJmNy1hZGJlLTU2ZTAtOTM3Ny05OGY2ZGFkODc5MjUifQ==",
    "nonce": 7837,
    "balances": {
      "current": "12959954935268118",
      "previous": "12959954935271330"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xab7ff788aebbf9338feb34edd56451b2c8dfba57",
    "nonce": 4,
    "balances": {
      "current": "3209",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:55.700Z",
  "updated": "2020-05-22T08:59:55.772Z",
  "id": "5ec7948b005df800101bcc7f"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000c89000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3209`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`