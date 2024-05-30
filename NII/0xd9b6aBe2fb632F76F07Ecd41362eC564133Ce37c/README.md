# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd9b6aBe2fb632F76F07Ecd41362eC564133Ce37c`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000168f755bc7a3e0900000000000000000000000000000000000000000000000000088edf97c94ae00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000088edf97c94ae000000000000000000000000000000000000000000000000000f02609bd8b79b2a9b543fb37df875cc8fda5c3cfbb4a3d41707e715215a2d6dc6d9d80188aea5f7616fa88d448b3045ce633a18eafac41b40b4040845ae326bcd90764d721c9e95f8bdb2fca4dfc11db4a193d92258990dd428cf1a9a98a140f366e0c004759ca000000000000000000000000000000000000000000000000000000000000001b38234b15f09a94ec4f1b6cce7bd9b222431f6889f8ae4db67bbbf7be679734e28ed3cd20dd0fa4678ba722dc98fb48eb2c0acad36e8a77db7b98834c8ef8023d0c2990cbb8a4408ca9e964590c1fbcd2440a5c25d39fc94588e09f4e76e7a376000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad02000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000097244844a99a71e25963000000000000000000000000000000000000000000009724484d3aaae6c0112200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000230dd146cdf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5baa9de1f5fce19250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a497a5a444e6d4e43316c4f446c6c4c5455354d4463744f575135596931694f446c6a4f446730597a646a5a6a416966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d9b6abe2fb632f76f07ecd41362ec564133ce37c0000000000000000000000000000000000000000000000000168f755bc7a3e090000000000000000000000000000000000000000000000000160687624b0f32900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa9b543fb37df875cc8fda5c3cfbb4a3d41707e715215a2d6dc6d9d80188aea5f",
      "signature": {
        "s": "0x5f8bdb2fca4dfc11db4a193d92258990dd428cf1a9a98a140f366e0c004759ca",
        "r": "0x7616fa88d448b3045ce633a18eafac41b40b4040845ae326bcd90764d721c9e9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x38234b15f09a94ec4f1b6cce7bd9b222431f6889f8ae4db67bbbf7be679734e2",
      "signature": {
        "s": "0x0c2990cbb8a4408ca9e964590c1fbcd2440a5c25d39fc94588e09f4e76e7a376",
        "r": "0x8ed3cd20dd0fa4678ba722dc98fb48eb2c0acad36e8a77db7b98834c8ef8023d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2408890789087968",
    "total": "67595817687153074"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2408890789087968",
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
            "amount": "27259291522857459128613"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2408890789087"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YzIzZDNmNC1lODllLTU5MDctOWQ5Yi1iODljODg0YzdjZjAifQ==",
    "nonce": 109826,
    "balances": {
      "current": "713746629173519918979427",
      "previous": "713746631584819598856482"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd9b6abe2fb632f76f07ecd41362ec564133ce37c",
    "nonce": 46,
    "balances": {
      "current": "101602939222244873",
      "previous": "99194048433156905"
    }
  },
  "blockNumber": "14709950",
  "created": "2022-05-04T08:50:07.670Z",
  "updated": "2022-05-04T08:50:07.775Z",
  "id": "62723e3f7832e20011830af0"
}
```
* *stageAmount*: `101602939222244873`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000088edf97c94ae00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000088edf97c94ae000000000000000000000000000000000000000000000000000f02609bd8b79b2a9b543fb37df875cc8fda5c3cfbb4a3d41707e715215a2d6dc6d9d80188aea5f7616fa88d448b3045ce633a18eafac41b40b4040845ae326bcd90764d721c9e95f8bdb2fca4dfc11db4a193d92258990dd428cf1a9a98a140f366e0c004759ca000000000000000000000000000000000000000000000000000000000000001b38234b15f09a94ec4f1b6cce7bd9b222431f6889f8ae4db67bbbf7be679734e28ed3cd20dd0fa4678ba722dc98fb48eb2c0acad36e8a77db7b98834c8ef8023d0c2990cbb8a4408ca9e964590c1fbcd2440a5c25d39fc94588e09f4e76e7a376000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad02000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000097244844a99a71e25963000000000000000000000000000000000000000000009724484d3aaae6c0112200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000230dd146cdf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5baa9de1f5fce19250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a497a5a444e6d4e43316c4f446c6c4c5455354d4463744f575135596931694f446c6a4f446730597a646a5a6a416966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d9b6abe2fb632f76f07ecd41362ec564133ce37c0000000000000000000000000000000000000000000000000168f755bc7a3e090000000000000000000000000000000000000000000000000160687624b0f32900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa9b543fb37df875cc8fda5c3cfbb4a3d41707e715215a2d6dc6d9d80188aea5f",
      "signature": {
        "s": "0x5f8bdb2fca4dfc11db4a193d92258990dd428cf1a9a98a140f366e0c004759ca",
        "r": "0x7616fa88d448b3045ce633a18eafac41b40b4040845ae326bcd90764d721c9e9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x38234b15f09a94ec4f1b6cce7bd9b222431f6889f8ae4db67bbbf7be679734e2",
      "signature": {
        "s": "0x0c2990cbb8a4408ca9e964590c1fbcd2440a5c25d39fc94588e09f4e76e7a376",
        "r": "0x8ed3cd20dd0fa4678ba722dc98fb48eb2c0acad36e8a77db7b98834c8ef8023d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2408890789087968",
    "total": "67595817687153074"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2408890789087968",
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
            "amount": "27259291522857459128613"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2408890789087"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YzIzZDNmNC1lODllLTU5MDctOWQ5Yi1iODljODg0YzdjZjAifQ==",
    "nonce": 109826,
    "balances": {
      "current": "713746629173519918979427",
      "previous": "713746631584819598856482"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd9b6abe2fb632f76f07ecd41362ec564133ce37c",
    "nonce": 46,
    "balances": {
      "current": "101602939222244873",
      "previous": "99194048433156905"
    }
  },
  "blockNumber": "14709950",
  "created": "2022-05-04T08:50:07.670Z",
  "updated": "2022-05-04T08:50:07.775Z",
  "id": "62723e3f7832e20011830af0"
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
0x0f200f9b0000000000000000000000000000000000000000000000000168f755bc7a3e090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `101602939222244873`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`