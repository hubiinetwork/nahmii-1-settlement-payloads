# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5433C3F4D872afec05827F3edBB38b1B097296B7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002360db7c7ab33d18ad000000000000000000000000000000000000000000000000e73214f2cf9916470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf99164700000000000000000000000000000000000000000000001957930097236f4c73c2b4add801e468de0c29ed2e87ccf3f0c057f6e8bcab82441d64b6121027fb330917bdea9726579d83f4a60b88cf12675c575042f81ac1a59e574da97d161f7120e05b3378464701c2d786aacd5fb378bf89f7791973b38036ae67e730ead9d2000000000000000000000000000000000000000000000000000000000000001cfe635e432918016d7f8103219a6ea24c87bb75e076f674de159699f971140b390633c9975d24d112096e7812989617d62998d599267794f1ca68f6b6c7734306609a31b74a34808b40b1af274f070b5037a5da7ad3294a9d74a1e5a3ed2ea52b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d000000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001af85000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000054098915781753d0094300000000000000000000000000000000000000000000540a7082bcad32775b3500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3bab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d6e4078467e17f57990000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f54597959324d774f5330334d545a6b4c5455304d6a55744f5759344d6931684d444d794e546b774d7a45324f47596966513d3d000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000005433c3f4d872afec05827f3edbb38b1b097296b700000000000000000000000000000000000000000000002360db7c7ab33d18ad00000000000000000000000000000000000000000000002279a96787e3a4026600000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b1a2bc2ec500000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc2b4add801e468de0c29ed2e87ccf3f0c057f6e8bcab82441d64b6121027fb33",
      "signature": {
        "s": "0x20e05b3378464701c2d786aacd5fb378bf89f7791973b38036ae67e730ead9d2",
        "r": "0x0917bdea9726579d83f4a60b88cf12675c575042f81ac1a59e574da97d161f71",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfe635e432918016d7f8103219a6ea24c87bb75e076f674de159699f971140b39",
      "signature": {
        "s": "0x609a31b74a34808b40b1af274f070b5037a5da7ad3294a9d74a1e5a3ed2ea52b",
        "r": "0x0633c9975d24d112096e7812989617d62998d599267794f1ca68f6b6c7734306",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16659401004694443591",
    "total": "467478989994749545587"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694443591",
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
            "amount": "27575866893469254375321"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694443"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxOTYyY2MwOS03MTZkLTU0MjUtOWY4Mi1hMDMyNTkwMzE2OGYifQ==",
    "nonce": 110469,
    "balances": {
      "current": "396854683191112876689731",
      "previous": "396871359251518575827765"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "50000000000000000"
          }
        }
      ]
    },
    "wallet": "0x5433c3f4d872afec05827f3edbb38b1b097296b7",
    "nonce": 47,
    "balances": {
      "current": "652615351493810002093",
      "previous": "635955950489115558502"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:26.872Z",
  "updated": "2022-05-04T08:53:26.942Z",
  "id": "62723f063592fd001130b4e3"
}
```
* *stageAmount*: `652615351493810002093`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000680000000000000000000000000000000000000000000000000e73214f2cf9916470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf99164700000000000000000000000000000000000000000000001957930097236f4c73c2b4add801e468de0c29ed2e87ccf3f0c057f6e8bcab82441d64b6121027fb330917bdea9726579d83f4a60b88cf12675c575042f81ac1a59e574da97d161f7120e05b3378464701c2d786aacd5fb378bf89f7791973b38036ae67e730ead9d2000000000000000000000000000000000000000000000000000000000000001cfe635e432918016d7f8103219a6ea24c87bb75e076f674de159699f971140b390633c9975d24d112096e7812989617d62998d599267794f1ca68f6b6c7734306609a31b74a34808b40b1af274f070b5037a5da7ad3294a9d74a1e5a3ed2ea52b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d000000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001af85000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000054098915781753d0094300000000000000000000000000000000000000000000540a7082bcad32775b3500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3bab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d6e4078467e17f57990000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f54597959324d774f5330334d545a6b4c5455304d6a55744f5759344d6931684d444d794e546b774d7a45324f47596966513d3d000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000005433c3f4d872afec05827f3edbb38b1b097296b700000000000000000000000000000000000000000000002360db7c7ab33d18ad00000000000000000000000000000000000000000000002279a96787e3a4026600000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b1a2bc2ec500000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc2b4add801e468de0c29ed2e87ccf3f0c057f6e8bcab82441d64b6121027fb33",
      "signature": {
        "s": "0x20e05b3378464701c2d786aacd5fb378bf89f7791973b38036ae67e730ead9d2",
        "r": "0x0917bdea9726579d83f4a60b88cf12675c575042f81ac1a59e574da97d161f71",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfe635e432918016d7f8103219a6ea24c87bb75e076f674de159699f971140b39",
      "signature": {
        "s": "0x609a31b74a34808b40b1af274f070b5037a5da7ad3294a9d74a1e5a3ed2ea52b",
        "r": "0x0633c9975d24d112096e7812989617d62998d599267794f1ca68f6b6c7734306",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16659401004694443591",
    "total": "467478989994749545587"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694443591",
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
            "amount": "27575866893469254375321"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694443"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxOTYyY2MwOS03MTZkLTU0MjUtOWY4Mi1hMDMyNTkwMzE2OGYifQ==",
    "nonce": 110469,
    "balances": {
      "current": "396854683191112876689731",
      "previous": "396871359251518575827765"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "50000000000000000"
          }
        }
      ]
    },
    "wallet": "0x5433c3f4d872afec05827f3edbb38b1b097296b7",
    "nonce": 47,
    "balances": {
      "current": "652615351493810002093",
      "previous": "635955950489115558502"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:26.872Z",
  "updated": "2022-05-04T08:53:26.942Z",
  "id": "62723f063592fd001130b4e3"
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
0x0f200f9b00000000000000000000000000000000000000000000002360db7c7ab33d18ad0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `652615351493810002093`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`