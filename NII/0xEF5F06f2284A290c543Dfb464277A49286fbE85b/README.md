# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xEF5F06f2284A290c543Dfb464277A49286fbE85b`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001324c3cb0b0001b98000000000000000000000000000000000000000000000000106713b0938b32910000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000106713b0938b32910000000000000000000000000000000000000000000000012ca0ca268f9206014b6163f2e73424818f52878b67be35fc62b8c3ad89162ca5efa1a20620de98aed23a5ae7f86bce80de917c15d2d524dd91b1e976e4999900c4cba40f78fb12ec6fbd8fbd5e81a6480c64888617c739017e3930e6881f2c9ed583de77ce529647000000000000000000000000000000000000000000000000000000000000001cc74d1a5d4258550a24473e9a0830f8cc05f0c21b80a44c0f580fce669ca5abe44d0d0cd7485c7fadd36a8be761affbad155c15b1c8a795a96df3320ba12a8b8d600b374d2546507d2b91e8a8d5e40d70decceacc32c2df526aaee4bbe3c32129000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b316000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003fc7dacfe145ee69c426000000000000000000000000000000000000000000003fc7eb3b27ed3654143400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000432f6b45f1d7d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc123cc812abe474c60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f544a695a4452684d43307a4f5746684c5455334d7a4974596d526a4d53307a595755354f574e6b4e7a597a4d7a516966513d3d000000000000000000000000000000000000000000000000000000000000001f000000000000000000000000ef5f06f2284a290c543dfb464277a49286fbe85b000000000000000000000000000000000000000000000001324c3cb0b0001b9800000000000000000000000000000000000000000000000121e529001c74e90700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4b6163f2e73424818f52878b67be35fc62b8c3ad89162ca5efa1a20620de98ae",
      "signature": {
        "s": "0x6fbd8fbd5e81a6480c64888617c739017e3930e6881f2c9ed583de77ce529647",
        "r": "0xd23a5ae7f86bce80de917c15d2d524dd91b1e976e4999900c4cba40f78fb12ec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc74d1a5d4258550a24473e9a0830f8cc05f0c21b80a44c0f580fce669ca5abe4",
      "signature": {
        "s": "0x600b374d2546507d2b91e8a8d5e40d70decceacc32c2df526aaee4bbe3c32129",
        "r": "0x4d0d0cd7485c7fadd36a8be761affbad155c15b1c8a795a96df3320ba12a8b8d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1181935076318589585",
    "total": "21662536474618365441"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1181935076318589585",
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
            "amount": "27671430255738131608774"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1181935076318589"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3OTJiZDRhMC0zOWFhLTU3MzItYmRjMS0zYWU5OWNkNzYzMzQifQ==",
    "nonce": 111382,
    "balances": {
      "current": "301195757559966765532198",
      "previous": "301196940676978160440372"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xef5f06f2284a290c543dfb464277a49286fbe85b",
    "nonce": 31,
    "balances": {
      "current": "22071082603400666008",
      "previous": "20889147527082076423"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:01.054Z",
  "updated": "2022-05-04T08:58:01.162Z",
  "id": "627240193592fd001130b61b"
}
```
* *stageAmount*: `22071082603400666008`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000106713b0938b32910000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000106713b0938b32910000000000000000000000000000000000000000000000012ca0ca268f9206014b6163f2e73424818f52878b67be35fc62b8c3ad89162ca5efa1a20620de98aed23a5ae7f86bce80de917c15d2d524dd91b1e976e4999900c4cba40f78fb12ec6fbd8fbd5e81a6480c64888617c739017e3930e6881f2c9ed583de77ce529647000000000000000000000000000000000000000000000000000000000000001cc74d1a5d4258550a24473e9a0830f8cc05f0c21b80a44c0f580fce669ca5abe44d0d0cd7485c7fadd36a8be761affbad155c15b1c8a795a96df3320ba12a8b8d600b374d2546507d2b91e8a8d5e40d70decceacc32c2df526aaee4bbe3c32129000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b316000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003fc7dacfe145ee69c426000000000000000000000000000000000000000000003fc7eb3b27ed3654143400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000432f6b45f1d7d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc123cc812abe474c60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f544a695a4452684d43307a4f5746684c5455334d7a4974596d526a4d53307a595755354f574e6b4e7a597a4d7a516966513d3d000000000000000000000000000000000000000000000000000000000000001f000000000000000000000000ef5f06f2284a290c543dfb464277a49286fbe85b000000000000000000000000000000000000000000000001324c3cb0b0001b9800000000000000000000000000000000000000000000000121e529001c74e90700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4b6163f2e73424818f52878b67be35fc62b8c3ad89162ca5efa1a20620de98ae",
      "signature": {
        "s": "0x6fbd8fbd5e81a6480c64888617c739017e3930e6881f2c9ed583de77ce529647",
        "r": "0xd23a5ae7f86bce80de917c15d2d524dd91b1e976e4999900c4cba40f78fb12ec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc74d1a5d4258550a24473e9a0830f8cc05f0c21b80a44c0f580fce669ca5abe4",
      "signature": {
        "s": "0x600b374d2546507d2b91e8a8d5e40d70decceacc32c2df526aaee4bbe3c32129",
        "r": "0x4d0d0cd7485c7fadd36a8be761affbad155c15b1c8a795a96df3320ba12a8b8d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1181935076318589585",
    "total": "21662536474618365441"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1181935076318589585",
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
            "amount": "27671430255738131608774"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1181935076318589"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3OTJiZDRhMC0zOWFhLTU3MzItYmRjMS0zYWU5OWNkNzYzMzQifQ==",
    "nonce": 111382,
    "balances": {
      "current": "301195757559966765532198",
      "previous": "301196940676978160440372"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xef5f06f2284a290c543dfb464277a49286fbe85b",
    "nonce": 31,
    "balances": {
      "current": "22071082603400666008",
      "previous": "20889147527082076423"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:01.054Z",
  "updated": "2022-05-04T08:58:01.162Z",
  "id": "627240193592fd001130b61b"
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
0x0f200f9b000000000000000000000000000000000000000000000001324c3cb0b0001b980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `22071082603400666008`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`