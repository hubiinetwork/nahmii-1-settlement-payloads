# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3a0496ce53aeD6F1E7Bd4077BEB8DDFEF3E57414`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000013b5759d0000000000000000000000000000000000000000000000000000000013b5759d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000013b5759d0000000000000000000000000000000000000000000000000000000013b5759d137d60b45d17a0efdc8b199133176b3cf9948e36b8d1eb4491f119b9ca0f124a9d998e3c4a3151c7d9a6538325eac27f7cb21d704a3c6efbb11bf005ff93c7453d69c42ef3b0930a3b2a7a849dace38a4ef38645f9fa1e56fa6d85ed3cb6adc3000000000000000000000000000000000000000000000000000000000000001b5b6298a11a1972ba1104671df6ca192ca4ec17a5e911727144f382e27ceccd52922a7989975489646022e7c315cf1a66c91c3d5fec7e363d6e6fae0dc43fa7a879e0688e8db52d4085d5701d359103cf782f7beed47039d4a46422010a89797b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56920000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000194f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17f70504a1ae000000000000000000000000000000000000000000000000002e17f718bf22ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000050ba3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1f6e0f57000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a6a4932597a51305a4330784d6d51314c54566c4d4449744f444d324d79316b4f5759774e5441314f5445774d6d496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003a0496ce53aed6f1e7bd4077beb8ddfef3e574140000000000000000000000000000000000000000000000000000000013b5759d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x137d60b45d17a0efdc8b199133176b3cf9948e36b8d1eb4491f119b9ca0f124a",
      "signature": {
        "s": "0x3d69c42ef3b0930a3b2a7a849dace38a4ef38645f9fa1e56fa6d85ed3cb6adc3",
        "r": "0x9d998e3c4a3151c7d9a6538325eac27f7cb21d704a3c6efbb11bf005ff93c745",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5b6298a11a1972ba1104671df6ca192ca4ec17a5e911727144f382e27ceccd52",
      "signature": {
        "s": "0x79e0688e8db52d4085d5701d359103cf782f7beed47039d4a46422010a89797b",
        "r": "0x922a7989975489646022e7c315cf1a66c91c3d5fec7e363d6e6fae0dc43fa7a8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "330659229",
    "total": "330659229"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "330659229",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "43476979543"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "330659"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZjI2YzQ0ZC0xMmQ1LTVlMDItODM2My1kOWYwNTA1OTEwMmIifQ==",
    "nonce": 6479,
    "balances": {
      "current": "12974198637240750",
      "previous": "12974198968230638"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3a0496ce53aed6f1e7bd4077beb8ddfef3e57414",
    "nonce": 22,
    "balances": {
      "current": "330659229",
      "previous": "0"
    }
  },
  "blockNumber": "10114706",
  "created": "2020-05-22T08:49:26.588Z",
  "updated": "2020-05-22T08:49:26.661Z",
  "id": "5ec79216005df800101bcaae"
}
```
* *stageAmount*: `330659229`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000013b5759d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000013b5759d0000000000000000000000000000000000000000000000000000000013b5759d137d60b45d17a0efdc8b199133176b3cf9948e36b8d1eb4491f119b9ca0f124a9d998e3c4a3151c7d9a6538325eac27f7cb21d704a3c6efbb11bf005ff93c7453d69c42ef3b0930a3b2a7a849dace38a4ef38645f9fa1e56fa6d85ed3cb6adc3000000000000000000000000000000000000000000000000000000000000001b5b6298a11a1972ba1104671df6ca192ca4ec17a5e911727144f382e27ceccd52922a7989975489646022e7c315cf1a66c91c3d5fec7e363d6e6fae0dc43fa7a879e0688e8db52d4085d5701d359103cf782f7beed47039d4a46422010a89797b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56920000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000194f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17f70504a1ae000000000000000000000000000000000000000000000000002e17f718bf22ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000050ba3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1f6e0f57000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a6a4932597a51305a4330784d6d51314c54566c4d4449744f444d324d79316b4f5759774e5441314f5445774d6d496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003a0496ce53aed6f1e7bd4077beb8ddfef3e574140000000000000000000000000000000000000000000000000000000013b5759d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x137d60b45d17a0efdc8b199133176b3cf9948e36b8d1eb4491f119b9ca0f124a",
      "signature": {
        "s": "0x3d69c42ef3b0930a3b2a7a849dace38a4ef38645f9fa1e56fa6d85ed3cb6adc3",
        "r": "0x9d998e3c4a3151c7d9a6538325eac27f7cb21d704a3c6efbb11bf005ff93c745",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5b6298a11a1972ba1104671df6ca192ca4ec17a5e911727144f382e27ceccd52",
      "signature": {
        "s": "0x79e0688e8db52d4085d5701d359103cf782f7beed47039d4a46422010a89797b",
        "r": "0x922a7989975489646022e7c315cf1a66c91c3d5fec7e363d6e6fae0dc43fa7a8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "330659229",
    "total": "330659229"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "330659229",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "43476979543"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "330659"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZjI2YzQ0ZC0xMmQ1LTVlMDItODM2My1kOWYwNTA1OTEwMmIifQ==",
    "nonce": 6479,
    "balances": {
      "current": "12974198637240750",
      "previous": "12974198968230638"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3a0496ce53aed6f1e7bd4077beb8ddfef3e57414",
    "nonce": 22,
    "balances": {
      "current": "330659229",
      "previous": "0"
    }
  },
  "blockNumber": "10114706",
  "created": "2020-05-22T08:49:26.588Z",
  "updated": "2020-05-22T08:49:26.661Z",
  "id": "5ec79216005df800101bcaae"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000013b5759d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `330659229`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`