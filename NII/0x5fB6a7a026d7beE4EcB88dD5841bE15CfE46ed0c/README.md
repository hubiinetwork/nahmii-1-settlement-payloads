# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5fB6a7a026d7beE4EcB88dD5841bE15CfE46ed0c`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000006e772d98a86ac4ef5c0000000000000000000000000000000000000000000000029e77a3268d5288820000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000029e77a3268d5288820000000000000000000000000000000000000000000000497df71b4fe94cb407d73623031437fe60a4b20e716481bfe0fa431d47e4bf0bf733f95f8b2dd33b65f00ad27f00385b0a80db896c9ad2486b1351960357fbe3ec7fdfc4c6bfba664c5d3db4b62b9acd15d12638b44c90f2231dfc6de9aa998479cc5b68a442a4ba52000000000000000000000000000000000000000000000000000000000000001c0b8acecff6a80b6a0839dcc48b4ad998b656408ce1ede62703c159725a98819062f3e42f7bead50bc5f4ec73e351ec99976f8e815a013dc9655c8b3972fbe8f11839fbf47b7b19999ad95510d23d03db1207dc2f88a5a9379bb40cf6196cb9c2000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad32000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096d59741bf6d0388713d0000000000000000000000000000000000000000000096d836650652d61ddfc500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000aba3bf4542e6060000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5cec9d6af25dc82630000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6a64694d4759785a53307a5a6d59784c54566b5a475574596a67774f43307a4e6a45355a5749304d6a55325a6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005fb6a7a026d7bee4ecb88dd5841be15cfe46ed0c00000000000000000000000000000000000000000000006e772d98a86ac4ef5c00000000000000000000000000000000000000000000006bd8b5f581dd7266da00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd73623031437fe60a4b20e716481bfe0fa431d47e4bf0bf733f95f8b2dd33b65",
      "signature": {
        "s": "0x5d3db4b62b9acd15d12638b44c90f2231dfc6de9aa998479cc5b68a442a4ba52",
        "r": "0xf00ad27f00385b0a80db896c9ad2486b1351960357fbe3ec7fdfc4c6bfba664c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0b8acecff6a80b6a0839dcc48b4ad998b656408ce1ede62703c159725a988190",
      "signature": {
        "s": "0x1839fbf47b7b19999ad95510d23d03db1207dc2f88a5a9379bb40cf6196cb9c2",
        "r": "0x62f3e42f7bead50bc5f4ec73e351ec99976f8e815a013dc9655c8b3972fbe8f1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "48312262913615366274",
    "total": "1355689070984816276487"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48312262913615366274",
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
            "amount": "27260741673758882562659"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48312262913615366"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2MjdiMGYxZS0zZmYxLTVkZGUtYjgwOC0zNjE5ZWI0MjU2ZjIifQ==",
    "nonce": 109874,
    "balances": {
      "current": "712295028121195061473597",
      "previous": "712343388696371590455237"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5fb6a7a026d7bee4ecb88dd5841be15cfe46ed0c",
    "nonce": 46,
    "balances": {
      "current": "2037729536021629300572",
      "previous": "1989417273108013934298"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:23.438Z",
  "updated": "2022-05-04T08:50:23.520Z",
  "id": "62723e4f7832e20011830b00"
}
```
* *stageAmount*: `2037729536021629300572`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000029e77a3268d5288820000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000029e77a3268d5288820000000000000000000000000000000000000000000000497df71b4fe94cb407d73623031437fe60a4b20e716481bfe0fa431d47e4bf0bf733f95f8b2dd33b65f00ad27f00385b0a80db896c9ad2486b1351960357fbe3ec7fdfc4c6bfba664c5d3db4b62b9acd15d12638b44c90f2231dfc6de9aa998479cc5b68a442a4ba52000000000000000000000000000000000000000000000000000000000000001c0b8acecff6a80b6a0839dcc48b4ad998b656408ce1ede62703c159725a98819062f3e42f7bead50bc5f4ec73e351ec99976f8e815a013dc9655c8b3972fbe8f11839fbf47b7b19999ad95510d23d03db1207dc2f88a5a9379bb40cf6196cb9c2000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad32000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096d59741bf6d0388713d0000000000000000000000000000000000000000000096d836650652d61ddfc500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000aba3bf4542e6060000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5cec9d6af25dc82630000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6a64694d4759785a53307a5a6d59784c54566b5a475574596a67774f43307a4e6a45355a5749304d6a55325a6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005fb6a7a026d7bee4ecb88dd5841be15cfe46ed0c00000000000000000000000000000000000000000000006e772d98a86ac4ef5c00000000000000000000000000000000000000000000006bd8b5f581dd7266da00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd73623031437fe60a4b20e716481bfe0fa431d47e4bf0bf733f95f8b2dd33b65",
      "signature": {
        "s": "0x5d3db4b62b9acd15d12638b44c90f2231dfc6de9aa998479cc5b68a442a4ba52",
        "r": "0xf00ad27f00385b0a80db896c9ad2486b1351960357fbe3ec7fdfc4c6bfba664c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0b8acecff6a80b6a0839dcc48b4ad998b656408ce1ede62703c159725a988190",
      "signature": {
        "s": "0x1839fbf47b7b19999ad95510d23d03db1207dc2f88a5a9379bb40cf6196cb9c2",
        "r": "0x62f3e42f7bead50bc5f4ec73e351ec99976f8e815a013dc9655c8b3972fbe8f1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "48312262913615366274",
    "total": "1355689070984816276487"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48312262913615366274",
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
            "amount": "27260741673758882562659"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48312262913615366"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2MjdiMGYxZS0zZmYxLTVkZGUtYjgwOC0zNjE5ZWI0MjU2ZjIifQ==",
    "nonce": 109874,
    "balances": {
      "current": "712295028121195061473597",
      "previous": "712343388696371590455237"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5fb6a7a026d7bee4ecb88dd5841be15cfe46ed0c",
    "nonce": 46,
    "balances": {
      "current": "2037729536021629300572",
      "previous": "1989417273108013934298"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:23.438Z",
  "updated": "2022-05-04T08:50:23.520Z",
  "id": "62723e4f7832e20011830b00"
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
0x0f200f9b00000000000000000000000000000000000000000000006e772d98a86ac4ef5c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2037729536021629300572`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`