# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xEC290b046Ef4e41AfD9c25b6a2C97A4b1594C001`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000076c000000000000000000000000000000000000000000000000000000000000076c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000076c000000000000000000000000000000000000000000000000000000000000076cf54c8ef46f6ebc9d06d14f296bb18c5e23222c81b137d70cd4cad90926fee4d9f2785a2477669459d8d490ce53c7cc68dddd5e8ac6c0bca793a5b09e6b19beb83d1e062fe53b35b6fbe3a91f8f539d910f923a1e2d1f103f7726e4265489ba99000000000000000000000000000000000000000000000000000000000000001b5fe79b3006ec2efffe278e76ab87680f6362bc2d2613bf6cbb2f89e685803681443e1d1f57c110c8e7177d12e0925b18f63b758ae11a18d6be0c9d57b54859d243e6808444ea478dfeff9b65604edca718408b0a553ba0526e6a4e7e6e43b9b7000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000019100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cca3b03f000000000000000000000000000000000000000000000000002386f2cca3b7ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008052900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d546c6b596a566c5a69316d5a6a466d4c5455335a4451744f47497a5a53307759574a68596a46685954566d4d54456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000ec290b046ef4e41afd9c25b6a2c97a4b1594c001000000000000000000000000000000000000000000000000000000000000076c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf54c8ef46f6ebc9d06d14f296bb18c5e23222c81b137d70cd4cad90926fee4d9",
      "signature": {
        "s": "0x3d1e062fe53b35b6fbe3a91f8f539d910f923a1e2d1f103f7726e4265489ba99",
        "r": "0xf2785a2477669459d8d490ce53c7cc68dddd5e8ac6c0bca793a5b09e6b19beb8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5fe79b3006ec2efffe278e76ab87680f6362bc2d2613bf6cbb2f89e685803681",
      "signature": {
        "s": "0x43e6808444ea478dfeff9b65604edca718408b0a553ba0526e6a4e7e6e43b9b7",
        "r": "0x443e1d1f57c110c8e7177d12e0925b18f63b758ae11a18d6be0c9d57b54859d2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1900",
    "total": "1900"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1900",
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
            "amount": "525609"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MTlkYjVlZi1mZjFmLTU3ZDQtOGIzZS0wYWJhYjFhYTVmMTEifQ==",
    "nonce": 401,
    "balances": {
      "current": "10000001558360127",
      "previous": "10000001558362028"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xec290b046ef4e41afd9c25b6a2c97a4b1594c001",
    "nonce": 20,
    "balances": {
      "current": "1900",
      "previous": "0"
    }
  },
  "blockNumber": "10114500",
  "created": "2020-05-22T08:01:49.818Z",
  "updated": "2020-05-22T08:01:49.885Z",
  "id": "5ec786ede5756b00111b7ff3"
}
```
* *stageAmount*: `1900`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000076c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000076c000000000000000000000000000000000000000000000000000000000000076cf54c8ef46f6ebc9d06d14f296bb18c5e23222c81b137d70cd4cad90926fee4d9f2785a2477669459d8d490ce53c7cc68dddd5e8ac6c0bca793a5b09e6b19beb83d1e062fe53b35b6fbe3a91f8f539d910f923a1e2d1f103f7726e4265489ba99000000000000000000000000000000000000000000000000000000000000001b5fe79b3006ec2efffe278e76ab87680f6362bc2d2613bf6cbb2f89e685803681443e1d1f57c110c8e7177d12e0925b18f63b758ae11a18d6be0c9d57b54859d243e6808444ea478dfeff9b65604edca718408b0a553ba0526e6a4e7e6e43b9b7000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000019100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cca3b03f000000000000000000000000000000000000000000000000002386f2cca3b7ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008052900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d546c6b596a566c5a69316d5a6a466d4c5455335a4451744f47497a5a53307759574a68596a46685954566d4d54456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000ec290b046ef4e41afd9c25b6a2c97a4b1594c001000000000000000000000000000000000000000000000000000000000000076c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf54c8ef46f6ebc9d06d14f296bb18c5e23222c81b137d70cd4cad90926fee4d9",
      "signature": {
        "s": "0x3d1e062fe53b35b6fbe3a91f8f539d910f923a1e2d1f103f7726e4265489ba99",
        "r": "0xf2785a2477669459d8d490ce53c7cc68dddd5e8ac6c0bca793a5b09e6b19beb8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5fe79b3006ec2efffe278e76ab87680f6362bc2d2613bf6cbb2f89e685803681",
      "signature": {
        "s": "0x43e6808444ea478dfeff9b65604edca718408b0a553ba0526e6a4e7e6e43b9b7",
        "r": "0x443e1d1f57c110c8e7177d12e0925b18f63b758ae11a18d6be0c9d57b54859d2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1900",
    "total": "1900"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1900",
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
            "amount": "525609"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MTlkYjVlZi1mZjFmLTU3ZDQtOGIzZS0wYWJhYjFhYTVmMTEifQ==",
    "nonce": 401,
    "balances": {
      "current": "10000001558360127",
      "previous": "10000001558362028"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xec290b046ef4e41afd9c25b6a2c97a4b1594c001",
    "nonce": 20,
    "balances": {
      "current": "1900",
      "previous": "0"
    }
  },
  "blockNumber": "10114500",
  "created": "2020-05-22T08:01:49.818Z",
  "updated": "2020-05-22T08:01:49.885Z",
  "id": "5ec786ede5756b00111b7ff3"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000076c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1900`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``