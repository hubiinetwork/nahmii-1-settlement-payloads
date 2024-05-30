# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC582d9145866614233B473BdfB9d9B966610d176`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000031a8545b23b00955050000000000000000000000000000000000000000000000000000000a42c48c610000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000a42c48c610000000000000000000000000000000000000000000000182898b5bcfb34cc71bb1754e8925332d0bc2cc9f78a138672ddfadd5380aac0aff130fa0b6e9481011893cbea35bafc9da81f65b0e333733e11927ca0670be7d0d8250766a2804fc044b8791969f7291d52bafed2b8ff4043299aaa7accf4aa1076d20354a75e7251000000000000000000000000000000000000000000000000000000000000001b2854c0233de87820c3f3e4757343a950d5ae083fc8443a9d50eab3822621e3f5cc1ced3624fcf6d8f49f075833443d689eb2d08f075961443508555aab62362f5a37e981ea0d9424cab09195b95ac5b9d0fa6ad9af8abddba60d13f469150f73000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad53000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096aebd99b73ce166205c0000000000000000000000000000000000000000000096aebd99b74726cb209700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002a073da0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5d8b96212ae3507e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d44517a59545a6b4f4330345a5459344c54557a4f4441745957526c5a5331695a57597759575a6b4d47526d4d546b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c582d9145866614233b473bdfb9d9b966610d176000000000000000000000000000000000000000000000031a8545b23b0095505000000000000000000000000000000000000000000000031a8545b196d44c8a400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbb1754e8925332d0bc2cc9f78a138672ddfadd5380aac0aff130fa0b6e948101",
      "signature": {
        "s": "0x44b8791969f7291d52bafed2b8ff4043299aaa7accf4aa1076d20354a75e7251",
        "r": "0x1893cbea35bafc9da81f65b0e333733e11927ca0670be7d0d8250766a2804fc0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2854c0233de87820c3f3e4757343a950d5ae083fc8443a9d50eab3822621e3f5",
      "signature": {
        "s": "0x5a37e981ea0d9424cab09195b95ac5b9d0fa6ad9af8abddba60d13f469150f73",
        "r": "0xcc1ced3624fcf6d8f49f075833443d689eb2d08f075961443508555aab62362f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "44069850209",
    "total": "445647145550279396465"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "44069850209",
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
            "amount": "27261457617884263286758"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "44069850"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMDQzYTZkOC04ZTY4LTUzODAtYWRlZS1iZWYwYWZkMGRmMTkifQ==",
    "nonce": 109907,
    "balances": {
      "current": "711578368051688956633180",
      "previous": "711578368051733070553239"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc582d9145866614233b473bdfb9d9b966610d176",
    "nonce": 46,
    "balances": {
      "current": "916019879517019002117",
      "previous": "916019879472949151908"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:33.049Z",
  "updated": "2022-05-04T08:50:33.116Z",
  "id": "62723e59bbd75600116d04b2"
}
```
* *stageAmount*: `916019879517019002117`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000a42c48c610000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000a42c48c610000000000000000000000000000000000000000000000182898b5bcfb34cc71bb1754e8925332d0bc2cc9f78a138672ddfadd5380aac0aff130fa0b6e9481011893cbea35bafc9da81f65b0e333733e11927ca0670be7d0d8250766a2804fc044b8791969f7291d52bafed2b8ff4043299aaa7accf4aa1076d20354a75e7251000000000000000000000000000000000000000000000000000000000000001b2854c0233de87820c3f3e4757343a950d5ae083fc8443a9d50eab3822621e3f5cc1ced3624fcf6d8f49f075833443d689eb2d08f075961443508555aab62362f5a37e981ea0d9424cab09195b95ac5b9d0fa6ad9af8abddba60d13f469150f73000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad53000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096aebd99b73ce166205c0000000000000000000000000000000000000000000096aebd99b74726cb209700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002a073da0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5d8b96212ae3507e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d44517a59545a6b4f4330345a5459344c54557a4f4441745957526c5a5331695a57597759575a6b4d47526d4d546b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c582d9145866614233b473bdfb9d9b966610d176000000000000000000000000000000000000000000000031a8545b23b0095505000000000000000000000000000000000000000000000031a8545b196d44c8a400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbb1754e8925332d0bc2cc9f78a138672ddfadd5380aac0aff130fa0b6e948101",
      "signature": {
        "s": "0x44b8791969f7291d52bafed2b8ff4043299aaa7accf4aa1076d20354a75e7251",
        "r": "0x1893cbea35bafc9da81f65b0e333733e11927ca0670be7d0d8250766a2804fc0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2854c0233de87820c3f3e4757343a950d5ae083fc8443a9d50eab3822621e3f5",
      "signature": {
        "s": "0x5a37e981ea0d9424cab09195b95ac5b9d0fa6ad9af8abddba60d13f469150f73",
        "r": "0xcc1ced3624fcf6d8f49f075833443d689eb2d08f075961443508555aab62362f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "44069850209",
    "total": "445647145550279396465"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "44069850209",
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
            "amount": "27261457617884263286758"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "44069850"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMDQzYTZkOC04ZTY4LTUzODAtYWRlZS1iZWYwYWZkMGRmMTkifQ==",
    "nonce": 109907,
    "balances": {
      "current": "711578368051688956633180",
      "previous": "711578368051733070553239"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc582d9145866614233b473bdfb9d9b966610d176",
    "nonce": 46,
    "balances": {
      "current": "916019879517019002117",
      "previous": "916019879472949151908"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:33.049Z",
  "updated": "2022-05-04T08:50:33.116Z",
  "id": "62723e59bbd75600116d04b2"
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
0x0f200f9b000000000000000000000000000000000000000000000031a8545b23b00955050000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `916019879517019002117`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`