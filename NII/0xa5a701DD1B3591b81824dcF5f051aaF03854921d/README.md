# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa5a701DD1B3591b81824dcF5f051aaF03854921d`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000016385a19115f18600000000000000000000000000000000000000000000000000086dd48de582590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000086dd48de5825900000000000000000000000000000000000000000000000000ec86d0e449247d0918eee8b8616b3e37a5dedfd7d676e2cbb7ad2e0cd2abb7edec4e3351cffcff0ab8c99deb6a87204af6a170738f99327cdb32798f1e77cb886cdae77420cdb46ab1fa99363b2ca8233d57d466449b57d400af1bfd9fe1575f7b64aa18a87048000000000000000000000000000000000000000000000000000000000000001b0330ea6bb6eebf2069cce9c032cd9c71deaff7ba19666e1196d3ffab4cb0d107eca759fe185e2b943db838445209aa135ebb61d1bb6ab71c58f9d59e8af7271202f217f402b5656eb93f0f68be85174a36d545fba47205e6d0b9c98582abf258000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afd2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052af2a07db9acf5d78080000000000000000000000000000000000000000000052af2a104b97c4d3d8f900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000002286790de980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d73c9ca13499c3fed90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d325a6a4d57457a4e53316b5a4459774c5455354f445974596a55354f5330344d544d354d6a63784d5749345957596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a5a701dd1b3591b81824dcf5f051aaf03854921d000000000000000000000000000000000000000000000000016385a19115f186000000000000000000000000000000000000000000000000015b17cd03306f2d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0918eee8b8616b3e37a5dedfd7d676e2cbb7ad2e0cd2abb7edec4e3351cffcff",
      "signature": {
        "s": "0x6ab1fa99363b2ca8233d57d466449b57d400af1bfd9fe1575f7b64aa18a87048",
        "r": "0x0ab8c99deb6a87204af6a170738f99327cdb32798f1e77cb886cdae77420cdb4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0330ea6bb6eebf2069cce9c032cd9c71deaff7ba19666e1196d3ffab4cb0d107",
      "signature": {
        "s": "0x02f217f402b5656eb93f0f68be85174a36d545fba47205e6d0b9c98582abf258",
        "r": "0xeca759fe185e2b943db838445209aa135ebb61d1bb6ab71c58f9d59e8af72712",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2372559494808153",
    "total": "66576326245033085"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2372559494808153",
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
            "amount": "27582249933181712334553"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2372559494808"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhM2ZjMWEzNS1kZDYwLTU5ODYtYjU5OS04MTM5MjcxMWI4YWYifQ==",
    "nonce": 110546,
    "balances": {
      "current": "390465260438942459459592",
      "previous": "390465262813874513762553"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa5a701dd1b3591b81824dcf5f051aaf03854921d",
    "nonce": 46,
    "balances": {
      "current": "100070545702646150",
      "previous": "97697986207837997"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:50.005Z",
  "updated": "2022-05-04T08:53:50.089Z",
  "id": "62723f1dbbd75600116d0590"
}
```
* *stageAmount*: `100070545702646150`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000086dd48de582590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000086dd48de5825900000000000000000000000000000000000000000000000000ec86d0e449247d0918eee8b8616b3e37a5dedfd7d676e2cbb7ad2e0cd2abb7edec4e3351cffcff0ab8c99deb6a87204af6a170738f99327cdb32798f1e77cb886cdae77420cdb46ab1fa99363b2ca8233d57d466449b57d400af1bfd9fe1575f7b64aa18a87048000000000000000000000000000000000000000000000000000000000000001b0330ea6bb6eebf2069cce9c032cd9c71deaff7ba19666e1196d3ffab4cb0d107eca759fe185e2b943db838445209aa135ebb61d1bb6ab71c58f9d59e8af7271202f217f402b5656eb93f0f68be85174a36d545fba47205e6d0b9c98582abf258000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afd2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052af2a07db9acf5d78080000000000000000000000000000000000000000000052af2a104b97c4d3d8f900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000002286790de980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d73c9ca13499c3fed90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d325a6a4d57457a4e53316b5a4459774c5455354f445974596a55354f5330344d544d354d6a63784d5749345957596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a5a701dd1b3591b81824dcf5f051aaf03854921d000000000000000000000000000000000000000000000000016385a19115f186000000000000000000000000000000000000000000000000015b17cd03306f2d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0918eee8b8616b3e37a5dedfd7d676e2cbb7ad2e0cd2abb7edec4e3351cffcff",
      "signature": {
        "s": "0x6ab1fa99363b2ca8233d57d466449b57d400af1bfd9fe1575f7b64aa18a87048",
        "r": "0x0ab8c99deb6a87204af6a170738f99327cdb32798f1e77cb886cdae77420cdb4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0330ea6bb6eebf2069cce9c032cd9c71deaff7ba19666e1196d3ffab4cb0d107",
      "signature": {
        "s": "0x02f217f402b5656eb93f0f68be85174a36d545fba47205e6d0b9c98582abf258",
        "r": "0xeca759fe185e2b943db838445209aa135ebb61d1bb6ab71c58f9d59e8af72712",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2372559494808153",
    "total": "66576326245033085"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2372559494808153",
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
            "amount": "27582249933181712334553"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2372559494808"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhM2ZjMWEzNS1kZDYwLTU5ODYtYjU5OS04MTM5MjcxMWI4YWYifQ==",
    "nonce": 110546,
    "balances": {
      "current": "390465260438942459459592",
      "previous": "390465262813874513762553"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa5a701dd1b3591b81824dcf5f051aaf03854921d",
    "nonce": 46,
    "balances": {
      "current": "100070545702646150",
      "previous": "97697986207837997"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:50.005Z",
  "updated": "2022-05-04T08:53:50.089Z",
  "id": "62723f1dbbd75600116d0590"
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
0x0f200f9b000000000000000000000000000000000000000000000000016385a19115f1860000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `100070545702646150`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`