# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC45aEC3433C434169e48120f2b815dF77381B03C`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000073f0e2578943172760000000000000000000000000000000000000000000000073f0e2578943172760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000073f0e2578943172760000000000000000000000000000000000000000000000073f0e2578943172762f8c146ee19a5579d1f24b02053d478fd6218a4b3d4268af7afa42e5d12ed422236ff15779ced43b609215ed7eff881d7b6522652a92d5a5e33a8ffb77cad0170b90324adbaf58f826faa9b614e43fb495476fda43ae3f2cc9e37b1c327ece61000000000000000000000000000000000000000000000000000000000000001bf83d6a44b2a212b59637fc54682b3277b1be794bc71ce311155e3a83a856ab19240578d55f4888ab0533095d68fcb62af1ec2624e70fa5cb97c54fa7e03ab33a185b3544bc99c77c80b3903c35dda2f3e962a8319385231216c739afb9d6c159000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000abcc1d0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000ddf8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000009d020f6730e7ef676a40000000000000000000000000000000000000000000009d761df7d6dd9f5c8b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001dae4e6c6cddf9a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000021b10e66b3e472904c70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e325931596a59794d6930795a6d51324c5455304e545174596d5a684e433168595452684e446b7a4e6d4d355a54596966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000c45aec3433c434169e48120f2b815df77381b03c0000000000000000000000000000000000000000000000073f0e257894317276000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2f8c146ee19a5579d1f24b02053d478fd6218a4b3d4268af7afa42e5d12ed422",
      "signature": {
        "s": "0x0b90324adbaf58f826faa9b614e43fb495476fda43ae3f2cc9e37b1c327ece61",
        "r": "0x236ff15779ced43b609215ed7eff881d7b6522652a92d5a5e33a8ffb77cad017",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf83d6a44b2a212b59637fc54682b3277b1be794bc71ce311155e3a83a856ab19",
      "signature": {
        "s": "0x185b3544bc99c77c80b3903c35dda2f3e962a8319385231216c739afb9d6c159",
        "r": "0x240578d55f4888ab0533095d68fcb62af1ec2624e70fa5cb97c54fa7e03ab33a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "133670818789842842230",
    "total": "133670818789842842230"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "133670818789842842230",
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
            "amount": "9944012834393924633799"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "133670818789842842"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5N2Y1YjYyMi0yZmQ2LTU0NTQtYmZhNC1hYTRhNDkzNmM5ZTYifQ==",
    "nonce": 56824,
    "balances": {
      "current": "46340596325517974992548",
      "previous": "46474400815126607677620"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc45aec3433c434169e48120f2b815df77381b03c",
    "nonce": 1,
    "balances": {
      "current": "133670818789842842230",
      "previous": "0"
    }
  },
  "blockNumber": "11258909",
  "created": "2020-11-14T23:41:13.456Z",
  "updated": "2020-11-14T23:41:13.523Z",
  "id": "5fb06b1915d35e00135e9e67"
}
```
* *stageAmount*: `133670818789842842230`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000073f0e2578943172760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000073f0e2578943172760000000000000000000000000000000000000000000000073f0e2578943172762f8c146ee19a5579d1f24b02053d478fd6218a4b3d4268af7afa42e5d12ed422236ff15779ced43b609215ed7eff881d7b6522652a92d5a5e33a8ffb77cad0170b90324adbaf58f826faa9b614e43fb495476fda43ae3f2cc9e37b1c327ece61000000000000000000000000000000000000000000000000000000000000001bf83d6a44b2a212b59637fc54682b3277b1be794bc71ce311155e3a83a856ab19240578d55f4888ab0533095d68fcb62af1ec2624e70fa5cb97c54fa7e03ab33a185b3544bc99c77c80b3903c35dda2f3e962a8319385231216c739afb9d6c159000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000abcc1d0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000ddf8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000009d020f6730e7ef676a40000000000000000000000000000000000000000000009d761df7d6dd9f5c8b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001dae4e6c6cddf9a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000021b10e66b3e472904c70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e325931596a59794d6930795a6d51324c5455304e545174596d5a684e433168595452684e446b7a4e6d4d355a54596966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000c45aec3433c434169e48120f2b815df77381b03c0000000000000000000000000000000000000000000000073f0e257894317276000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2f8c146ee19a5579d1f24b02053d478fd6218a4b3d4268af7afa42e5d12ed422",
      "signature": {
        "s": "0x0b90324adbaf58f826faa9b614e43fb495476fda43ae3f2cc9e37b1c327ece61",
        "r": "0x236ff15779ced43b609215ed7eff881d7b6522652a92d5a5e33a8ffb77cad017",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf83d6a44b2a212b59637fc54682b3277b1be794bc71ce311155e3a83a856ab19",
      "signature": {
        "s": "0x185b3544bc99c77c80b3903c35dda2f3e962a8319385231216c739afb9d6c159",
        "r": "0x240578d55f4888ab0533095d68fcb62af1ec2624e70fa5cb97c54fa7e03ab33a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "133670818789842842230",
    "total": "133670818789842842230"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "133670818789842842230",
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
            "amount": "9944012834393924633799"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "133670818789842842"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5N2Y1YjYyMi0yZmQ2LTU0NTQtYmZhNC1hYTRhNDkzNmM5ZTYifQ==",
    "nonce": 56824,
    "balances": {
      "current": "46340596325517974992548",
      "previous": "46474400815126607677620"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc45aec3433c434169e48120f2b815df77381b03c",
    "nonce": 1,
    "balances": {
      "current": "133670818789842842230",
      "previous": "0"
    }
  },
  "blockNumber": "11258909",
  "created": "2020-11-14T23:41:13.456Z",
  "updated": "2020-11-14T23:41:13.523Z",
  "id": "5fb06b1915d35e00135e9e67"
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
0x0f200f9b0000000000000000000000000000000000000000000000073f0e2578943172760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `133670818789842842230`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`