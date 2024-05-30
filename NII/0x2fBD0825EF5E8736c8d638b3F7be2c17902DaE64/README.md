# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2fBD0825EF5E8736c8d638b3F7be2c17902DaE64`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de7bd0027e8132a000000000000000000000000000000000000000000000000640b834e19ca80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000640b834e19ca8000000000000000000000000000000000000000000000000000640b834e19ca8000a17125c55f9912e18abb99dd095e66c4cc5af7e2d11be10791f35baf54521622ad070b53502fdfe6e8b9b30362bc9b40c96bef79902d20bea67c8390d84c298a627d3ad0a17b794b25479ecdd706bc67956b0e6d40430de6876e6c588e871b21000000000000000000000000000000000000000000000000000000000000001bc31e5f65f699937ed6b196f89144e7f707b999defaa000c651236ca047e5f100be327f683462f91447281b332284a00cf5e4ad61710a4c042ccafa55a95f83ac5d3f7c713c56c4d0dcf307d2b6572870708a635751f5e9691ebbdcafa1320038000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1be64000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000240000000000000000000000002fbd0825ef5e8736c8d638b3f7be2c17902dae640000000000000000000000000000000000000000000000000de7bd0027e8132a000000000000000000000000000000000000000000000000720cdcda5de2232a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000199c8c1c2f90000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000199c8c1c2f90000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d5745354d4749325a533169596a4d314c545179596a41744f4463784e79316b5a445a68596d526d4f5441345a54676966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000009c90562b8283623b2636630ae7cc6b61d68b49ff0000000000000000000000000000000000000000000007694540d4303e5c0aee000000000000000000000000000000000000000000000768e13550e224918aee00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa17125c55f9912e18abb99dd095e66c4cc5af7e2d11be10791f35baf54521622",
      "signature": {
        "s": "0x627d3ad0a17b794b25479ecdd706bc67956b0e6d40430de6876e6c588e871b21",
        "r": "0xad070b53502fdfe6e8b9b30362bc9b40c96bef79902d20bea67c8390d84c298a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc31e5f65f699937ed6b196f89144e7f707b999defaa000c651236ca047e5f100",
      "signature": {
        "s": "0x5d3f7c713c56c4d0dcf307d2b6572870708a635751f5e9691ebbdcafa1320038",
        "r": "0xbe327f683462f91447281b332284a00cf5e4ad61710a4c042ccafa55a95f83ac",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7209000000000000000",
    "total": "7209000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7209000000000000000",
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
            "amount": "7209000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7209000000000000"
      }
    },
    "wallet": "0x2fbd0825ef5e8736c8d638b3f7be2c17902dae64",
    "data": "eyJyZWYiOiJiMWE5MGI2ZS1iYjM1LTQyYjAtODcxNy1kZDZhYmRmOTA4ZTgifQ==",
    "nonce": 36,
    "balances": {
      "current": "1001977250480395050",
      "previous": "8218186250480395050"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c90562b8283623b2636630ae7cc6b61d68b49ff",
    "nonce": 6,
    "balances": {
      "current": "34998463729517815663342",
      "previous": "34991254729517815663342"
    }
  },
  "blockNumber": "14794340",
  "created": "2022-05-17T19:20:37.382Z",
  "updated": "2022-05-17T19:20:37.473Z",
  "id": "6283f5853592fd001130b822"
}
```
* *stageAmount*: `1001977250480395050`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000640b834e19ca80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000640b834e19ca8000000000000000000000000000000000000000000000000000640b834e19ca8000a17125c55f9912e18abb99dd095e66c4cc5af7e2d11be10791f35baf54521622ad070b53502fdfe6e8b9b30362bc9b40c96bef79902d20bea67c8390d84c298a627d3ad0a17b794b25479ecdd706bc67956b0e6d40430de6876e6c588e871b21000000000000000000000000000000000000000000000000000000000000001bc31e5f65f699937ed6b196f89144e7f707b999defaa000c651236ca047e5f100be327f683462f91447281b332284a00cf5e4ad61710a4c042ccafa55a95f83ac5d3f7c713c56c4d0dcf307d2b6572870708a635751f5e9691ebbdcafa1320038000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1be64000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000240000000000000000000000002fbd0825ef5e8736c8d638b3f7be2c17902dae640000000000000000000000000000000000000000000000000de7bd0027e8132a000000000000000000000000000000000000000000000000720cdcda5de2232a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000199c8c1c2f90000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000199c8c1c2f90000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d5745354d4749325a533169596a4d314c545179596a41744f4463784e79316b5a445a68596d526d4f5441345a54676966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000009c90562b8283623b2636630ae7cc6b61d68b49ff0000000000000000000000000000000000000000000007694540d4303e5c0aee000000000000000000000000000000000000000000000768e13550e224918aee00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa17125c55f9912e18abb99dd095e66c4cc5af7e2d11be10791f35baf54521622",
      "signature": {
        "s": "0x627d3ad0a17b794b25479ecdd706bc67956b0e6d40430de6876e6c588e871b21",
        "r": "0xad070b53502fdfe6e8b9b30362bc9b40c96bef79902d20bea67c8390d84c298a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc31e5f65f699937ed6b196f89144e7f707b999defaa000c651236ca047e5f100",
      "signature": {
        "s": "0x5d3f7c713c56c4d0dcf307d2b6572870708a635751f5e9691ebbdcafa1320038",
        "r": "0xbe327f683462f91447281b332284a00cf5e4ad61710a4c042ccafa55a95f83ac",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7209000000000000000",
    "total": "7209000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7209000000000000000",
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
            "amount": "7209000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7209000000000000"
      }
    },
    "wallet": "0x2fbd0825ef5e8736c8d638b3f7be2c17902dae64",
    "data": "eyJyZWYiOiJiMWE5MGI2ZS1iYjM1LTQyYjAtODcxNy1kZDZhYmRmOTA4ZTgifQ==",
    "nonce": 36,
    "balances": {
      "current": "1001977250480395050",
      "previous": "8218186250480395050"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c90562b8283623b2636630ae7cc6b61d68b49ff",
    "nonce": 6,
    "balances": {
      "current": "34998463729517815663342",
      "previous": "34991254729517815663342"
    }
  },
  "blockNumber": "14794340",
  "created": "2022-05-17T19:20:37.382Z",
  "updated": "2022-05-17T19:20:37.473Z",
  "id": "6283f5853592fd001130b822"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de7bd0027e8132a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1001977250480395050`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`