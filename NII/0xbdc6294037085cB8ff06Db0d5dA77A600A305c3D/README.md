# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbdc6294037085cB8ff06Db0d5dA77A600A305c3D`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000347921cb45d6f801f300000000000000000000000000000000000000000000000000000019096115630000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001909611563000000000000000000000000000000000000000000000000000002484db165b34c0685dfffc929f65f1bad6b80f81e8cce41a1acf7dbbb5407302430b71d71994a17d3e33afc46e8cd732484fbef8d5e4a1db30341ec6e587ff1d077a0f73969081d2173187644237fd4087ea9c90b7d15c81c21d1140e1634b193e69a0787e9000000000000000000000000000000000000000000000000000000000000001b6d152aee9b5b2d8b31c32cff6f1520606340a0171cda8b132af845cb9c033830d2289b5ba270fb75b245c5586e2e6359ded0cbfeb21c0192ab6039ce38b7ae9c3c6d3c1d9b8570a87020b50f8e7a014c59dbc33593199cd9caef44ee184ba09e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b364000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c8863632bec2afcb60e000000000000000000000000000000000000000000003c8863632c053ac6988400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000668cd130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce6e1556cc879a9d50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f4455784f4459315a6930794e5441324c545532593251744f544534595330785a4467354f44566a5a4451304d474d6966513d3d0000000000000000000000000000000000000000000000000000000000000020000000000000000000000000bdc6294037085cb8ff06db0d5da77a600a305c3d0000000000000000000000000000000000000000000000347921cb45d6f801f30000000000000000000000000000000000000000000000347921cb2ccd96ec9000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4c0685dfffc929f65f1bad6b80f81e8cce41a1acf7dbbb5407302430b71d7199",
      "signature": {
        "s": "0x081d2173187644237fd4087ea9c90b7d15c81c21d1140e1634b193e69a0787e9",
        "r": "0x4a17d3e33afc46e8cd732484fbef8d5e4a1db30341ec6e587ff1d077a0f73969",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6d152aee9b5b2d8b31c32cff6f1520606340a0171cda8b132af845cb9c033830",
      "signature": {
        "s": "0x3c6d3c1d9b8570a87020b50f8e7a014c59dbc33593199cd9caef44ee184ba09e",
        "r": "0xd2289b5ba270fb75b245c5586e2e6359ded0cbfeb21c0192ab6039ce38b7ae9c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "107531539811",
    "total": "2509564372403"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "107531539811",
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
            "amount": "27686752782988518992341"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "107531539"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ODUxODY1Zi0yNTA2LTU2Y2QtOTE4YS0xZDg5ODVjZDQ0MGMifQ==",
    "nonce": 111460,
    "balances": {
      "current": "285857907782328994543118",
      "previous": "285857907782436633614468"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbdc6294037085cb8ff06db0d5da77a600a305c3d",
    "nonce": 32,
    "balances": {
      "current": "967959172886537175539",
      "previous": "967959172779005635728"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:25.776Z",
  "updated": "2022-05-04T08:58:25.871Z",
  "id": "627240317832e20011830d0b"
}
```
* *stageAmount*: `967959172886537175539`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000019096115630000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001909611563000000000000000000000000000000000000000000000000000002484db165b34c0685dfffc929f65f1bad6b80f81e8cce41a1acf7dbbb5407302430b71d71994a17d3e33afc46e8cd732484fbef8d5e4a1db30341ec6e587ff1d077a0f73969081d2173187644237fd4087ea9c90b7d15c81c21d1140e1634b193e69a0787e9000000000000000000000000000000000000000000000000000000000000001b6d152aee9b5b2d8b31c32cff6f1520606340a0171cda8b132af845cb9c033830d2289b5ba270fb75b245c5586e2e6359ded0cbfeb21c0192ab6039ce38b7ae9c3c6d3c1d9b8570a87020b50f8e7a014c59dbc33593199cd9caef44ee184ba09e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b364000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c8863632bec2afcb60e000000000000000000000000000000000000000000003c8863632c053ac6988400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000668cd130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce6e1556cc879a9d50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f4455784f4459315a6930794e5441324c545532593251744f544534595330785a4467354f44566a5a4451304d474d6966513d3d0000000000000000000000000000000000000000000000000000000000000020000000000000000000000000bdc6294037085cb8ff06db0d5da77a600a305c3d0000000000000000000000000000000000000000000000347921cb45d6f801f30000000000000000000000000000000000000000000000347921cb2ccd96ec9000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4c0685dfffc929f65f1bad6b80f81e8cce41a1acf7dbbb5407302430b71d7199",
      "signature": {
        "s": "0x081d2173187644237fd4087ea9c90b7d15c81c21d1140e1634b193e69a0787e9",
        "r": "0x4a17d3e33afc46e8cd732484fbef8d5e4a1db30341ec6e587ff1d077a0f73969",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6d152aee9b5b2d8b31c32cff6f1520606340a0171cda8b132af845cb9c033830",
      "signature": {
        "s": "0x3c6d3c1d9b8570a87020b50f8e7a014c59dbc33593199cd9caef44ee184ba09e",
        "r": "0xd2289b5ba270fb75b245c5586e2e6359ded0cbfeb21c0192ab6039ce38b7ae9c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "107531539811",
    "total": "2509564372403"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "107531539811",
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
            "amount": "27686752782988518992341"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "107531539"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ODUxODY1Zi0yNTA2LTU2Y2QtOTE4YS0xZDg5ODVjZDQ0MGMifQ==",
    "nonce": 111460,
    "balances": {
      "current": "285857907782328994543118",
      "previous": "285857907782436633614468"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbdc6294037085cb8ff06db0d5da77a600a305c3d",
    "nonce": 32,
    "balances": {
      "current": "967959172886537175539",
      "previous": "967959172779005635728"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:25.776Z",
  "updated": "2022-05-04T08:58:25.871Z",
  "id": "627240317832e20011830d0b"
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
0x0f200f9b0000000000000000000000000000000000000000000000347921cb45d6f801f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `967959172886537175539`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`