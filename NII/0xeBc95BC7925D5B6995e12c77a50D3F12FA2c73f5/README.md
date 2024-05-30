# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xeBc95BC7925D5B6995e12c77a50D3F12FA2c73f5`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000130e4163762bd8bccf00000000000000000000000000000000000000000000000073a86d6100dbb6270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000073a86d6100dbb62700000000000000000000000000000000000000000000000cad7941ca4e5632cef89c4d5b0ec7d7e48b6ca23b670b53efc6b8b0e2a750cbc0c877a8c7bce07de5832ac5a527b02d0845012e963841119187875eae87b32174cd8f57e00cec932f63b767c0f540503d21b32946e9deceff024980516ea3731bbbfd56f1549aad2c000000000000000000000000000000000000000000000000000000000000001b4a968614202e83c2833a0e7d6abb90937d4ada292f055731bdef954f7dd832f70310d4a2a57ee32e2fc76be57a8fbf509649090021684e748adfae27beaf5c4062ec077bcd74b1c23f1971e4e938d355531ec7c1210c959f1202475ea304411f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abdd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c18b9da0853b3b80e38000000000000000000000000000000000000000000009c192da0117698297da400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001d9bc1e395b9450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c47644301f306d37380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5954686a4e7a49334d4330315a6d55344c5455314e7a63744f575a69596930314e5755774e324e6c597a67784d6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000ebc95bc7925d5b6995e12c77a50d3f12fa2c73f50000000000000000000000000000000000000000000000130e4163762bd8bccf0000000000000000000000000000000000000000000000129a98f6152afd06a800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf89c4d5b0ec7d7e48b6ca23b670b53efc6b8b0e2a750cbc0c877a8c7bce07de5",
      "signature": {
        "s": "0x63b767c0f540503d21b32946e9deceff024980516ea3731bbbfd56f1549aad2c",
        "r": "0x832ac5a527b02d0845012e963841119187875eae87b32174cd8f57e00cec932f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4a968614202e83c2833a0e7d6abb90937d4ada292f055731bdef954f7dd832f7",
      "signature": {
        "s": "0x62ec077bcd74b1c23f1971e4e938d355531ec7c1210c959f1202475ea304411f",
        "r": "0x0310d4a2a57ee32e2fc76be57a8fbf509649090021684e748adfae27beaf5c40",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8334031373842757159",
    "total": "233861023462411612878"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8334031373842757159",
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
            "amount": "27235916242100704589624"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8334031373842757"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYThjNzI3MC01ZmU4LTU1NzctOWZiYi01NWUwN2NlYzgxMjkifQ==",
    "nonce": 109533,
    "balances": {
      "current": "737145285211031212658232",
      "previous": "737153627576436429258148"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xebc95bc7925d5b6995e12c77a50d3f12fa2c73f5",
    "nonce": 46,
    "balances": {
      "current": "351515348949691579599",
      "previous": "343181317575848822440"
    }
  },
  "blockNumber": "14709943",
  "created": "2022-05-04T08:48:35.563Z",
  "updated": "2022-05-04T08:48:35.632Z",
  "id": "62723de3bbd75600116d042f"
}
```
* *stageAmount*: `351515348949691579599`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000073a86d6100dbb6270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000073a86d6100dbb62700000000000000000000000000000000000000000000000cad7941ca4e5632cef89c4d5b0ec7d7e48b6ca23b670b53efc6b8b0e2a750cbc0c877a8c7bce07de5832ac5a527b02d0845012e963841119187875eae87b32174cd8f57e00cec932f63b767c0f540503d21b32946e9deceff024980516ea3731bbbfd56f1549aad2c000000000000000000000000000000000000000000000000000000000000001b4a968614202e83c2833a0e7d6abb90937d4ada292f055731bdef954f7dd832f70310d4a2a57ee32e2fc76be57a8fbf509649090021684e748adfae27beaf5c4062ec077bcd74b1c23f1971e4e938d355531ec7c1210c959f1202475ea304411f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abdd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c18b9da0853b3b80e38000000000000000000000000000000000000000000009c192da0117698297da400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001d9bc1e395b9450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c47644301f306d37380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5954686a4e7a49334d4330315a6d55344c5455314e7a63744f575a69596930314e5755774e324e6c597a67784d6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000ebc95bc7925d5b6995e12c77a50d3f12fa2c73f50000000000000000000000000000000000000000000000130e4163762bd8bccf0000000000000000000000000000000000000000000000129a98f6152afd06a800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf89c4d5b0ec7d7e48b6ca23b670b53efc6b8b0e2a750cbc0c877a8c7bce07de5",
      "signature": {
        "s": "0x63b767c0f540503d21b32946e9deceff024980516ea3731bbbfd56f1549aad2c",
        "r": "0x832ac5a527b02d0845012e963841119187875eae87b32174cd8f57e00cec932f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4a968614202e83c2833a0e7d6abb90937d4ada292f055731bdef954f7dd832f7",
      "signature": {
        "s": "0x62ec077bcd74b1c23f1971e4e938d355531ec7c1210c959f1202475ea304411f",
        "r": "0x0310d4a2a57ee32e2fc76be57a8fbf509649090021684e748adfae27beaf5c40",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8334031373842757159",
    "total": "233861023462411612878"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8334031373842757159",
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
            "amount": "27235916242100704589624"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8334031373842757"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYThjNzI3MC01ZmU4LTU1NzctOWZiYi01NWUwN2NlYzgxMjkifQ==",
    "nonce": 109533,
    "balances": {
      "current": "737145285211031212658232",
      "previous": "737153627576436429258148"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xebc95bc7925d5b6995e12c77a50d3f12fa2c73f5",
    "nonce": 46,
    "balances": {
      "current": "351515348949691579599",
      "previous": "343181317575848822440"
    }
  },
  "blockNumber": "14709943",
  "created": "2022-05-04T08:48:35.563Z",
  "updated": "2022-05-04T08:48:35.632Z",
  "id": "62723de3bbd75600116d042f"
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
0x0f200f9b0000000000000000000000000000000000000000000000130e4163762bd8bccf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `351515348949691579599`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`