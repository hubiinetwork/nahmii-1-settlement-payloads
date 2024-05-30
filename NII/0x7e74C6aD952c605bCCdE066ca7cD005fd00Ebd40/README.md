# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7e74C6aD952c605bCCdE066ca7cD005fd00Ebd40`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000e0c3307c309842000000000000000000000000000000000000000000000003201fb507dd25800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000003201fb507dd258000000000000000000000000000000000000000000000000003201fb507dd2580000f8f2ee49f77530a5a547fbdcb7822c25b19ba1ba9ae3f68bca94beb725e164491075942552c9291d41bafc3f2b485d136e5132d4a92f7b31841f50f4342d45b66de84ceade85c4a0275045880874ed06384ef466dae3d52799afa99a2cc9cc29000000000000000000000000000000000000000000000000000000000000001ba472e50da3093fb9c6694e07b30f166d0db0b6f3ed174cf0636289c69fd0164991ae768629e470e29a19f9badef3d28a53ef8fbc309b55bd8e39458e8dcb61a03188bf9ab54b226d6fecce666fad1f98225656780c48d8dc81137e949619b652000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e22c90000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000140000000000000000000000007e74c6ad952c605bccde066ca7cd005fd00ebd400000000000000000000000000000000000000000000000000e0c3307c30984200000000000000000000000000000000000000000000000321cd4d231bdc8842000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000ccd4eac286700000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ccd4eac286700000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694933595441314e4749354f533168596d56694c54517a4d7a59744f57557a5a5330304d6a55314e6d466c4d4751354d32496966513d3d0000000000000000000000000000000000000000000000000000000000000069000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000593ac9b6ef1620be4770000000000000000000000000000000000000000000005908c7bb9e984e66477000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8f2ee49f77530a5a547fbdcb7822c25b19ba1ba9ae3f68bca94beb725e16449",
      "signature": {
        "s": "0x6de84ceade85c4a0275045880874ed06384ef466dae3d52799afa99a2cc9cc29",
        "r": "0x1075942552c9291d41bafc3f2b485d136e5132d4a92f7b31841f50f4342d45b6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa472e50da3093fb9c6694e07b30f166d0db0b6f3ed174cf0636289c69fd01649",
      "signature": {
        "s": "0x3188bf9ab54b226d6fecce666fad1f98225656780c48d8dc81137e949619b652",
        "r": "0x91ae768629e470e29a19f9badef3d28a53ef8fbc309b55bd8e39458e8dcb61a0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "922480000000000000000",
    "total": "922480000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "922480000000000000000",
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
            "amount": "922480000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "922480000000000000"
      }
    },
    "wallet": "0x7e74c6ad952c605bccde066ca7cd005fd00ebd40",
    "data": "eyJyZWYiOiI3YTA1NGI5OS1hYmViLTQzMzYtOWUzZS00MjU1NmFlMGQ5M2IifQ==",
    "nonce": 20,
    "balances": {
      "current": "1012240124681487392",
      "previous": "924414720124681487392"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 105,
    "balances": {
      "current": "421375063199399280527216",
      "previous": "420452583199399280527216"
    }
  },
  "blockNumber": "14822544",
  "created": "2022-05-22T09:22:01.950Z",
  "updated": "2022-05-22T09:22:02.064Z",
  "id": "628a00b97832e20011830f32"
}
```
* *stageAmount*: `1012240124681487392`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000003201fb507dd25800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000003201fb507dd258000000000000000000000000000000000000000000000000003201fb507dd2580000f8f2ee49f77530a5a547fbdcb7822c25b19ba1ba9ae3f68bca94beb725e164491075942552c9291d41bafc3f2b485d136e5132d4a92f7b31841f50f4342d45b66de84ceade85c4a0275045880874ed06384ef466dae3d52799afa99a2cc9cc29000000000000000000000000000000000000000000000000000000000000001ba472e50da3093fb9c6694e07b30f166d0db0b6f3ed174cf0636289c69fd0164991ae768629e470e29a19f9badef3d28a53ef8fbc309b55bd8e39458e8dcb61a03188bf9ab54b226d6fecce666fad1f98225656780c48d8dc81137e949619b652000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e22c90000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000140000000000000000000000007e74c6ad952c605bccde066ca7cd005fd00ebd400000000000000000000000000000000000000000000000000e0c3307c30984200000000000000000000000000000000000000000000000321cd4d231bdc8842000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000ccd4eac286700000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ccd4eac286700000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694933595441314e4749354f533168596d56694c54517a4d7a59744f57557a5a5330304d6a55314e6d466c4d4751354d32496966513d3d0000000000000000000000000000000000000000000000000000000000000069000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000593ac9b6ef1620be4770000000000000000000000000000000000000000000005908c7bb9e984e66477000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8f2ee49f77530a5a547fbdcb7822c25b19ba1ba9ae3f68bca94beb725e16449",
      "signature": {
        "s": "0x6de84ceade85c4a0275045880874ed06384ef466dae3d52799afa99a2cc9cc29",
        "r": "0x1075942552c9291d41bafc3f2b485d136e5132d4a92f7b31841f50f4342d45b6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa472e50da3093fb9c6694e07b30f166d0db0b6f3ed174cf0636289c69fd01649",
      "signature": {
        "s": "0x3188bf9ab54b226d6fecce666fad1f98225656780c48d8dc81137e949619b652",
        "r": "0x91ae768629e470e29a19f9badef3d28a53ef8fbc309b55bd8e39458e8dcb61a0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "922480000000000000000",
    "total": "922480000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "922480000000000000000",
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
            "amount": "922480000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "922480000000000000"
      }
    },
    "wallet": "0x7e74c6ad952c605bccde066ca7cd005fd00ebd40",
    "data": "eyJyZWYiOiI3YTA1NGI5OS1hYmViLTQzMzYtOWUzZS00MjU1NmFlMGQ5M2IifQ==",
    "nonce": 20,
    "balances": {
      "current": "1012240124681487392",
      "previous": "924414720124681487392"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 105,
    "balances": {
      "current": "421375063199399280527216",
      "previous": "420452583199399280527216"
    }
  },
  "blockNumber": "14822544",
  "created": "2022-05-22T09:22:01.950Z",
  "updated": "2022-05-22T09:22:02.064Z",
  "id": "628a00b97832e20011830f32"
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
0x0f200f9b0000000000000000000000000000000000000000000000000e0c3307c30984200000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1012240124681487392`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`