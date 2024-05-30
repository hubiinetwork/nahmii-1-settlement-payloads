# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCfcb7551b64A107AE1865F8c749250D83c6Ffa6f`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000007a85752c2887cce5b000000000000000000000000000000000000000000000001505b54ac82dfb0f10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001505b54ac82dfb0f1000000000000000000000000000000000000000000000007a85752c2887cce5b99d46d72b5606ef484c2675e753fe8d48e104585f0a5daccdd9c16069b559de9bc056fe0c62ccaa765b6df30db22d534c0112e51d533d1f254ffe4e124e5b792149c3d524b8b5ac994167dd09b12d198eeec1a7df0d758fc75a1a7e4c29137c8000000000000000000000000000000000000000000000000000000000000001bce9604f769b9bb6012d7bbb92c91dff75850492bc79fa8a2bd03091c1154c450f0aa95c8a52ce30e3bc7669aa5cec0ec68a9a74409a8f79eba4e9561b0225fc5776ba07db41d36653fccd636cc1c045ce1ce983e246c1c7790d7e863e26fa148000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5dd00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012ce4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000028b0af50868eff835cb30000000000000000000000000000000000000000000028b20001f6b589af90a200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000561b7a074c82fe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038e42d28c5e802a42160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6d49775a4751355979316c4d6a6c6b4c54566c5a6d497459544e694f4330324e4759784d7a41345954686d5a6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000cfcb7551b64a107ae1865f8c749250d83c6ffa6f000000000000000000000000000000000000000000000007a85752c2887cce5b00000000000000000000000000000000000000000000000657fbfe16059d1d6a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x99d46d72b5606ef484c2675e753fe8d48e104585f0a5daccdd9c16069b559de9",
      "signature": {
        "s": "0x149c3d524b8b5ac994167dd09b12d198eeec1a7df0d758fc75a1a7e4c29137c8",
        "r": "0xbc056fe0c62ccaa765b6df30db22d534c0112e51d533d1f254ffe4e124e5b792",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xce9604f769b9bb6012d7bbb92c91dff75850492bc79fa8a2bd03091c1154c450",
      "signature": {
        "s": "0x776ba07db41d36653fccd636cc1c045ce1ce983e246c1c7790d7e863e26fa148",
        "r": "0xf0aa95c8a52ce30e3bc7669aa5cec0ec68a9a74409a8f79eba4e9561b0225fc5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "24237058919531262193",
    "total": "141257463632779595355"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24237058919531262193",
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
            "amount": "16791352172364809519638"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "24237058919531262"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZmIwZGQ5Yy1lMjlkLTVlZmItYTNiOC02NGYxMzA4YThmZjkifQ==",
    "nonce": 77028,
    "balances": {
      "current": "192153919016662194150579",
      "previous": "192178180312640644944034"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcfcb7551b64a107ae1865f8c749250d83c6ffa6f",
    "nonce": 6,
    "balances": {
      "current": "141257463632779595355",
      "previous": "117020404713248333162"
    }
  },
  "blockNumber": "12568029",
  "created": "2021-06-04T12:45:12.886Z",
  "updated": "2021-06-04T12:45:12.963Z",
  "id": "60ba20583a79970010e7b03b"
}
```
* *stageAmount*: `141257463632779595355`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001505b54ac82dfb0f10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001505b54ac82dfb0f1000000000000000000000000000000000000000000000007a85752c2887cce5b99d46d72b5606ef484c2675e753fe8d48e104585f0a5daccdd9c16069b559de9bc056fe0c62ccaa765b6df30db22d534c0112e51d533d1f254ffe4e124e5b792149c3d524b8b5ac994167dd09b12d198eeec1a7df0d758fc75a1a7e4c29137c8000000000000000000000000000000000000000000000000000000000000001bce9604f769b9bb6012d7bbb92c91dff75850492bc79fa8a2bd03091c1154c450f0aa95c8a52ce30e3bc7669aa5cec0ec68a9a74409a8f79eba4e9561b0225fc5776ba07db41d36653fccd636cc1c045ce1ce983e246c1c7790d7e863e26fa148000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5dd00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012ce4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000028b0af50868eff835cb30000000000000000000000000000000000000000000028b20001f6b589af90a200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000561b7a074c82fe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038e42d28c5e802a42160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6d49775a4751355979316c4d6a6c6b4c54566c5a6d497459544e694f4330324e4759784d7a41345954686d5a6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000cfcb7551b64a107ae1865f8c749250d83c6ffa6f000000000000000000000000000000000000000000000007a85752c2887cce5b00000000000000000000000000000000000000000000000657fbfe16059d1d6a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x99d46d72b5606ef484c2675e753fe8d48e104585f0a5daccdd9c16069b559de9",
      "signature": {
        "s": "0x149c3d524b8b5ac994167dd09b12d198eeec1a7df0d758fc75a1a7e4c29137c8",
        "r": "0xbc056fe0c62ccaa765b6df30db22d534c0112e51d533d1f254ffe4e124e5b792",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xce9604f769b9bb6012d7bbb92c91dff75850492bc79fa8a2bd03091c1154c450",
      "signature": {
        "s": "0x776ba07db41d36653fccd636cc1c045ce1ce983e246c1c7790d7e863e26fa148",
        "r": "0xf0aa95c8a52ce30e3bc7669aa5cec0ec68a9a74409a8f79eba4e9561b0225fc5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "24237058919531262193",
    "total": "141257463632779595355"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24237058919531262193",
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
            "amount": "16791352172364809519638"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "24237058919531262"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZmIwZGQ5Yy1lMjlkLTVlZmItYTNiOC02NGYxMzA4YThmZjkifQ==",
    "nonce": 77028,
    "balances": {
      "current": "192153919016662194150579",
      "previous": "192178180312640644944034"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcfcb7551b64a107ae1865f8c749250d83c6ffa6f",
    "nonce": 6,
    "balances": {
      "current": "141257463632779595355",
      "previous": "117020404713248333162"
    }
  },
  "blockNumber": "12568029",
  "created": "2021-06-04T12:45:12.886Z",
  "updated": "2021-06-04T12:45:12.963Z",
  "id": "60ba20583a79970010e7b03b"
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
0x0f200f9b000000000000000000000000000000000000000000000007a85752c2887cce5b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `141257463632779595355`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`