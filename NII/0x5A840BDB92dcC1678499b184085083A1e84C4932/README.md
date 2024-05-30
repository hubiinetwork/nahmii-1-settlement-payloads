# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5A840BDB92dcC1678499b184085083A1e84C4932`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000026591d887db99aae000000000000000000000000000000000000000000000000049fb8bd12d848df0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000049fb8bd12d848df00000000000000000000000000000000000000000000000026591d887db99aaeb39b11724503f7619616333569f9bb2d2013f3e8219f7913c3afe12e1952ffccc94369bce4a01c744010e5ff879c8d8cfc5eb0b5c08afa2216c074c9beb39a6569d856035045020436c79b0356a37522dbd0b65bc08296c67412f30db7f63bb3000000000000000000000000000000000000000000000000000000000000001cc6337fa5bfb8fbff9d939915a304b343ecd4219d42ec2d57773604e7fcc239bc68e21ec5b43c6a3a695d2ecf398ffb9233903e1bcde7d1ba55628f248a35d2c9007fb93c7ed34a85b1e7e08aed400640778175eebd783195e5b04dfeb4bcaea8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b62c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000319718a36a0a70ae98330000000000000000000000000000000000000000000031971d4451cfe514eb6200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000012f08618e0a500000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfb34b6743d572d4ba0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979597a4930596a41315979316b597a63774c5455354e7a41745954686a4e53316d596a49314d7a45794e6a4130596a496966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000005a840bdb92dcc1678499b184085083a1e84c493200000000000000000000000000000000000000000000000026591d887db99aae00000000000000000000000000000000000000000000000021b964cb6ae151cf00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb39b11724503f7619616333569f9bb2d2013f3e8219f7913c3afe12e1952ffcc",
      "signature": {
        "s": "0x69d856035045020436c79b0356a37522dbd0b65bc08296c67412f30db7f63bb3",
        "r": "0xc94369bce4a01c744010e5ff879c8d8cfc5eb0b5c08afa2216c074c9beb39a65",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc6337fa5bfb8fbff9d939915a304b343ecd4219d42ec2d57773604e7fcc239bc",
      "signature": {
        "s": "0x007fb93c7ed34a85b1e7e08aed400640778175eebd783195e5b04dfeb4bcaea8",
        "r": "0x68e21ec5b43c6a3a695d2ecf398ffb9233903e1bcde7d1ba55628f248a35d2c9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "333188019653200095",
    "total": "2763272318430583470"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "333188019653200095",
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
            "amount": "27738375876282540020922"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "333188019653200"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyYzI0YjA1Yy1kYzcwLTU5NzAtYThjNS1mYjI1MzEyNjA0YjIifQ==",
    "nonce": 112172,
    "balances": {
      "current": "234183191395013944580147",
      "previous": "234183524916221617433442"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5a840bdb92dcc1678499b184085083a1e84c4932",
    "nonce": 9,
    "balances": {
      "current": "2763272318430583470",
      "previous": "2430084298777383375"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:23.271Z",
  "updated": "2022-05-04T09:02:23.329Z",
  "id": "6272411f7832e20011830dfd"
}
```
* *stageAmount*: `2763272318430583470`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000049fb8bd12d848df0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000049fb8bd12d848df00000000000000000000000000000000000000000000000026591d887db99aaeb39b11724503f7619616333569f9bb2d2013f3e8219f7913c3afe12e1952ffccc94369bce4a01c744010e5ff879c8d8cfc5eb0b5c08afa2216c074c9beb39a6569d856035045020436c79b0356a37522dbd0b65bc08296c67412f30db7f63bb3000000000000000000000000000000000000000000000000000000000000001cc6337fa5bfb8fbff9d939915a304b343ecd4219d42ec2d57773604e7fcc239bc68e21ec5b43c6a3a695d2ecf398ffb9233903e1bcde7d1ba55628f248a35d2c9007fb93c7ed34a85b1e7e08aed400640778175eebd783195e5b04dfeb4bcaea8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b62c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000319718a36a0a70ae98330000000000000000000000000000000000000000000031971d4451cfe514eb6200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000012f08618e0a500000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfb34b6743d572d4ba0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979597a4930596a41315979316b597a63774c5455354e7a41745954686a4e53316d596a49314d7a45794e6a4130596a496966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000005a840bdb92dcc1678499b184085083a1e84c493200000000000000000000000000000000000000000000000026591d887db99aae00000000000000000000000000000000000000000000000021b964cb6ae151cf00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb39b11724503f7619616333569f9bb2d2013f3e8219f7913c3afe12e1952ffcc",
      "signature": {
        "s": "0x69d856035045020436c79b0356a37522dbd0b65bc08296c67412f30db7f63bb3",
        "r": "0xc94369bce4a01c744010e5ff879c8d8cfc5eb0b5c08afa2216c074c9beb39a65",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc6337fa5bfb8fbff9d939915a304b343ecd4219d42ec2d57773604e7fcc239bc",
      "signature": {
        "s": "0x007fb93c7ed34a85b1e7e08aed400640778175eebd783195e5b04dfeb4bcaea8",
        "r": "0x68e21ec5b43c6a3a695d2ecf398ffb9233903e1bcde7d1ba55628f248a35d2c9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "333188019653200095",
    "total": "2763272318430583470"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "333188019653200095",
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
            "amount": "27738375876282540020922"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "333188019653200"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyYzI0YjA1Yy1kYzcwLTU5NzAtYThjNS1mYjI1MzEyNjA0YjIifQ==",
    "nonce": 112172,
    "balances": {
      "current": "234183191395013944580147",
      "previous": "234183524916221617433442"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5a840bdb92dcc1678499b184085083a1e84c4932",
    "nonce": 9,
    "balances": {
      "current": "2763272318430583470",
      "previous": "2430084298777383375"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:23.271Z",
  "updated": "2022-05-04T09:02:23.329Z",
  "id": "6272411f7832e20011830dfd"
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
0x0f200f9b00000000000000000000000000000000000000000000000026591d887db99aae0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2763272318430583470`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`