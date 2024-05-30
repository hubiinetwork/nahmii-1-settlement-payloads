# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3961B486bee403E712B52c87827266aD8adD1424`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000003457c8fe89130000000000000000000000000000000000000000000000000000013db199b2720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000013db199b272000000000000000000000000000000000000000000000000000022d2cba9aae598bb8d3d1a3337b92845238b3dfd02a66958fd035b44dc0df616fa77b68460eb67a8a0f5b6ccc83fd805296eedd71a9b3343fd80393fbc58813fb9180128ab9d280f590412b495987416dd4e7dcd2e9bc1065248bf37bdaef3649c90cc2cf725000000000000000000000000000000000000000000000000000000000000001cd546a5d07811bc38ef33b105886b8e6a626c9b3bbc4c68ce53f7032df2fc9142b0ff8058b403ddf294891a50cf4e07070bc91ae0bfaec4f083f2bb7ce5c8885928e852625d6453bebbb15c6d0b83e97dca745a7f380ccae94874d30b7a42e0bf000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ba0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac73000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a852c2aa4801738c6d5000000000000000000000000000000000000000000009a852c2aa5be1a26d9f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000515460b00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4dd790be7e770aa950000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6a67354e4751334d5331684d5445344c5455304e7a6374596d59314e7930334d6a51344d6a6b354f5467314d6d596966513d3d000000000000000000000000000000000000000000000000000000000000002d0000000000000000000000003961b486bee403e712b52c87827266ad8add142400000000000000000000000000000000000000000000000000003457c8fe89130000000000000000000000000000000000000000000000000000331a1764d6a100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x98bb8d3d1a3337b92845238b3dfd02a66958fd035b44dc0df616fa77b68460eb",
      "signature": {
        "s": "0x280f590412b495987416dd4e7dcd2e9bc1065248bf37bdaef3649c90cc2cf725",
        "r": "0x67a8a0f5b6ccc83fd805296eedd71a9b3343fd80393fbc58813fb9180128ab9d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd546a5d07811bc38ef33b105886b8e6a626c9b3bbc4c68ce53f7032df2fc9142",
      "signature": {
        "s": "0x28e852625d6453bebbb15c6d0b83e97dca745a7f380ccae94874d30b7a42e0bf",
        "r": "0xb0ff8058b403ddf294891a50cf4e07070bc91ae0bfaec4f083f2bb7ce5c88859",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1364484272754",
    "total": "38288755370725"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1364484272754",
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
            "amount": "27243353052640510519957"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1364484272"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZjg5NGQ3MS1hMTE4LTU0NzctYmY1Ny03MjQ4Mjk5OTg1MmYifQ==",
    "nonce": 109683,
    "balances": {
      "current": "729701037860685476316885",
      "previous": "729701037862051325073911"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3961b486bee403e712b52c87827266ad8add1424",
    "nonce": 45,
    "balances": {
      "current": "57551638923539",
      "previous": "56187154650785"
    }
  },
  "blockNumber": "14709946",
  "created": "2022-05-04T08:49:22.626Z",
  "updated": "2022-05-04T08:49:22.735Z",
  "id": "62723e123592fd001130b3e2"
}
```
* *stageAmount*: `57551638923539`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000013db199b2720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000013db199b272000000000000000000000000000000000000000000000000000022d2cba9aae598bb8d3d1a3337b92845238b3dfd02a66958fd035b44dc0df616fa77b68460eb67a8a0f5b6ccc83fd805296eedd71a9b3343fd80393fbc58813fb9180128ab9d280f590412b495987416dd4e7dcd2e9bc1065248bf37bdaef3649c90cc2cf725000000000000000000000000000000000000000000000000000000000000001cd546a5d07811bc38ef33b105886b8e6a626c9b3bbc4c68ce53f7032df2fc9142b0ff8058b403ddf294891a50cf4e07070bc91ae0bfaec4f083f2bb7ce5c8885928e852625d6453bebbb15c6d0b83e97dca745a7f380ccae94874d30b7a42e0bf000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ba0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac73000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a852c2aa4801738c6d5000000000000000000000000000000000000000000009a852c2aa5be1a26d9f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000515460b00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4dd790be7e770aa950000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6a67354e4751334d5331684d5445344c5455304e7a6374596d59314e7930334d6a51344d6a6b354f5467314d6d596966513d3d000000000000000000000000000000000000000000000000000000000000002d0000000000000000000000003961b486bee403e712b52c87827266ad8add142400000000000000000000000000000000000000000000000000003457c8fe89130000000000000000000000000000000000000000000000000000331a1764d6a100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x98bb8d3d1a3337b92845238b3dfd02a66958fd035b44dc0df616fa77b68460eb",
      "signature": {
        "s": "0x280f590412b495987416dd4e7dcd2e9bc1065248bf37bdaef3649c90cc2cf725",
        "r": "0x67a8a0f5b6ccc83fd805296eedd71a9b3343fd80393fbc58813fb9180128ab9d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd546a5d07811bc38ef33b105886b8e6a626c9b3bbc4c68ce53f7032df2fc9142",
      "signature": {
        "s": "0x28e852625d6453bebbb15c6d0b83e97dca745a7f380ccae94874d30b7a42e0bf",
        "r": "0xb0ff8058b403ddf294891a50cf4e07070bc91ae0bfaec4f083f2bb7ce5c88859",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1364484272754",
    "total": "38288755370725"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1364484272754",
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
            "amount": "27243353052640510519957"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1364484272"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZjg5NGQ3MS1hMTE4LTU0NzctYmY1Ny03MjQ4Mjk5OTg1MmYifQ==",
    "nonce": 109683,
    "balances": {
      "current": "729701037860685476316885",
      "previous": "729701037862051325073911"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3961b486bee403e712b52c87827266ad8add1424",
    "nonce": 45,
    "balances": {
      "current": "57551638923539",
      "previous": "56187154650785"
    }
  },
  "blockNumber": "14709946",
  "created": "2022-05-04T08:49:22.626Z",
  "updated": "2022-05-04T08:49:22.735Z",
  "id": "62723e123592fd001130b3e2"
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
0x0f200f9b00000000000000000000000000000000000000000000000000003457c8fe89130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `57551638923539`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`