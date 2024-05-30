# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x94e7F4d3a3158d845C30a17D5454607551D4b572`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000b6d6dc8d828ebf3d7000000000000000000000000000000000000000000000000455bcddb625c8de70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000455bcddb625c8de70000000000000000000000000000000000000000000000079a4520afb0fb0e31f8d73f4da59e8ed1b3bf41e514ddc2337fc1c657f732a6ee37fc515a448ae37686d3d039841a5211832236800cab735c493398a06850da17bd23a4bfef391fdc19da9c7840c5dde3df9c506c62e0503b16b052bce6e6cc14f3428c3b5c67d1d7000000000000000000000000000000000000000000000000000000000000001b4223d3cd2c2afc09510c6d493591071508febed8f9387a5ec5e574e62c9168060587f6fbf45e5ebde02a487b0605f7344022afc8b72a6247409c495569c572f44a589deeebd814070b8f9f7235ae15eba2c4819492995cf071625ff9052f0dfc000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adf6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009640949a03790464d65d000000000000000000000000000000000000000000009640da0792d0c7e0b75900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000011c17c611f53150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f4e5a065fe385b090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f4463784e5463325a5331685a6a6b7a4c5455354e7a4d74596d46695a6930304d474a6c595745325a4451324e6d596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000094e7f4d3a3158d845c30a17d5454607551d4b57200000000000000000000000000000000000000000000000b6d6dc8d828ebf3d700000000000000000000000000000000000000000000000b2811fafcc68f65f000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8d73f4da59e8ed1b3bf41e514ddc2337fc1c657f732a6ee37fc515a448ae376",
      "signature": {
        "s": "0x19da9c7840c5dde3df9c506c62e0503b16b052bce6e6cc14f3428c3b5c67d1d7",
        "r": "0x86d3d039841a5211832236800cab735c493398a06850da17bd23a4bfef391fdc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4223d3cd2c2afc09510c6d493591071508febed8f9387a5ec5e574e62c916806",
      "signature": {
        "s": "0x4a589deeebd814070b8f9f7235ae15eba2c4819492995cf071625ff9052f0dfc",
        "r": "0x0587f6fbf45e5ebde02a487b0605f7344022afc8b72a6247409c495569c572f4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4997814553629461991",
    "total": "140243535710161407537"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4997814553629461991",
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
            "amount": "27263487683943846140681"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4997814553629461"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiODcxNTc2ZS1hZjkzLTU5NzMtYmFiZi00MGJlYWE2ZDQ2NmYifQ==",
    "nonce": 110070,
    "balances": {
      "current": "709546271926046519776861",
      "previous": "709551274738414702868313"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x94e7f4d3a3158d845c30a17d5454607551d4b572",
    "nonce": 46,
    "balances": {
      "current": "210799364164125717463",
      "previous": "205801549610496255472"
    }
  },
  "blockNumber": "14709961",
  "created": "2022-05-04T08:51:24.226Z",
  "updated": "2022-05-04T08:51:24.314Z",
  "id": "62723e8cbbd75600116d04ed"
}
```
* *stageAmount*: `210799364164125717463`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000455bcddb625c8de70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000455bcddb625c8de70000000000000000000000000000000000000000000000079a4520afb0fb0e31f8d73f4da59e8ed1b3bf41e514ddc2337fc1c657f732a6ee37fc515a448ae37686d3d039841a5211832236800cab735c493398a06850da17bd23a4bfef391fdc19da9c7840c5dde3df9c506c62e0503b16b052bce6e6cc14f3428c3b5c67d1d7000000000000000000000000000000000000000000000000000000000000001b4223d3cd2c2afc09510c6d493591071508febed8f9387a5ec5e574e62c9168060587f6fbf45e5ebde02a487b0605f7344022afc8b72a6247409c495569c572f44a589deeebd814070b8f9f7235ae15eba2c4819492995cf071625ff9052f0dfc000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adf6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009640949a03790464d65d000000000000000000000000000000000000000000009640da0792d0c7e0b75900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000011c17c611f53150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f4e5a065fe385b090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f4463784e5463325a5331685a6a6b7a4c5455354e7a4d74596d46695a6930304d474a6c595745325a4451324e6d596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000094e7f4d3a3158d845c30a17d5454607551d4b57200000000000000000000000000000000000000000000000b6d6dc8d828ebf3d700000000000000000000000000000000000000000000000b2811fafcc68f65f000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8d73f4da59e8ed1b3bf41e514ddc2337fc1c657f732a6ee37fc515a448ae376",
      "signature": {
        "s": "0x19da9c7840c5dde3df9c506c62e0503b16b052bce6e6cc14f3428c3b5c67d1d7",
        "r": "0x86d3d039841a5211832236800cab735c493398a06850da17bd23a4bfef391fdc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4223d3cd2c2afc09510c6d493591071508febed8f9387a5ec5e574e62c916806",
      "signature": {
        "s": "0x4a589deeebd814070b8f9f7235ae15eba2c4819492995cf071625ff9052f0dfc",
        "r": "0x0587f6fbf45e5ebde02a487b0605f7344022afc8b72a6247409c495569c572f4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4997814553629461991",
    "total": "140243535710161407537"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4997814553629461991",
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
            "amount": "27263487683943846140681"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4997814553629461"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiODcxNTc2ZS1hZjkzLTU5NzMtYmFiZi00MGJlYWE2ZDQ2NmYifQ==",
    "nonce": 110070,
    "balances": {
      "current": "709546271926046519776861",
      "previous": "709551274738414702868313"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x94e7f4d3a3158d845c30a17d5454607551d4b572",
    "nonce": 46,
    "balances": {
      "current": "210799364164125717463",
      "previous": "205801549610496255472"
    }
  },
  "blockNumber": "14709961",
  "created": "2022-05-04T08:51:24.226Z",
  "updated": "2022-05-04T08:51:24.314Z",
  "id": "62723e8cbbd75600116d04ed"
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
0x0f200f9b00000000000000000000000000000000000000000000000b6d6dc8d828ebf3d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `210799364164125717463`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`