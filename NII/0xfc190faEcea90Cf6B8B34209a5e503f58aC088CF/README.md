# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xfc190faEcea90Cf6B8B34209a5e503f58aC088CF`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000007420d3495d26000000000000000000000000000000000000000000000000000002c0d63acc470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000002c0d63acc4700000000000000000000000000000000000000000000000000004d426829d8b67438e9693b326be980bb2c5c9bf77738566a0d2e1b00a2c082d5ebaeb4831d9912faab95f5c9c8419f5385df03b86cf9cc41f874174b8f24a9821c3d5b3c529c4172383fb23fced09740ca3cf4fa2eb4bb0f3590ed16437039f4fba6659fb4ba000000000000000000000000000000000000000000000000000000000000001b2dd73d6ce37c7f27e4f0ce8eeb336d9e57a8709995bce289970277e035b22ecd1c10d0f9a271e5652c448bfd5fd064b51a9d07d0e576b37509c6011286d87e143247e04671db59742cdb89eb8badde3966260c2160e5b1591e7b58aa3c1ddd21000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af39000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000084f1d927026036802c930000000000000000000000000000000000000000000084f1d9270521c12b28ab00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000b4702fd10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ca620802dc6d6b38000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f4445354f57566b4d5330354d6a6c6b4c54566d4e6a59744f444a6d4d5330794f544d324e4467345a444535596a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000fc190faecea90cf6b8b34209a5e503f58ac088cf00000000000000000000000000000000000000000000000000007420d3495d260000000000000000000000000000000000000000000000000000715ffd0e90df00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7438e9693b326be980bb2c5c9bf77738566a0d2e1b00a2c082d5ebaeb4831d99",
      "signature": {
        "s": "0x4172383fb23fced09740ca3cf4fa2eb4bb0f3590ed16437039f4fba6659fb4ba",
        "r": "0x12faab95f5c9c8419f5385df03b86cf9cc41f874174b8f24a9821c3d5b3c529c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2dd73d6ce37c7f27e4f0ce8eeb336d9e57a8709995bce289970277e035b22ecd",
      "signature": {
        "s": "0x3247e04671db59742cdb89eb8badde3966260c2160e5b1591e7b58aa3c1ddd21",
        "r": "0x1c10d0f9a271e5652c448bfd5fd064b51a9d07d0e576b37509c6011286d87e14",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3027251153991",
    "total": "84947610753206"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3027251153991",
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
            "amount": "27345138616398837921792"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3027251153"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyODE5OWVkMS05MjlkLTVmNjYtODJmMS0yOTM2NDg4ZDE5YjMifQ==",
    "nonce": 110393,
    "balances": {
      "current": "627813688538599746710675",
      "previous": "627813688541630025115819"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfc190faecea90cf6b8b34209a5e503f58ac088cf",
    "nonce": 45,
    "balances": {
      "current": "127684332576038",
      "previous": "124657081422047"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:03.472Z",
  "updated": "2022-05-04T08:53:03.615Z",
  "id": "62723eefbbd75600116d0558"
}
```
* *stageAmount*: `127684332576038`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000002c0d63acc470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000002c0d63acc4700000000000000000000000000000000000000000000000000004d426829d8b67438e9693b326be980bb2c5c9bf77738566a0d2e1b00a2c082d5ebaeb4831d9912faab95f5c9c8419f5385df03b86cf9cc41f874174b8f24a9821c3d5b3c529c4172383fb23fced09740ca3cf4fa2eb4bb0f3590ed16437039f4fba6659fb4ba000000000000000000000000000000000000000000000000000000000000001b2dd73d6ce37c7f27e4f0ce8eeb336d9e57a8709995bce289970277e035b22ecd1c10d0f9a271e5652c448bfd5fd064b51a9d07d0e576b37509c6011286d87e143247e04671db59742cdb89eb8badde3966260c2160e5b1591e7b58aa3c1ddd21000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af39000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000084f1d927026036802c930000000000000000000000000000000000000000000084f1d9270521c12b28ab00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000b4702fd10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ca620802dc6d6b38000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f4445354f57566b4d5330354d6a6c6b4c54566d4e6a59744f444a6d4d5330794f544d324e4467345a444535596a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000fc190faecea90cf6b8b34209a5e503f58ac088cf00000000000000000000000000000000000000000000000000007420d3495d260000000000000000000000000000000000000000000000000000715ffd0e90df00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7438e9693b326be980bb2c5c9bf77738566a0d2e1b00a2c082d5ebaeb4831d99",
      "signature": {
        "s": "0x4172383fb23fced09740ca3cf4fa2eb4bb0f3590ed16437039f4fba6659fb4ba",
        "r": "0x12faab95f5c9c8419f5385df03b86cf9cc41f874174b8f24a9821c3d5b3c529c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2dd73d6ce37c7f27e4f0ce8eeb336d9e57a8709995bce289970277e035b22ecd",
      "signature": {
        "s": "0x3247e04671db59742cdb89eb8badde3966260c2160e5b1591e7b58aa3c1ddd21",
        "r": "0x1c10d0f9a271e5652c448bfd5fd064b51a9d07d0e576b37509c6011286d87e14",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3027251153991",
    "total": "84947610753206"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3027251153991",
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
            "amount": "27345138616398837921792"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3027251153"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyODE5OWVkMS05MjlkLTVmNjYtODJmMS0yOTM2NDg4ZDE5YjMifQ==",
    "nonce": 110393,
    "balances": {
      "current": "627813688538599746710675",
      "previous": "627813688541630025115819"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfc190faecea90cf6b8b34209a5e503f58ac088cf",
    "nonce": 45,
    "balances": {
      "current": "127684332576038",
      "previous": "124657081422047"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:03.472Z",
  "updated": "2022-05-04T08:53:03.615Z",
  "id": "62723eefbbd75600116d0558"
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
0x0f200f9b00000000000000000000000000000000000000000000000000007420d3495d260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `127684332576038`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`