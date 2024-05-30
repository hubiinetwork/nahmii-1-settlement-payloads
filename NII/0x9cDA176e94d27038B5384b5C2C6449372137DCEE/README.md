# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9cDA176e94d27038B5384b5C2C6449372137DCEE`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000d6b27829865681f1000000000000000000000000000000000000000000000000000000001c1b84770000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001c1b84770000000000000000000000000000000000000000000000004195b6375f06f571d9794737fa0466ad4d62fd2a7a751720b5acafc8ad88d2d42cf43e5e7a17713972b6bacf6908e8b361febbf778e015576f77927628df68d2b2494649b88d16bd3a2876228fe0e8b9b53bc1cc9979efbb6bc26cc0d0e80d6a12c8ce8e77960ef2000000000000000000000000000000000000000000000000000000000000001b35814fb9a9a8d3295657770df0fc7d045036cc452082bbff135ed7bd84a924f2d5dff59dca90fa3a90b6459b5c72a582e5feb8168d40b204fde21cd804e361343635cdb88690518c1d9feacbd5dddbe780ba578af64c04f24b8aa63217f3830a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2ad000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000472d0c3017067f19ba4500000000000000000000000000000000000000000000472d0c3017069b3c70c900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000007320d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da2e107110f1d2610b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e7a68684f4459794e69316d5a6a49304c54557859545974596a45334e69316a5a574e685a4445304d3249354d7a456966513d3d000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000009cda176e94d27038b5384b5c2c6449372137dcee000000000000000000000000000000000000000000000000d6b27829865681f1000000000000000000000000000000000000000000000000d6b278296a3afd7a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd9794737fa0466ad4d62fd2a7a751720b5acafc8ad88d2d42cf43e5e7a177139",
      "signature": {
        "s": "0x3a2876228fe0e8b9b53bc1cc9979efbb6bc26cc0d0e80d6a12c8ce8e77960ef2",
        "r": "0x72b6bacf6908e8b361febbf778e015576f77927628df68d2b2494649b88d16bd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x35814fb9a9a8d3295657770df0fc7d045036cc452082bbff135ed7bd84a924f2",
      "signature": {
        "s": "0x3635cdb88690518c1d9feacbd5dddbe780ba578af64c04f24b8aa63217f3830a",
        "r": "0xd5dff59dca90fa3a90b6459b5c72a582e5feb8168d40b204fde21cd804e36134",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "471565431",
    "total": "4725883732928951665"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "471565431",
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
            "amount": "27636541899659870888203"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "471565"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjNzhhODYyNi1mZjI0LTUxYTYtYjE3Ni1jZWNhZDE0M2I5MzEifQ==",
    "nonce": 111277,
    "balances": {
      "current": "336119001994305746876997",
      "previous": "336119001994306218913993"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9cda176e94d27038b5384b5c2c6449372137dcee",
    "nonce": 30,
    "balances": {
      "current": "15470559789713883633",
      "previous": "15470559789242318202"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:28.094Z",
  "updated": "2022-05-04T08:57:28.151Z",
  "id": "62723ff83592fd001130b5f7"
}
```
* *stageAmount*: `15470559789713883633`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001c1b84770000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001c1b84770000000000000000000000000000000000000000000000004195b6375f06f571d9794737fa0466ad4d62fd2a7a751720b5acafc8ad88d2d42cf43e5e7a17713972b6bacf6908e8b361febbf778e015576f77927628df68d2b2494649b88d16bd3a2876228fe0e8b9b53bc1cc9979efbb6bc26cc0d0e80d6a12c8ce8e77960ef2000000000000000000000000000000000000000000000000000000000000001b35814fb9a9a8d3295657770df0fc7d045036cc452082bbff135ed7bd84a924f2d5dff59dca90fa3a90b6459b5c72a582e5feb8168d40b204fde21cd804e361343635cdb88690518c1d9feacbd5dddbe780ba578af64c04f24b8aa63217f3830a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2ad000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000472d0c3017067f19ba4500000000000000000000000000000000000000000000472d0c3017069b3c70c900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000007320d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da2e107110f1d2610b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e7a68684f4459794e69316d5a6a49304c54557859545974596a45334e69316a5a574e685a4445304d3249354d7a456966513d3d000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000009cda176e94d27038b5384b5c2c6449372137dcee000000000000000000000000000000000000000000000000d6b27829865681f1000000000000000000000000000000000000000000000000d6b278296a3afd7a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd9794737fa0466ad4d62fd2a7a751720b5acafc8ad88d2d42cf43e5e7a177139",
      "signature": {
        "s": "0x3a2876228fe0e8b9b53bc1cc9979efbb6bc26cc0d0e80d6a12c8ce8e77960ef2",
        "r": "0x72b6bacf6908e8b361febbf778e015576f77927628df68d2b2494649b88d16bd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x35814fb9a9a8d3295657770df0fc7d045036cc452082bbff135ed7bd84a924f2",
      "signature": {
        "s": "0x3635cdb88690518c1d9feacbd5dddbe780ba578af64c04f24b8aa63217f3830a",
        "r": "0xd5dff59dca90fa3a90b6459b5c72a582e5feb8168d40b204fde21cd804e36134",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "471565431",
    "total": "4725883732928951665"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "471565431",
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
            "amount": "27636541899659870888203"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "471565"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjNzhhODYyNi1mZjI0LTUxYTYtYjE3Ni1jZWNhZDE0M2I5MzEifQ==",
    "nonce": 111277,
    "balances": {
      "current": "336119001994305746876997",
      "previous": "336119001994306218913993"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9cda176e94d27038b5384b5c2c6449372137dcee",
    "nonce": 30,
    "balances": {
      "current": "15470559789713883633",
      "previous": "15470559789242318202"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:28.094Z",
  "updated": "2022-05-04T08:57:28.151Z",
  "id": "62723ff83592fd001130b5f7"
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
0x0f200f9b000000000000000000000000000000000000000000000000d6b27829865681f10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `15470559789713883633`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`