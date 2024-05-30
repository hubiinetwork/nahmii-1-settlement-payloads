# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFB904394a2Ad887046DAC4791C20c1e9d3367aa1`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000002cefabc7000000000000000000000000000000000000000000000000000000002cefabc7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002cefabc7000000000000000000000000000000000000000000000000000000002cefabc74b72ecf911eade77499f45ec09c6e8c8578bb8122fc2751c5e91218e7ee65be25de46eb7fddf8e21b98f6ff265e66f41f95963c998956cc0d5a7b60891614d0e22906a8e6aa6b197aa90479a5214593d15d10750824c1570bfc9cb63d6df36d0000000000000000000000000000000000000000000000000000000000000001b86fdec2b54bbd047af16ae572f90b61def233f25de020f4e6d3197ffb8f58e2c3efdafc12a3916aa4d695d30c093c1f4d3120739128c64d387739b78c92d58695259bdc17efe89c087399560b3831aee8426d83674f597bfa6fde99bea460140000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000193200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18096305f84b000000000000000000000000000000000000000000000000002e18099001250200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000b80f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1abb8c99000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d324a6a4d6a67774f433031595459334c5455315a5467744f5445324e5330355a57566b4d5449345a6a59314f474d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fb904394a2ad887046dac4791c20c1e9d3367aa1000000000000000000000000000000000000000000000000000000002cefabc7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4b72ecf911eade77499f45ec09c6e8c8578bb8122fc2751c5e91218e7ee65be2",
      "signature": {
        "s": "0x22906a8e6aa6b197aa90479a5214593d15d10750824c1570bfc9cb63d6df36d0",
        "r": "0x5de46eb7fddf8e21b98f6ff265e66f41f95963c998956cc0d5a7b60891614d0e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x86fdec2b54bbd047af16ae572f90b61def233f25de020f4e6d3197ffb8f58e2c",
      "signature": {
        "s": "0x5259bdc17efe89c087399560b3831aee8426d83674f597bfa6fde99bea460140",
        "r": "0x3efdafc12a3916aa4d695d30c093c1f4d3120739128c64d387739b78c92d5869",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "753904583",
    "total": "753904583"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "753904583",
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
            "amount": "43398171801"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "753904"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiM2JjMjgwOC01YTY3LTU1ZTgtOTE2NS05ZWVkMTI4ZjY1OGMifQ==",
    "nonce": 6450,
    "balances": {
      "current": "12974277523798091",
      "previous": "12974278278456578"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfb904394a2ad887046dac4791c20c1e9d3367aa1",
    "nonce": 22,
    "balances": {
      "current": "753904583",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:14.861Z",
  "updated": "2020-05-22T08:49:15.940Z",
  "id": "5ec7920a005df800101bcaa4"
}
```
* *stageAmount*: `753904583`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000002cefabc7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002cefabc7000000000000000000000000000000000000000000000000000000002cefabc74b72ecf911eade77499f45ec09c6e8c8578bb8122fc2751c5e91218e7ee65be25de46eb7fddf8e21b98f6ff265e66f41f95963c998956cc0d5a7b60891614d0e22906a8e6aa6b197aa90479a5214593d15d10750824c1570bfc9cb63d6df36d0000000000000000000000000000000000000000000000000000000000000001b86fdec2b54bbd047af16ae572f90b61def233f25de020f4e6d3197ffb8f58e2c3efdafc12a3916aa4d695d30c093c1f4d3120739128c64d387739b78c92d58695259bdc17efe89c087399560b3831aee8426d83674f597bfa6fde99bea460140000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000193200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18096305f84b000000000000000000000000000000000000000000000000002e18099001250200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000b80f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1abb8c99000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d324a6a4d6a67774f433031595459334c5455315a5467744f5445324e5330355a57566b4d5449345a6a59314f474d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fb904394a2ad887046dac4791c20c1e9d3367aa1000000000000000000000000000000000000000000000000000000002cefabc7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4b72ecf911eade77499f45ec09c6e8c8578bb8122fc2751c5e91218e7ee65be2",
      "signature": {
        "s": "0x22906a8e6aa6b197aa90479a5214593d15d10750824c1570bfc9cb63d6df36d0",
        "r": "0x5de46eb7fddf8e21b98f6ff265e66f41f95963c998956cc0d5a7b60891614d0e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x86fdec2b54bbd047af16ae572f90b61def233f25de020f4e6d3197ffb8f58e2c",
      "signature": {
        "s": "0x5259bdc17efe89c087399560b3831aee8426d83674f597bfa6fde99bea460140",
        "r": "0x3efdafc12a3916aa4d695d30c093c1f4d3120739128c64d387739b78c92d5869",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "753904583",
    "total": "753904583"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "753904583",
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
            "amount": "43398171801"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "753904"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiM2JjMjgwOC01YTY3LTU1ZTgtOTE2NS05ZWVkMTI4ZjY1OGMifQ==",
    "nonce": 6450,
    "balances": {
      "current": "12974277523798091",
      "previous": "12974278278456578"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfb904394a2ad887046dac4791c20c1e9d3367aa1",
    "nonce": 22,
    "balances": {
      "current": "753904583",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:14.861Z",
  "updated": "2020-05-22T08:49:15.940Z",
  "id": "5ec7920a005df800101bcaa4"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000002cefabc7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `753904583`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`