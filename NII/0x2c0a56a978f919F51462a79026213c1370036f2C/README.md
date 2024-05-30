# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2c0a56a978f919F51462a79026213c1370036f2C`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000006e85c495ca77ac000000000000000000000000000000000000000000000000006e85c495ca77ac0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000006e85c495ca77ac000000000000000000000000000000000000000000000000006e85c495ca77ac5d0c21fcb30826253971b99d66845455bc19e67ad6f82df441c37bda5694a33e6b3552c4de949f35272b1afff8caa590980c9794c95c9ce2912c84b8cdb089225198596373d796dc1ff9b3c5ee1a05bcc125c02dd2e25970b40423108e4632a6000000000000000000000000000000000000000000000000000000000000001c3d531d052c95b5bd89ac1c9b6006b67e221e97a094233053dbb7760e25c94184271796a35763a55b48fa037c9eef76779910c54aad6e129f5a6919b6dfe085102163f9e7501b0bff3b20858ad2804858b82945eae3c0de482b4d0912abae3276000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012df9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002366bab82d5282b6ea3e000000000000000000000000000000000000000000002366bb26cf624ce112ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000001c4b345fb0c20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9d16ba7e04826fad0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d54637a4d4745774d53316c5a57526c4c5455314d7a6b744f4745794f4330304d44517a4e7a4e6c4e44517959546b6966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000002c0a56a978f919f51462a79026213c1370036f2c000000000000000000000000000000000000000000000000006e85c495ca77ac000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5d0c21fcb30826253971b99d66845455bc19e67ad6f82df441c37bda5694a33e",
      "signature": {
        "s": "0x5198596373d796dc1ff9b3c5ee1a05bcc125c02dd2e25970b40423108e4632a6",
        "r": "0x6b3552c4de949f35272b1afff8caa590980c9794c95c9ce2912c84b8cdb08922",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3d531d052c95b5bd89ac1c9b6006b67e221e97a094233053dbb7760e25c94184",
      "signature": {
        "s": "0x2163f9e7501b0bff3b20858ad2804858b82945eae3c0de482b4d0912abae3276",
        "r": "0x271796a35763a55b48fa037c9eef76779910c54aad6e129f5a6919b6dfe08510",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "31109326811330476",
    "total": "31109326811330476"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31109326811330476",
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
            "amount": "16816303290913248145325"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31109326811330"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjMTczMGEwMS1lZWRlLTU1MzktOGEyOC00MDQzNzNlNDQyYTkifQ==",
    "nonce": 77305,
    "balances": {
      "current": "167177849349675129694782",
      "previous": "167177880490111267836588"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2c0a56a978f919f51462a79026213c1370036f2c",
    "nonce": 1,
    "balances": {
      "current": "31109326811330476",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:32.479Z",
  "updated": "2021-06-04T12:46:32.559Z",
  "id": "60ba20a8010ba300120bfdd2"
}
```
* *stageAmount*: `31109326811330476`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000006e85c495ca77ac0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000006e85c495ca77ac000000000000000000000000000000000000000000000000006e85c495ca77ac5d0c21fcb30826253971b99d66845455bc19e67ad6f82df441c37bda5694a33e6b3552c4de949f35272b1afff8caa590980c9794c95c9ce2912c84b8cdb089225198596373d796dc1ff9b3c5ee1a05bcc125c02dd2e25970b40423108e4632a6000000000000000000000000000000000000000000000000000000000000001c3d531d052c95b5bd89ac1c9b6006b67e221e97a094233053dbb7760e25c94184271796a35763a55b48fa037c9eef76779910c54aad6e129f5a6919b6dfe085102163f9e7501b0bff3b20858ad2804858b82945eae3c0de482b4d0912abae3276000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012df9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002366bab82d5282b6ea3e000000000000000000000000000000000000000000002366bb26cf624ce112ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000001c4b345fb0c20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9d16ba7e04826fad0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d54637a4d4745774d53316c5a57526c4c5455314d7a6b744f4745794f4330304d44517a4e7a4e6c4e44517959546b6966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000002c0a56a978f919f51462a79026213c1370036f2c000000000000000000000000000000000000000000000000006e85c495ca77ac000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5d0c21fcb30826253971b99d66845455bc19e67ad6f82df441c37bda5694a33e",
      "signature": {
        "s": "0x5198596373d796dc1ff9b3c5ee1a05bcc125c02dd2e25970b40423108e4632a6",
        "r": "0x6b3552c4de949f35272b1afff8caa590980c9794c95c9ce2912c84b8cdb08922",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3d531d052c95b5bd89ac1c9b6006b67e221e97a094233053dbb7760e25c94184",
      "signature": {
        "s": "0x2163f9e7501b0bff3b20858ad2804858b82945eae3c0de482b4d0912abae3276",
        "r": "0x271796a35763a55b48fa037c9eef76779910c54aad6e129f5a6919b6dfe08510",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "31109326811330476",
    "total": "31109326811330476"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31109326811330476",
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
            "amount": "16816303290913248145325"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31109326811330"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjMTczMGEwMS1lZWRlLTU1MzktOGEyOC00MDQzNzNlNDQyYTkifQ==",
    "nonce": 77305,
    "balances": {
      "current": "167177849349675129694782",
      "previous": "167177880490111267836588"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2c0a56a978f919f51462a79026213c1370036f2c",
    "nonce": 1,
    "balances": {
      "current": "31109326811330476",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:32.479Z",
  "updated": "2021-06-04T12:46:32.559Z",
  "id": "60ba20a8010ba300120bfdd2"
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
0x0f200f9b000000000000000000000000000000000000000000000000006e85c495ca77ac0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `31109326811330476`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`