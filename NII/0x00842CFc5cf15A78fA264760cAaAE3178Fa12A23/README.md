# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x00842CFc5cf15A78fA264760cAaAE3178Fa12A23`.

The ordered steps of contract function invocations are included below and in
the corresponding [steps.json](./steps.json). Please read [the general recipe
for settling Nahmii 1 balance](../../README.md) before starting on the first
step of settlement.

## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a))
#### Method name
*stopChallenge*
#### Method payload
```
0xc19df1e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
### Step 2
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000320fd0e751b025c62e000000000000000000000000000000000000000000000000002cbce7173a08400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000002cbce7173a08400000000000000000000000000000000000000000000000c9f59b6282d449c34cedd1220b0f2661f21b755baaa51d2b337100db83dfd810629752755d6afcf17ea97098f3b46039cbd796355868469b4e7e5ca3d2ae452d5e10fe0125391637803a2dcc2cc39884dc4cea062e89c076412efbd9d4ee08f2034554a924cd0a64ad000000000000000000000000000000000000000000000000000000000000001b724dc74b605e43c95e593fd813f5a6b989683ec0d60bf7c12ca5f5c1dc2615b1b6fd32c86b104c7ba4bcfb1ab0395e3bf9e43470c492c4d0321e5d264c7cdac5442fd615fabba7052d8185bb25de8ee065ebc2e20807da0bae838e85997b9641000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d700000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b2a3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004744a729cff95c592b92000000000000000000000000000000000000000000004744a7569854650198b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000b73f16e64df0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da2806fc431567ab9f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d444a6d4d324669596930304e6d51784c5456694e7a4174596d46694e4330324e44526d4e4455325a575a6c4e47556966513d3d000000000000000000000000000000000000000000000000000000000000003900000000000000000000000000842cfc5cf15a78fa264760caaae3178fa12a230000000000000000000000000000000000000000000000320fd0e751b025c62e0000000000000000000000000000000000000000000000320fa42a6a98ebbdee00000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002ef939aaa3be00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xedd1220b0f2661f21b755baaa51d2b337100db83dfd810629752755d6afcf17e",
      "signature": {
        "s": "0x3a2dcc2cc39884dc4cea062e89c076412efbd9d4ee08f2034554a924cd0a64ad",
        "r": "0xa97098f3b46039cbd796355868469b4e7e5ca3d2ae452d5e10fe012539163780",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x724dc74b605e43c95e593fd813f5a6b989683ec0d60bf7c12ca5f5c1dc2615b1",
      "signature": {
        "s": "0x442fd615fabba7052d8185bb25de8ee065ebc2e20807da0bae838e85997b9641",
        "r": "0xb6fd32c86b104c7ba4bcfb1ab0395e3bf9e43470c492c4d0321e5d264c7cdac5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12592599688415296",
    "total": "3725493406290349245260"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12592599688415296",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27636106892393337826207"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12592599688415"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MDJmM2FiYi00NmQxLTViNzAtYmFiNC02NDRmNDU2ZWZlNGUifQ==",
    "nonce": 111267,
    "balances": {
      "current": "336554444268105341938578",
      "previous": "336554456873297630042289"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "3384800000000000000"
          }
        }
      ]
    },
    "wallet": "0x00842cfc5cf15a78fa264760caaae3178fa12a23",
    "nonce": 57,
    "balances": {
      "current": "923476868729235949102",
      "previous": "923464276129547533806"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:24.908Z",
  "updated": "2022-05-04T08:57:24.984Z",
  "id": "62723ff43592fd001130b5f2"
}
```
* *stageAmount*: `923476868729235949102`
### Step 3
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000680000000000000000000000000000000000000000000000000002cbce7173a08400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000002cbce7173a08400000000000000000000000000000000000000000000000c9f59b6282d449c34cedd1220b0f2661f21b755baaa51d2b337100db83dfd810629752755d6afcf17ea97098f3b46039cbd796355868469b4e7e5ca3d2ae452d5e10fe0125391637803a2dcc2cc39884dc4cea062e89c076412efbd9d4ee08f2034554a924cd0a64ad000000000000000000000000000000000000000000000000000000000000001b724dc74b605e43c95e593fd813f5a6b989683ec0d60bf7c12ca5f5c1dc2615b1b6fd32c86b104c7ba4bcfb1ab0395e3bf9e43470c492c4d0321e5d264c7cdac5442fd615fabba7052d8185bb25de8ee065ebc2e20807da0bae838e85997b9641000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d700000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b2a3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004744a729cff95c592b92000000000000000000000000000000000000000000004744a7569854650198b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000b73f16e64df0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da2806fc431567ab9f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d444a6d4d324669596930304e6d51784c5456694e7a4174596d46694e4330324e44526d4e4455325a575a6c4e47556966513d3d000000000000000000000000000000000000000000000000000000000000003900000000000000000000000000842cfc5cf15a78fa264760caaae3178fa12a230000000000000000000000000000000000000000000000320fd0e751b025c62e0000000000000000000000000000000000000000000000320fa42a6a98ebbdee00000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002ef939aaa3be00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xedd1220b0f2661f21b755baaa51d2b337100db83dfd810629752755d6afcf17e",
      "signature": {
        "s": "0x3a2dcc2cc39884dc4cea062e89c076412efbd9d4ee08f2034554a924cd0a64ad",
        "r": "0xa97098f3b46039cbd796355868469b4e7e5ca3d2ae452d5e10fe012539163780",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x724dc74b605e43c95e593fd813f5a6b989683ec0d60bf7c12ca5f5c1dc2615b1",
      "signature": {
        "s": "0x442fd615fabba7052d8185bb25de8ee065ebc2e20807da0bae838e85997b9641",
        "r": "0xb6fd32c86b104c7ba4bcfb1ab0395e3bf9e43470c492c4d0321e5d264c7cdac5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12592599688415296",
    "total": "3725493406290349245260"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12592599688415296",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27636106892393337826207"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12592599688415"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MDJmM2FiYi00NmQxLTViNzAtYmFiNC02NDRmNDU2ZWZlNGUifQ==",
    "nonce": 111267,
    "balances": {
      "current": "336554444268105341938578",
      "previous": "336554456873297630042289"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "3384800000000000000"
          }
        }
      ]
    },
    "wallet": "0x00842cfc5cf15a78fa264760caaae3178fa12a23",
    "nonce": 57,
    "balances": {
      "current": "923476868729235949102",
      "previous": "923464276129547533806"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:24.908Z",
  "updated": "2022-05-04T08:57:24.984Z",
  "id": "62723ff43592fd001130b5f2"
}
```
* *standard*: `ERC20`
### Step 4
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000320fd0e751b025c62e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `923476868729235949102`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`