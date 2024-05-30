# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0Eb8Adcc72f89262c769272a874EB042Ca0801c8`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000d8755846f288fb4f8000000000000000000000000000000000000000000000001da7823f4119815510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001da7823f41198155100000000000000000000000000000000000000000000000d8755846f288fb4f8e7fce90742e1c31d91eaffee487800b86732dd32fd16b4c931e9bf59e868d1c4aba975465983b61cd75bda992f929d04beddf8c5a84413edbcac6214284fe1ec597f918f6249542a67a5176d21d7aa9b615dfb0b454a278a8283ed1d3c71cd61000000000000000000000000000000000000000000000000000000000000001ce716832b95de790a01d0dd64c5eb3c5f40ff168c191233c31487aa1de5d1fe86a01967522a41876249c342a043e7c8100db65eb8f5a43e5ad47deafe286faaa61dc7e313677d85a21fd07710c724b4d9d7c52ac15761c599017689c8be152ffc000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000b6b692000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000109a8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023153b5bcb513ce2520e000000000000000000000000000000000000000000002317164d661736f1988b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000007976d1e877312c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002ed3a28decd9c43ce650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f445930596d46695969316b4d6a426c4c54566d4e6a6b74596a49334d69307959324a684d475a6c4e4751314d7a636966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000000eb8adcc72f89262c769272a874eb042ca0801c800000000000000000000000000000000000000000000000d8755846f288fb4f800000000000000000000000000000000000000000000000bacdd607b16f79fa700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe7fce90742e1c31d91eaffee487800b86732dd32fd16b4c931e9bf59e868d1c4",
      "signature": {
        "s": "0x597f918f6249542a67a5176d21d7aa9b615dfb0b454a278a8283ed1d3c71cd61",
        "r": "0xaba975465983b61cd75bda992f929d04beddf8c5a84413edbcac6214284fe1ec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe716832b95de790a01d0dd64c5eb3c5f40ff168c191233c31487aa1de5d1fe86",
      "signature": {
        "s": "0x1dc7e313677d85a21fd07710c724b4d9d7c52ac15761c599017689c8be152ffc",
        "r": "0xa01967522a41876249c342a043e7c8100db65eb8f5a43e5ad47deafe286faaa6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "34189116102357292369",
    "total": "249559519139321591032"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "34189116102357292369",
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
            "amount": "13820802155636393758309"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "34189116102357292"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkODY0YmFiYi1kMjBlLTVmNjktYjI3Mi0yY2JhMGZlNGQ1MzcifQ==",
    "nonce": 68008,
    "balances": {
      "current": "165674485761806375735822",
      "previous": "165708709067024835385483"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0eb8adcc72f89262c769272a874eb042ca0801c8",
    "nonce": 3,
    "balances": {
      "current": "249559519139321591032",
      "previous": "215370403036964298663"
    }
  },
  "blockNumber": "11974290",
  "created": "2021-03-04T21:48:21.737Z",
  "updated": "2021-03-04T21:48:21.806Z",
  "id": "604155a5c22ca00010a6fba4"
}
```
* *stageAmount*: `249559519139321591032`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001da7823f4119815510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001da7823f41198155100000000000000000000000000000000000000000000000d8755846f288fb4f8e7fce90742e1c31d91eaffee487800b86732dd32fd16b4c931e9bf59e868d1c4aba975465983b61cd75bda992f929d04beddf8c5a84413edbcac6214284fe1ec597f918f6249542a67a5176d21d7aa9b615dfb0b454a278a8283ed1d3c71cd61000000000000000000000000000000000000000000000000000000000000001ce716832b95de790a01d0dd64c5eb3c5f40ff168c191233c31487aa1de5d1fe86a01967522a41876249c342a043e7c8100db65eb8f5a43e5ad47deafe286faaa61dc7e313677d85a21fd07710c724b4d9d7c52ac15761c599017689c8be152ffc000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000b6b692000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000109a8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023153b5bcb513ce2520e000000000000000000000000000000000000000000002317164d661736f1988b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000007976d1e877312c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002ed3a28decd9c43ce650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f445930596d46695969316b4d6a426c4c54566d4e6a6b74596a49334d69307959324a684d475a6c4e4751314d7a636966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000000eb8adcc72f89262c769272a874eb042ca0801c800000000000000000000000000000000000000000000000d8755846f288fb4f800000000000000000000000000000000000000000000000bacdd607b16f79fa700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe7fce90742e1c31d91eaffee487800b86732dd32fd16b4c931e9bf59e868d1c4",
      "signature": {
        "s": "0x597f918f6249542a67a5176d21d7aa9b615dfb0b454a278a8283ed1d3c71cd61",
        "r": "0xaba975465983b61cd75bda992f929d04beddf8c5a84413edbcac6214284fe1ec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe716832b95de790a01d0dd64c5eb3c5f40ff168c191233c31487aa1de5d1fe86",
      "signature": {
        "s": "0x1dc7e313677d85a21fd07710c724b4d9d7c52ac15761c599017689c8be152ffc",
        "r": "0xa01967522a41876249c342a043e7c8100db65eb8f5a43e5ad47deafe286faaa6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "34189116102357292369",
    "total": "249559519139321591032"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "34189116102357292369",
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
            "amount": "13820802155636393758309"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "34189116102357292"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkODY0YmFiYi1kMjBlLTVmNjktYjI3Mi0yY2JhMGZlNGQ1MzcifQ==",
    "nonce": 68008,
    "balances": {
      "current": "165674485761806375735822",
      "previous": "165708709067024835385483"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0eb8adcc72f89262c769272a874eb042ca0801c8",
    "nonce": 3,
    "balances": {
      "current": "249559519139321591032",
      "previous": "215370403036964298663"
    }
  },
  "blockNumber": "11974290",
  "created": "2021-03-04T21:48:21.737Z",
  "updated": "2021-03-04T21:48:21.806Z",
  "id": "604155a5c22ca00010a6fba4"
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
0x0f200f9b00000000000000000000000000000000000000000000000d8755846f288fb4f80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `249559519139321591032`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`