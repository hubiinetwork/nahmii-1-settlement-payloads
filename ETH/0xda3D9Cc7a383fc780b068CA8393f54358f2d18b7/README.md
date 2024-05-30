# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xda3D9Cc7a383fc780b068CA8393f54358f2d18b7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000507a000000000000000000000000000000000000000000000000000000000000507a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000507a000000000000000000000000000000000000000000000000000000000000507ae922a6caa7d12413b1a216f9cb486aee0de2375d1f4de44ba6d31ae8a0d50da3bf24270f39aaceb6fbd1c532d3b3a9faf1a91c7d15a9bbecd19783bea9f1671a7021d60b506aecd5e7407cfc8bf5bb05ed3172a0fb8a632cfde3597ca1eaedc4000000000000000000000000000000000000000000000000000000000000001b0883faf0f229963e100a31245f5192a97e580f6c07748430bcd27b8087e0383771721e5b39dccc04e929b7ebd1520114d173bf3937334c90bbfe990563ec3eaf0063fc86d88ae6aaf824d2183206c5ef80e2bc3cd3884faefca3478306cc28d2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004ec00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7dca849000000000000000000000000000000000000000000000000002386f2c7dcf8d700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000014000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000093cf500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e7a4e6a597a5578595330345a4751314c5455774d6a59744f4755315a5330784f4451304e54566d5a5455334e47456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da3d9cc7a383fc780b068ca8393f54358f2d18b7000000000000000000000000000000000000000000000000000000000000507a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe922a6caa7d12413b1a216f9cb486aee0de2375d1f4de44ba6d31ae8a0d50da3",
      "signature": {
        "s": "0x7021d60b506aecd5e7407cfc8bf5bb05ed3172a0fb8a632cfde3597ca1eaedc4",
        "r": "0xbf24270f39aaceb6fbd1c532d3b3a9faf1a91c7d15a9bbecd19783bea9f1671a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0883faf0f229963e100a31245f5192a97e580f6c07748430bcd27b8087e03837",
      "signature": {
        "s": "0x0063fc86d88ae6aaf824d2183206c5ef80e2bc3cd3884faefca3478306cc28d2",
        "r": "0x71721e5b39dccc04e929b7ebd1520114d173bf3937334c90bbfe990563ec3eaf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "20602",
    "total": "20602"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20602",
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
            "amount": "605429"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "20"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NzNjYzUxYS04ZGQ1LTUwMjYtOGU1ZS0xODQ0NTVmZTU3NGEifQ==",
    "nonce": 1260,
    "balances": {
      "current": "10000001478207561",
      "previous": "10000001478228183"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda3d9cc7a383fc780b068ca8393f54358f2d18b7",
    "nonce": 20,
    "balances": {
      "current": "20602",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:02.935Z",
  "updated": "2020-05-22T08:08:03.010Z",
  "id": "5ec78862b0c6090011d5aa6c"
}
```
* *stageAmount*: `20602`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000507a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000507a000000000000000000000000000000000000000000000000000000000000507ae922a6caa7d12413b1a216f9cb486aee0de2375d1f4de44ba6d31ae8a0d50da3bf24270f39aaceb6fbd1c532d3b3a9faf1a91c7d15a9bbecd19783bea9f1671a7021d60b506aecd5e7407cfc8bf5bb05ed3172a0fb8a632cfde3597ca1eaedc4000000000000000000000000000000000000000000000000000000000000001b0883faf0f229963e100a31245f5192a97e580f6c07748430bcd27b8087e0383771721e5b39dccc04e929b7ebd1520114d173bf3937334c90bbfe990563ec3eaf0063fc86d88ae6aaf824d2183206c5ef80e2bc3cd3884faefca3478306cc28d2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004ec00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7dca849000000000000000000000000000000000000000000000000002386f2c7dcf8d700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000014000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000093cf500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e7a4e6a597a5578595330345a4751314c5455774d6a59744f4755315a5330784f4451304e54566d5a5455334e47456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da3d9cc7a383fc780b068ca8393f54358f2d18b7000000000000000000000000000000000000000000000000000000000000507a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe922a6caa7d12413b1a216f9cb486aee0de2375d1f4de44ba6d31ae8a0d50da3",
      "signature": {
        "s": "0x7021d60b506aecd5e7407cfc8bf5bb05ed3172a0fb8a632cfde3597ca1eaedc4",
        "r": "0xbf24270f39aaceb6fbd1c532d3b3a9faf1a91c7d15a9bbecd19783bea9f1671a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0883faf0f229963e100a31245f5192a97e580f6c07748430bcd27b8087e03837",
      "signature": {
        "s": "0x0063fc86d88ae6aaf824d2183206c5ef80e2bc3cd3884faefca3478306cc28d2",
        "r": "0x71721e5b39dccc04e929b7ebd1520114d173bf3937334c90bbfe990563ec3eaf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "20602",
    "total": "20602"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20602",
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
            "amount": "605429"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "20"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NzNjYzUxYS04ZGQ1LTUwMjYtOGU1ZS0xODQ0NTVmZTU3NGEifQ==",
    "nonce": 1260,
    "balances": {
      "current": "10000001478207561",
      "previous": "10000001478228183"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda3d9cc7a383fc780b068ca8393f54358f2d18b7",
    "nonce": 20,
    "balances": {
      "current": "20602",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:02.935Z",
  "updated": "2020-05-22T08:08:03.010Z",
  "id": "5ec78862b0c6090011d5aa6c"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000507a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `20602`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``