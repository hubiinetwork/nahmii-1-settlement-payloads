# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4d89dcb7273592b2C19F0722D6F95a7C8a70bfba`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001a4d0000000000000000000000000000000000000000000000000000000000001a4d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001a4d0000000000000000000000000000000000000000000000000000000000001a4d6fc267c26be2370f57a7807e13a7080a499b852963838e36f70b648583cebb82f4af8b8a914818be8ebaf22b39d2ad92b0f51d42957fe17c521ff284f3f129d42a0283b5fc58802331dbf267648fcf3f14654dabb5a4646f8ca6b16dcec2bd59000000000000000000000000000000000000000000000000000000000000001c60051bbae29af945c9fc0d00bb6a188dd5973b1ba34be5bdd87040bf2b30d480185787ef93116d0ba82cb0f3c13dd7d74fd8cae28ef2da85b02347dac48670215de2d84c01dff594e6e4a1878c08059c0b2cdff38aa063e4cf33be018f02916d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000012100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ccfb4068000000000000000000000000000000000000000000000000002386f2ccfb5abb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007eec700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e5746684f5751314d4330355a5459344c5456695a6d4d744f5441334d43316b4d44646d4d6d49304e4441354d6d596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000004d89dcb7273592b2c19f0722d6f95a7c8a70bfba0000000000000000000000000000000000000000000000000000000000001a4d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6fc267c26be2370f57a7807e13a7080a499b852963838e36f70b648583cebb82",
      "signature": {
        "s": "0x2a0283b5fc58802331dbf267648fcf3f14654dabb5a4646f8ca6b16dcec2bd59",
        "r": "0xf4af8b8a914818be8ebaf22b39d2ad92b0f51d42957fe17c521ff284f3f129d4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x60051bbae29af945c9fc0d00bb6a188dd5973b1ba34be5bdd87040bf2b30d480",
      "signature": {
        "s": "0x5de2d84c01dff594e6e4a1878c08059c0b2cdff38aa063e4cf33be018f02916d",
        "r": "0x185787ef93116d0ba82cb0f3c13dd7d74fd8cae28ef2da85b02347dac4867021",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6733",
    "total": "6733"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6733",
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
            "amount": "519879"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2NWFhOWQ1MC05ZTY4LTViZmMtOTA3MC1kMDdmMmI0NDA5MmYifQ==",
    "nonce": 289,
    "balances": {
      "current": "10000001564098664",
      "previous": "10000001564105403"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4d89dcb7273592b2c19f0722d6f95a7c8a70bfba",
    "nonce": 20,
    "balances": {
      "current": "6733",
      "previous": "0"
    }
  },
  "blockNumber": "10114494",
  "created": "2020-05-22T08:00:53.978Z",
  "updated": "2020-05-22T08:00:54.049Z",
  "id": "5ec786b5005df800101bc276"
}
```
* *stageAmount*: `6733`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000001a4d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001a4d0000000000000000000000000000000000000000000000000000000000001a4d6fc267c26be2370f57a7807e13a7080a499b852963838e36f70b648583cebb82f4af8b8a914818be8ebaf22b39d2ad92b0f51d42957fe17c521ff284f3f129d42a0283b5fc58802331dbf267648fcf3f14654dabb5a4646f8ca6b16dcec2bd59000000000000000000000000000000000000000000000000000000000000001c60051bbae29af945c9fc0d00bb6a188dd5973b1ba34be5bdd87040bf2b30d480185787ef93116d0ba82cb0f3c13dd7d74fd8cae28ef2da85b02347dac48670215de2d84c01dff594e6e4a1878c08059c0b2cdff38aa063e4cf33be018f02916d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000012100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ccfb4068000000000000000000000000000000000000000000000000002386f2ccfb5abb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007eec700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e5746684f5751314d4330355a5459344c5456695a6d4d744f5441334d43316b4d44646d4d6d49304e4441354d6d596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000004d89dcb7273592b2c19f0722d6f95a7c8a70bfba0000000000000000000000000000000000000000000000000000000000001a4d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6fc267c26be2370f57a7807e13a7080a499b852963838e36f70b648583cebb82",
      "signature": {
        "s": "0x2a0283b5fc58802331dbf267648fcf3f14654dabb5a4646f8ca6b16dcec2bd59",
        "r": "0xf4af8b8a914818be8ebaf22b39d2ad92b0f51d42957fe17c521ff284f3f129d4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x60051bbae29af945c9fc0d00bb6a188dd5973b1ba34be5bdd87040bf2b30d480",
      "signature": {
        "s": "0x5de2d84c01dff594e6e4a1878c08059c0b2cdff38aa063e4cf33be018f02916d",
        "r": "0x185787ef93116d0ba82cb0f3c13dd7d74fd8cae28ef2da85b02347dac4867021",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6733",
    "total": "6733"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6733",
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
            "amount": "519879"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2NWFhOWQ1MC05ZTY4LTViZmMtOTA3MC1kMDdmMmI0NDA5MmYifQ==",
    "nonce": 289,
    "balances": {
      "current": "10000001564098664",
      "previous": "10000001564105403"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4d89dcb7273592b2c19f0722d6f95a7c8a70bfba",
    "nonce": 20,
    "balances": {
      "current": "6733",
      "previous": "0"
    }
  },
  "blockNumber": "10114494",
  "created": "2020-05-22T08:00:53.978Z",
  "updated": "2020-05-22T08:00:54.049Z",
  "id": "5ec786b5005df800101bc276"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000001a4d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6733`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``