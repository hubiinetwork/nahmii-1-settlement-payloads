# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9B20092Ec9b769cD6EA46c39393f8D43fD7278f4`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000043a77aabd007800000000000000000000000000000000000000000000000000043a77aabd007800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000043a77aabd007800000000000000000000000000000000000000000000000000043a77aabd00780000f46dbae3fed6f1ded3776f9cb5f652018bc8a742fd1a93a630c5d76f7d6236eab604d40c5609800583bd1b6b955487794dbc9c5f321bb1742e9811c6d48e8e3c33c015231dc8c1cb7990dc885065e713d327bb3e9ef174769f940e629011a5db000000000000000000000000000000000000000000000000000000000000001ccd8ac735da1cfc3bcecee400ccc3a8af2221b791a2d8e3ad33266e1e8c55f4a9c80ea6a7a90b8ac9946d3258ea4bea81cae02f8459d3c34019bc5872add9efb26e3ae6b46352960ce4af2531806ce154a2946935efa76455eda6f93471c97934000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000cac1120000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000080f7fb6b346fdc537f3649d449447dce39c3ad210000000000000000000000000000000000000000000000ca0939dffed0a736c50000000000000000000000000000000000000000000000ce44c6a752059a36c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001151c96347b00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000082468ba1b8650000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e3246684d4449315a53316d4e7a4e6d4c5451794d544574596d4e6b5a533032596a5932596a6334596d557a4d32556966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000009b20092ec9b769cd6ea46c39393f8d43fd7278f40000000000000000000000000000000000000000000000043a77aabd00780000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf46dbae3fed6f1ded3776f9cb5f652018bc8a742fd1a93a630c5d76f7d6236ea",
      "signature": {
        "s": "0x33c015231dc8c1cb7990dc885065e713d327bb3e9ef174769f940e629011a5db",
        "r": "0xb604d40c5609800583bd1b6b955487794dbc9c5f321bb1742e9811c6d48e8e3c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcd8ac735da1cfc3bcecee400ccc3a8af2221b791a2d8e3ad33266e1e8c55f4a9",
      "signature": {
        "s": "0x6e3ae6b46352960ce4af2531806ce154a2946935efa76455eda6f93471c97934",
        "r": "0xc80ea6a7a90b8ac9946d3258ea4bea81cae02f8459d3c34019bc5872add9efb2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "78000000000000000000",
    "total": "78000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "78000000000000000000",
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
            "amount": "586709000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "78000000000000000"
      }
    },
    "wallet": "0x80f7fb6b346fdc537f3649d449447dce39c3ad21",
    "data": "eyJyZWYiOiIyN2FhMDI1ZS1mNzNmLTQyMTEtYmNkZS02YjY2Yjc4YmUzM2UifQ==",
    "nonce": 46,
    "balances": {
      "current": "3726907111594858591941",
      "previous": "3804985111594858591941"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9b20092ec9b769cd6ea46c39393f8d43fd7278f4",
    "nonce": 1,
    "balances": {
      "current": "78000000000000000000",
      "previous": "0"
    }
  },
  "blockNumber": "13287698",
  "created": "2021-09-24T09:30:15.926Z",
  "updated": "2021-09-24T09:30:16.148Z",
  "id": "614d9aa7a2be2100101cc981"
}
```
* *stageAmount*: `78000000000000000000`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000043a77aabd007800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000043a77aabd007800000000000000000000000000000000000000000000000000043a77aabd00780000f46dbae3fed6f1ded3776f9cb5f652018bc8a742fd1a93a630c5d76f7d6236eab604d40c5609800583bd1b6b955487794dbc9c5f321bb1742e9811c6d48e8e3c33c015231dc8c1cb7990dc885065e713d327bb3e9ef174769f940e629011a5db000000000000000000000000000000000000000000000000000000000000001ccd8ac735da1cfc3bcecee400ccc3a8af2221b791a2d8e3ad33266e1e8c55f4a9c80ea6a7a90b8ac9946d3258ea4bea81cae02f8459d3c34019bc5872add9efb26e3ae6b46352960ce4af2531806ce154a2946935efa76455eda6f93471c97934000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000cac1120000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000080f7fb6b346fdc537f3649d449447dce39c3ad210000000000000000000000000000000000000000000000ca0939dffed0a736c50000000000000000000000000000000000000000000000ce44c6a752059a36c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001151c96347b00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000082468ba1b8650000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e3246684d4449315a53316d4e7a4e6d4c5451794d544574596d4e6b5a533032596a5932596a6334596d557a4d32556966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000009b20092ec9b769cd6ea46c39393f8d43fd7278f40000000000000000000000000000000000000000000000043a77aabd00780000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf46dbae3fed6f1ded3776f9cb5f652018bc8a742fd1a93a630c5d76f7d6236ea",
      "signature": {
        "s": "0x33c015231dc8c1cb7990dc885065e713d327bb3e9ef174769f940e629011a5db",
        "r": "0xb604d40c5609800583bd1b6b955487794dbc9c5f321bb1742e9811c6d48e8e3c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcd8ac735da1cfc3bcecee400ccc3a8af2221b791a2d8e3ad33266e1e8c55f4a9",
      "signature": {
        "s": "0x6e3ae6b46352960ce4af2531806ce154a2946935efa76455eda6f93471c97934",
        "r": "0xc80ea6a7a90b8ac9946d3258ea4bea81cae02f8459d3c34019bc5872add9efb2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "78000000000000000000",
    "total": "78000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "78000000000000000000",
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
            "amount": "586709000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "78000000000000000"
      }
    },
    "wallet": "0x80f7fb6b346fdc537f3649d449447dce39c3ad21",
    "data": "eyJyZWYiOiIyN2FhMDI1ZS1mNzNmLTQyMTEtYmNkZS02YjY2Yjc4YmUzM2UifQ==",
    "nonce": 46,
    "balances": {
      "current": "3726907111594858591941",
      "previous": "3804985111594858591941"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9b20092ec9b769cd6ea46c39393f8d43fd7278f4",
    "nonce": 1,
    "balances": {
      "current": "78000000000000000000",
      "previous": "0"
    }
  },
  "blockNumber": "13287698",
  "created": "2021-09-24T09:30:15.926Z",
  "updated": "2021-09-24T09:30:16.148Z",
  "id": "614d9aa7a2be2100101cc981"
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
0x0f200f9b0000000000000000000000000000000000000000000000043a77aabd007800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `78000000000000000000`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`