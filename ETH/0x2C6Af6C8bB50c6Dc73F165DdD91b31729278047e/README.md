# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2C6Af6C8bB50c6Dc73F165DdD91b31729278047e`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000023120000000000000000000000000000000000000000000000000000000000002312000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000023120000000000000000000000000000000000000000000000000000000000002312f51ddd2e1c274523539734828accd463f3aaecfebbcd77b1bb9729a3490969def8fb45b8ec73351422385b3c1e1d0e59381cfcbf97a7cc77c38b03e30b8a676723f56681a9bf15b277ecc4fac42c73f4f4cdf89f42ab52850a243e1f65ef3e9e000000000000000000000000000000000000000000000000000000000000001cb2e107f40512cb9ee82f09ede3fd0fa53f3ff5a9e743c57e1b4a2adc860e5d0f3175ad2b153d97ee1b5218795961ca3fe55aee6125589ab9773b9b4c41f837977f4f11d1aae54bfe5a85e2d2ded272b28db1e976923756cfb861103e5ed20169000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000019300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cca38c6d000000000000000000000000000000000000000000000000002386f2cca3af8700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008053200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e7a566959324e6c4f53316a4d574e6d4c54566d593255744f445a6c4d7930774e3251314e4756684d6d59795a44556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002c6af6c8bb50c6dc73f165ddd91b31729278047e0000000000000000000000000000000000000000000000000000000000002312000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf51ddd2e1c274523539734828accd463f3aaecfebbcd77b1bb9729a3490969de",
      "signature": {
        "s": "0x23f56681a9bf15b277ecc4fac42c73f4f4cdf89f42ab52850a243e1f65ef3e9e",
        "r": "0xf8fb45b8ec73351422385b3c1e1d0e59381cfcbf97a7cc77c38b03e30b8a6767",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb2e107f40512cb9ee82f09ede3fd0fa53f3ff5a9e743c57e1b4a2adc860e5d0f",
      "signature": {
        "s": "0x7f4f11d1aae54bfe5a85e2d2ded272b28db1e976923756cfb861103e5ed20169",
        "r": "0x3175ad2b153d97ee1b5218795961ca3fe55aee6125589ab9773b9b4c41f83797",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8978",
    "total": "8978"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8978",
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
            "amount": "525618"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NzViY2NlOS1jMWNmLTVmY2UtODZlMy0wN2Q1NGVhMmYyZDUifQ==",
    "nonce": 403,
    "balances": {
      "current": "10000001558350957",
      "previous": "10000001558359943"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2c6af6c8bb50c6dc73f165ddd91b31729278047e",
    "nonce": 20,
    "balances": {
      "current": "8978",
      "previous": "0"
    }
  },
  "blockNumber": "10114500",
  "created": "2020-05-22T08:01:50.255Z",
  "updated": "2020-05-22T08:01:50.315Z",
  "id": "5ec786eee5756b00111b7ff4"
}
```
* *stageAmount*: `8978`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000002312000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000023120000000000000000000000000000000000000000000000000000000000002312f51ddd2e1c274523539734828accd463f3aaecfebbcd77b1bb9729a3490969def8fb45b8ec73351422385b3c1e1d0e59381cfcbf97a7cc77c38b03e30b8a676723f56681a9bf15b277ecc4fac42c73f4f4cdf89f42ab52850a243e1f65ef3e9e000000000000000000000000000000000000000000000000000000000000001cb2e107f40512cb9ee82f09ede3fd0fa53f3ff5a9e743c57e1b4a2adc860e5d0f3175ad2b153d97ee1b5218795961ca3fe55aee6125589ab9773b9b4c41f837977f4f11d1aae54bfe5a85e2d2ded272b28db1e976923756cfb861103e5ed20169000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000019300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cca38c6d000000000000000000000000000000000000000000000000002386f2cca3af8700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008053200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e7a566959324e6c4f53316a4d574e6d4c54566d593255744f445a6c4d7930774e3251314e4756684d6d59795a44556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002c6af6c8bb50c6dc73f165ddd91b31729278047e0000000000000000000000000000000000000000000000000000000000002312000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf51ddd2e1c274523539734828accd463f3aaecfebbcd77b1bb9729a3490969de",
      "signature": {
        "s": "0x23f56681a9bf15b277ecc4fac42c73f4f4cdf89f42ab52850a243e1f65ef3e9e",
        "r": "0xf8fb45b8ec73351422385b3c1e1d0e59381cfcbf97a7cc77c38b03e30b8a6767",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb2e107f40512cb9ee82f09ede3fd0fa53f3ff5a9e743c57e1b4a2adc860e5d0f",
      "signature": {
        "s": "0x7f4f11d1aae54bfe5a85e2d2ded272b28db1e976923756cfb861103e5ed20169",
        "r": "0x3175ad2b153d97ee1b5218795961ca3fe55aee6125589ab9773b9b4c41f83797",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8978",
    "total": "8978"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8978",
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
            "amount": "525618"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NzViY2NlOS1jMWNmLTVmY2UtODZlMy0wN2Q1NGVhMmYyZDUifQ==",
    "nonce": 403,
    "balances": {
      "current": "10000001558350957",
      "previous": "10000001558359943"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2c6af6c8bb50c6dc73f165ddd91b31729278047e",
    "nonce": 20,
    "balances": {
      "current": "8978",
      "previous": "0"
    }
  },
  "blockNumber": "10114500",
  "created": "2020-05-22T08:01:50.255Z",
  "updated": "2020-05-22T08:01:50.315Z",
  "id": "5ec786eee5756b00111b7ff4"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000023120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8978`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``