# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFdeC300375196264D3A235362CD31C8B711A7934`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de0bfa4d3fcac1e00000000000000000000000000000000000000000000000a5907e62a257c60000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000a5907e62a257c600000000000000000000000000000000000000000000000000a5907e62a257c6000ef5819977a7cbdc3042442378499e9fc7e68e9a7edf5367b30774bbc47a4a4a72bd43b870652c07d3332267c44cb0052c1db2a3fd7c99c809328097848de71e9050d4dc272bcb3d1fe1a4a6acd1b37e5cc95a77c9b1110b2229711f9daebabcf000000000000000000000000000000000000000000000000000000000000001c7d96b7334a1e5e221437d8affdf27301e9c78f3f572076593f3e712a8f2151a08c8cc9651fd3bc0835e3c3e42bbdcada588a6e9135fc8107a3f9275683f9737709bb277eca310faafa5f71df347bb5773ef2ad5c03edc5ae74a58dcaa50c1cb8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1e68d0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000fdec300375196264d3a235362cd31c8b711a79340000000000000000000000000000000000000000000000000de0bfa4d3fcac1e00000000000000000000000000000000000000000000000a698eccb1d528881e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000002a626e2dbaf7c000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002a626e2dbaf7c000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e57566c4d6d45304d7930325a446b7a4c5451305a445974595467314f433034597a67324e6a49305a54497a4d44416966513d3d000000000000000000000000000000000000000000000000000000000000003e000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000002900d0f936793baee6280000000000000000000000000000000000000000000028f677f1504f1632862800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xef5819977a7cbdc3042442378499e9fc7e68e9a7edf5367b30774bbc47a4a4a7",
      "signature": {
        "s": "0x050d4dc272bcb3d1fe1a4a6acd1b37e5cc95a77c9b1110b2229711f9daebabcf",
        "r": "0x2bd43b870652c07d3332267c44cb0052c1db2a3fd7c99c809328097848de71e9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7d96b7334a1e5e221437d8affdf27301e9c78f3f572076593f3e712a8f2151a0",
      "signature": {
        "s": "0x09bb277eca310faafa5f71df347bb5773ef2ad5c03edc5ae74a58dcaa50c1cb8",
        "r": "0x8c8cc9651fd3bc0835e3c3e42bbdcada588a6e9135fc8107a3f9275683f97377",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "190882790000000000000",
    "total": "190882790000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "190882790000000000000",
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
            "amount": "190882790000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "190882790000000000"
      }
    },
    "wallet": "0xfdec300375196264d3a235362cd31c8b711a7934",
    "data": "eyJyZWYiOiI0NWVlMmE0My02ZDkzLTQ0ZDYtYTg1OC04Yzg2NjI0ZTIzMDAifQ==",
    "nonce": 13,
    "balances": {
      "current": "1000009831928343582",
      "previous": "192073682621928343582"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 62,
    "balances": {
      "current": "193632083924378863986216",
      "previous": "193441201134378863986216"
    }
  },
  "blockNumber": "14804621",
  "created": "2022-05-19T11:15:51.414Z",
  "updated": "2022-05-19T11:15:51.516Z",
  "id": "628626e77832e20011830f11"
}
```
* *stageAmount*: `1000009831928343582`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000a5907e62a257c60000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000a5907e62a257c600000000000000000000000000000000000000000000000000a5907e62a257c6000ef5819977a7cbdc3042442378499e9fc7e68e9a7edf5367b30774bbc47a4a4a72bd43b870652c07d3332267c44cb0052c1db2a3fd7c99c809328097848de71e9050d4dc272bcb3d1fe1a4a6acd1b37e5cc95a77c9b1110b2229711f9daebabcf000000000000000000000000000000000000000000000000000000000000001c7d96b7334a1e5e221437d8affdf27301e9c78f3f572076593f3e712a8f2151a08c8cc9651fd3bc0835e3c3e42bbdcada588a6e9135fc8107a3f9275683f9737709bb277eca310faafa5f71df347bb5773ef2ad5c03edc5ae74a58dcaa50c1cb8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1e68d0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000fdec300375196264d3a235362cd31c8b711a79340000000000000000000000000000000000000000000000000de0bfa4d3fcac1e00000000000000000000000000000000000000000000000a698eccb1d528881e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000002a626e2dbaf7c000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002a626e2dbaf7c000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e57566c4d6d45304d7930325a446b7a4c5451305a445974595467314f433034597a67324e6a49305a54497a4d44416966513d3d000000000000000000000000000000000000000000000000000000000000003e000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000002900d0f936793baee6280000000000000000000000000000000000000000000028f677f1504f1632862800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xef5819977a7cbdc3042442378499e9fc7e68e9a7edf5367b30774bbc47a4a4a7",
      "signature": {
        "s": "0x050d4dc272bcb3d1fe1a4a6acd1b37e5cc95a77c9b1110b2229711f9daebabcf",
        "r": "0x2bd43b870652c07d3332267c44cb0052c1db2a3fd7c99c809328097848de71e9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7d96b7334a1e5e221437d8affdf27301e9c78f3f572076593f3e712a8f2151a0",
      "signature": {
        "s": "0x09bb277eca310faafa5f71df347bb5773ef2ad5c03edc5ae74a58dcaa50c1cb8",
        "r": "0x8c8cc9651fd3bc0835e3c3e42bbdcada588a6e9135fc8107a3f9275683f97377",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "190882790000000000000",
    "total": "190882790000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "190882790000000000000",
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
            "amount": "190882790000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "190882790000000000"
      }
    },
    "wallet": "0xfdec300375196264d3a235362cd31c8b711a7934",
    "data": "eyJyZWYiOiI0NWVlMmE0My02ZDkzLTQ0ZDYtYTg1OC04Yzg2NjI0ZTIzMDAifQ==",
    "nonce": 13,
    "balances": {
      "current": "1000009831928343582",
      "previous": "192073682621928343582"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 62,
    "balances": {
      "current": "193632083924378863986216",
      "previous": "193441201134378863986216"
    }
  },
  "blockNumber": "14804621",
  "created": "2022-05-19T11:15:51.414Z",
  "updated": "2022-05-19T11:15:51.516Z",
  "id": "628626e77832e20011830f11"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de0bfa4d3fcac1e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000009831928343582`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`