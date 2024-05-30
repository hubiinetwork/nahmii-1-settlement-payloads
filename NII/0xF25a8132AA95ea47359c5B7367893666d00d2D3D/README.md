# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF25a8132AA95ea47359c5B7367893666d00d2D3D`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000dd23ae50b1235fb1100000000000000000000000000000000000000000000000000000002936fb7dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002936fb7dc0000000000000000000000000000000000000000000000076b7221f4db6cfde0790e158a7e0a0d1164aa72f3d6f89876488a684056caff00a2693e642f91df2c047fc6a485fc68d22e56e00beedb291458a96ec88204222857b6655bd941706f310fca3dfec129d83849d2a6cda303f0145fd4e2f3a4c506dae62fa533d631e2000000000000000000000000000000000000000000000000000000000000001bf36a5eb17faf2b4a1470a66b84d314e958fe6281711298f6926c7a2225060e1ecd03f41918f98c5f59b8812c129492b1f5affff2f370eeb740496430ebe55d9836cdc840e1c69b61f4719e39ee988b4fdcacfcd7c0e0314e33ecbd1d72593912000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af27000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095ac7774ccd24c8f01760000000000000000000000000000000000000000000095ac7774ccd4e0a78a2400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000a8d0d20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61ac6b7fb422d0ee90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a4449315a6a4d7a5a53316a597a51774c5455304e7a45744f545a694f5330304d54633359544d795a445a6b597a456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f25a8132aa95ea47359c5b7367893666d00d2d3d00000000000000000000000000000000000000000000000dd23ae50b1235fb1100000000000000000000000000000000000000000000000dd23ae5087ec6433500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x790e158a7e0a0d1164aa72f3d6f89876488a684056caff00a2693e642f91df2c",
      "signature": {
        "s": "0x310fca3dfec129d83849d2a6cda303f0145fd4e2f3a4c506dae62fa533d631e2",
        "r": "0x047fc6a485fc68d22e56e00beedb291458a96ec88204222857b6655bd941706f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf36a5eb17faf2b4a1470a66b84d314e958fe6281711298f6926c7a2225060e1e",
      "signature": {
        "s": "0x36cdc840e1c69b61f4719e39ee988b4fdcacfcd7c0e0314e33ecbd1d72593912",
        "r": "0xcd03f41918f98c5f59b8812c129492b1f5affff2f370eeb740496430ebe55d98",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11063506908",
    "total": "136869496560907255264"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11063506908",
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
            "amount": "27266217172722867048169"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11063506"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZDI1ZjMzZS1jYzQwLTU0NzEtOTZiOS00MTc3YTMyZDZkYzEifQ==",
    "nonce": 110375,
    "balances": {
      "current": "706814053658246591218038",
      "previous": "706814053658257665788452"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf25a8132aa95ea47359c5b7367893666d00d2d3d",
    "nonce": 46,
    "balances": {
      "current": "254956345090551184145",
      "previous": "254956345079487677237"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:57.619Z",
  "updated": "2022-05-04T08:52:57.701Z",
  "id": "62723ee93592fd001130b4c7"
}
```
* *stageAmount*: `254956345090551184145`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000002936fb7dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002936fb7dc0000000000000000000000000000000000000000000000076b7221f4db6cfde0790e158a7e0a0d1164aa72f3d6f89876488a684056caff00a2693e642f91df2c047fc6a485fc68d22e56e00beedb291458a96ec88204222857b6655bd941706f310fca3dfec129d83849d2a6cda303f0145fd4e2f3a4c506dae62fa533d631e2000000000000000000000000000000000000000000000000000000000000001bf36a5eb17faf2b4a1470a66b84d314e958fe6281711298f6926c7a2225060e1ecd03f41918f98c5f59b8812c129492b1f5affff2f370eeb740496430ebe55d9836cdc840e1c69b61f4719e39ee988b4fdcacfcd7c0e0314e33ecbd1d72593912000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af27000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095ac7774ccd24c8f01760000000000000000000000000000000000000000000095ac7774ccd4e0a78a2400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000a8d0d20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61ac6b7fb422d0ee90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a4449315a6a4d7a5a53316a597a51774c5455304e7a45744f545a694f5330304d54633359544d795a445a6b597a456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f25a8132aa95ea47359c5b7367893666d00d2d3d00000000000000000000000000000000000000000000000dd23ae50b1235fb1100000000000000000000000000000000000000000000000dd23ae5087ec6433500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x790e158a7e0a0d1164aa72f3d6f89876488a684056caff00a2693e642f91df2c",
      "signature": {
        "s": "0x310fca3dfec129d83849d2a6cda303f0145fd4e2f3a4c506dae62fa533d631e2",
        "r": "0x047fc6a485fc68d22e56e00beedb291458a96ec88204222857b6655bd941706f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf36a5eb17faf2b4a1470a66b84d314e958fe6281711298f6926c7a2225060e1e",
      "signature": {
        "s": "0x36cdc840e1c69b61f4719e39ee988b4fdcacfcd7c0e0314e33ecbd1d72593912",
        "r": "0xcd03f41918f98c5f59b8812c129492b1f5affff2f370eeb740496430ebe55d98",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11063506908",
    "total": "136869496560907255264"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11063506908",
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
            "amount": "27266217172722867048169"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11063506"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZDI1ZjMzZS1jYzQwLTU0NzEtOTZiOS00MTc3YTMyZDZkYzEifQ==",
    "nonce": 110375,
    "balances": {
      "current": "706814053658246591218038",
      "previous": "706814053658257665788452"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf25a8132aa95ea47359c5b7367893666d00d2d3d",
    "nonce": 46,
    "balances": {
      "current": "254956345090551184145",
      "previous": "254956345079487677237"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:57.619Z",
  "updated": "2022-05-04T08:52:57.701Z",
  "id": "62723ee93592fd001130b4c7"
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
0x0f200f9b00000000000000000000000000000000000000000000000dd23ae50b1235fb110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `254956345090551184145`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`