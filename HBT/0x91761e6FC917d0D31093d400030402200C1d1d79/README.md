# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x91761e6FC917d0D31093d400030402200C1d1d79`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000cdf4033000000000000000000000000000000000000000000000000000000000cdf4033000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000cdf4033000000000000000000000000000000000000000000000000000000000cdf4033abcf612902dd58c333d29a02d2bc92b00d900c1b61cdc9afa0855ebce43f8e3dea9ca9ef6ca8a2d914f99c08c0610c41c3cc0a4f0bb0f755529ae96aa02a9d6025bc8f2a65a1bec399783b65aa6506c7aca505d9889593436407cce5f743f4f8000000000000000000000000000000000000000000000000000000000000001b26b7c6583daa918f078eed15153c163acd02dfc231f8b1b0a279f7c3ae7bab176148d65b3645fbd658f0d0f3d5ca70a04e6058a0cfb7352b371f7f70b258769661e7ad7abf2e2c59e35e5a15008e6e7dcb96f45b479452f1a34051d215ecab0d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b2b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a54eeab737000000000000000000000000000000000000000000000000002e15a55bcd42ff00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000034b95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab744a6ef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979595751354d7a6b344d53316d5a446b784c5455304d444d744f4442684e43316b4d44686b4e44566d4e4749354d6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000091761e6fc917d0d31093d400030402200c1d1d79000000000000000000000000000000000000000000000000000000000cdf4033000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xabcf612902dd58c333d29a02d2bc92b00d900c1b61cdc9afa0855ebce43f8e3d",
      "signature": {
        "s": "0x25bc8f2a65a1bec399783b65aa6506c7aca505d9889593436407cce5f743f4f8",
        "r": "0xea9ca9ef6ca8a2d914f99c08c0610c41c3cc0a4f0bb0f755529ae96aa02a9d60",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x26b7c6583daa918f078eed15153c163acd02dfc231f8b1b0a279f7c3ae7bab17",
      "signature": {
        "s": "0x61e7ad7abf2e2c59e35e5a15008e6e7dcb96f45b479452f1a34051d215ecab0d",
        "r": "0x6148d65b3645fbd658f0d0f3d5ca70a04e6058a0cfb7352b371f7f70b2587696",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "215957555",
    "total": "215957555"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "215957555",
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
            "amount": "46024402671"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "215957"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYWQ5Mzk4MS1mZDkxLTU0MDMtODBhNC1kMDhkNDVmNGI5MmMifQ==",
    "nonce": 6955,
    "balances": {
      "current": "12971648666482487",
      "previous": "12971648882655999"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x91761e6fc917d0d31093d400030402200c1d1d79",
    "nonce": 22,
    "balances": {
      "current": "215957555",
      "previous": "0"
    }
  },
  "blockNumber": "10114723",
  "created": "2020-05-22T08:53:00.360Z",
  "updated": "2020-05-22T08:53:00.445Z",
  "id": "5ec792ec005df800101bcb4e"
}
```
* *stageAmount*: `215957555`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000cdf4033000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000cdf4033000000000000000000000000000000000000000000000000000000000cdf4033abcf612902dd58c333d29a02d2bc92b00d900c1b61cdc9afa0855ebce43f8e3dea9ca9ef6ca8a2d914f99c08c0610c41c3cc0a4f0bb0f755529ae96aa02a9d6025bc8f2a65a1bec399783b65aa6506c7aca505d9889593436407cce5f743f4f8000000000000000000000000000000000000000000000000000000000000001b26b7c6583daa918f078eed15153c163acd02dfc231f8b1b0a279f7c3ae7bab176148d65b3645fbd658f0d0f3d5ca70a04e6058a0cfb7352b371f7f70b258769661e7ad7abf2e2c59e35e5a15008e6e7dcb96f45b479452f1a34051d215ecab0d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b2b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a54eeab737000000000000000000000000000000000000000000000000002e15a55bcd42ff00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000034b95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab744a6ef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979595751354d7a6b344d53316d5a446b784c5455304d444d744f4442684e43316b4d44686b4e44566d4e4749354d6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000091761e6fc917d0d31093d400030402200c1d1d79000000000000000000000000000000000000000000000000000000000cdf4033000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xabcf612902dd58c333d29a02d2bc92b00d900c1b61cdc9afa0855ebce43f8e3d",
      "signature": {
        "s": "0x25bc8f2a65a1bec399783b65aa6506c7aca505d9889593436407cce5f743f4f8",
        "r": "0xea9ca9ef6ca8a2d914f99c08c0610c41c3cc0a4f0bb0f755529ae96aa02a9d60",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x26b7c6583daa918f078eed15153c163acd02dfc231f8b1b0a279f7c3ae7bab17",
      "signature": {
        "s": "0x61e7ad7abf2e2c59e35e5a15008e6e7dcb96f45b479452f1a34051d215ecab0d",
        "r": "0x6148d65b3645fbd658f0d0f3d5ca70a04e6058a0cfb7352b371f7f70b2587696",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "215957555",
    "total": "215957555"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "215957555",
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
            "amount": "46024402671"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "215957"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYWQ5Mzk4MS1mZDkxLTU0MDMtODBhNC1kMDhkNDVmNGI5MmMifQ==",
    "nonce": 6955,
    "balances": {
      "current": "12971648666482487",
      "previous": "12971648882655999"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x91761e6fc917d0d31093d400030402200c1d1d79",
    "nonce": 22,
    "balances": {
      "current": "215957555",
      "previous": "0"
    }
  },
  "blockNumber": "10114723",
  "created": "2020-05-22T08:53:00.360Z",
  "updated": "2020-05-22T08:53:00.445Z",
  "id": "5ec792ec005df800101bcb4e"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000cdf4033000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `215957555`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`