# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7858267C70a407d7105FB12A2EddC2FEda90eF4E`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000ad19af5dbab92000000000000000000000000000000000000000000000000000045963976df700000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000045963976df70000000000000000000000000000000000000000000000000000ad19af5dbab9267956c1b0d7893dbe858221e184d0ac22d7daf308e181ffba0fe2fb23c076a3af8a70771055e707e29396c56000e19503bce6c3455a8253f5a1f331f831073c45e268966f9b35c25d4051b5b9a5bbe015c07c42c90f1d419409aa43974e671cb000000000000000000000000000000000000000000000000000000000000001cec164e07f18c0f1dcea73874fa49ed93b0d5aec52a4b6e98cad297514b2827b26cbf722e6adc004f664bf39ca1061359c26d8cd2218fff031f16013d7e5853f37b74e2ffb777961f6558e574d37adc4f6646e813495692da523cba20723cbe08000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b4ad000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000394366e9dfec2360a67100000000000000000000000000000000000000000000394366ea25942d4889af00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000011d07103ce0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddbcef43dac0cf7dbf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69597a4d344e4755334e6930324e6a4e684c5455325a57457459544d334d4330354f5446684e545a6c5a4755314d6d496966513d3d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000007858267c70a407d7105fb12a2eddc2feda90ef4e000000000000000000000000000000000000000000000000000ad19af5dbab92000000000000000000000000000000000000000000000000000a8c04bc64cc2200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x67956c1b0d7893dbe858221e184d0ac22d7daf308e181ffba0fe2fb23c076a3a",
      "signature": {
        "s": "0x5e268966f9b35c25d4051b5b9a5bbe015c07c42c90f1d419409aa43974e671cb",
        "r": "0xf8a70771055e707e29396c56000e19503bce6c3455a8253f5a1f331f831073c4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xec164e07f18c0f1dcea73874fa49ed93b0d5aec52a4b6e98cad297514b2827b2",
      "signature": {
        "s": "0x7b74e2ffb777961f6558e574d37adc4f6646e813495692da523cba20723cbe08",
        "r": "0x6cbf722e6adc004f664bf39ca1061359c26d8cd2218fff031f16013d7e5853f3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "76511511502704",
    "total": "3045213247089554"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76511511502704",
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
            "amount": "27702177029443418029503"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "76511511502"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiYzM4NGU3Ni02NjNhLTU2ZWEtYTM3MC05OTFhNTZlZGU1MmIifQ==",
    "nonce": 111789,
    "balances": {
      "current": "270418237080975058183793",
      "previous": "270418237157563081197999"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7858267c70a407d7105fb12a2eddc2feda90ef4e",
    "nonce": 27,
    "balances": {
      "current": "3045213247089554",
      "previous": "2968701735586850"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T09:00:13.438Z",
  "updated": "2022-05-04T09:00:13.514Z",
  "id": "6272409d3592fd001130b6a6"
}
```
* *stageAmount*: `3045213247089554`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000045963976df700000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000045963976df70000000000000000000000000000000000000000000000000000ad19af5dbab9267956c1b0d7893dbe858221e184d0ac22d7daf308e181ffba0fe2fb23c076a3af8a70771055e707e29396c56000e19503bce6c3455a8253f5a1f331f831073c45e268966f9b35c25d4051b5b9a5bbe015c07c42c90f1d419409aa43974e671cb000000000000000000000000000000000000000000000000000000000000001cec164e07f18c0f1dcea73874fa49ed93b0d5aec52a4b6e98cad297514b2827b26cbf722e6adc004f664bf39ca1061359c26d8cd2218fff031f16013d7e5853f37b74e2ffb777961f6558e574d37adc4f6646e813495692da523cba20723cbe08000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b4ad000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000394366e9dfec2360a67100000000000000000000000000000000000000000000394366ea25942d4889af00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000011d07103ce0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddbcef43dac0cf7dbf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69597a4d344e4755334e6930324e6a4e684c5455325a57457459544d334d4330354f5446684e545a6c5a4755314d6d496966513d3d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000007858267c70a407d7105fb12a2eddc2feda90ef4e000000000000000000000000000000000000000000000000000ad19af5dbab92000000000000000000000000000000000000000000000000000a8c04bc64cc2200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x67956c1b0d7893dbe858221e184d0ac22d7daf308e181ffba0fe2fb23c076a3a",
      "signature": {
        "s": "0x5e268966f9b35c25d4051b5b9a5bbe015c07c42c90f1d419409aa43974e671cb",
        "r": "0xf8a70771055e707e29396c56000e19503bce6c3455a8253f5a1f331f831073c4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xec164e07f18c0f1dcea73874fa49ed93b0d5aec52a4b6e98cad297514b2827b2",
      "signature": {
        "s": "0x7b74e2ffb777961f6558e574d37adc4f6646e813495692da523cba20723cbe08",
        "r": "0x6cbf722e6adc004f664bf39ca1061359c26d8cd2218fff031f16013d7e5853f3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "76511511502704",
    "total": "3045213247089554"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76511511502704",
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
            "amount": "27702177029443418029503"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "76511511502"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiYzM4NGU3Ni02NjNhLTU2ZWEtYTM3MC05OTFhNTZlZGU1MmIifQ==",
    "nonce": 111789,
    "balances": {
      "current": "270418237080975058183793",
      "previous": "270418237157563081197999"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7858267c70a407d7105fb12a2eddc2feda90ef4e",
    "nonce": 27,
    "balances": {
      "current": "3045213247089554",
      "previous": "2968701735586850"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T09:00:13.438Z",
  "updated": "2022-05-04T09:00:13.514Z",
  "id": "6272409d3592fd001130b6a6"
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
0x0f200f9b000000000000000000000000000000000000000000000000000ad19af5dbab920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3045213247089554`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`