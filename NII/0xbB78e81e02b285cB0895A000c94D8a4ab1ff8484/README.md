# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbB78e81e02b285cB0895A000c94D8a4ab1ff8484`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000003bdbb14c83347784820000000000000000000000000000000000000000000000016b4eb3346ad85fc40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000016b4eb3346ad85fc4000000000000000000000000000000000000000000000027d2c26ea45da765d2e594b8781827ac093322fa37e1408ed8ba72e5d43948eafb8180caaf7f6ba975f048a95887f76d35b9eb2f66f76923f4464abd51b89678ba6ac0fcf6cbf4cd527b216ef8f776d95d29d4962897780f9c4ece838d7fab2ab15a666d022f839203000000000000000000000000000000000000000000000000000000000000001c25b89086db5309dc1735be8fcf01e9846a2cfdbf166158065ee88cb64ed07d816a21ed960b50dbb5ef1cc45820de93f12b5787d9a3000d9f897116fa81764da651df5f8c7ca46911fc3a54935162f62a7a41e9e4843783c97e7a325203b4a174000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad31000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096d836650652d61ddfc50000000000000000000000000000000000000000000096d9a210bb3e589ee99d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000005d01b717a8aa140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ce1e32efe0999c5d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a5a6c4d444a6c4d4330335a6d4d784c5455344e6a4d74596a6c6859533079596a6c6c597a49345a6a63324f47516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000bb78e81e02b285cb0895a000c94d8a4ab1ff848400000000000000000000000000000000000000000000003bdbb14c833477848200000000000000000000000000000000000000000000003a7062994ec99f24be00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe594b8781827ac093322fa37e1408ed8ba72e5d43948eafb8180caaf7f6ba975",
      "signature": {
        "s": "0x7b216ef8f776d95d29d4962897780f9c4ece838d7fab2ab15a666d022f839203",
        "r": "0xf048a95887f76d35b9eb2f66f76923f4464abd51b89678ba6ac0fcf6cbf4cd52",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x25b89086db5309dc1735be8fcf01e9846a2cfdbf166158065ee88cb64ed07d81",
      "signature": {
        "s": "0x51df5f8c7ca46911fc3a54935162f62a7a41e9e4843783c97e7a325203b4a174",
        "r": "0x6a21ed960b50dbb5ef1cc45820de93f12b5787d9a3000d9f897116fa81764da6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "26179058721663508420",
    "total": "734609841420344190418"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26179058721663508420",
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
            "amount": "27260693361495968947293"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "26179058721663508"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNzZlMDJlMC03ZmMxLTU4NjMtYjlhYS0yYjllYzI4Zjc2OGQifQ==",
    "nonce": 109873,
    "balances": {
      "current": "712343388696371590455237",
      "previous": "712369593934151975627165"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbb78e81e02b285cb0895a000c94d8a4ab1ff8484",
    "nonce": 46,
    "balances": {
      "current": "1104188418640452224130",
      "previous": "1078009359918788715710"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:23.029Z",
  "updated": "2022-05-04T08:50:23.131Z",
  "id": "62723e4f3592fd001130b41e"
}
```
* *stageAmount*: `1104188418640452224130`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000016b4eb3346ad85fc40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000016b4eb3346ad85fc4000000000000000000000000000000000000000000000027d2c26ea45da765d2e594b8781827ac093322fa37e1408ed8ba72e5d43948eafb8180caaf7f6ba975f048a95887f76d35b9eb2f66f76923f4464abd51b89678ba6ac0fcf6cbf4cd527b216ef8f776d95d29d4962897780f9c4ece838d7fab2ab15a666d022f839203000000000000000000000000000000000000000000000000000000000000001c25b89086db5309dc1735be8fcf01e9846a2cfdbf166158065ee88cb64ed07d816a21ed960b50dbb5ef1cc45820de93f12b5787d9a3000d9f897116fa81764da651df5f8c7ca46911fc3a54935162f62a7a41e9e4843783c97e7a325203b4a174000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad31000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096d836650652d61ddfc50000000000000000000000000000000000000000000096d9a210bb3e589ee99d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000005d01b717a8aa140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ce1e32efe0999c5d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a5a6c4d444a6c4d4330335a6d4d784c5455344e6a4d74596a6c6859533079596a6c6c597a49345a6a63324f47516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000bb78e81e02b285cb0895a000c94d8a4ab1ff848400000000000000000000000000000000000000000000003bdbb14c833477848200000000000000000000000000000000000000000000003a7062994ec99f24be00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe594b8781827ac093322fa37e1408ed8ba72e5d43948eafb8180caaf7f6ba975",
      "signature": {
        "s": "0x7b216ef8f776d95d29d4962897780f9c4ece838d7fab2ab15a666d022f839203",
        "r": "0xf048a95887f76d35b9eb2f66f76923f4464abd51b89678ba6ac0fcf6cbf4cd52",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x25b89086db5309dc1735be8fcf01e9846a2cfdbf166158065ee88cb64ed07d81",
      "signature": {
        "s": "0x51df5f8c7ca46911fc3a54935162f62a7a41e9e4843783c97e7a325203b4a174",
        "r": "0x6a21ed960b50dbb5ef1cc45820de93f12b5787d9a3000d9f897116fa81764da6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "26179058721663508420",
    "total": "734609841420344190418"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26179058721663508420",
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
            "amount": "27260693361495968947293"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "26179058721663508"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNzZlMDJlMC03ZmMxLTU4NjMtYjlhYS0yYjllYzI4Zjc2OGQifQ==",
    "nonce": 109873,
    "balances": {
      "current": "712343388696371590455237",
      "previous": "712369593934151975627165"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbb78e81e02b285cb0895a000c94d8a4ab1ff8484",
    "nonce": 46,
    "balances": {
      "current": "1104188418640452224130",
      "previous": "1078009359918788715710"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:23.029Z",
  "updated": "2022-05-04T08:50:23.131Z",
  "id": "62723e4f3592fd001130b41e"
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
0x0f200f9b00000000000000000000000000000000000000000000003bdbb14c83347784820000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1104188418640452224130`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`