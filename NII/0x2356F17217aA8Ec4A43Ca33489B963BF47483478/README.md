# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2356F17217aA8Ec4A43Ca33489B963BF47483478`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000013dfe4715e1fc21600000000000000000000000000000000000000000000001f633d3853972c00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001f633d3853972c000000000000000000000000000000000000000000000000001f633d3853972c000023ea5531fdc2c7fbe406dd492c549ef8ca4334314fe2321b534e62d7d189f885d31d73523a4506898f40676813d8fa7f03b719769655a238eb796520da96c427730915fd28084db34df0ca4632ba67db7656820e8b0d73f07f2b37793bd83c8e000000000000000000000000000000000000000000000000000000000000001b2b2004c6b75d087e5dfcea24e644213ee1e6bc4a1416eb02bb4226f245dd00bb03ea40e67439e36e29c30d1569fb3cc951f5b24f6c680535b45d3c966f1decdb5cee73f9a4aecaca1886e38fc891257a82d39652afd5c223ee38fcd79a4202f4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e26c2d0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000002356f17217aa8ec4a43ca33489b963bf4748347800000000000000000000000000000000000000000000000013dfe4715e1fc21600000000000000000000000000000000000000000000001f7f262233a23f421600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000809056eacf380000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000809056eacf380000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a6a5530597a4d314f5331695a54566d4c5451314f544974596d51315a6930795a6a4e6c597a5535595745794e57596966513d3d0000000000000000000000000000000000000000000000000000000000000095000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000007802e7360d65abf339400000000000000000000000000000000000000000000077e383f8d51214c7394000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x23ea5531fdc2c7fbe406dd492c549ef8ca4334314fe2321b534e62d7d189f885",
      "signature": {
        "s": "0x730915fd28084db34df0ca4632ba67db7656820e8b0d73f07f2b37793bd83c8e",
        "r": "0xd31d73523a4506898f40676813d8fa7f03b719769655a238eb796520da96c427",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2b2004c6b75d087e5dfcea24e644213ee1e6bc4a1416eb02bb4226f245dd00bb",
      "signature": {
        "s": "0x5cee73f9a4aecaca1886e38fc891257a82d39652afd5c223ee38fcd79a4202f4",
        "r": "0x03ea40e67439e36e29c30d1569fb3cc951f5b24f6c680535b45d3c966f1decdb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "579000000000000000000",
    "total": "579000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "579000000000000000000",
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
            "amount": "579000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "579000000000000000"
      }
    },
    "wallet": "0x2356f17217aa8ec4a43ca33489b963bf47483478",
    "data": "eyJyZWYiOiJkZjU0YzM1OS1iZTVmLTQ1OTItYmQ1Zi0yZjNlYzU5YWEyNWYifQ==",
    "nonce": 13,
    "balances": {
      "current": "1432114382088684054",
      "previous": "581011114382088684054"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 149,
    "balances": {
      "current": "566737531951106676177216",
      "previous": "566158531951106676177216"
    }
  },
  "blockNumber": "14838829",
  "created": "2022-05-25T00:47:44.006Z",
  "updated": "2022-05-25T00:47:44.106Z",
  "id": "628d7cafbbd75600116d08f0"
}
```
* *stageAmount*: `1432114382088684054`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000001f633d3853972c00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001f633d3853972c000000000000000000000000000000000000000000000000001f633d3853972c000023ea5531fdc2c7fbe406dd492c549ef8ca4334314fe2321b534e62d7d189f885d31d73523a4506898f40676813d8fa7f03b719769655a238eb796520da96c427730915fd28084db34df0ca4632ba67db7656820e8b0d73f07f2b37793bd83c8e000000000000000000000000000000000000000000000000000000000000001b2b2004c6b75d087e5dfcea24e644213ee1e6bc4a1416eb02bb4226f245dd00bb03ea40e67439e36e29c30d1569fb3cc951f5b24f6c680535b45d3c966f1decdb5cee73f9a4aecaca1886e38fc891257a82d39652afd5c223ee38fcd79a4202f4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e26c2d0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000002356f17217aa8ec4a43ca33489b963bf4748347800000000000000000000000000000000000000000000000013dfe4715e1fc21600000000000000000000000000000000000000000000001f7f262233a23f421600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000809056eacf380000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000809056eacf380000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a6a5530597a4d314f5331695a54566d4c5451314f544974596d51315a6930795a6a4e6c597a5535595745794e57596966513d3d0000000000000000000000000000000000000000000000000000000000000095000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000007802e7360d65abf339400000000000000000000000000000000000000000000077e383f8d51214c7394000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x23ea5531fdc2c7fbe406dd492c549ef8ca4334314fe2321b534e62d7d189f885",
      "signature": {
        "s": "0x730915fd28084db34df0ca4632ba67db7656820e8b0d73f07f2b37793bd83c8e",
        "r": "0xd31d73523a4506898f40676813d8fa7f03b719769655a238eb796520da96c427",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2b2004c6b75d087e5dfcea24e644213ee1e6bc4a1416eb02bb4226f245dd00bb",
      "signature": {
        "s": "0x5cee73f9a4aecaca1886e38fc891257a82d39652afd5c223ee38fcd79a4202f4",
        "r": "0x03ea40e67439e36e29c30d1569fb3cc951f5b24f6c680535b45d3c966f1decdb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "579000000000000000000",
    "total": "579000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "579000000000000000000",
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
            "amount": "579000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "579000000000000000"
      }
    },
    "wallet": "0x2356f17217aa8ec4a43ca33489b963bf47483478",
    "data": "eyJyZWYiOiJkZjU0YzM1OS1iZTVmLTQ1OTItYmQ1Zi0yZjNlYzU5YWEyNWYifQ==",
    "nonce": 13,
    "balances": {
      "current": "1432114382088684054",
      "previous": "581011114382088684054"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 149,
    "balances": {
      "current": "566737531951106676177216",
      "previous": "566158531951106676177216"
    }
  },
  "blockNumber": "14838829",
  "created": "2022-05-25T00:47:44.006Z",
  "updated": "2022-05-25T00:47:44.106Z",
  "id": "628d7cafbbd75600116d08f0"
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
0x0f200f9b00000000000000000000000000000000000000000000000013dfe4715e1fc2160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1432114382088684054`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`