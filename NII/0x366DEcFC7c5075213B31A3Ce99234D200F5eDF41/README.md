# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x366DEcFC7c5075213B31A3Ce99234D200F5eDF41`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000980f9abb03b12b09b300000000000000000000000000000000000000000000008f86473f246f37c7380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000008f86473f246f37c7380000000000000000000000000000000000000000000000980f9abb03b12b09b3ba163a8427c241042b5b2d7a314d19c87a825f6f538e55463157b26762c8c513c78174ded8257448c82577a838df1988f235f341da6928d01bb8c2cf7d507ddd2b29fa990ab5fbae749da8f112a86b8a6e240db8ee9b97762d1b7a7dbaf676d6000000000000000000000000000000000000000000000000000000000000001b3ab704469b64a162222f4b236a63b7855a0641408733e6bf3ca558e4a8020f740401f5f1e6e7849e234de4f38e5c0e7f085bcc592e63e312a011a63d49eac1eb133ec0fa05e8c753c9f94c4e346c430ee1c25990e77739215fb55ecb155c155c000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000a65a5c0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000c649000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017d88d02aa311cc1053a0000000000000000000000000000000000000000000018683807ef490a08fb7e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000024be05f37e102f0c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001ab2a4f9dabfe8fac0e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a6a686a5a6a59334e6930335a6a4d774c54566c5932517459574a684d79316a4f44646b4e6d5a69596d4a6b4d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000366decfc7c5075213b31a3ce99234d200f5edf410000000000000000000000000000000000000000000000980f9abb03b12b09b300000000000000000000000000000000000000000000000889537bdf41f3427b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba163a8427c241042b5b2d7a314d19c87a825f6f538e55463157b26762c8c513",
      "signature": {
        "s": "0x2b29fa990ab5fbae749da8f112a86b8a6e240db8ee9b97762d1b7a7dbaf676d6",
        "r": "0xc78174ded8257448c82577a838df1988f235f341da6928d01bb8c2cf7d507ddd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3ab704469b64a162222f4b236a63b7855a0641408733e6bf3ca558e4a8020f74",
      "signature": {
        "s": "0x133ec0fa05e8c753c9f94c4e346c430ee1c25990e77739215fb55ecb155c155c",
        "r": "0x0401f5f1e6e7849e234de4f38e5c0e7f085bcc592e63e312a011a63d49eac1eb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2647560174290611980088",
    "total": "2805029515885365889459"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2647560174290611980088",
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
            "amount": "7879808548308767452174"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2647560174290611980"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1ZjhjZjY3Ni03ZjMwLTVlY2QtYWJhMy1jODdkNmZiYmJkMmUifQ==",
    "nonce": 50761,
    "balances": {
      "current": "112609086696760316855610",
      "previous": "115259294431225219447678"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x366decfc7c5075213b31a3ce99234d200f5edf41",
    "nonce": 2,
    "balances": {
      "current": "2805029515885365889459",
      "previous": "157469341594753909371"
    }
  },
  "blockNumber": "10902108",
  "created": "2020-09-20T23:00:26.569Z",
  "updated": "2020-09-20T23:00:26.633Z",
  "id": "5f67df0a627b8700118110ba"
}
```
* *stageAmount*: `2805029515885365889459`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000008f86473f246f37c7380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000008f86473f246f37c7380000000000000000000000000000000000000000000000980f9abb03b12b09b3ba163a8427c241042b5b2d7a314d19c87a825f6f538e55463157b26762c8c513c78174ded8257448c82577a838df1988f235f341da6928d01bb8c2cf7d507ddd2b29fa990ab5fbae749da8f112a86b8a6e240db8ee9b97762d1b7a7dbaf676d6000000000000000000000000000000000000000000000000000000000000001b3ab704469b64a162222f4b236a63b7855a0641408733e6bf3ca558e4a8020f740401f5f1e6e7849e234de4f38e5c0e7f085bcc592e63e312a011a63d49eac1eb133ec0fa05e8c753c9f94c4e346c430ee1c25990e77739215fb55ecb155c155c000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000a65a5c0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000c649000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017d88d02aa311cc1053a0000000000000000000000000000000000000000000018683807ef490a08fb7e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000024be05f37e102f0c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001ab2a4f9dabfe8fac0e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a6a686a5a6a59334e6930335a6a4d774c54566c5932517459574a684d79316a4f44646b4e6d5a69596d4a6b4d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000366decfc7c5075213b31a3ce99234d200f5edf410000000000000000000000000000000000000000000000980f9abb03b12b09b300000000000000000000000000000000000000000000000889537bdf41f3427b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba163a8427c241042b5b2d7a314d19c87a825f6f538e55463157b26762c8c513",
      "signature": {
        "s": "0x2b29fa990ab5fbae749da8f112a86b8a6e240db8ee9b97762d1b7a7dbaf676d6",
        "r": "0xc78174ded8257448c82577a838df1988f235f341da6928d01bb8c2cf7d507ddd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3ab704469b64a162222f4b236a63b7855a0641408733e6bf3ca558e4a8020f74",
      "signature": {
        "s": "0x133ec0fa05e8c753c9f94c4e346c430ee1c25990e77739215fb55ecb155c155c",
        "r": "0x0401f5f1e6e7849e234de4f38e5c0e7f085bcc592e63e312a011a63d49eac1eb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2647560174290611980088",
    "total": "2805029515885365889459"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2647560174290611980088",
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
            "amount": "7879808548308767452174"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2647560174290611980"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1ZjhjZjY3Ni03ZjMwLTVlY2QtYWJhMy1jODdkNmZiYmJkMmUifQ==",
    "nonce": 50761,
    "balances": {
      "current": "112609086696760316855610",
      "previous": "115259294431225219447678"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x366decfc7c5075213b31a3ce99234d200f5edf41",
    "nonce": 2,
    "balances": {
      "current": "2805029515885365889459",
      "previous": "157469341594753909371"
    }
  },
  "blockNumber": "10902108",
  "created": "2020-09-20T23:00:26.569Z",
  "updated": "2020-09-20T23:00:26.633Z",
  "id": "5f67df0a627b8700118110ba"
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
0x0f200f9b0000000000000000000000000000000000000000000000980f9abb03b12b09b30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2805029515885365889459`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`