# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA3910b7904B0c1B2ca6997713498D040b306548C`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de20fca974077e20000000000000000000000000000000000000000000004806c704a55f8e980000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000004806c704a55f8e980000000000000000000000000000000000000000000000004806c704a55f8e98000a745d177d2bb53afe50b280807236820a0e1d546b04fa8c6b9c0bc93d2048f870a2e715297faaeaddc98619f5f48debd75d87a74ab4265bdb5f8290d07a1952f5e8bc7f9472f35e3317f0a71a4de12d94866f6cc0165af542d4d551824d9498b000000000000000000000000000000000000000000000000000000000000001cd2e70f253d14060364b4dac3aa0679db3d58aa2f8973b3dbd5c125f6f2c5747c9575aff9389d4505acbcbaf8249bae0b33bf1b71dc5f389d1ccb9a2ea4e021d0558971629e2966050c9253055e9ec46810bdba28dc8ac89a3d2ee4642cdbc46a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e305100000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000a3910b7904b0c1b2ca6997713498d040b306548c0000000000000000000000000000000000000000000000000de20fca974077e2000000000000000000000000000000000000000000000481a1579597f1f2e7e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000127053b7761c8f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000127053b7761c8f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d7a426b5a5755774d5330774e6a4a684c5451784d474d7459574d774d6930784e6a55345a5752694f444d795a444d6966513d3d00000000000000000000000000000000000000000000000000000000000000f4000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000001095c3a5912959bc40a5f0000000000000000000000000000000000000000000104dbcde8c83fa2da8a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa745d177d2bb53afe50b280807236820a0e1d546b04fa8c6b9c0bc93d2048f87",
      "signature": {
        "s": "0x5e8bc7f9472f35e3317f0a71a4de12d94866f6cc0165af542d4d551824d9498b",
        "r": "0x0a2e715297faaeaddc98619f5f48debd75d87a74ab4265bdb5f8290d07a1952f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd2e70f253d14060364b4dac3aa0679db3d58aa2f8973b3dbd5c125f6f2c5747c",
      "signature": {
        "s": "0x558971629e2966050c9253055e9ec46810bdba28dc8ac89a3d2ee4642cdbc46a",
        "r": "0x9575aff9389d4505acbcbaf8249bae0b33bf1b71dc5f389d1ccb9a2ea4e021d0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21258463000000000000000",
    "total": "21258463000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21258463000000000000000",
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
            "amount": "21258463000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21258463000000000000"
      }
    },
    "wallet": "0xa3910b7904b0c1b2ca6997713498d040b306548c",
    "data": "eyJyZWYiOiI5MzBkZWUwMS0wNjJhLTQxMGMtYWMwMi0xNjU4ZWRiODMyZDMifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000379430025066466",
      "previous": "21280721842430025066466"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 244,
    "balances": {
      "current": "1253128422827398160190047",
      "previous": "1231869959827398160190047"
    }
  },
  "blockNumber": "14877968",
  "created": "2022-05-31T09:34:18.747Z",
  "updated": "2022-05-31T09:34:18.845Z",
  "id": "6295e11a7832e20011830f6c"
}
```
* *stageAmount*: `1000379430025066466`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000004806c704a55f8e980000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000004806c704a55f8e980000000000000000000000000000000000000000000000004806c704a55f8e98000a745d177d2bb53afe50b280807236820a0e1d546b04fa8c6b9c0bc93d2048f870a2e715297faaeaddc98619f5f48debd75d87a74ab4265bdb5f8290d07a1952f5e8bc7f9472f35e3317f0a71a4de12d94866f6cc0165af542d4d551824d9498b000000000000000000000000000000000000000000000000000000000000001cd2e70f253d14060364b4dac3aa0679db3d58aa2f8973b3dbd5c125f6f2c5747c9575aff9389d4505acbcbaf8249bae0b33bf1b71dc5f389d1ccb9a2ea4e021d0558971629e2966050c9253055e9ec46810bdba28dc8ac89a3d2ee4642cdbc46a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e305100000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f000000000000000000000000a3910b7904b0c1b2ca6997713498d040b306548c0000000000000000000000000000000000000000000000000de20fca974077e2000000000000000000000000000000000000000000000481a1579597f1f2e7e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000127053b7761c8f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000127053b7761c8f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d7a426b5a5755774d5330774e6a4a684c5451784d474d7459574d774d6930784e6a55345a5752694f444d795a444d6966513d3d00000000000000000000000000000000000000000000000000000000000000f4000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000001095c3a5912959bc40a5f0000000000000000000000000000000000000000000104dbcde8c83fa2da8a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa745d177d2bb53afe50b280807236820a0e1d546b04fa8c6b9c0bc93d2048f87",
      "signature": {
        "s": "0x5e8bc7f9472f35e3317f0a71a4de12d94866f6cc0165af542d4d551824d9498b",
        "r": "0x0a2e715297faaeaddc98619f5f48debd75d87a74ab4265bdb5f8290d07a1952f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd2e70f253d14060364b4dac3aa0679db3d58aa2f8973b3dbd5c125f6f2c5747c",
      "signature": {
        "s": "0x558971629e2966050c9253055e9ec46810bdba28dc8ac89a3d2ee4642cdbc46a",
        "r": "0x9575aff9389d4505acbcbaf8249bae0b33bf1b71dc5f389d1ccb9a2ea4e021d0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21258463000000000000000",
    "total": "21258463000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21258463000000000000000",
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
            "amount": "21258463000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21258463000000000000"
      }
    },
    "wallet": "0xa3910b7904b0c1b2ca6997713498d040b306548c",
    "data": "eyJyZWYiOiI5MzBkZWUwMS0wNjJhLTQxMGMtYWMwMi0xNjU4ZWRiODMyZDMifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000379430025066466",
      "previous": "21280721842430025066466"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 244,
    "balances": {
      "current": "1253128422827398160190047",
      "previous": "1231869959827398160190047"
    }
  },
  "blockNumber": "14877968",
  "created": "2022-05-31T09:34:18.747Z",
  "updated": "2022-05-31T09:34:18.845Z",
  "id": "6295e11a7832e20011830f6c"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de20fca974077e20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000379430025066466`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`