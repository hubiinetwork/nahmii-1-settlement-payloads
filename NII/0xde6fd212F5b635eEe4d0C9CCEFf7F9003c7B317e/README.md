# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xde6fd212F5b635eEe4d0C9CCEFf7F9003c7B317e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000016ab6a5e365e89721000000000000000000000000000000000000000000000000640a2e1507c7d9ff0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000640a2e1507c7d9ff0000000000000000000000000000000000000000000000016ab6a5e365e897217cf88e43dfc9441e25ed1ab18a3cc14db59aa18f68de7b42dacf3136d4a3cce8226097e8781e9db227bad425c7c948559ebebfc8ea0348ca1148358b3b2772d0529f96f949afde2506ab73048361f8c7e97ce1881a8d0785a8c2cd0f5701a201000000000000000000000000000000000000000000000000000000000000001ba5e6fda476edabbe1bdb3e055169404506eb92f7b157501cef1d2d044ad9a5d4da9f71b5be203a5b0e17c37ed4be65e68d8f22a13eb8a4a9399f4cf25583618d293f2ed6f5edb0780b70f47e38a6da6440de3e6799ef44b91cce05a75cd01909000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7db000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000019db3e10c7cf90621c6b0000000000000000000000000000000000000000000019dba234921959f6b4d700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000199c34c1ccbe6d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e5c528c4c611015a8b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d6d4535596a41774f5330304e4451324c54566d5a446b744f4755324f43316b4d7a6c69596d4533597a6b324f47596966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000de6fd212f5b635eee4d0c9cceff7f9003c7b317e0000000000000000000000000000000000000000000000016ab6a5e365e8972100000000000000000000000000000000000000000000000106ac77ce5e20bd2200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7cf88e43dfc9441e25ed1ab18a3cc14db59aa18f68de7b42dacf3136d4a3cce8",
      "signature": {
        "s": "0x529f96f949afde2506ab73048361f8c7e97ce1881a8d0785a8c2cd0f5701a201",
        "r": "0x226097e8781e9db227bad425c7c948559ebebfc8ea0348ca1148358b3b2772d0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa5e6fda476edabbe1bdb3e055169404506eb92f7b157501cef1d2d044ad9a5d4",
      "signature": {
        "s": "0x293f2ed6f5edb0780b70f47e38a6da6440de3e6799ef44b91cce05a75cd01909",
        "r": "0xda9f71b5be203a5b0e17c37ed4be65e68d8f22a13eb8a4a9399f4cf25583618d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7208624821419629055",
    "total": "26136259883577153313"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7208624821419629055",
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
            "amount": "27850343628607221488267"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7208624821419629"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMmE5YjAwOS00NDQ2LTVmZDktOGU2OC1kMzliYmE3Yzk2OGYifQ==",
    "nonce": 112603,
    "balances": {
      "current": "122103471318007795555435",
      "previous": "122110687151454036604119"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xde6fd212f5b635eee4d0c9cceff7f9003c7b317e",
    "nonce": 5,
    "balances": {
      "current": "26136259883577153313",
      "previous": "18927635062157524258"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:44.526Z",
  "updated": "2022-05-04T09:04:44.628Z",
  "id": "627241ac3592fd001130b7bc"
}
```
* *stageAmount*: `26136259883577153313`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000640a2e1507c7d9ff0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000640a2e1507c7d9ff0000000000000000000000000000000000000000000000016ab6a5e365e897217cf88e43dfc9441e25ed1ab18a3cc14db59aa18f68de7b42dacf3136d4a3cce8226097e8781e9db227bad425c7c948559ebebfc8ea0348ca1148358b3b2772d0529f96f949afde2506ab73048361f8c7e97ce1881a8d0785a8c2cd0f5701a201000000000000000000000000000000000000000000000000000000000000001ba5e6fda476edabbe1bdb3e055169404506eb92f7b157501cef1d2d044ad9a5d4da9f71b5be203a5b0e17c37ed4be65e68d8f22a13eb8a4a9399f4cf25583618d293f2ed6f5edb0780b70f47e38a6da6440de3e6799ef44b91cce05a75cd01909000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7db000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000019db3e10c7cf90621c6b0000000000000000000000000000000000000000000019dba234921959f6b4d700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000199c34c1ccbe6d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e5c528c4c611015a8b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d6d4535596a41774f5330304e4451324c54566d5a446b744f4755324f43316b4d7a6c69596d4533597a6b324f47596966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000de6fd212f5b635eee4d0c9cceff7f9003c7b317e0000000000000000000000000000000000000000000000016ab6a5e365e8972100000000000000000000000000000000000000000000000106ac77ce5e20bd2200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7cf88e43dfc9441e25ed1ab18a3cc14db59aa18f68de7b42dacf3136d4a3cce8",
      "signature": {
        "s": "0x529f96f949afde2506ab73048361f8c7e97ce1881a8d0785a8c2cd0f5701a201",
        "r": "0x226097e8781e9db227bad425c7c948559ebebfc8ea0348ca1148358b3b2772d0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa5e6fda476edabbe1bdb3e055169404506eb92f7b157501cef1d2d044ad9a5d4",
      "signature": {
        "s": "0x293f2ed6f5edb0780b70f47e38a6da6440de3e6799ef44b91cce05a75cd01909",
        "r": "0xda9f71b5be203a5b0e17c37ed4be65e68d8f22a13eb8a4a9399f4cf25583618d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7208624821419629055",
    "total": "26136259883577153313"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7208624821419629055",
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
            "amount": "27850343628607221488267"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7208624821419629"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMmE5YjAwOS00NDQ2LTVmZDktOGU2OC1kMzliYmE3Yzk2OGYifQ==",
    "nonce": 112603,
    "balances": {
      "current": "122103471318007795555435",
      "previous": "122110687151454036604119"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xde6fd212f5b635eee4d0c9cceff7f9003c7b317e",
    "nonce": 5,
    "balances": {
      "current": "26136259883577153313",
      "previous": "18927635062157524258"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:44.526Z",
  "updated": "2022-05-04T09:04:44.628Z",
  "id": "627241ac3592fd001130b7bc"
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
0x0f200f9b0000000000000000000000000000000000000000000000016ab6a5e365e897210000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `26136259883577153313`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`