# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCfa606742FD2bEBFE7818CFeaF79Ea79Db94F2c8`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000003a0b5688753d19a760000000000000000000000000000000000000000000000001604c50aef327a520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001604c50aef327a5200000000000000000000000000000000000000000000000269dd3d0234105c08a7ff27ce26e62a54f65d061097dea7619bac090b2994d6becbdb6adba02e980bf824cc788441fb12cf73e83d273095c06fac238ec861587d0d7b8dd933b96d0d0fe055c37a8d6ec9b0972d39e56026cd866314145742d24c009ba8c84f46afde000000000000000000000000000000000000000000000000000000000000001c40652056e82103504255c7e01307d58de7d6c25f683641c2594108571468620de3d6e1b77fd39fb861e8266d1955cd5b7a44e75928b6e4d019b2c6e4e4a4363a3a3fdc0df7402b965edf7dd2fe95c7d33499509fa1b38a92459ad71b7edf8145000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1dd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a7afa02346eab8d18b0000000000000000000000000000000000000000000004a7b100c9c7cf183fa0a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005a30356c467080000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d955b905e145a958a90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d474e6b4e575934597931695a544a684c5456684d6d55744f544d774e5330794d6a6c6d4f44557a4d7a45324f47596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000cfa606742fd2bebfe7818cfeaf79ea79db94f2c8000000000000000000000000000000000000000000000003a0b5688753d19a760000000000000000000000000000000000000000000000038ab0a37c649f202400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa7ff27ce26e62a54f65d061097dea7619bac090b2994d6becbdb6adba02e980b",
      "signature": {
        "s": "0x0fe055c37a8d6ec9b0972d39e56026cd866314145742d24c009ba8c84f46afde",
        "r": "0xf824cc788441fb12cf73e83d273095c06fac238ec861587d0d7b8dd933b96d0d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x40652056e82103504255c7e01307d58de7d6c25f683641c2594108571468620d",
      "signature": {
        "s": "0x3a3fdc0df7402b965edf7dd2fe95c7d33499509fa1b38a92459ad71b7edf8145",
        "r": "0xe3d6e1b77fd39fb861e8266d1955cd5b7a44e75928b6e4d019b2c6e4e4a4363a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1586609619494664786",
    "total": "44521808570927307784"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1586609619494664786",
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
            "amount": "27620952853172208621737"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1586609619494664"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhMGNkNWY4Yy1iZTJhLTVhMmUtOTMwNS0yMjlmODUzMzE2OGYifQ==",
    "nonce": 111069,
    "balances": {
      "current": "351723637528455675713712",
      "previous": "351725225724684789873162"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcfa606742fd2bebfe7818cfeaf79ea79db94f2c8",
    "nonce": 46,
    "balances": {
      "current": "66920509168417872502",
      "previous": "65333899548923207716"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:24.952Z",
  "updated": "2022-05-04T08:56:25.058Z",
  "id": "62723fb8bbd75600116d063e"
}
```
* *stageAmount*: `66920509168417872502`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000001604c50aef327a520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001604c50aef327a5200000000000000000000000000000000000000000000000269dd3d0234105c08a7ff27ce26e62a54f65d061097dea7619bac090b2994d6becbdb6adba02e980bf824cc788441fb12cf73e83d273095c06fac238ec861587d0d7b8dd933b96d0d0fe055c37a8d6ec9b0972d39e56026cd866314145742d24c009ba8c84f46afde000000000000000000000000000000000000000000000000000000000000001c40652056e82103504255c7e01307d58de7d6c25f683641c2594108571468620de3d6e1b77fd39fb861e8266d1955cd5b7a44e75928b6e4d019b2c6e4e4a4363a3a3fdc0df7402b965edf7dd2fe95c7d33499509fa1b38a92459ad71b7edf8145000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1dd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a7afa02346eab8d18b0000000000000000000000000000000000000000000004a7b100c9c7cf183fa0a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005a30356c467080000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d955b905e145a958a90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d474e6b4e575934597931695a544a684c5456684d6d55744f544d774e5330794d6a6c6d4f44557a4d7a45324f47596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000cfa606742fd2bebfe7818cfeaf79ea79db94f2c8000000000000000000000000000000000000000000000003a0b5688753d19a760000000000000000000000000000000000000000000000038ab0a37c649f202400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa7ff27ce26e62a54f65d061097dea7619bac090b2994d6becbdb6adba02e980b",
      "signature": {
        "s": "0x0fe055c37a8d6ec9b0972d39e56026cd866314145742d24c009ba8c84f46afde",
        "r": "0xf824cc788441fb12cf73e83d273095c06fac238ec861587d0d7b8dd933b96d0d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x40652056e82103504255c7e01307d58de7d6c25f683641c2594108571468620d",
      "signature": {
        "s": "0x3a3fdc0df7402b965edf7dd2fe95c7d33499509fa1b38a92459ad71b7edf8145",
        "r": "0xe3d6e1b77fd39fb861e8266d1955cd5b7a44e75928b6e4d019b2c6e4e4a4363a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1586609619494664786",
    "total": "44521808570927307784"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1586609619494664786",
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
            "amount": "27620952853172208621737"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1586609619494664"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhMGNkNWY4Yy1iZTJhLTVhMmUtOTMwNS0yMjlmODUzMzE2OGYifQ==",
    "nonce": 111069,
    "balances": {
      "current": "351723637528455675713712",
      "previous": "351725225724684789873162"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcfa606742fd2bebfe7818cfeaf79ea79db94f2c8",
    "nonce": 46,
    "balances": {
      "current": "66920509168417872502",
      "previous": "65333899548923207716"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:24.952Z",
  "updated": "2022-05-04T08:56:25.058Z",
  "id": "62723fb8bbd75600116d063e"
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
0x0f200f9b000000000000000000000000000000000000000000000003a0b5688753d19a760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `66920509168417872502`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`