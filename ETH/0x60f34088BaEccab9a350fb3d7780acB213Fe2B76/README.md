# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x60f34088BaEccab9a350fb3d7780acB213Fe2B76`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001db70000000000000000000000000000000000000000000000000000000000001db700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001db70000000000000000000000000000000000000000000000000000000000001db7e40bf2d8aa0526f86313a9d9e8e44f36dfa817d106c600cf1c2766351fd4170bdde2ad7a65d007b5247a3f51ba802926c642fbacea530ce34ab57621e7b5126244acbd3599da9fbd9d4886e9b9732aca7fda8a05056ebafac32b9a993f5f52d2000000000000000000000000000000000000000000000000000000000000001bb14916b8130f3239b06c86b512d75d3be8a192fab8a2b89d5be2dd1d587543a150686b4bdefa886b7138ca25b5070115b21e64016fa88f9e71085fff0725c8e41f57baf99280b2f11abfdee064cc6131025b730d9e58d2166e8e84b8f0e65770000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000086400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcb33a77000000000000000000000000000000000000000000000000002386f2bcb3583500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c167f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934593255344d444a684d43316b5a575a6b4c54566a4d4441744f5745774d79316d4e574d345a5441344d7a4e6a4e6d556966513d3d000000000000000000000000000000000000000000000000000000000000000e00000000000000000000000060f34088baeccab9a350fb3d7780acb213fe2b760000000000000000000000000000000000000000000000000000000000001db7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe40bf2d8aa0526f86313a9d9e8e44f36dfa817d106c600cf1c2766351fd4170b",
      "signature": {
        "s": "0x44acbd3599da9fbd9d4886e9b9732aca7fda8a05056ebafac32b9a993f5f52d2",
        "r": "0xdde2ad7a65d007b5247a3f51ba802926c642fbacea530ce34ab57621e7b51262",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb14916b8130f3239b06c86b512d75d3be8a192fab8a2b89d5be2dd1d587543a1",
      "signature": {
        "s": "0x1f57baf99280b2f11abfdee064cc6131025b730d9e58d2166e8e84b8f0e65770",
        "r": "0x50686b4bdefa886b7138ca25b5070115b21e64016fa88f9e71085fff0725c8e4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7607",
    "total": "7607"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7607",
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
            "amount": "792191"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "7"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4Y2U4MDJhMC1kZWZkLTVjMDAtOWEwMy1mNWM4ZTA4MzNjNmUifQ==",
    "nonce": 2148,
    "balances": {
      "current": "10000001290943095",
      "previous": "10000001290950709"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x60f34088baeccab9a350fb3d7780acb213fe2b76",
    "nonce": 14,
    "balances": {
      "current": "7607",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:39.660Z",
  "updated": "2020-05-22T08:14:39.816Z",
  "id": "5ec789efb0c6090011d5ab9f"
}
```
* *stageAmount*: `7607`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000001db700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001db70000000000000000000000000000000000000000000000000000000000001db7e40bf2d8aa0526f86313a9d9e8e44f36dfa817d106c600cf1c2766351fd4170bdde2ad7a65d007b5247a3f51ba802926c642fbacea530ce34ab57621e7b5126244acbd3599da9fbd9d4886e9b9732aca7fda8a05056ebafac32b9a993f5f52d2000000000000000000000000000000000000000000000000000000000000001bb14916b8130f3239b06c86b512d75d3be8a192fab8a2b89d5be2dd1d587543a150686b4bdefa886b7138ca25b5070115b21e64016fa88f9e71085fff0725c8e41f57baf99280b2f11abfdee064cc6131025b730d9e58d2166e8e84b8f0e65770000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000086400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcb33a77000000000000000000000000000000000000000000000000002386f2bcb3583500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c167f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934593255344d444a684d43316b5a575a6b4c54566a4d4441744f5745774d79316d4e574d345a5441344d7a4e6a4e6d556966513d3d000000000000000000000000000000000000000000000000000000000000000e00000000000000000000000060f34088baeccab9a350fb3d7780acb213fe2b760000000000000000000000000000000000000000000000000000000000001db7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe40bf2d8aa0526f86313a9d9e8e44f36dfa817d106c600cf1c2766351fd4170b",
      "signature": {
        "s": "0x44acbd3599da9fbd9d4886e9b9732aca7fda8a05056ebafac32b9a993f5f52d2",
        "r": "0xdde2ad7a65d007b5247a3f51ba802926c642fbacea530ce34ab57621e7b51262",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb14916b8130f3239b06c86b512d75d3be8a192fab8a2b89d5be2dd1d587543a1",
      "signature": {
        "s": "0x1f57baf99280b2f11abfdee064cc6131025b730d9e58d2166e8e84b8f0e65770",
        "r": "0x50686b4bdefa886b7138ca25b5070115b21e64016fa88f9e71085fff0725c8e4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7607",
    "total": "7607"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7607",
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
            "amount": "792191"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "7"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4Y2U4MDJhMC1kZWZkLTVjMDAtOWEwMy1mNWM4ZTA4MzNjNmUifQ==",
    "nonce": 2148,
    "balances": {
      "current": "10000001290943095",
      "previous": "10000001290950709"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x60f34088baeccab9a350fb3d7780acb213fe2b76",
    "nonce": 14,
    "balances": {
      "current": "7607",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:39.660Z",
  "updated": "2020-05-22T08:14:39.816Z",
  "id": "5ec789efb0c6090011d5ab9f"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000001db70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7607`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``