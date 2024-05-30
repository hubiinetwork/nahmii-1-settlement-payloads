# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xDC85BDE63eEc1f3317B86f1589D681170a6a01BE`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de25eab380d1aab000000000000000000000000000000000000000000000003e7f33b3dd5ff00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000003e7f33b3dd5ff0000000000000000000000000000000000000000000000000003e7f33b3dd5ff0000e061240eef0fa275a6bdf4368b83c654e37c8dc7912dcd3b6aa942104a51e53bb0abb19e4ad616a570cd602b2fb2cdc23ce45a19af293c13103cead5fcdf76862ec929a19a0bd7074116e4257c98cd3342f010845a767ec5af017600cbb83a7e000000000000000000000000000000000000000000000000000000000000001b7906a92e777a4a9637920bf3ba9b60fddd13c1073f81e36694dcece4e5d2978ad76c6a8f5e84db65942bd58144a8fdeaa7da0b4612ad47d5306dba6540f71ae91089ce74cabcc7c465d5636ab5eb65709cdfc0fced75398bbf0a0eb043e20080000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1cc6000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000026000000000000000000000000dc85bde63eec1f3317b86f1589d681170a6a01be0000000000000000000000000000000000000000000000000de25eab380d1aab000000000000000000000000000000000000000000000003f6d596a440b17aab00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000fffcbb32a560000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000012f42206e491a0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e6a4d784d546c684e7930324e7a49774c54526d596d5974596d4a6a5a43316b5a6a6b784e324579597a6b785a6a676966513d3d0000000000000000000000000000000000000000000000000000000000000023000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001d46142dc7e2a857ba47000000000000000000000000000000000000000000001d422c3a8ca4d258ba4700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe061240eef0fa275a6bdf4368b83c654e37c8dc7912dcd3b6aa942104a51e53b",
      "signature": {
        "s": "0x2ec929a19a0bd7074116e4257c98cd3342f010845a767ec5af017600cbb83a7e",
        "r": "0xb0abb19e4ad616a570cd602b2fb2cdc23ce45a19af293c13103cead5fcdf7686",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7906a92e777a4a9637920bf3ba9b60fddd13c1073f81e36694dcece4e5d2978a",
      "signature": {
        "s": "0x1089ce74cabcc7c465d5636ab5eb65709cdfc0fced75398bbf0a0eb043e20080",
        "r": "0xd76c6a8f5e84db65942bd58144a8fdeaa7da0b4612ad47d5306dba6540f71ae9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "72054000000000000000",
    "total": "72054000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "72054000000000000000",
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
            "amount": "1365754000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "72054000000000000"
      }
    },
    "wallet": "0xdc85bde63eec1f3317b86f1589d681170a6a01be",
    "data": "eyJyZWYiOiI3NjMxMTlhNy02NzIwLTRmYmYtYmJjZC1kZjkxN2EyYzkxZjgifQ==",
    "nonce": 38,
    "balances": {
      "current": "1000466156702472875",
      "previous": "73126520156702472875"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 35,
    "balances": {
      "current": "138241354126410391206471",
      "previous": "138169300126410391206471"
    }
  },
  "blockNumber": "14797920",
  "created": "2022-05-18T09:01:25.225Z",
  "updated": "2022-05-18T09:01:25.318Z",
  "id": "6284b5e57832e20011830eff"
}
```
* *stageAmount*: `1000466156702472875`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000003e7f33b3dd5ff00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000003e7f33b3dd5ff0000000000000000000000000000000000000000000000000003e7f33b3dd5ff0000e061240eef0fa275a6bdf4368b83c654e37c8dc7912dcd3b6aa942104a51e53bb0abb19e4ad616a570cd602b2fb2cdc23ce45a19af293c13103cead5fcdf76862ec929a19a0bd7074116e4257c98cd3342f010845a767ec5af017600cbb83a7e000000000000000000000000000000000000000000000000000000000000001b7906a92e777a4a9637920bf3ba9b60fddd13c1073f81e36694dcece4e5d2978ad76c6a8f5e84db65942bd58144a8fdeaa7da0b4612ad47d5306dba6540f71ae91089ce74cabcc7c465d5636ab5eb65709cdfc0fced75398bbf0a0eb043e20080000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1cc6000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000026000000000000000000000000dc85bde63eec1f3317b86f1589d681170a6a01be0000000000000000000000000000000000000000000000000de25eab380d1aab000000000000000000000000000000000000000000000003f6d596a440b17aab00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000fffcbb32a560000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000012f42206e491a0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e6a4d784d546c684e7930324e7a49774c54526d596d5974596d4a6a5a43316b5a6a6b784e324579597a6b785a6a676966513d3d0000000000000000000000000000000000000000000000000000000000000023000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001d46142dc7e2a857ba47000000000000000000000000000000000000000000001d422c3a8ca4d258ba4700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe061240eef0fa275a6bdf4368b83c654e37c8dc7912dcd3b6aa942104a51e53b",
      "signature": {
        "s": "0x2ec929a19a0bd7074116e4257c98cd3342f010845a767ec5af017600cbb83a7e",
        "r": "0xb0abb19e4ad616a570cd602b2fb2cdc23ce45a19af293c13103cead5fcdf7686",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7906a92e777a4a9637920bf3ba9b60fddd13c1073f81e36694dcece4e5d2978a",
      "signature": {
        "s": "0x1089ce74cabcc7c465d5636ab5eb65709cdfc0fced75398bbf0a0eb043e20080",
        "r": "0xd76c6a8f5e84db65942bd58144a8fdeaa7da0b4612ad47d5306dba6540f71ae9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "72054000000000000000",
    "total": "72054000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "72054000000000000000",
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
            "amount": "1365754000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "72054000000000000"
      }
    },
    "wallet": "0xdc85bde63eec1f3317b86f1589d681170a6a01be",
    "data": "eyJyZWYiOiI3NjMxMTlhNy02NzIwLTRmYmYtYmJjZC1kZjkxN2EyYzkxZjgifQ==",
    "nonce": 38,
    "balances": {
      "current": "1000466156702472875",
      "previous": "73126520156702472875"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 35,
    "balances": {
      "current": "138241354126410391206471",
      "previous": "138169300126410391206471"
    }
  },
  "blockNumber": "14797920",
  "created": "2022-05-18T09:01:25.225Z",
  "updated": "2022-05-18T09:01:25.318Z",
  "id": "6284b5e57832e20011830eff"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de25eab380d1aab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000466156702472875`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`