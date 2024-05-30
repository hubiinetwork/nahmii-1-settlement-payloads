# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x08398735881381A4B02bEC663a36be4Eb27fBd3F`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000009168050bcc4062c88b0000000000000000000000000000000000000000000000000000001968156eee0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001968156eee000000000000000000000000000000000000000000000052441c370b72a330359ea1b2bf818e7da86df735ffd94703cf29b8f5da684f259a585ec13090ca4cbb2db658892ea1f000d00727a8eefb7b3353c25e22894677f6dba26992c122930077027d8f1a17c260ac3c556852cb5884c58a77221105398b5472a79241245ff6000000000000000000000000000000000000000000000000000000000000001c1544ea621b74a05bc5127bf53b16c40e87d99ffa9d2d98ba6cb9f4821844b60f57253ddaac342d602d1631ff299db248e51e5acc4220428da5593e59ca9c7cfa089b1f6ffa2d1957d4f4b9f4e9fbc57a170893bcd1fef89574ceac065f8a2bd6000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b207000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c30c6c4d3e786dbd7c0000000000000000000000000000000000000000000049c30c6c4d57e704380b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000006810ba10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d984c2e418d117dbdc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d5445794e444a6c4d793030593245304c5455355a5463744f544d344d5330325a4451344d545535595756694f546b6966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000008398735881381a4b02bec663a36be4eb27fbd3f00000000000000000000000000000000000000000000009168050bcc4062c88b00000000000000000000000000000000000000000000009168050bb2d84d599d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9ea1b2bf818e7da86df735ffd94703cf29b8f5da684f259a585ec13090ca4cbb",
      "signature": {
        "s": "0x77027d8f1a17c260ac3c556852cb5884c58a77221105398b5472a79241245ff6",
        "r": "0x2db658892ea1f000d00727a8eefb7b3353c25e22894677f6dba26992c1229300",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1544ea621b74a05bc5127bf53b16c40e87d99ffa9d2d98ba6cb9f4821844b60f",
      "signature": {
        "s": "0x089b1f6ffa2d1957d4f4b9f4e9fbc57a170893bcd1fef89574ceac065f8a2bd6",
        "r": "0x57253ddaac342d602d1631ff299db248e51e5acc4220428da5593e59ca9c7cfa",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "109120417518",
    "total": "1517540872260417695797"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "109120417518",
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
            "amount": "27624342337696925473756"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "109120417"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlMTEyNDJlMy00Y2E0LTU5ZTctOTM4MS02ZDQ4MTU5YWViOTkifQ==",
    "nonce": 111111,
    "balances": {
      "current": "348330763519214106819964",
      "previous": "348330763519323336357899"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x08398735881381a4b02bec663a36be4eb27fbd3f",
    "nonce": 46,
    "balances": {
      "current": "2682273300814594492555",
      "previous": "2682273300705474075037"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:36.833Z",
  "updated": "2022-05-04T08:56:36.911Z",
  "id": "62723fc43592fd001130b5ba"
}
```
* *stageAmount*: `2682273300814594492555`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000001968156eee0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001968156eee000000000000000000000000000000000000000000000052441c370b72a330359ea1b2bf818e7da86df735ffd94703cf29b8f5da684f259a585ec13090ca4cbb2db658892ea1f000d00727a8eefb7b3353c25e22894677f6dba26992c122930077027d8f1a17c260ac3c556852cb5884c58a77221105398b5472a79241245ff6000000000000000000000000000000000000000000000000000000000000001c1544ea621b74a05bc5127bf53b16c40e87d99ffa9d2d98ba6cb9f4821844b60f57253ddaac342d602d1631ff299db248e51e5acc4220428da5593e59ca9c7cfa089b1f6ffa2d1957d4f4b9f4e9fbc57a170893bcd1fef89574ceac065f8a2bd6000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b207000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c30c6c4d3e786dbd7c0000000000000000000000000000000000000000000049c30c6c4d57e704380b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000006810ba10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d984c2e418d117dbdc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d5445794e444a6c4d793030593245304c5455355a5463744f544d344d5330325a4451344d545535595756694f546b6966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000008398735881381a4b02bec663a36be4eb27fbd3f00000000000000000000000000000000000000000000009168050bcc4062c88b00000000000000000000000000000000000000000000009168050bb2d84d599d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9ea1b2bf818e7da86df735ffd94703cf29b8f5da684f259a585ec13090ca4cbb",
      "signature": {
        "s": "0x77027d8f1a17c260ac3c556852cb5884c58a77221105398b5472a79241245ff6",
        "r": "0x2db658892ea1f000d00727a8eefb7b3353c25e22894677f6dba26992c1229300",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1544ea621b74a05bc5127bf53b16c40e87d99ffa9d2d98ba6cb9f4821844b60f",
      "signature": {
        "s": "0x089b1f6ffa2d1957d4f4b9f4e9fbc57a170893bcd1fef89574ceac065f8a2bd6",
        "r": "0x57253ddaac342d602d1631ff299db248e51e5acc4220428da5593e59ca9c7cfa",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "109120417518",
    "total": "1517540872260417695797"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "109120417518",
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
            "amount": "27624342337696925473756"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "109120417"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlMTEyNDJlMy00Y2E0LTU5ZTctOTM4MS02ZDQ4MTU5YWViOTkifQ==",
    "nonce": 111111,
    "balances": {
      "current": "348330763519214106819964",
      "previous": "348330763519323336357899"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x08398735881381a4b02bec663a36be4eb27fbd3f",
    "nonce": 46,
    "balances": {
      "current": "2682273300814594492555",
      "previous": "2682273300705474075037"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:36.833Z",
  "updated": "2022-05-04T08:56:36.911Z",
  "id": "62723fc43592fd001130b5ba"
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
0x0f200f9b00000000000000000000000000000000000000000000009168050bcc4062c88b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2682273300814594492555`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`