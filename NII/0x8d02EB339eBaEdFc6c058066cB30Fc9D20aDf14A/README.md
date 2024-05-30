# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8d02EB339eBaEdFc6c058066cB30Fc9D20aDf14A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000005e2167d3c95ab120000000000000000000000000000000000000000000000000023b527de1731a00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000023b527de1731a000000000000000000000000000000000000000000000000003e9fdb7bd1b051122647d443c486da4dd38fbbe0afab959b926fbe96ca8e8c81d3f4321addd7d7f507ca681fa73e1e2984175f2c468552e76020222a80efb884e7d93962ae61aad3a2492ebc04799577ff5741ba0e01e1758199b16bc3bac4d7894f66e9eb6ad2d000000000000000000000000000000000000000000000000000000000000001c0bffac623e784936a5c840165667ff4d4983d3f09791917f7c46e712645039d88e2e4e57e3beefe09a6184b6e595578fe17ba045dae987a7aaf8a5f2266c92665f57ec214fe0cf3772fbb3bd50cad304e40b3fc4937a6c2b754a219157acebd5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac11000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009aaa17dc086e44b7d4f0000000000000000000000000000000000000000000009aaa17ffc6ba45973da600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000092422c837160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d407d490b68c29190000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a4749355a446b304e7930324d44426b4c5455784d4751744f474d31596930325a4455324e4445325a6a4d304f47456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008d02eb339ebaedfc6c058066cb30fc9d20adf14a00000000000000000000000000000000000000000000000005e2167d3c95ab1200000000000000000000000000000000000000000000000005be61555e7e797200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x22647d443c486da4dd38fbbe0afab959b926fbe96ca8e8c81d3f4321addd7d7f",
      "signature": {
        "s": "0x3a2492ebc04799577ff5741ba0e01e1758199b16bc3bac4d7894f66e9eb6ad2d",
        "r": "0x507ca681fa73e1e2984175f2c468552e76020222a80efb884e7d93962ae61aad",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0bffac623e784936a5c840165667ff4d4983d3f09791917f7c46e712645039d8",
      "signature": {
        "s": "0x5f57ec214fe0cf3772fbb3bd50cad304e40b3fc4937a6c2b754a219157acebd5",
        "r": "0x8e2e4e57e3beefe09a6184b6e595578fe17ba045dae987a7aaf8a5f2266c9266",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10050807019286944",
    "total": "282035417280873745"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10050807019286944",
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
            "amount": "27242672666774178900249"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10050807019286"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZGI5ZDk0Ny02MDBkLTUxMGQtOGM1Yi02ZDU2NDE2ZjM0OGEifQ==",
    "nonce": 109585,
    "balances": {
      "current": "730382104112883427693808",
      "previous": "730382114173741254000038"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8d02eb339ebaedfc6c058066cb30fc9d20adf14a",
    "nonce": 46,
    "balances": {
      "current": "423926042069412626",
      "previous": "413875235050125682"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:50.976Z",
  "updated": "2022-05-04T08:48:51.066Z",
  "id": "62723df27832e20011830a9b"
}
```
* *stageAmount*: `423926042069412626`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000023b527de1731a00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000023b527de1731a000000000000000000000000000000000000000000000000003e9fdb7bd1b051122647d443c486da4dd38fbbe0afab959b926fbe96ca8e8c81d3f4321addd7d7f507ca681fa73e1e2984175f2c468552e76020222a80efb884e7d93962ae61aad3a2492ebc04799577ff5741ba0e01e1758199b16bc3bac4d7894f66e9eb6ad2d000000000000000000000000000000000000000000000000000000000000001c0bffac623e784936a5c840165667ff4d4983d3f09791917f7c46e712645039d88e2e4e57e3beefe09a6184b6e595578fe17ba045dae987a7aaf8a5f2266c92665f57ec214fe0cf3772fbb3bd50cad304e40b3fc4937a6c2b754a219157acebd5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac11000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009aaa17dc086e44b7d4f0000000000000000000000000000000000000000000009aaa17ffc6ba45973da600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000092422c837160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d407d490b68c29190000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a4749355a446b304e7930324d44426b4c5455784d4751744f474d31596930325a4455324e4445325a6a4d304f47456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008d02eb339ebaedfc6c058066cb30fc9d20adf14a00000000000000000000000000000000000000000000000005e2167d3c95ab1200000000000000000000000000000000000000000000000005be61555e7e797200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x22647d443c486da4dd38fbbe0afab959b926fbe96ca8e8c81d3f4321addd7d7f",
      "signature": {
        "s": "0x3a2492ebc04799577ff5741ba0e01e1758199b16bc3bac4d7894f66e9eb6ad2d",
        "r": "0x507ca681fa73e1e2984175f2c468552e76020222a80efb884e7d93962ae61aad",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0bffac623e784936a5c840165667ff4d4983d3f09791917f7c46e712645039d8",
      "signature": {
        "s": "0x5f57ec214fe0cf3772fbb3bd50cad304e40b3fc4937a6c2b754a219157acebd5",
        "r": "0x8e2e4e57e3beefe09a6184b6e595578fe17ba045dae987a7aaf8a5f2266c9266",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10050807019286944",
    "total": "282035417280873745"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10050807019286944",
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
            "amount": "27242672666774178900249"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10050807019286"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZGI5ZDk0Ny02MDBkLTUxMGQtOGM1Yi02ZDU2NDE2ZjM0OGEifQ==",
    "nonce": 109585,
    "balances": {
      "current": "730382104112883427693808",
      "previous": "730382114173741254000038"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8d02eb339ebaedfc6c058066cb30fc9d20adf14a",
    "nonce": 46,
    "balances": {
      "current": "423926042069412626",
      "previous": "413875235050125682"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:50.976Z",
  "updated": "2022-05-04T08:48:51.066Z",
  "id": "62723df27832e20011830a9b"
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
0x0f200f9b00000000000000000000000000000000000000000000000005e2167d3c95ab120000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `423926042069412626`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`