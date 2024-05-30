# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdBd8494b2CEb4297924270d3366618Fe4d3dEa42`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000a8db3d3e8d95f5d5700000000000000000000000000000000000000000000000000000002d25b2a770000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002d25b2a770000000000000000000000000000000000000000000000038a936db01d542080c5db73195b23a09c228bef4f4a332601b8d68f7fdf5c9091d84a639ffc16f93391ecaf258a57b8978320ef0f8da331532c71f060e9c97c52013f5e961a659a206db6974876dad16e8ceabf9c0282bf1010cec1e0113b3adf74d92b50a63e328f000000000000000000000000000000000000000000000000000000000000001c6038f9dfa4a298e57d51a0a56a7b057b4dfd28a4426c1fa1b017a3282783b8da9f2072d04e966e35cd4ac287572f7647ed6a694fbf97311ce9e986e6f1e221fb5254b8c54d670178135658ef8d0f79a4a3db72e70e3913fc13f247ceba4fb630000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adfc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000963fe748e1debee4422c00000000000000000000000000000000000000000000963fe748e1e191f858f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000b8ec540000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f511f38c8240ec6f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d6a4d324e4445334f5331684d4468684c545530596a5974596a45355a693168593256684e574a684e444a6b5a47556966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000dbd8494b2ceb4297924270d3366618fe4d3dea4200000000000000000000000000000000000000000000000a8db3d3e8d95f5d5700000000000000000000000000000000000000000000000a8db3d3e6070432e000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc5db73195b23a09c228bef4f4a332601b8d68f7fdf5c9091d84a639ffc16f933",
      "signature": {
        "s": "0x6db6974876dad16e8ceabf9c0282bf1010cec1e0113b3adf74d92b50a63e328f",
        "r": "0x91ecaf258a57b8978320ef0f8da331532c71f060e9c97c52013f5e961a659a20",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6038f9dfa4a298e57d51a0a56a7b057b4dfd28a4426c1fa1b017a3282783b8da",
      "signature": {
        "s": "0x5254b8c54d670178135658ef8d0f79a4a3db72e70e3913fc13f247ceba4fb630",
        "r": "0x9f2072d04e966e35cd4ac287572f7647ed6a694fbf97311ce9e986e6f1e221fb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12119124599",
    "total": "65325677623112900736"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12119124599",
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
            "amount": "27263500160267710426223"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12119124"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4MjM2NDE3OS1hMDhhLTU0YjYtYjE5Zi1hY2VhNWJhNDJkZGUifQ==",
    "nonce": 110076,
    "balances": {
      "current": "709533783125858369946156",
      "previous": "709533783125870501189879"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdbd8494b2ceb4297924270d3366618fe4d3dea42",
    "nonce": 46,
    "balances": {
      "current": "194678178514307341655",
      "previous": "194678178502188217056"
    }
  },
  "blockNumber": "14709961",
  "created": "2022-05-04T08:51:25.829Z",
  "updated": "2022-05-04T08:51:25.981Z",
  "id": "62723e8d7832e20011830b3d"
}
```
* *stageAmount*: `194678178514307341655`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000002d25b2a770000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002d25b2a770000000000000000000000000000000000000000000000038a936db01d542080c5db73195b23a09c228bef4f4a332601b8d68f7fdf5c9091d84a639ffc16f93391ecaf258a57b8978320ef0f8da331532c71f060e9c97c52013f5e961a659a206db6974876dad16e8ceabf9c0282bf1010cec1e0113b3adf74d92b50a63e328f000000000000000000000000000000000000000000000000000000000000001c6038f9dfa4a298e57d51a0a56a7b057b4dfd28a4426c1fa1b017a3282783b8da9f2072d04e966e35cd4ac287572f7647ed6a694fbf97311ce9e986e6f1e221fb5254b8c54d670178135658ef8d0f79a4a3db72e70e3913fc13f247ceba4fb630000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adfc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000963fe748e1debee4422c00000000000000000000000000000000000000000000963fe748e1e191f858f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000b8ec540000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f511f38c8240ec6f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d6a4d324e4445334f5331684d4468684c545530596a5974596a45355a693168593256684e574a684e444a6b5a47556966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000dbd8494b2ceb4297924270d3366618fe4d3dea4200000000000000000000000000000000000000000000000a8db3d3e8d95f5d5700000000000000000000000000000000000000000000000a8db3d3e6070432e000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc5db73195b23a09c228bef4f4a332601b8d68f7fdf5c9091d84a639ffc16f933",
      "signature": {
        "s": "0x6db6974876dad16e8ceabf9c0282bf1010cec1e0113b3adf74d92b50a63e328f",
        "r": "0x91ecaf258a57b8978320ef0f8da331532c71f060e9c97c52013f5e961a659a20",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6038f9dfa4a298e57d51a0a56a7b057b4dfd28a4426c1fa1b017a3282783b8da",
      "signature": {
        "s": "0x5254b8c54d670178135658ef8d0f79a4a3db72e70e3913fc13f247ceba4fb630",
        "r": "0x9f2072d04e966e35cd4ac287572f7647ed6a694fbf97311ce9e986e6f1e221fb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12119124599",
    "total": "65325677623112900736"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12119124599",
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
            "amount": "27263500160267710426223"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12119124"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4MjM2NDE3OS1hMDhhLTU0YjYtYjE5Zi1hY2VhNWJhNDJkZGUifQ==",
    "nonce": 110076,
    "balances": {
      "current": "709533783125858369946156",
      "previous": "709533783125870501189879"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdbd8494b2ceb4297924270d3366618fe4d3dea42",
    "nonce": 46,
    "balances": {
      "current": "194678178514307341655",
      "previous": "194678178502188217056"
    }
  },
  "blockNumber": "14709961",
  "created": "2022-05-04T08:51:25.829Z",
  "updated": "2022-05-04T08:51:25.981Z",
  "id": "62723e8d7832e20011830b3d"
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
0x0f200f9b00000000000000000000000000000000000000000000000a8db3d3e8d95f5d570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `194678178514307341655`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`