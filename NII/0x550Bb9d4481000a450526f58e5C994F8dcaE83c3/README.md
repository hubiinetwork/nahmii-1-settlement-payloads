# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x550Bb9d4481000a450526f58e5C994F8dcaE83c3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000213db99109ee178d0000000000000000000000000000000000000000000000000097cdb3f75b29e30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000097cdb3f75b29e300000000000000000000000000000000000000000000000010a3c12116eee6cc041050e3088ea05678d997a2a1ff2d092d26ecb30c2a89e0e28f1b1a8467c4692cd56a9455f5ccc29c2160cffe6c9d30707516ccea108b424dadb927de7da772450a0b4417969c304bd027d30285abea4d15e5fcdb88c3d85ff71cc479897770000000000000000000000000000000000000000000000000000000000000001c76ed66c3548b7c3089d126f12a98e30171f72839e9d5a16507addebc36bb996c8cb12ab433cc995f1b7068465c69d1abebfb0f974b9d57dbe3e0a8f847dd16d526637b0446a3aff7c9e1dc86ddd0eb37363f39f9c3431d29af54726c15a268af000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b31e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003e01934f2c1b32d66b40000000000000000000000000000000000000000000003e0193e720abc2c2d36200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000026dc98913e3f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc866ab036c62a6be60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595755325a575134595330324f47526b4c5455344f574d744f4464695a69316b4e5455355954466b4e44646b4e474d6966513d3d000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000550bb9d4481000a450526f58e5c994f8dcae83c3000000000000000000000000000000000000000000000000213db99109ee178d00000000000000000000000000000000000000000000000020a5ebdd1292edaa00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x041050e3088ea05678d997a2a1ff2d092d26ecb30c2a89e0e28f1b1a8467c469",
      "signature": {
        "s": "0x450a0b4417969c304bd027d30285abea4d15e5fcdb88c3d85ff71cc479897770",
        "r": "0x2cd56a9455f5ccc29c2160cffe6c9d30707516ccea108b424dadb927de7da772",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x76ed66c3548b7c3089d126f12a98e30171f72839e9d5a16507addebc36bb996c",
      "signature": {
        "s": "0x26637b0446a3aff7c9e1dc86ddd0eb37363f39f9c3431d29af54726c15a268af",
        "r": "0x8cb12ab433cc995f1b7068465c69d1abebfb0f974b9d57dbe3e0a8f847dd16d5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "42728894316095971",
    "total": "1199014273673520844"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "42728894316095971",
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
            "amount": "27679801858262240488422"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "42728894316095"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5YWU2ZWQ4YS02OGRkLTU4OWMtODdiZi1kNTU5YTFkNDdkNGMifQ==",
    "nonce": 111390,
    "balances": {
      "current": "292815783433333777001280",
      "previous": "292815826204956987413346"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x550bb9d4481000a450526f58e5c994f8dcae83c3",
    "nonce": 47,
    "balances": {
      "current": "2395274609418966925",
      "previous": "2352545715102870954"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:03.894Z",
  "updated": "2022-05-04T08:58:04.010Z",
  "id": "6272401bbbd75600116d069d"
}
```
* *stageAmount*: `2395274609418966925`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000097cdb3f75b29e30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000097cdb3f75b29e300000000000000000000000000000000000000000000000010a3c12116eee6cc041050e3088ea05678d997a2a1ff2d092d26ecb30c2a89e0e28f1b1a8467c4692cd56a9455f5ccc29c2160cffe6c9d30707516ccea108b424dadb927de7da772450a0b4417969c304bd027d30285abea4d15e5fcdb88c3d85ff71cc479897770000000000000000000000000000000000000000000000000000000000000001c76ed66c3548b7c3089d126f12a98e30171f72839e9d5a16507addebc36bb996c8cb12ab433cc995f1b7068465c69d1abebfb0f974b9d57dbe3e0a8f847dd16d526637b0446a3aff7c9e1dc86ddd0eb37363f39f9c3431d29af54726c15a268af000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b31e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003e01934f2c1b32d66b40000000000000000000000000000000000000000000003e0193e720abc2c2d36200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000026dc98913e3f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc866ab036c62a6be60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595755325a575134595330324f47526b4c5455344f574d744f4464695a69316b4e5455355954466b4e44646b4e474d6966513d3d000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000550bb9d4481000a450526f58e5c994f8dcae83c3000000000000000000000000000000000000000000000000213db99109ee178d00000000000000000000000000000000000000000000000020a5ebdd1292edaa00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x041050e3088ea05678d997a2a1ff2d092d26ecb30c2a89e0e28f1b1a8467c469",
      "signature": {
        "s": "0x450a0b4417969c304bd027d30285abea4d15e5fcdb88c3d85ff71cc479897770",
        "r": "0x2cd56a9455f5ccc29c2160cffe6c9d30707516ccea108b424dadb927de7da772",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x76ed66c3548b7c3089d126f12a98e30171f72839e9d5a16507addebc36bb996c",
      "signature": {
        "s": "0x26637b0446a3aff7c9e1dc86ddd0eb37363f39f9c3431d29af54726c15a268af",
        "r": "0x8cb12ab433cc995f1b7068465c69d1abebfb0f974b9d57dbe3e0a8f847dd16d5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "42728894316095971",
    "total": "1199014273673520844"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "42728894316095971",
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
            "amount": "27679801858262240488422"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "42728894316095"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5YWU2ZWQ4YS02OGRkLTU4OWMtODdiZi1kNTU5YTFkNDdkNGMifQ==",
    "nonce": 111390,
    "balances": {
      "current": "292815783433333777001280",
      "previous": "292815826204956987413346"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x550bb9d4481000a450526f58e5c994f8dcae83c3",
    "nonce": 47,
    "balances": {
      "current": "2395274609418966925",
      "previous": "2352545715102870954"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:03.894Z",
  "updated": "2022-05-04T08:58:04.010Z",
  "id": "6272401bbbd75600116d069d"
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
0x0f200f9b000000000000000000000000000000000000000000000000213db99109ee178d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2395274609418966925`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`