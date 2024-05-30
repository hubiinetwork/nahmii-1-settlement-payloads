# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFbd431706498d51B6F028623BDbb2af9B874Fe38`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000e47b46fefb6e44200000000000000000000000000000000000000000000021ee47e68600af400000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000021ee47e68600af4000000000000000000000000000000000000000000000000021ee47e68600af4000060da37ed44339b4cd8fa87b885f93a75fa7c23921713c2f1efc1ba36ae4776869f40dd572162a0c9c366b10e9c00f751410e5d5ad0958f5d775eca6af9da6689372d9f519401ae70943a8609fc73fc155e64ff865bad32790cecf4449742de7a000000000000000000000000000000000000000000000000000000000000001bf3fa0c193645e896c87918a14a306bfd5d64f040dc7ff07a8219cf94e6a9b8738706792a7fb96b191f2793ade1a5cdcc55d83f4d28c74dfabca0f93a465355ce30a8c09a2c8d10bc36183c47799fe3af41f90b59cc71cb1a7853ce8857185b73000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1f52700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000044000000000000000000000000fbd431706498d51b6f028623bdbb2af9b874fe380000000000000000000000000000000000000000000000000e47b46fefb6e44200000000000000000000000000000000000000000000021f7dc11e73ea4b644200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000008afb01a3efa080000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a251f88eecd030000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f44597a5a475a6a4e6930324d54466b4c54526b4e546374595464685a5330334e446b345a6d526b5957457a4d6d456966513d3d000000000000000000000000000000000000000000000000000000000000004b000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000003046b9a71c6dd7d05628000000000000000000000000000000000000000000002e27d528b40dccdc562800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60da37ed44339b4cd8fa87b885f93a75fa7c23921713c2f1efc1ba36ae477686",
      "signature": {
        "s": "0x372d9f519401ae70943a8609fc73fc155e64ff865bad32790cecf4449742de7a",
        "r": "0x9f40dd572162a0c9c366b10e9c00f751410e5d5ad0958f5d775eca6af9da6689",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf3fa0c193645e896c87918a14a306bfd5d64f040dc7ff07a8219cf94e6a9b873",
      "signature": {
        "s": "0x30a8c09a2c8d10bc36183c47799fe3af41f90b59cc71cb1a7853ce8857185b73",
        "r": "0x8706792a7fb96b191f2793ade1a5cdcc55d83f4d28c74dfabca0f93a465355ce",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10014600000000000000000",
    "total": "10014600000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10014600000000000000000",
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
            "amount": "11696403000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10014600000000000000"
      }
    },
    "wallet": "0xfbd431706498d51b6f028623bdbb2af9b874fe38",
    "data": "eyJyZWYiOiIxODYzZGZjNi02MTFkLTRkNTctYTdhZS03NDk4ZmRkYWEzMmEifQ==",
    "nonce": 68,
    "balances": {
      "current": "1028989432733557826",
      "previous": "10025643589432733557826"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 75,
    "balances": {
      "current": "227978240955378863986216",
      "previous": "217963640955378863986216"
    }
  },
  "blockNumber": "14808359",
  "created": "2022-05-20T01:48:39.696Z",
  "updated": "2022-05-20T01:48:39.813Z",
  "id": "6286f377bbd75600116d08c7"
}
```
* *stageAmount*: `1028989432733557826`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000021ee47e68600af400000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000021ee47e68600af4000000000000000000000000000000000000000000000000021ee47e68600af4000060da37ed44339b4cd8fa87b885f93a75fa7c23921713c2f1efc1ba36ae4776869f40dd572162a0c9c366b10e9c00f751410e5d5ad0958f5d775eca6af9da6689372d9f519401ae70943a8609fc73fc155e64ff865bad32790cecf4449742de7a000000000000000000000000000000000000000000000000000000000000001bf3fa0c193645e896c87918a14a306bfd5d64f040dc7ff07a8219cf94e6a9b8738706792a7fb96b191f2793ade1a5cdcc55d83f4d28c74dfabca0f93a465355ce30a8c09a2c8d10bc36183c47799fe3af41f90b59cc71cb1a7853ce8857185b73000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1f52700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000044000000000000000000000000fbd431706498d51b6f028623bdbb2af9b874fe380000000000000000000000000000000000000000000000000e47b46fefb6e44200000000000000000000000000000000000000000000021f7dc11e73ea4b644200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000008afb01a3efa080000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a251f88eecd030000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f44597a5a475a6a4e6930324d54466b4c54526b4e546374595464685a5330334e446b345a6d526b5957457a4d6d456966513d3d000000000000000000000000000000000000000000000000000000000000004b000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000003046b9a71c6dd7d05628000000000000000000000000000000000000000000002e27d528b40dccdc562800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60da37ed44339b4cd8fa87b885f93a75fa7c23921713c2f1efc1ba36ae477686",
      "signature": {
        "s": "0x372d9f519401ae70943a8609fc73fc155e64ff865bad32790cecf4449742de7a",
        "r": "0x9f40dd572162a0c9c366b10e9c00f751410e5d5ad0958f5d775eca6af9da6689",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf3fa0c193645e896c87918a14a306bfd5d64f040dc7ff07a8219cf94e6a9b873",
      "signature": {
        "s": "0x30a8c09a2c8d10bc36183c47799fe3af41f90b59cc71cb1a7853ce8857185b73",
        "r": "0x8706792a7fb96b191f2793ade1a5cdcc55d83f4d28c74dfabca0f93a465355ce",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10014600000000000000000",
    "total": "10014600000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10014600000000000000000",
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
            "amount": "11696403000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10014600000000000000"
      }
    },
    "wallet": "0xfbd431706498d51b6f028623bdbb2af9b874fe38",
    "data": "eyJyZWYiOiIxODYzZGZjNi02MTFkLTRkNTctYTdhZS03NDk4ZmRkYWEzMmEifQ==",
    "nonce": 68,
    "balances": {
      "current": "1028989432733557826",
      "previous": "10025643589432733557826"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 75,
    "balances": {
      "current": "227978240955378863986216",
      "previous": "217963640955378863986216"
    }
  },
  "blockNumber": "14808359",
  "created": "2022-05-20T01:48:39.696Z",
  "updated": "2022-05-20T01:48:39.813Z",
  "id": "6286f377bbd75600116d08c7"
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
0x0f200f9b0000000000000000000000000000000000000000000000000e47b46fefb6e4420000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1028989432733557826`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`