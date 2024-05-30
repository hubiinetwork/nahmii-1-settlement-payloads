# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x742C3bdCD0f48B2937Db96BB5e87e9624544B14e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000005cdef0f896a057840000000000000000000000000000000000000000000000000233ad4de4b86c6c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000233ad4de4b86c6c0000000000000000000000000000000000000000000000003dc952e69ed364b0545694875a273859b08d4c845760c15e44c64785a33a1d863500ad3ba524aadaa96ef54e0c1e2ed5d3a29dc92e928b3257c9f201ffdc75755b286a8d53b01a9757f63294cb9801522b3b9e53c38228cb3346f05dff89514dd7616469708f7198000000000000000000000000000000000000000000000000000000000000001c1ef8108566246fb0c408bd5b7e79627fdd003e574ca3af3306489d15d965be4beacea245294b73535661b4eb6965f84b1a7c1fe6a771b66e59bce0a7620949e633568022fbafd871c75888a556b8b170288eb7ffccd06c5da4b1ce444343e806000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac03000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009aac64c39d6810ffaf43000000000000000000000000000000000000000000009aac66f7db0317fef2d400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000904d2246d7250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d37138ab0f9921c00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4f4455774f47526c5a693169596d51784c54566c595451744f5467784d5331694e7a49315a5467794d3245325a6a416966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000742c3bdcd0f48b2937db96bb5e87e9624544b14e0000000000000000000000000000000000000000000000005cdef0f896a057840000000000000000000000000000000000000000000000005aab43aab1e7eb1800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x545694875a273859b08d4c845760c15e44c64785a33a1d863500ad3ba524aada",
      "signature": {
        "s": "0x57f63294cb9801522b3b9e53c38228cb3346f05dff89514dd7616469708f7198",
        "r": "0xa96ef54e0c1e2ed5d3a29dc92e928b3257c9f201ffdc75755b286a8d53b01a97",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1ef8108566246fb0c408bd5b7e79627fdd003e574ca3af3306489d15d965be4b",
      "signature": {
        "s": "0x33568022fbafd871c75888a556b8b170288eb7ffccd06c5da4b1ce444343e806",
        "r": "0xeacea245294b73535661b4eb6965f84b1a7c1fe6a771b66e59bce0a7620949e6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "158660961949477996",
    "total": "4452180857093055664"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949477996",
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
            "amount": "27242630274117021540800"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949477"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjODUwOGRlZi1iYmQxLTVlYTQtOTgxMS1iNzI1ZTgyM2E2ZjAifQ==",
    "nonce": 109571,
    "balances": {
      "current": "730424539162697944510275",
      "previous": "730424697982320855937748"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x742c3bdcd0f48b2937db96bb5e87e9624544b14e",
    "nonce": 46,
    "balances": {
      "current": "6692051046788781956",
      "previous": "6533390084839303960"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:47.034Z",
  "updated": "2022-05-04T08:48:47.106Z",
  "id": "62723def3592fd001130b3c0"
}
```
* *stageAmount*: `6692051046788781956`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000233ad4de4b86c6c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000233ad4de4b86c6c0000000000000000000000000000000000000000000000003dc952e69ed364b0545694875a273859b08d4c845760c15e44c64785a33a1d863500ad3ba524aadaa96ef54e0c1e2ed5d3a29dc92e928b3257c9f201ffdc75755b286a8d53b01a9757f63294cb9801522b3b9e53c38228cb3346f05dff89514dd7616469708f7198000000000000000000000000000000000000000000000000000000000000001c1ef8108566246fb0c408bd5b7e79627fdd003e574ca3af3306489d15d965be4beacea245294b73535661b4eb6965f84b1a7c1fe6a771b66e59bce0a7620949e633568022fbafd871c75888a556b8b170288eb7ffccd06c5da4b1ce444343e806000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac03000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009aac64c39d6810ffaf43000000000000000000000000000000000000000000009aac66f7db0317fef2d400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000904d2246d7250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d37138ab0f9921c00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4f4455774f47526c5a693169596d51784c54566c595451744f5467784d5331694e7a49315a5467794d3245325a6a416966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000742c3bdcd0f48b2937db96bb5e87e9624544b14e0000000000000000000000000000000000000000000000005cdef0f896a057840000000000000000000000000000000000000000000000005aab43aab1e7eb1800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x545694875a273859b08d4c845760c15e44c64785a33a1d863500ad3ba524aada",
      "signature": {
        "s": "0x57f63294cb9801522b3b9e53c38228cb3346f05dff89514dd7616469708f7198",
        "r": "0xa96ef54e0c1e2ed5d3a29dc92e928b3257c9f201ffdc75755b286a8d53b01a97",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1ef8108566246fb0c408bd5b7e79627fdd003e574ca3af3306489d15d965be4b",
      "signature": {
        "s": "0x33568022fbafd871c75888a556b8b170288eb7ffccd06c5da4b1ce444343e806",
        "r": "0xeacea245294b73535661b4eb6965f84b1a7c1fe6a771b66e59bce0a7620949e6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "158660961949477996",
    "total": "4452180857093055664"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949477996",
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
            "amount": "27242630274117021540800"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949477"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjODUwOGRlZi1iYmQxLTVlYTQtOTgxMS1iNzI1ZTgyM2E2ZjAifQ==",
    "nonce": 109571,
    "balances": {
      "current": "730424539162697944510275",
      "previous": "730424697982320855937748"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x742c3bdcd0f48b2937db96bb5e87e9624544b14e",
    "nonce": 46,
    "balances": {
      "current": "6692051046788781956",
      "previous": "6533390084839303960"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:47.034Z",
  "updated": "2022-05-04T08:48:47.106Z",
  "id": "62723def3592fd001130b3c0"
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
0x0f200f9b0000000000000000000000000000000000000000000000005cdef0f896a057840000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6692051046788781956`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`