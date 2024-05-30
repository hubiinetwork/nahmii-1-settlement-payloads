# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC1b968e63bE634e1D0C6351c68fed94F54B93a13`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de44200011f1aed0000000000000000000000000000000000000000000005e0a7e972e592412a000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000005e0a7e972e592412a000000000000000000000000000000000000000000000005e0a7e972e592412a0022b0ea3cb07376affc54e776d818a6afffe4ed093adfa81bcaa1d699b8e2f257176d117aabff6ccd3c087f75326fb65467bed0df597daaa3e19210754b3ab06a3160a01bd3bc2cd13c53512c412338325fd4c6cc819083f158dc079ae245722a000000000000000000000000000000000000000000000000000000000000001c58823ce8e3c8cdd81c4907b651608ddeda3451867b973f7c4d992c84b5ccc753c4ba15203204fbe641218947804420cf9542884cdf4cdd091a22cf30d9b93ece1bfaa0b7748bd3a667d9c4bef12cbbc64681f4d114ce294da2e66f35b8eb64e8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e261f10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000003c000000000000000000000000c1b968e63be634e1d0c6351c68fed94f54b93a130000000000000000000000000000000000000000000000000de44200011f1aed0000000000000000000000000000000000000000000005e236fed609221d432d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000001813121238ebcfe400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001813121238ebcfe400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5755304e32466a5a69316d5a574d334c5451794e5745744f4445774d433078596a55775a4755324e4456685a6a456966513d3d0000000000000000000000000000000000000000000000000000000000000089000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000006eb93e85469873737f700000000000000000000000000000000000000000000068d8969bd3b2e132557000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x22b0ea3cb07376affc54e776d818a6afffe4ed093adfa81bcaa1d699b8e2f257",
      "signature": {
        "s": "0x3160a01bd3bc2cd13c53512c412338325fd4c6cc819083f158dc079ae245722a",
        "r": "0x176d117aabff6ccd3c087f75326fb65467bed0df597daaa3e19210754b3ab06a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x58823ce8e3c8cdd81c4907b651608ddeda3451867b973f7c4d992c84b5ccc753",
      "signature": {
        "s": "0x1bfaa0b7748bd3a667d9c4bef12cbbc64681f4d114ce294da2e66f35b8eb64e8",
        "r": "0xc4ba15203204fbe641218947804420cf9542884cdf4cdd091a22cf30d9b93ece",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "27756002415063400000000",
    "total": "27756002415063400000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27756002415063400000000",
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
            "amount": "27756002415063400000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "27756002415063400000"
      }
    },
    "wallet": "0xc1b968e63be634e1d0c6351c68fed94f54b93a13",
    "data": "eyJyZWYiOiI3ZWU0N2FjZi1mZWM3LTQyNWEtODEwMC0xYjUwZGU2NDVhZjEifQ==",
    "nonce": 60,
    "balances": {
      "current": "1000997584969341677",
      "previous": "27784759415063432741677"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 137,
    "balances": {
      "current": "522877465853920080527216",
      "previous": "495121463438856680527216"
    }
  },
  "blockNumber": "14836209",
  "created": "2022-05-24T14:12:36.147Z",
  "updated": "2022-05-24T14:12:36.279Z",
  "id": "628ce7d4bbd75600116d08ec"
}
```
* *stageAmount*: `1000997584969341677`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000005e0a7e972e592412a000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000005e0a7e972e592412a000000000000000000000000000000000000000000000005e0a7e972e592412a0022b0ea3cb07376affc54e776d818a6afffe4ed093adfa81bcaa1d699b8e2f257176d117aabff6ccd3c087f75326fb65467bed0df597daaa3e19210754b3ab06a3160a01bd3bc2cd13c53512c412338325fd4c6cc819083f158dc079ae245722a000000000000000000000000000000000000000000000000000000000000001c58823ce8e3c8cdd81c4907b651608ddeda3451867b973f7c4d992c84b5ccc753c4ba15203204fbe641218947804420cf9542884cdf4cdd091a22cf30d9b93ece1bfaa0b7748bd3a667d9c4bef12cbbc64681f4d114ce294da2e66f35b8eb64e8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e261f10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000003c000000000000000000000000c1b968e63be634e1d0c6351c68fed94f54b93a130000000000000000000000000000000000000000000000000de44200011f1aed0000000000000000000000000000000000000000000005e236fed609221d432d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000001813121238ebcfe400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001813121238ebcfe400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5755304e32466a5a69316d5a574d334c5451794e5745744f4445774d433078596a55775a4755324e4456685a6a456966513d3d0000000000000000000000000000000000000000000000000000000000000089000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000006eb93e85469873737f700000000000000000000000000000000000000000000068d8969bd3b2e132557000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x22b0ea3cb07376affc54e776d818a6afffe4ed093adfa81bcaa1d699b8e2f257",
      "signature": {
        "s": "0x3160a01bd3bc2cd13c53512c412338325fd4c6cc819083f158dc079ae245722a",
        "r": "0x176d117aabff6ccd3c087f75326fb65467bed0df597daaa3e19210754b3ab06a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x58823ce8e3c8cdd81c4907b651608ddeda3451867b973f7c4d992c84b5ccc753",
      "signature": {
        "s": "0x1bfaa0b7748bd3a667d9c4bef12cbbc64681f4d114ce294da2e66f35b8eb64e8",
        "r": "0xc4ba15203204fbe641218947804420cf9542884cdf4cdd091a22cf30d9b93ece",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "27756002415063400000000",
    "total": "27756002415063400000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27756002415063400000000",
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
            "amount": "27756002415063400000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "27756002415063400000"
      }
    },
    "wallet": "0xc1b968e63be634e1d0c6351c68fed94f54b93a13",
    "data": "eyJyZWYiOiI3ZWU0N2FjZi1mZWM3LTQyNWEtODEwMC0xYjUwZGU2NDVhZjEifQ==",
    "nonce": 60,
    "balances": {
      "current": "1000997584969341677",
      "previous": "27784759415063432741677"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 137,
    "balances": {
      "current": "522877465853920080527216",
      "previous": "495121463438856680527216"
    }
  },
  "blockNumber": "14836209",
  "created": "2022-05-24T14:12:36.147Z",
  "updated": "2022-05-24T14:12:36.279Z",
  "id": "628ce7d4bbd75600116d08ec"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de44200011f1aed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000997584969341677`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`