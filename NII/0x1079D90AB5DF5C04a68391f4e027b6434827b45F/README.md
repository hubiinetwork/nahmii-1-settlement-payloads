# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1079D90AB5DF5C04a68391f4e027b6434827b45F`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000066ec71ebb0592e000000000000000000000000000000000000000000000000000000000013cc5a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000013cc5a0000000000000000000000000000000000000000000000000000000001ce0c963a4438b3e9dbe547bec0a8e4ec1f5554a5146b96ab2b9e8ad176d5f0b05009a5ace1a69ca550d18775bc4708bba085542d309b002e483a62767aff9118ac44f638a1cfb323319858e72179e6b43ab15146cec4e73a8affa8478eef22c8feb177000000000000000000000000000000000000000000000000000000000000001c7540c5c18737fde9e86d820d79d1667f3942d9de839e7dafb8ff53da5c0863f357c8c968ddf1f9b8773bfc3f98f70624976e7439afb432de7d9d085f0d16849122ea22469bbad96f36bf5a276460c422380778c8a9bb35d291f6e1e3f01606b8000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b465000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039af0d021b688fb4e3590000000000000000000000000000000000000000000039af0d021b688fc8b4c400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000005110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dda16770ce5a67934b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d44426b4d5745784d793035595463304c54566c4d6a5174596d526c5a6930324f5459324f4446694e6d55324d54676966513d3d000000000000000000000000000000000000000000000000000000000000001f0000000000000000000000001079d90ab5df5c04a68391f4e027b6434827b45f0000000000000000000000000000000000000000000000000066ec71ebb0592e0000000000000000000000000000000000000000000000000066ec71eb9c8cd400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3a4438b3e9dbe547bec0a8e4ec1f5554a5146b96ab2b9e8ad176d5f0b05009a5",
      "signature": {
        "s": "0x38a1cfb323319858e72179e6b43ab15146cec4e73a8affa8478eef22c8feb177",
        "r": "0xace1a69ca550d18775bc4708bba085542d309b002e483a62767aff9118ac44f6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7540c5c18737fde9e86d820d79d1667f3942d9de839e7dafb8ff53da5c0863f3",
      "signature": {
        "s": "0x22ea22469bbad96f36bf5a276460c422380778c8a9bb35d291f6e1e3f01606b8",
        "r": "0x57c8c968ddf1f9b8773bfc3f98f70624976e7439afb432de7d9d085f0d168491",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1297498",
    "total": "30280854"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1297498",
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
            "amount": "27700193243232326882123"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1297"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1MDBkMWExMy05YTc0LTVlMjQtYmRlZi02OTY2ODFiNmU2MTgifQ==",
    "nonce": 111717,
    "balances": {
      "current": "272404007078277296743257",
      "previous": "272404007078277298042052"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1079d90ab5df5c04a68391f4e027b6434827b45f",
    "nonce": 31,
    "balances": {
      "current": "28970421654149422",
      "previous": "28970421652851924"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:47.402Z",
  "updated": "2022-05-04T08:59:47.512Z",
  "id": "627240833592fd001130b68d"
}
```
* *stageAmount*: `28970421654149422`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000013cc5a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000013cc5a0000000000000000000000000000000000000000000000000000000001ce0c963a4438b3e9dbe547bec0a8e4ec1f5554a5146b96ab2b9e8ad176d5f0b05009a5ace1a69ca550d18775bc4708bba085542d309b002e483a62767aff9118ac44f638a1cfb323319858e72179e6b43ab15146cec4e73a8affa8478eef22c8feb177000000000000000000000000000000000000000000000000000000000000001c7540c5c18737fde9e86d820d79d1667f3942d9de839e7dafb8ff53da5c0863f357c8c968ddf1f9b8773bfc3f98f70624976e7439afb432de7d9d085f0d16849122ea22469bbad96f36bf5a276460c422380778c8a9bb35d291f6e1e3f01606b8000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b465000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039af0d021b688fb4e3590000000000000000000000000000000000000000000039af0d021b688fc8b4c400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000005110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dda16770ce5a67934b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d44426b4d5745784d793035595463304c54566c4d6a5174596d526c5a6930324f5459324f4446694e6d55324d54676966513d3d000000000000000000000000000000000000000000000000000000000000001f0000000000000000000000001079d90ab5df5c04a68391f4e027b6434827b45f0000000000000000000000000000000000000000000000000066ec71ebb0592e0000000000000000000000000000000000000000000000000066ec71eb9c8cd400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3a4438b3e9dbe547bec0a8e4ec1f5554a5146b96ab2b9e8ad176d5f0b05009a5",
      "signature": {
        "s": "0x38a1cfb323319858e72179e6b43ab15146cec4e73a8affa8478eef22c8feb177",
        "r": "0xace1a69ca550d18775bc4708bba085542d309b002e483a62767aff9118ac44f6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7540c5c18737fde9e86d820d79d1667f3942d9de839e7dafb8ff53da5c0863f3",
      "signature": {
        "s": "0x22ea22469bbad96f36bf5a276460c422380778c8a9bb35d291f6e1e3f01606b8",
        "r": "0x57c8c968ddf1f9b8773bfc3f98f70624976e7439afb432de7d9d085f0d168491",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1297498",
    "total": "30280854"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1297498",
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
            "amount": "27700193243232326882123"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1297"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1MDBkMWExMy05YTc0LTVlMjQtYmRlZi02OTY2ODFiNmU2MTgifQ==",
    "nonce": 111717,
    "balances": {
      "current": "272404007078277296743257",
      "previous": "272404007078277298042052"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1079d90ab5df5c04a68391f4e027b6434827b45f",
    "nonce": 31,
    "balances": {
      "current": "28970421654149422",
      "previous": "28970421652851924"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:47.402Z",
  "updated": "2022-05-04T08:59:47.512Z",
  "id": "627240833592fd001130b68d"
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
0x0f200f9b0000000000000000000000000000000000000000000000000066ec71ebb0592e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `28970421654149422`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`