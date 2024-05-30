# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCa7824ef015Ada937EdBF8f9F6e03cc896d9EA27`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000d9a460c488d7dd28d80000000000000000000000000000000000000000000000000000002987d4303d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002987d4303d0000000000000000000000000000000000000000000000726e9a3aa64e9ac5fe785042e9db6101a7d16663bdf7bc26f20d6f5adf39661f43846868c0b1413e7311454f151e8656d2550acc43e4a2274458e1a4059a806304f50e2f2e4209332e2058e5acf2d140761f388d5432d1777ad2a75030505327bc6bd5f5bdf74dc21d000000000000000000000000000000000000000000000000000000000000001bd370c1a6a85b773f5bedcdd54d022fbafc374909f68e413005d033782eece265a682319808c9c43c5234c68e3c6d906a5692555580f300c3ddc1a4b490d5dc71237ae53000b18ebc6a77fe1d3670a0d322b2df0a20788430a11f1400f01e36eb000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b08a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004cf05eb62e3e92889783000000000000000000000000000000000000000000004cf05eb62e6824fe874900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000aa1bf890000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8b4c24e4303b459bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a686c4f544d324e7930794d44646c4c54566c4d6d5574595442694e533169597a49314f54566b4e4459345932516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000ca7824ef015ada937edbf8f9f6e03cc896d9ea270000000000000000000000000000000000000000000000d9a460c488d7dd28d80000000000000000000000000000000000000000000000d9a460c45f5008f89b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x785042e9db6101a7d16663bdf7bc26f20d6f5adf39661f43846868c0b1413e73",
      "signature": {
        "s": "0x2058e5acf2d140761f388d5432d1777ad2a75030505327bc6bd5f5bdf74dc21d",
        "r": "0x11454f151e8656d2550acc43e4a2274458e1a4059a806304f50e2f2e4209332e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd370c1a6a85b773f5bedcdd54d022fbafc374909f68e413005d033782eece265",
      "signature": {
        "s": "0x237ae53000b18ebc6a77fe1d3670a0d322b2df0a20788430a11f1400f01e36eb",
        "r": "0xa682319808c9c43c5234c68e3c6d906a5692555580f300c3ddc1a4b490d5dc71",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "178372489277",
    "total": "2110898571379432146430"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "178372489277",
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
            "amount": "27609354193391530039739"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "178372489"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMzhlOTM2Ny0yMDdlLTVlMmUtYTBiNS1iYzI1OTVkNDY4Y2QifQ==",
    "nonce": 110730,
    "balances": {
      "current": "363333895968914936469379",
      "previous": "363333895969093487331145"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca7824ef015ada937edbf8f9f6e03cc896d9ea27",
    "nonce": 46,
    "balances": {
      "current": "4014788147106973296856",
      "previous": "4014788146928600807579"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:44.200Z",
  "updated": "2022-05-04T08:54:44.269Z",
  "id": "62723f543592fd001130b53d"
}
```
* *stageAmount*: `4014788147106973296856`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000002987d4303d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002987d4303d0000000000000000000000000000000000000000000000726e9a3aa64e9ac5fe785042e9db6101a7d16663bdf7bc26f20d6f5adf39661f43846868c0b1413e7311454f151e8656d2550acc43e4a2274458e1a4059a806304f50e2f2e4209332e2058e5acf2d140761f388d5432d1777ad2a75030505327bc6bd5f5bdf74dc21d000000000000000000000000000000000000000000000000000000000000001bd370c1a6a85b773f5bedcdd54d022fbafc374909f68e413005d033782eece265a682319808c9c43c5234c68e3c6d906a5692555580f300c3ddc1a4b490d5dc71237ae53000b18ebc6a77fe1d3670a0d322b2df0a20788430a11f1400f01e36eb000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b08a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004cf05eb62e3e92889783000000000000000000000000000000000000000000004cf05eb62e6824fe874900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000aa1bf890000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8b4c24e4303b459bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a686c4f544d324e7930794d44646c4c54566c4d6d5574595442694e533169597a49314f54566b4e4459345932516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000ca7824ef015ada937edbf8f9f6e03cc896d9ea270000000000000000000000000000000000000000000000d9a460c488d7dd28d80000000000000000000000000000000000000000000000d9a460c45f5008f89b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x785042e9db6101a7d16663bdf7bc26f20d6f5adf39661f43846868c0b1413e73",
      "signature": {
        "s": "0x2058e5acf2d140761f388d5432d1777ad2a75030505327bc6bd5f5bdf74dc21d",
        "r": "0x11454f151e8656d2550acc43e4a2274458e1a4059a806304f50e2f2e4209332e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd370c1a6a85b773f5bedcdd54d022fbafc374909f68e413005d033782eece265",
      "signature": {
        "s": "0x237ae53000b18ebc6a77fe1d3670a0d322b2df0a20788430a11f1400f01e36eb",
        "r": "0xa682319808c9c43c5234c68e3c6d906a5692555580f300c3ddc1a4b490d5dc71",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "178372489277",
    "total": "2110898571379432146430"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "178372489277",
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
            "amount": "27609354193391530039739"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "178372489"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMzhlOTM2Ny0yMDdlLTVlMmUtYTBiNS1iYzI1OTVkNDY4Y2QifQ==",
    "nonce": 110730,
    "balances": {
      "current": "363333895968914936469379",
      "previous": "363333895969093487331145"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca7824ef015ada937edbf8f9f6e03cc896d9ea27",
    "nonce": 46,
    "balances": {
      "current": "4014788147106973296856",
      "previous": "4014788146928600807579"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:44.200Z",
  "updated": "2022-05-04T08:54:44.269Z",
  "id": "62723f543592fd001130b53d"
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
0x0f200f9b0000000000000000000000000000000000000000000000d9a460c488d7dd28d80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4014788147106973296856`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`