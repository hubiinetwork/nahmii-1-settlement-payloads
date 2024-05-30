# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAf45eB7b3B6B88D5465223f17fdC76a28856596A`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000004ae9cb2cde53a89800000000000000000000000000000000000000000000000270801d946c9400000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000270801d946c94000000000000000000000000000000000000000000000000000270801d946c940000ababb3545bc49fe5993d88037a5dc608920f67836f12d6ae1501beb2197bbfa939c2015f1d76316e5a65c821f5b737ed89ea94401d27d7cbdf6640f6d118da6740eba0daa5284eb486ac84cc3b4d149175ef6039c886a33c962e8340a1d67308000000000000000000000000000000000000000000000000000000000000001c56e1809df53b4e893f68c3ed0c68fbc0f077faa5a88a65c85e6005eb34b346e687bd00762a8ba726ad581fc610dcaacbdca9ec87c6e044b427cd140901ee98ea24e4ccea6af5954d8dce41432949e9ffd2e14233399bcc541c5871a046b3c451000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e2427b00000000000000000000000000000000000000000000000000000000000005c00000000000000000000000000000000000000000000000000000000000000012000000000000000000000000af45eb7b3b6b88d5465223f17fdc76a28856596a0000000000000000000000000000000000000000000000004ae9cb2cde53a898000000000000000000000000000000000000000000000002bc09c80441cc289800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000009fdf42f6e480000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000236322baddaa0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e324a694d546b344d4330784d4745794c54526c4f445574596a41314e53316c4d4445304e47466d5a5755315a54456966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000089b754df9d2bd896d7d34fde97c0c6d3d655cc78000000000000000000000000000000000000000000000015454a790528cdf823000000000000000000000000000000000000000000000012d4ca5b70bc39f82300000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000012419847ba06c0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xababb3545bc49fe5993d88037a5dc608920f67836f12d6ae1501beb2197bbfa9",
      "signature": {
        "s": "0x40eba0daa5284eb486ac84cc3b4d149175ef6039c886a33c962e8340a1d67308",
        "r": "0x39c2015f1d76316e5a65c821f5b737ed89ea94401d27d7cbdf6640f6d118da67",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x56e1809df53b4e893f68c3ed0c68fbc0f077faa5a88a65c85e6005eb34b346e6",
      "signature": {
        "s": "0x24e4ccea6af5954d8dce41432949e9ffd2e14233399bcc541c5871a046b3c451",
        "r": "0x87bd00762a8ba726ad581fc610dcaacbdca9ec87c6e044b427cd140901ee98ea",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "45000000000000000000",
    "total": "45000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "45000000000000000000",
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
            "amount": "159370000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "45000000000000000"
      }
    },
    "wallet": "0xaf45eb7b3b6b88d5465223f17fdc76a28856596a",
    "data": "eyJyZWYiOiIyN2JiMTk4MC0xMGEyLTRlODUtYjA1NS1lMDE0NGFmZWU1ZTEifQ==",
    "nonce": 18,
    "balances": {
      "current": "5398069021949274264",
      "previous": "50443069021949274264"
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
            "amount": "1315500000000000000"
          }
        }
      ]
    },
    "wallet": "0x89b754df9d2bd896d7d34fde97c0c6d3d655cc78",
    "nonce": 13,
    "balances": {
      "current": "392374561747860584483",
      "previous": "347374561747860584483"
    }
  },
  "blockNumber": "14828155",
  "created": "2022-05-23T07:03:42.111Z",
  "updated": "2022-05-23T07:03:42.250Z",
  "id": "628b31ce3592fd001130b876"
}
```
* *stageAmount*: `5398069021949274264`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000068000000000000000000000000000000000000000000000000270801d946c9400000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000270801d946c94000000000000000000000000000000000000000000000000000270801d946c940000ababb3545bc49fe5993d88037a5dc608920f67836f12d6ae1501beb2197bbfa939c2015f1d76316e5a65c821f5b737ed89ea94401d27d7cbdf6640f6d118da6740eba0daa5284eb486ac84cc3b4d149175ef6039c886a33c962e8340a1d67308000000000000000000000000000000000000000000000000000000000000001c56e1809df53b4e893f68c3ed0c68fbc0f077faa5a88a65c85e6005eb34b346e687bd00762a8ba726ad581fc610dcaacbdca9ec87c6e044b427cd140901ee98ea24e4ccea6af5954d8dce41432949e9ffd2e14233399bcc541c5871a046b3c451000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e2427b00000000000000000000000000000000000000000000000000000000000005c00000000000000000000000000000000000000000000000000000000000000012000000000000000000000000af45eb7b3b6b88d5465223f17fdc76a28856596a0000000000000000000000000000000000000000000000004ae9cb2cde53a898000000000000000000000000000000000000000000000002bc09c80441cc289800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000009fdf42f6e480000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000236322baddaa0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e324a694d546b344d4330784d4745794c54526c4f445574596a41314e53316c4d4445304e47466d5a5755315a54456966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000089b754df9d2bd896d7d34fde97c0c6d3d655cc78000000000000000000000000000000000000000000000015454a790528cdf823000000000000000000000000000000000000000000000012d4ca5b70bc39f82300000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000012419847ba06c0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xababb3545bc49fe5993d88037a5dc608920f67836f12d6ae1501beb2197bbfa9",
      "signature": {
        "s": "0x40eba0daa5284eb486ac84cc3b4d149175ef6039c886a33c962e8340a1d67308",
        "r": "0x39c2015f1d76316e5a65c821f5b737ed89ea94401d27d7cbdf6640f6d118da67",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x56e1809df53b4e893f68c3ed0c68fbc0f077faa5a88a65c85e6005eb34b346e6",
      "signature": {
        "s": "0x24e4ccea6af5954d8dce41432949e9ffd2e14233399bcc541c5871a046b3c451",
        "r": "0x87bd00762a8ba726ad581fc610dcaacbdca9ec87c6e044b427cd140901ee98ea",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "45000000000000000000",
    "total": "45000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "45000000000000000000",
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
            "amount": "159370000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "45000000000000000"
      }
    },
    "wallet": "0xaf45eb7b3b6b88d5465223f17fdc76a28856596a",
    "data": "eyJyZWYiOiIyN2JiMTk4MC0xMGEyLTRlODUtYjA1NS1lMDE0NGFmZWU1ZTEifQ==",
    "nonce": 18,
    "balances": {
      "current": "5398069021949274264",
      "previous": "50443069021949274264"
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
            "amount": "1315500000000000000"
          }
        }
      ]
    },
    "wallet": "0x89b754df9d2bd896d7d34fde97c0c6d3d655cc78",
    "nonce": 13,
    "balances": {
      "current": "392374561747860584483",
      "previous": "347374561747860584483"
    }
  },
  "blockNumber": "14828155",
  "created": "2022-05-23T07:03:42.111Z",
  "updated": "2022-05-23T07:03:42.250Z",
  "id": "628b31ce3592fd001130b876"
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
0x0f200f9b0000000000000000000000000000000000000000000000004ae9cb2cde53a8980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5398069021949274264`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`