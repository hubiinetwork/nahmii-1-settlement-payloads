# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x11102719cfFfc09d938B5b705bd008d15955CDF3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000cbcc05735a4a576b000000000000000000000000000000000000000000000000cbcc05735a4a576b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000cbcc05735a4a576b000000000000000000000000000000000000000000000000cbcc05735a4a576b4583d5c0d427e4bcb2c7d726c82eeb355bde37629ce95f1612f712a7c13eb30cadbd09926cd3e194e6bbab84b155f4563012fffb81b665da646feb2c27918d59572fe031780e12f7cb62230de1d2ae4c73c7284b35e5df4d280a564bfcc834f9000000000000000000000000000000000000000000000000000000000000001c4c80b116db07046ac106d6d7d687ae1754821a1858bac33fd2a55ec7a8735369d78335e7e90b836c4b61f4bf8036a7aad5abe6d7631cd0412843075bdfe7cc2a2c42d9ad1ca4a927e1ad1c16d5a8c0a8f44d92e9874bbe4d6beefe6d5d543b00000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012e2b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000022dac2643b08e4a767690000000000000000000000000000000000000000000022db8e646c85d54e7de400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000342c09965cbf100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038fc0e2a3f91aa953130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a4449314f54517a4d7930344d6a55334c545669596a41745954466d4e43316b4d4751354d4449794d3246695a6a556966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000011102719cfffc09d938b5b705bd008d15955cdf3000000000000000000000000000000000000000000000000cbcc05735a4a576b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4583d5c0d427e4bcb2c7d726c82eeb355bde37629ce95f1612f712a7c13eb30c",
      "signature": {
        "s": "0x572fe031780e12f7cb62230de1d2ae4c73c7284b35e5df4d280a564bfcc834f9",
        "r": "0xadbd09926cd3e194e6bbab84b155f4563012fffb81b665da646feb2c27918d59",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4c80b116db07046ac106d6d7d687ae1754821a1858bac33fd2a55ec7a8735369",
      "signature": {
        "s": "0x2c42d9ad1ca4a927e1ad1c16d5a8c0a8f44d92e9874bbe4d6beefe6d5d543b00",
        "r": "0xd78335e7e90b836c4b61f4bf8036a7aad5abe6d7631cd0412843075bdfe7cc2a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "14685118477942544235",
    "total": "14685118477942544235"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14685118477942544235",
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
            "amount": "16818882702839709782803"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "14685118477942544"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhZDI1OTQzMy04MjU3LTViYjAtYTFmNC1kMGQ5MDIyM2FiZjUifQ==",
    "nonce": 77355,
    "balances": {
      "current": "164595858011287030556521",
      "previous": "164610557814883451043300"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x11102719cfffc09d938b5b705bd008d15955cdf3",
    "nonce": 1,
    "balances": {
      "current": "14685118477942544235",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:45.234Z",
  "updated": "2021-06-04T12:46:45.313Z",
  "id": "60ba20b5010ba300120bfddc"
}
```
* *stageAmount*: `14685118477942544235`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000cbcc05735a4a576b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000cbcc05735a4a576b000000000000000000000000000000000000000000000000cbcc05735a4a576b4583d5c0d427e4bcb2c7d726c82eeb355bde37629ce95f1612f712a7c13eb30cadbd09926cd3e194e6bbab84b155f4563012fffb81b665da646feb2c27918d59572fe031780e12f7cb62230de1d2ae4c73c7284b35e5df4d280a564bfcc834f9000000000000000000000000000000000000000000000000000000000000001c4c80b116db07046ac106d6d7d687ae1754821a1858bac33fd2a55ec7a8735369d78335e7e90b836c4b61f4bf8036a7aad5abe6d7631cd0412843075bdfe7cc2a2c42d9ad1ca4a927e1ad1c16d5a8c0a8f44d92e9874bbe4d6beefe6d5d543b00000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012e2b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000022dac2643b08e4a767690000000000000000000000000000000000000000000022db8e646c85d54e7de400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000342c09965cbf100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038fc0e2a3f91aa953130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a4449314f54517a4d7930344d6a55334c545669596a41745954466d4e43316b4d4751354d4449794d3246695a6a556966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000011102719cfffc09d938b5b705bd008d15955cdf3000000000000000000000000000000000000000000000000cbcc05735a4a576b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4583d5c0d427e4bcb2c7d726c82eeb355bde37629ce95f1612f712a7c13eb30c",
      "signature": {
        "s": "0x572fe031780e12f7cb62230de1d2ae4c73c7284b35e5df4d280a564bfcc834f9",
        "r": "0xadbd09926cd3e194e6bbab84b155f4563012fffb81b665da646feb2c27918d59",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4c80b116db07046ac106d6d7d687ae1754821a1858bac33fd2a55ec7a8735369",
      "signature": {
        "s": "0x2c42d9ad1ca4a927e1ad1c16d5a8c0a8f44d92e9874bbe4d6beefe6d5d543b00",
        "r": "0xd78335e7e90b836c4b61f4bf8036a7aad5abe6d7631cd0412843075bdfe7cc2a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "14685118477942544235",
    "total": "14685118477942544235"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14685118477942544235",
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
            "amount": "16818882702839709782803"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "14685118477942544"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhZDI1OTQzMy04MjU3LTViYjAtYTFmNC1kMGQ5MDIyM2FiZjUifQ==",
    "nonce": 77355,
    "balances": {
      "current": "164595858011287030556521",
      "previous": "164610557814883451043300"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x11102719cfffc09d938b5b705bd008d15955cdf3",
    "nonce": 1,
    "balances": {
      "current": "14685118477942544235",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:45.234Z",
  "updated": "2021-06-04T12:46:45.313Z",
  "id": "60ba20b5010ba300120bfddc"
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
0x0f200f9b000000000000000000000000000000000000000000000000cbcc05735a4a576b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14685118477942544235`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`