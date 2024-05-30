# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x870cA5c4319F8e534e2b5eB3EF0D82D6d4279e5d`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de2ba37f371f11800000000000000000000000000000000000000000000026afede29f1756880000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000026afede29f17568800000000000000000000000000000000000000000000000026afede29f175688000decc6d9436555d77dc3f2d021cf9225824c36a62e97ecff3cf0733d2877b7168642af9733b156d6c8ae434c81308659c116ea01ea6c8574a0aea29475946f39e78abbf4a1400a0a21c5f937ed9553ce7e3f0ce123eeba09f42c6a7860b5318f2000000000000000000000000000000000000000000000000000000000000001c43a6412e6714b9a992b0c56a51f80428c910aef132c37e6fddac7c183954fe1a409bfb961cff8365bb9b478abf55d4822d96f5c428f0ee69158eaf8257445a581ca8f371a242f5be7f91690e96df724f7002659d55b9e3389dac881ebfd043e0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e262d500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000032000000000000000000000000870ca5c4319f8e534e2b5eb3ef0d82d6d4279e5d0000000000000000000000000000000000000000000000000de2ba37f371f11800000000000000000000000000000000000000000000026bab3762aaee58c11800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000009e767e81857e50000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009e767e81857e50000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f544d7a5a6a49334d7930774f4759354c54517a4f5445745954426b4d69316a4e574a6c4d32466d595759785932556966513d3d000000000000000000000000000000000000000000000000000000000000008b000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000712f777a7146a041ff70000000000000000000000000000000000000000000006ec4789c47552ad97f7000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdecc6d9436555d77dc3f2d021cf9225824c36a62e97ecff3cf0733d2877b7168",
      "signature": {
        "s": "0x78abbf4a1400a0a21c5f937ed9553ce7e3f0ce123eeba09f42c6a7860b5318f2",
        "r": "0x642af9733b156d6c8ae434c81308659c116ea01ea6c8574a0aea29475946f39e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x43a6412e6714b9a992b0c56a51f80428c910aef132c37e6fddac7c183954fe1a",
      "signature": {
        "s": "0x1ca8f371a242f5be7f91690e96df724f7002659d55b9e3389dac881ebfd043e0",
        "r": "0x409bfb961cff8365bb9b478abf55d4822d96f5c428f0ee69158eaf8257445a58",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11418453000000000000000",
    "total": "11418453000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11418453000000000000000",
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
            "amount": "11418453000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11418453000000000000"
      }
    },
    "wallet": "0x870ca5c4319f8e534e2b5eb3ef0d82d6d4279e5d",
    "data": "eyJyZWYiOiIwOTMzZjI3My0wOGY5LTQzOTEtYTBkMi1jNWJlM2FmYWYxY2UifQ==",
    "nonce": 50,
    "balances": {
      "current": "1000566816699969816",
      "previous": "11430872019816699969816"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 139,
    "balances": {
      "current": "534503018853920080527216",
      "previous": "523084565853920080527216"
    }
  },
  "blockNumber": "14836437",
  "created": "2022-05-24T15:07:07.829Z",
  "updated": "2022-05-24T15:07:07.935Z",
  "id": "628cf49b7832e20011830f46"
}
```
* *stageAmount*: `1000566816699969816`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000026afede29f1756880000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000026afede29f17568800000000000000000000000000000000000000000000000026afede29f175688000decc6d9436555d77dc3f2d021cf9225824c36a62e97ecff3cf0733d2877b7168642af9733b156d6c8ae434c81308659c116ea01ea6c8574a0aea29475946f39e78abbf4a1400a0a21c5f937ed9553ce7e3f0ce123eeba09f42c6a7860b5318f2000000000000000000000000000000000000000000000000000000000000001c43a6412e6714b9a992b0c56a51f80428c910aef132c37e6fddac7c183954fe1a409bfb961cff8365bb9b478abf55d4822d96f5c428f0ee69158eaf8257445a581ca8f371a242f5be7f91690e96df724f7002659d55b9e3389dac881ebfd043e0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e262d500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000032000000000000000000000000870ca5c4319f8e534e2b5eb3ef0d82d6d4279e5d0000000000000000000000000000000000000000000000000de2ba37f371f11800000000000000000000000000000000000000000000026bab3762aaee58c11800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000009e767e81857e50000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009e767e81857e50000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f544d7a5a6a49334d7930774f4759354c54517a4f5445745954426b4d69316a4e574a6c4d32466d595759785932556966513d3d000000000000000000000000000000000000000000000000000000000000008b000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000712f777a7146a041ff70000000000000000000000000000000000000000000006ec4789c47552ad97f7000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdecc6d9436555d77dc3f2d021cf9225824c36a62e97ecff3cf0733d2877b7168",
      "signature": {
        "s": "0x78abbf4a1400a0a21c5f937ed9553ce7e3f0ce123eeba09f42c6a7860b5318f2",
        "r": "0x642af9733b156d6c8ae434c81308659c116ea01ea6c8574a0aea29475946f39e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x43a6412e6714b9a992b0c56a51f80428c910aef132c37e6fddac7c183954fe1a",
      "signature": {
        "s": "0x1ca8f371a242f5be7f91690e96df724f7002659d55b9e3389dac881ebfd043e0",
        "r": "0x409bfb961cff8365bb9b478abf55d4822d96f5c428f0ee69158eaf8257445a58",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11418453000000000000000",
    "total": "11418453000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11418453000000000000000",
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
            "amount": "11418453000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11418453000000000000"
      }
    },
    "wallet": "0x870ca5c4319f8e534e2b5eb3ef0d82d6d4279e5d",
    "data": "eyJyZWYiOiIwOTMzZjI3My0wOGY5LTQzOTEtYTBkMi1jNWJlM2FmYWYxY2UifQ==",
    "nonce": 50,
    "balances": {
      "current": "1000566816699969816",
      "previous": "11430872019816699969816"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 139,
    "balances": {
      "current": "534503018853920080527216",
      "previous": "523084565853920080527216"
    }
  },
  "blockNumber": "14836437",
  "created": "2022-05-24T15:07:07.829Z",
  "updated": "2022-05-24T15:07:07.935Z",
  "id": "628cf49b7832e20011830f46"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de2ba37f371f1180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000566816699969816`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`