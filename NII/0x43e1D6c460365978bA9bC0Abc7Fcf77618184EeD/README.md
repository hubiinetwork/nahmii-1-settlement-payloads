# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x43e1D6c460365978bA9bC0Abc7Fcf77618184EeD`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001e2edb1e4847fc12e0000000000000000000000000000000000000000000000000b731ec83ef244500000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b731ec83ef24450000000000000000000000000000000000000000000000001414a157c06b39247f8bfba7352439db19011f7a254e185e3e1d4b8e8c1a1e6dbf0f1301435dae2eba8217fa0f7872d61e70e5cca2cfd9ac2d05b8b738dfad0a563b72eaa14febb244924747dc2f26d5fcfc18e853b8b1293f95313698ab352afb2b11cd468b76b29000000000000000000000000000000000000000000000000000000000000001c5573e1171a478db5fbb074d8b96afab10451187be4f5cdf2c0caa3d972927b4ca8a6dc907b48f08ac5611d333fe4165543d64335500ebf1b471fd994b9e9bca528667f9e2f23a791b8d67f7297731bf2dc62ca79233ec25d65fc5e26ac88cf7e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ab98000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000d1d7162b40d8fd63d97200000000000000000000000000000000000000000000d1d721a14dff21c67c8b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002ee5de5705ec90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005b6b7a508ae45d5e6580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977597a49314e4751344e793032596a6b774c5455314d57517459544a6a595330794d474530596a4a6d5a47526b5a54416966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000043e1d6c460365978ba9bc0abc7fcf77618184eed000000000000000000000000000000000000000000000001e2edb1e4847fc12e000000000000000000000000000000000000000000000001d77a931c458d7cde00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8bfba7352439db19011f7a254e185e3e1d4b8e8c1a1e6dbf0f1301435dae2eb",
      "signature": {
        "s": "0x4924747dc2f26d5fcfc18e853b8b1293f95313698ab352afb2b11cd468b76b29",
        "r": "0xa8217fa0f7872d61e70e5cca2cfd9ac2d05b8b738dfad0a563b72eaa14febb24",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5573e1171a478db5fbb074d8b96afab10451187be4f5cdf2c0caa3d972927b4c",
      "signature": {
        "s": "0x28667f9e2f23a791b8d67f7297731bf2dc62ca79233ec25d65fc5e26ac88cf7e",
        "r": "0xa8a6dc907b48f08ac5611d333fe4165543d64335500ebf1b471fd994b9e9bca5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "825037002137289808",
    "total": "23151340456884015687"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "825037002137289808",
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
            "amount": "26982372828388051510872"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "825037002137289"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwYzI1NGQ4Ny02YjkwLTU1MWQtYTJjYS0yMGE0YjJmZGRkZTAifQ==",
    "nonce": 109464,
    "balances": {
      "current": "990942242337396944525682",
      "previous": "990943068199436083952779"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x43e1d6c460365978ba9bc0abc7fcf77618184eed",
    "nonce": 46,
    "balances": {
      "current": "34798665490795315502",
      "previous": "33973628488658025694"
    }
  },
  "blockNumber": "14709941",
  "created": "2022-05-04T08:48:14.462Z",
  "updated": "2022-05-04T08:48:14.544Z",
  "id": "62723dcebbd75600116d0419"
}
```
* *stageAmount*: `34798665490795315502`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000b731ec83ef244500000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b731ec83ef24450000000000000000000000000000000000000000000000001414a157c06b39247f8bfba7352439db19011f7a254e185e3e1d4b8e8c1a1e6dbf0f1301435dae2eba8217fa0f7872d61e70e5cca2cfd9ac2d05b8b738dfad0a563b72eaa14febb244924747dc2f26d5fcfc18e853b8b1293f95313698ab352afb2b11cd468b76b29000000000000000000000000000000000000000000000000000000000000001c5573e1171a478db5fbb074d8b96afab10451187be4f5cdf2c0caa3d972927b4ca8a6dc907b48f08ac5611d333fe4165543d64335500ebf1b471fd994b9e9bca528667f9e2f23a791b8d67f7297731bf2dc62ca79233ec25d65fc5e26ac88cf7e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ab98000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000d1d7162b40d8fd63d97200000000000000000000000000000000000000000000d1d721a14dff21c67c8b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002ee5de5705ec90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005b6b7a508ae45d5e6580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977597a49314e4751344e793032596a6b774c5455314d57517459544a6a595330794d474530596a4a6d5a47526b5a54416966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000043e1d6c460365978ba9bc0abc7fcf77618184eed000000000000000000000000000000000000000000000001e2edb1e4847fc12e000000000000000000000000000000000000000000000001d77a931c458d7cde00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8bfba7352439db19011f7a254e185e3e1d4b8e8c1a1e6dbf0f1301435dae2eb",
      "signature": {
        "s": "0x4924747dc2f26d5fcfc18e853b8b1293f95313698ab352afb2b11cd468b76b29",
        "r": "0xa8217fa0f7872d61e70e5cca2cfd9ac2d05b8b738dfad0a563b72eaa14febb24",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5573e1171a478db5fbb074d8b96afab10451187be4f5cdf2c0caa3d972927b4c",
      "signature": {
        "s": "0x28667f9e2f23a791b8d67f7297731bf2dc62ca79233ec25d65fc5e26ac88cf7e",
        "r": "0xa8a6dc907b48f08ac5611d333fe4165543d64335500ebf1b471fd994b9e9bca5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "825037002137289808",
    "total": "23151340456884015687"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "825037002137289808",
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
            "amount": "26982372828388051510872"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "825037002137289"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwYzI1NGQ4Ny02YjkwLTU1MWQtYTJjYS0yMGE0YjJmZGRkZTAifQ==",
    "nonce": 109464,
    "balances": {
      "current": "990942242337396944525682",
      "previous": "990943068199436083952779"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x43e1d6c460365978ba9bc0abc7fcf77618184eed",
    "nonce": 46,
    "balances": {
      "current": "34798665490795315502",
      "previous": "33973628488658025694"
    }
  },
  "blockNumber": "14709941",
  "created": "2022-05-04T08:48:14.462Z",
  "updated": "2022-05-04T08:48:14.544Z",
  "id": "62723dcebbd75600116d0419"
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
0x0f200f9b000000000000000000000000000000000000000000000001e2edb1e4847fc12e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `34798665490795315502`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`