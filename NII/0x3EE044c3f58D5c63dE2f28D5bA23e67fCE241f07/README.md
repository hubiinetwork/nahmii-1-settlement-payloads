# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3EE044c3f58D5c63dE2f28D5bA23e67fCE241f07`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de0b6b3a764038f000000000000000000000000000000000000000000000029da1b483f1badab800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000029da1b483f1badab80000000000000000000000000000000000000000000000029da1b483f1badab8010138f6f14c095b032575737ad6b79956663c1040c899d52d6b08f0f993691a5334a674d6c50775aa462cb4812a7ef714e193ce4effb441d0f89bbe351113313306ce05ab840f8e847e092cf8d7c6d77b84477c72c578f1a0d93a3ea06b5a125000000000000000000000000000000000000000000000000000000000000001bc7b2e843813f516c3a2a43799d154a11a1d6b028ec929194e3b86f8e078b83cf70457db961768d0cffa9f1ce01725f17ba7e2ae2c229afa486bea98ab07752f860a6edae9ae92a4be4992430d417bf9e6c6d58f7baa99f12f60a3581cab7d702000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e277850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000f0000000000000000000000003ee044c3f58d5c63de2f28d5ba23e67fce241f070000000000000000000000000000000000000000000000000de0b6b3a764038f000000000000000000000000000000000000000000000029f2b2cea2f3fe253f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000ab6cfb030ec76300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab6cfb030ec76300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a574930597a59774d4330795a445a6d4c5452685a6a55744f4749774d43307a4e7a646b4d474579597a417a4e32556966513d3d000000000000000000000000000000000000000000000000000000000000009d000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000792770d9fa2ba4bb24c00000000000000000000000000000000000000000000078fd96beb1ec890d794000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x10138f6f14c095b032575737ad6b79956663c1040c899d52d6b08f0f993691a5",
      "signature": {
        "s": "0x306ce05ab840f8e847e092cf8d7c6d77b84477c72c578f1a0d93a3ea06b5a125",
        "r": "0x334a674d6c50775aa462cb4812a7ef714e193ce4effb441d0f89bbe351113313",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc7b2e843813f516c3a2a43799d154a11a1d6b028ec929194e3b86f8e078b83cf",
      "signature": {
        "s": "0x60a6edae9ae92a4be4992430d417bf9e6c6d58f7baa99f12f60a3581cab7d702",
        "r": "0x70457db961768d0cffa9f1ce01725f17ba7e2ae2c229afa486bea98ab07752f8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "772032741782615600000",
    "total": "772032741782615600000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "772032741782615600000",
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
            "amount": "772032741782615600"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "772032741782615600"
      }
    },
    "wallet": "0x3ee044c3f58d5c63de2f28d5ba23e67fce241f07",
    "data": "eyJyZWYiOiI1ZWI0YzYwMC0yZDZmLTRhZjUtOGIwMC0zNzdkMGEyYzAzN2UifQ==",
    "nonce": 15,
    "balances": {
      "current": "1000000000000000911",
      "previous": "773804774524398216511"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 157,
    "balances": {
      "current": "572133899251769291777216",
      "previous": "571361866509986676177216"
    }
  },
  "blockNumber": "14841733",
  "created": "2022-05-25T11:56:30.309Z",
  "updated": "2022-05-25T11:56:30.447Z",
  "id": "628e196e3592fd001130b891"
}
```
* *stageAmount*: `1000000000000000911`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000029da1b483f1badab800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000029da1b483f1badab80000000000000000000000000000000000000000000000029da1b483f1badab8010138f6f14c095b032575737ad6b79956663c1040c899d52d6b08f0f993691a5334a674d6c50775aa462cb4812a7ef714e193ce4effb441d0f89bbe351113313306ce05ab840f8e847e092cf8d7c6d77b84477c72c578f1a0d93a3ea06b5a125000000000000000000000000000000000000000000000000000000000000001bc7b2e843813f516c3a2a43799d154a11a1d6b028ec929194e3b86f8e078b83cf70457db961768d0cffa9f1ce01725f17ba7e2ae2c229afa486bea98ab07752f860a6edae9ae92a4be4992430d417bf9e6c6d58f7baa99f12f60a3581cab7d702000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e277850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000f0000000000000000000000003ee044c3f58d5c63de2f28d5ba23e67fce241f070000000000000000000000000000000000000000000000000de0b6b3a764038f000000000000000000000000000000000000000000000029f2b2cea2f3fe253f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000ab6cfb030ec76300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab6cfb030ec76300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a574930597a59774d4330795a445a6d4c5452685a6a55744f4749774d43307a4e7a646b4d474579597a417a4e32556966513d3d000000000000000000000000000000000000000000000000000000000000009d000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000792770d9fa2ba4bb24c00000000000000000000000000000000000000000000078fd96beb1ec890d794000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x10138f6f14c095b032575737ad6b79956663c1040c899d52d6b08f0f993691a5",
      "signature": {
        "s": "0x306ce05ab840f8e847e092cf8d7c6d77b84477c72c578f1a0d93a3ea06b5a125",
        "r": "0x334a674d6c50775aa462cb4812a7ef714e193ce4effb441d0f89bbe351113313",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc7b2e843813f516c3a2a43799d154a11a1d6b028ec929194e3b86f8e078b83cf",
      "signature": {
        "s": "0x60a6edae9ae92a4be4992430d417bf9e6c6d58f7baa99f12f60a3581cab7d702",
        "r": "0x70457db961768d0cffa9f1ce01725f17ba7e2ae2c229afa486bea98ab07752f8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "772032741782615600000",
    "total": "772032741782615600000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "772032741782615600000",
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
            "amount": "772032741782615600"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "772032741782615600"
      }
    },
    "wallet": "0x3ee044c3f58d5c63de2f28d5ba23e67fce241f07",
    "data": "eyJyZWYiOiI1ZWI0YzYwMC0yZDZmLTRhZjUtOGIwMC0zNzdkMGEyYzAzN2UifQ==",
    "nonce": 15,
    "balances": {
      "current": "1000000000000000911",
      "previous": "773804774524398216511"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 157,
    "balances": {
      "current": "572133899251769291777216",
      "previous": "571361866509986676177216"
    }
  },
  "blockNumber": "14841733",
  "created": "2022-05-25T11:56:30.309Z",
  "updated": "2022-05-25T11:56:30.447Z",
  "id": "628e196e3592fd001130b891"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de0b6b3a764038f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000000000000000911`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`