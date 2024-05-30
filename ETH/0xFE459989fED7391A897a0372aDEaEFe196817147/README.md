# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFE459989fED7391A897a0372aDEaEFe196817147`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000000000000000000000000000000000000000000d036d7d225ded5e9905375aea83da4588a3fd085ed886f4dd45f478ba9f5701e358bbb8f86bc486ee1055c39671efecf7b26b9b606e98074fb840a20e8bcdf2fa02140b3c7c57360db9372e6219794390d7b23db19eb6102fa508977668678d91000000000000000000000000000000000000000000000000000000000000001b9622a3238763b87d9bb2e50d8e2deeb9608995382c5edee4b92477f9e9eb6e723e82e4b9a2c03312b29ced7a528f7875655588ffd041119c315b21a043c6f0f92eea034b1213adbef995f72c805f95db91e83fc045be93e14f189930850755da000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000042900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c97cdb2d000000000000000000000000000000000000000000000000002386f2c97cdb3b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d2af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e324e6b4d444178595330795a6a426b4c54566b5a475174596a5a6b596930355a575a6b4e444a694e5442694f54676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000fe459989fed7391a897a0372adeaefe196817147000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x036d7d225ded5e9905375aea83da4588a3fd085ed886f4dd45f478ba9f5701e3",
      "signature": {
        "s": "0x02140b3c7c57360db9372e6219794390d7b23db19eb6102fa508977668678d91",
        "r": "0x58bbb8f86bc486ee1055c39671efecf7b26b9b606e98074fb840a20e8bcdf2fa",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9622a3238763b87d9bb2e50d8e2deeb9608995382c5edee4b92477f9e9eb6e72",
      "signature": {
        "s": "0x2eea034b1213adbef995f72c805f95db91e83fc045be93e14f189930850755da",
        "r": "0x3e82e4b9a2c03312b29ced7a528f7875655588ffd041119c315b21a043c6f0f9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "13",
    "total": "13"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "578223"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4N2NkMDAxYS0yZjBkLTVkZGQtYjZkYi05ZWZkNDJiNTBiOTgifQ==",
    "nonce": 1065,
    "balances": {
      "current": "10000001505483565",
      "previous": "10000001505483579"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe459989fed7391a897a0372adeaefe196817147",
    "nonce": 20,
    "balances": {
      "current": "13",
      "previous": "0"
    }
  },
  "blockNumber": "10114517",
  "created": "2020-05-22T08:06:34.659Z",
  "updated": "2020-05-22T08:06:34.722Z",
  "id": "5ec7880ab0c6090011d5aa2e"
}
```
* *stageAmount*: `13`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000000000000000000000000000000000000000000d036d7d225ded5e9905375aea83da4588a3fd085ed886f4dd45f478ba9f5701e358bbb8f86bc486ee1055c39671efecf7b26b9b606e98074fb840a20e8bcdf2fa02140b3c7c57360db9372e6219794390d7b23db19eb6102fa508977668678d91000000000000000000000000000000000000000000000000000000000000001b9622a3238763b87d9bb2e50d8e2deeb9608995382c5edee4b92477f9e9eb6e723e82e4b9a2c03312b29ced7a528f7875655588ffd041119c315b21a043c6f0f92eea034b1213adbef995f72c805f95db91e83fc045be93e14f189930850755da000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000042900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c97cdb2d000000000000000000000000000000000000000000000000002386f2c97cdb3b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d2af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e324e6b4d444178595330795a6a426b4c54566b5a475174596a5a6b596930355a575a6b4e444a694e5442694f54676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000fe459989fed7391a897a0372adeaefe196817147000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x036d7d225ded5e9905375aea83da4588a3fd085ed886f4dd45f478ba9f5701e3",
      "signature": {
        "s": "0x02140b3c7c57360db9372e6219794390d7b23db19eb6102fa508977668678d91",
        "r": "0x58bbb8f86bc486ee1055c39671efecf7b26b9b606e98074fb840a20e8bcdf2fa",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9622a3238763b87d9bb2e50d8e2deeb9608995382c5edee4b92477f9e9eb6e72",
      "signature": {
        "s": "0x2eea034b1213adbef995f72c805f95db91e83fc045be93e14f189930850755da",
        "r": "0x3e82e4b9a2c03312b29ced7a528f7875655588ffd041119c315b21a043c6f0f9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "13",
    "total": "13"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "578223"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4N2NkMDAxYS0yZjBkLTVkZGQtYjZkYi05ZWZkNDJiNTBiOTgifQ==",
    "nonce": 1065,
    "balances": {
      "current": "10000001505483565",
      "previous": "10000001505483579"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe459989fed7391a897a0372adeaefe196817147",
    "nonce": 20,
    "balances": {
      "current": "13",
      "previous": "0"
    }
  },
  "blockNumber": "10114517",
  "created": "2020-05-22T08:06:34.659Z",
  "updated": "2020-05-22T08:06:34.722Z",
  "id": "5ec7880ab0c6090011d5aa2e"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``