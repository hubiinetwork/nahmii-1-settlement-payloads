# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x24896b0180D6a33Fb5205C9cbF72e65A4f762C9f`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000004e5624d3c2e776b500000000000000000000000000000000000000000000000000000000316d86f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000316d86f30000000000000000000000000000000000000000000000000000000481902448600b5442a4cfcd8dffea4a00d04421d40b4abe77893212525462e62bb4f6c66820eb0c4d265b3690760d009d3fbc92b90fe79043f4706529043b6c2dd4aef59036f6d82adafc5a3fca48eabca7269952d103858738856de67280a9d86f17d12f000000000000000000000000000000000000000000000000000000000000001b09c2a3d2fdba1e746a9b011af308a1ca05441d49ef98e6d4e1e1dec0201daf3bfb964277959873b71b5c4df1106fdf71236caba5d86c24db9d5b9e5ad4dfd26c478c655de43308a19b70cca84578b245d22ca79c37b1a1093c63c74f5604c4d0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac18000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009aa922664b81a3c7968e000000000000000000000000000000000000000000009aa922664b81d541c4ce00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000ca74d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d4469af4b09206e10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e57557a4d546c6b4f433169596a497a4c5455795932597459575a694e4330304e6a4a69596a41304f4749795a54556966513d3d000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000024896b0180d6a33fb5205c9cbf72e65a4f762c9f0000000000000000000000000000000000000000000000004e5624d3c2e776b50000000000000000000000000000000000000000000000004e5624d39179efc200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x600b5442a4cfcd8dffea4a00d04421d40b4abe77893212525462e62bb4f6c668",
      "signature": {
        "s": "0x36f6d82adafc5a3fca48eabca7269952d103858738856de67280a9d86f17d12f",
        "r": "0x20eb0c4d265b3690760d009d3fbc92b90fe79043f4706529043b6c2dd4aef590",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x09c2a3d2fdba1e746a9b011af308a1ca05441d49ef98e6d4e1e1dec0201daf3b",
      "signature": {
        "s": "0x478c655de43308a19b70cca84578b245d22ca79c37b1a1093c63c74f5604c4d0",
        "r": "0xfb964277959873b71b5c4df1106fdf71236caba5d86c24db9d5b9e5ad4dfd26c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "829261555",
    "total": "19353576520"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "829261555",
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
            "amount": "27242690336355433711329"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "829261"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlNWUzMTlkOC1iYjIzLTUyY2YtYWZiNC00NjJiYjA0OGIyZTUifQ==",
    "nonce": 109592,
    "balances": {
      "current": "730364416862047361799822",
      "previous": "730364416862048191890638"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x24896b0180d6a33fb5205c9cbf72e65a4f762c9f",
    "nonce": 30,
    "balances": {
      "current": "5644739674882143925",
      "previous": "5644739674052882370"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:52.883Z",
  "updated": "2022-05-04T08:48:52.955Z",
  "id": "62723df43592fd001130b3c6"
}
```
* *stageAmount*: `5644739674882143925`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000316d86f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000316d86f30000000000000000000000000000000000000000000000000000000481902448600b5442a4cfcd8dffea4a00d04421d40b4abe77893212525462e62bb4f6c66820eb0c4d265b3690760d009d3fbc92b90fe79043f4706529043b6c2dd4aef59036f6d82adafc5a3fca48eabca7269952d103858738856de67280a9d86f17d12f000000000000000000000000000000000000000000000000000000000000001b09c2a3d2fdba1e746a9b011af308a1ca05441d49ef98e6d4e1e1dec0201daf3bfb964277959873b71b5c4df1106fdf71236caba5d86c24db9d5b9e5ad4dfd26c478c655de43308a19b70cca84578b245d22ca79c37b1a1093c63c74f5604c4d0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac18000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009aa922664b81a3c7968e000000000000000000000000000000000000000000009aa922664b81d541c4ce00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000ca74d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d4469af4b09206e10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e57557a4d546c6b4f433169596a497a4c5455795932597459575a694e4330304e6a4a69596a41304f4749795a54556966513d3d000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000024896b0180d6a33fb5205c9cbf72e65a4f762c9f0000000000000000000000000000000000000000000000004e5624d3c2e776b50000000000000000000000000000000000000000000000004e5624d39179efc200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x600b5442a4cfcd8dffea4a00d04421d40b4abe77893212525462e62bb4f6c668",
      "signature": {
        "s": "0x36f6d82adafc5a3fca48eabca7269952d103858738856de67280a9d86f17d12f",
        "r": "0x20eb0c4d265b3690760d009d3fbc92b90fe79043f4706529043b6c2dd4aef590",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x09c2a3d2fdba1e746a9b011af308a1ca05441d49ef98e6d4e1e1dec0201daf3b",
      "signature": {
        "s": "0x478c655de43308a19b70cca84578b245d22ca79c37b1a1093c63c74f5604c4d0",
        "r": "0xfb964277959873b71b5c4df1106fdf71236caba5d86c24db9d5b9e5ad4dfd26c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "829261555",
    "total": "19353576520"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "829261555",
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
            "amount": "27242690336355433711329"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "829261"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlNWUzMTlkOC1iYjIzLTUyY2YtYWZiNC00NjJiYjA0OGIyZTUifQ==",
    "nonce": 109592,
    "balances": {
      "current": "730364416862047361799822",
      "previous": "730364416862048191890638"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x24896b0180d6a33fb5205c9cbf72e65a4f762c9f",
    "nonce": 30,
    "balances": {
      "current": "5644739674882143925",
      "previous": "5644739674052882370"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:52.883Z",
  "updated": "2022-05-04T08:48:52.955Z",
  "id": "62723df43592fd001130b3c6"
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
0x0f200f9b0000000000000000000000000000000000000000000000004e5624d3c2e776b50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5644739674882143925`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`