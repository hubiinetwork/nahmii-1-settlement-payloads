# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x29AD08bCeAa6f5C6bf6B5A23433334170ad7B2D1`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000003f23ccfaed6865d94000000000000000000000000000000000000000000000000c62aedb6e70538cd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000c62aedb6e70538cd0000000000000000000000000000000000000000000000a8e0853dc85f9233789574ffbe20f62d7abc4a5add47bc95f0c42d4ba977601cc78989704ea591a20fac8bf960354cdf32bfe9b49c615be28bd6ed0166649d807a8476709c24222a6f567b18d7a220464e776d23d6a8b54added6c8f971dd1ae337c80335f57c47463000000000000000000000000000000000000000000000000000000000000001ce6602806d24ae31b628bb96fc04a4445566305d54cc85090e609e6a491e7473a479b7fd96dab19435624a0c10a88e454e4ed3a2a08e7bfd73c4725ec34a916b565180cfeb3b117da7e8215681aef9758c98f33f56d86c21f557c824cf84d51cc000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d900000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b30c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003fe49f3b4c4599da685c000000000000000000000000000000000000000000003fe56598f51aa368984100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000032bb1e2288f7180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc0ae15f9f54c4a1a30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a546c6b4f474e6c4e79316b4f5441344c5456684d5759744f575669597930794d5759325a446b354e4445324d6a516966513d3d000000000000000000000000000000000000000000000000000000000000003b00000000000000000000000029ad08bceaa6f5c6bf6b5a23433334170ad7b2d1000000000000000000000000000000000000000000000003f23ccfaed6865d940000000000000000000000000000000000000000000000032c11e1f7ef8124c700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000357bcda193e0c0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x9574ffbe20f62d7abc4a5add47bc95f0c42d4ba977601cc78989704ea591a20f",
      "signature": {
        "s": "0x567b18d7a220464e776d23d6a8b54added6c8f971dd1ae337c80335f57c47463",
        "r": "0xac8bf960354cdf32bfe9b49c615be28bd6ed0166649d807a8476709c24222a6f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe6602806d24ae31b628bb96fc04a4445566305d54cc85090e609e6a491e7473a",
      "signature": {
        "s": "0x65180cfeb3b117da7e8215681aef9758c98f33f56d86c21f557c824cf84d51cc",
        "r": "0x479b7fd96dab19435624a0c10a88e454e4ed3a2a08e7bfd73c4725ec34a916b5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14279486938347288781",
    "total": "3115231409550409216888"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14279486938347288781",
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
            "amount": "27670900123512393212323"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "14279486938347288"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1ZTlkOGNlNy1kOTA4LTVhMWYtOWViYy0yMWY2ZDk5NDE2MjQifQ==",
    "nonce": 111372,
    "balances": {
      "current": "301726419917930900383836",
      "previous": "301740713684356186019905"
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
            "amount": "3853900000000000000"
          }
        }
      ]
    },
    "wallet": "0x29ad08bceaa6f5c6bf6b5a23433334170ad7b2d1",
    "nonce": 59,
    "balances": {
      "current": "72795286826740243860",
      "previous": "58515799888392955079"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:57:57.963Z",
  "updated": "2022-05-04T08:57:58.063Z",
  "id": "62724015bbd75600116d0695"
}
```
* *stageAmount*: `72795286826740243860`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000680000000000000000000000000000000000000000000000000c62aedb6e70538cd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000c62aedb6e70538cd0000000000000000000000000000000000000000000000a8e0853dc85f9233789574ffbe20f62d7abc4a5add47bc95f0c42d4ba977601cc78989704ea591a20fac8bf960354cdf32bfe9b49c615be28bd6ed0166649d807a8476709c24222a6f567b18d7a220464e776d23d6a8b54added6c8f971dd1ae337c80335f57c47463000000000000000000000000000000000000000000000000000000000000001ce6602806d24ae31b628bb96fc04a4445566305d54cc85090e609e6a491e7473a479b7fd96dab19435624a0c10a88e454e4ed3a2a08e7bfd73c4725ec34a916b565180cfeb3b117da7e8215681aef9758c98f33f56d86c21f557c824cf84d51cc000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d900000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b30c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003fe49f3b4c4599da685c000000000000000000000000000000000000000000003fe56598f51aa368984100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000032bb1e2288f7180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc0ae15f9f54c4a1a30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a546c6b4f474e6c4e79316b4f5441344c5456684d5759744f575669597930794d5759325a446b354e4445324d6a516966513d3d000000000000000000000000000000000000000000000000000000000000003b00000000000000000000000029ad08bceaa6f5c6bf6b5a23433334170ad7b2d1000000000000000000000000000000000000000000000003f23ccfaed6865d940000000000000000000000000000000000000000000000032c11e1f7ef8124c700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000357bcda193e0c0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x9574ffbe20f62d7abc4a5add47bc95f0c42d4ba977601cc78989704ea591a20f",
      "signature": {
        "s": "0x567b18d7a220464e776d23d6a8b54added6c8f971dd1ae337c80335f57c47463",
        "r": "0xac8bf960354cdf32bfe9b49c615be28bd6ed0166649d807a8476709c24222a6f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe6602806d24ae31b628bb96fc04a4445566305d54cc85090e609e6a491e7473a",
      "signature": {
        "s": "0x65180cfeb3b117da7e8215681aef9758c98f33f56d86c21f557c824cf84d51cc",
        "r": "0x479b7fd96dab19435624a0c10a88e454e4ed3a2a08e7bfd73c4725ec34a916b5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14279486938347288781",
    "total": "3115231409550409216888"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14279486938347288781",
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
            "amount": "27670900123512393212323"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "14279486938347288"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1ZTlkOGNlNy1kOTA4LTVhMWYtOWViYy0yMWY2ZDk5NDE2MjQifQ==",
    "nonce": 111372,
    "balances": {
      "current": "301726419917930900383836",
      "previous": "301740713684356186019905"
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
            "amount": "3853900000000000000"
          }
        }
      ]
    },
    "wallet": "0x29ad08bceaa6f5c6bf6b5a23433334170ad7b2d1",
    "nonce": 59,
    "balances": {
      "current": "72795286826740243860",
      "previous": "58515799888392955079"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:57:57.963Z",
  "updated": "2022-05-04T08:57:58.063Z",
  "id": "62724015bbd75600116d0695"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000003f23ccfaed6865d940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `72795286826740243860`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`