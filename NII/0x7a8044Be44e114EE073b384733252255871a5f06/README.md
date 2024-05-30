# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7a8044Be44e114EE073b384733252255871a5f06`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000d488a366adda2c0e1000000000000000000000000000000000000000000000000631576b25635af3f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000631576b25635af3f000000000000000000000000000000000000000000000006994f9349ddfe790bd67b389f54947a1550a08e67a9879279e191bb6675e8b90c5fb05f4560ebf4392847b60ba721928f9aafa9b4d0072e1e036cc4caa2f2d34ca7fcf51813e75ae067ca77182c99e908703751a0b8558186531956d2f381556fa333656d1472ac71000000000000000000000000000000000000000000000000000000000000001b15e62e46e90ae7546c50f4a2b88bff8951ea712d75e353114a1a013f37eba3e1618d9acaef168b418ccae89bcfbebb0eb4efb0ab51613e3df73c63b614f10800784ada7c0ec67352c09f850e15022152027cd2df851669831ac6a1eab95674fa000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b36a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c880034578d8e7f9373000000000000000000000000000000000000000000003c8863632bceeb73442600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000195d8f06be01740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce6fab2fbd6b290470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a6d46694d57597a596930784d444a694c54566d4e7a4d744f474d7a4e4330784d6a67334d574e6b5a574e6d5a47456966513d3d00000000000000000000000000000000000000000000000000000000000000240000000000000000000000007a8044be44e114ee073b384733252255871a5f0600000000000000000000000000000000000000000000000d488a366adda2c0e100000000000000000000000000000000000000000000000ce574bfb8876d11a200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd67b389f54947a1550a08e67a9879279e191bb6675e8b90c5fb05f4560ebf439",
      "signature": {
        "s": "0x67ca77182c99e908703751a0b8558186531956d2f381556fa333656d1472ac71",
        "r": "0x2847b60ba721928f9aafa9b4d0072e1e036cc4caa2f2d34ca7fcf51813e75ae0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x15e62e46e90ae7546c50f4a2b88bff8951ea712d75e353114a1a013f37eba3e1",
      "signature": {
        "s": "0x784ada7c0ec67352c09f850e15022152027cd2df851669831ac6a1eab95674fa",
        "r": "0x618d9acaef168b418ccae89bcfbebb0eb4efb0ab51613e3df73c63b614f10800",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7139743292588404543",
    "total": "121727674798686763275"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7139743292588404543",
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
            "amount": "27686759922731937075271"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7139743292588404"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0ZmFiMWYzYi0xMDJiLTVmNzMtOGMzNC0xMjg3MWNkZWNmZGEifQ==",
    "nonce": 111466,
    "balances": {
      "current": "285850760899167493526387",
      "previous": "285857907782203374519334"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7a8044be44e114ee073b384733252255871a5f06",
    "nonce": 36,
    "balances": {
      "current": "245034723108353917153",
      "previous": "237894979815765512610"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:27.905Z",
  "updated": "2022-05-04T08:58:28.010Z",
  "id": "627240337832e20011830d0c"
}
```
* *stageAmount*: `245034723108353917153`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000631576b25635af3f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000631576b25635af3f000000000000000000000000000000000000000000000006994f9349ddfe790bd67b389f54947a1550a08e67a9879279e191bb6675e8b90c5fb05f4560ebf4392847b60ba721928f9aafa9b4d0072e1e036cc4caa2f2d34ca7fcf51813e75ae067ca77182c99e908703751a0b8558186531956d2f381556fa333656d1472ac71000000000000000000000000000000000000000000000000000000000000001b15e62e46e90ae7546c50f4a2b88bff8951ea712d75e353114a1a013f37eba3e1618d9acaef168b418ccae89bcfbebb0eb4efb0ab51613e3df73c63b614f10800784ada7c0ec67352c09f850e15022152027cd2df851669831ac6a1eab95674fa000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b36a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c880034578d8e7f9373000000000000000000000000000000000000000000003c8863632bceeb73442600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000195d8f06be01740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce6fab2fbd6b290470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a6d46694d57597a596930784d444a694c54566d4e7a4d744f474d7a4e4330784d6a67334d574e6b5a574e6d5a47456966513d3d00000000000000000000000000000000000000000000000000000000000000240000000000000000000000007a8044be44e114ee073b384733252255871a5f0600000000000000000000000000000000000000000000000d488a366adda2c0e100000000000000000000000000000000000000000000000ce574bfb8876d11a200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd67b389f54947a1550a08e67a9879279e191bb6675e8b90c5fb05f4560ebf439",
      "signature": {
        "s": "0x67ca77182c99e908703751a0b8558186531956d2f381556fa333656d1472ac71",
        "r": "0x2847b60ba721928f9aafa9b4d0072e1e036cc4caa2f2d34ca7fcf51813e75ae0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x15e62e46e90ae7546c50f4a2b88bff8951ea712d75e353114a1a013f37eba3e1",
      "signature": {
        "s": "0x784ada7c0ec67352c09f850e15022152027cd2df851669831ac6a1eab95674fa",
        "r": "0x618d9acaef168b418ccae89bcfbebb0eb4efb0ab51613e3df73c63b614f10800",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7139743292588404543",
    "total": "121727674798686763275"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7139743292588404543",
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
            "amount": "27686759922731937075271"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7139743292588404"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0ZmFiMWYzYi0xMDJiLTVmNzMtOGMzNC0xMjg3MWNkZWNmZGEifQ==",
    "nonce": 111466,
    "balances": {
      "current": "285850760899167493526387",
      "previous": "285857907782203374519334"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7a8044be44e114ee073b384733252255871a5f06",
    "nonce": 36,
    "balances": {
      "current": "245034723108353917153",
      "previous": "237894979815765512610"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:27.905Z",
  "updated": "2022-05-04T08:58:28.010Z",
  "id": "627240337832e20011830d0c"
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
0x0f200f9b00000000000000000000000000000000000000000000000d488a366adda2c0e10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `245034723108353917153`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`