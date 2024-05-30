# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x29AD08bCeAa6f5C6bf6B5A23433334170ad7B2D1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000051632000000000000000000000000000000000000000000000000000000000005163200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000051632000000000000000000000000000000000000000000000000000000000005163224924e19220f25a739bde588ff34901e4f60d73368f2ac8d538f67e226b49a1c10ae6684e8a78a2d2a1c353fbad71af24e83b1acf03b65cdf2421ef0ce127fd06761691a2f0bd046aadce6125e15b606d7e59b9160109f3b271c03a7dd26cebc000000000000000000000000000000000000000000000000000000000000001c534832b03a7e3a5063765be5e5a5dd75173477c5b6302a7c2291eb71519d290e6d5a7a10e2179bf4004ccba3a263426e9cfd01d3eb079b3a9a467f64f54b739a3f95b5763000f6e7d66b5f2d77c832bc127ed6d0cd56bb6f65e6ef5bc8885210000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000005200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2dce018d3000000000000000000000000000000000000000000000000002386f2dce5305200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000014d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003de7600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a6d59335a6d566b5a4330314d6d4e694c545535596d55744f444d304d79316b4d544d305a5745315957526c5a6a676966513d3d000000000000000000000000000000000000000000000000000000000000001900000000000000000000000029ad08bceaa6f5c6bf6b5a23433334170ad7b2d10000000000000000000000000000000000000000000000000000000000051632000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x24924e19220f25a739bde588ff34901e4f60d73368f2ac8d538f67e226b49a1c",
      "signature": {
        "s": "0x6761691a2f0bd046aadce6125e15b606d7e59b9160109f3b271c03a7dd26cebc",
        "r": "0x10ae6684e8a78a2d2a1c353fbad71af24e83b1acf03b65cdf2421ef0ce127fd0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x534832b03a7e3a5063765be5e5a5dd75173477c5b6302a7c2291eb71519d290e",
      "signature": {
        "s": "0x3f95b5763000f6e7d66b5f2d77c832bc127ed6d0cd56bb6f65e6ef5bc8885210",
        "r": "0x6d5a7a10e2179bf4004ccba3a263426e9cfd01d3eb079b3a9a467f64f54b739a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "333362",
    "total": "333362"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "333362",
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
            "amount": "253558"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "333"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZmY3ZmVkZC01MmNiLTU5YmUtODM0My1kMTM0ZWE1YWRlZjgifQ==",
    "nonce": 82,
    "balances": {
      "current": "10000001830754515",
      "previous": "10000001831088210"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x29ad08bceaa6f5c6bf6b5a23433334170ad7b2d1",
    "nonce": 25,
    "balances": {
      "current": "333362",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:30.946Z",
  "updated": "2020-05-22T07:59:31.023Z",
  "id": "5ec78662e5756b00111b7f8a"
}
```
* *stageAmount*: `333362`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000005163200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000051632000000000000000000000000000000000000000000000000000000000005163224924e19220f25a739bde588ff34901e4f60d73368f2ac8d538f67e226b49a1c10ae6684e8a78a2d2a1c353fbad71af24e83b1acf03b65cdf2421ef0ce127fd06761691a2f0bd046aadce6125e15b606d7e59b9160109f3b271c03a7dd26cebc000000000000000000000000000000000000000000000000000000000000001c534832b03a7e3a5063765be5e5a5dd75173477c5b6302a7c2291eb71519d290e6d5a7a10e2179bf4004ccba3a263426e9cfd01d3eb079b3a9a467f64f54b739a3f95b5763000f6e7d66b5f2d77c832bc127ed6d0cd56bb6f65e6ef5bc8885210000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000005200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2dce018d3000000000000000000000000000000000000000000000000002386f2dce5305200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000014d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003de7600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a6d59335a6d566b5a4330314d6d4e694c545535596d55744f444d304d79316b4d544d305a5745315957526c5a6a676966513d3d000000000000000000000000000000000000000000000000000000000000001900000000000000000000000029ad08bceaa6f5c6bf6b5a23433334170ad7b2d10000000000000000000000000000000000000000000000000000000000051632000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x24924e19220f25a739bde588ff34901e4f60d73368f2ac8d538f67e226b49a1c",
      "signature": {
        "s": "0x6761691a2f0bd046aadce6125e15b606d7e59b9160109f3b271c03a7dd26cebc",
        "r": "0x10ae6684e8a78a2d2a1c353fbad71af24e83b1acf03b65cdf2421ef0ce127fd0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x534832b03a7e3a5063765be5e5a5dd75173477c5b6302a7c2291eb71519d290e",
      "signature": {
        "s": "0x3f95b5763000f6e7d66b5f2d77c832bc127ed6d0cd56bb6f65e6ef5bc8885210",
        "r": "0x6d5a7a10e2179bf4004ccba3a263426e9cfd01d3eb079b3a9a467f64f54b739a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "333362",
    "total": "333362"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "333362",
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
            "amount": "253558"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "333"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZmY3ZmVkZC01MmNiLTU5YmUtODM0My1kMTM0ZWE1YWRlZjgifQ==",
    "nonce": 82,
    "balances": {
      "current": "10000001830754515",
      "previous": "10000001831088210"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x29ad08bceaa6f5c6bf6b5a23433334170ad7b2d1",
    "nonce": 25,
    "balances": {
      "current": "333362",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:30.946Z",
  "updated": "2020-05-22T07:59:31.023Z",
  "id": "5ec78662e5756b00111b7f8a"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000516320000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `333362`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``