# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x0Fc773e816074091CAc89CD4c701D49027e7E128`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000009c02e8c83080000000000000000000000000000000000000000000000000000001581f551b10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001581f551b100000000000000000000000000000000000000000000001187b6539a93c789512711dece01d7fdaccb7a73539c4cc6b8926df2864b0f21bd4d0db13acc2498ee64bf2b5e60f7ba830a2b6a8124be15e5c872b8ca4cad4a6b6aca303095ff32c971333723b0914df6d7284cedba152d7ed34662918424ce2e773e929085403f88000000000000000000000000000000000000000000000000000000000000001c6ee89d226fb6b4298b44f71fa37b245265b1815392759f045efc5d97548f22ab2a6131154485ef5d4ac078fb3fa070b0a690bb3b53905c1ad11b2741cec128dd5abc9ef1c69b1a0d187a1d4137a9d63ae56f49ba80a68d4caf26b580965ea920000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1b0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a915944ea389cf3106d000000000000000000000000000000000000000000004a915944ea4e2469e89900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000581867b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d950004f18d29757bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68596a6b774d57466c4d69316b4e7a526c4c54566c4e6a6374596d4a6d4e79316d5a54686d4d44686a4d6d56685a6d456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000000fc773e816074091cac89cd4c701d49027e7e128000000000000000000000000000000000000000000000000000009c02e8c8308000000000000000000000000000000000000000000000000000009aaac97315700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x2711dece01d7fdaccb7a73539c4cc6b8926df2864b0f21bd4d0db13acc2498ee",
      "signature": {
        "s": "0x71333723b0914df6d7284cedba152d7ed34662918424ce2e773e929085403f88",
        "r": "0x64bf2b5e60f7ba830a2b6a8124be15e5c872b8ca4cad4a6b6aca303095ff32c9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6ee89d226fb6b4298b44f71fa37b245265b1815392759f045efc5d97548f22ab",
      "signature": {
        "s": "0x5abc9ef1c69b1a0d187a1d4137a9d63ae56f49ba80a68d4caf26b580965ea920",
        "r": "0x2a6131154485ef5d4ac078fb3fa070b0a690bb3b53905c1ad11b2741cec128dd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "92374651313",
    "total": "323373744817313384785"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "92374651313",
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
            "amount": "27620540572834263947196"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "92374651"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhYjkwMWFlMi1kNzRlLTVlNjctYmJmNy1mZThmMDhjMmVhZmEifQ==",
    "nonce": 111024,
    "balances": {
      "current": "352136330146738294952045",
      "previous": "352136330146830761978009"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fc773e816074091cac89cd4c701d49027e7e128",
    "nonce": 46,
    "balances": {
      "current": "10721019331336",
      "previous": "10628644680023"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:12.160Z",
  "updated": "2022-05-04T08:56:12.225Z",
  "id": "62723fac7832e20011830c75"
}
```
* *stageAmount*: `10721019331336`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000001581f551b10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001581f551b100000000000000000000000000000000000000000000001187b6539a93c789512711dece01d7fdaccb7a73539c4cc6b8926df2864b0f21bd4d0db13acc2498ee64bf2b5e60f7ba830a2b6a8124be15e5c872b8ca4cad4a6b6aca303095ff32c971333723b0914df6d7284cedba152d7ed34662918424ce2e773e929085403f88000000000000000000000000000000000000000000000000000000000000001c6ee89d226fb6b4298b44f71fa37b245265b1815392759f045efc5d97548f22ab2a6131154485ef5d4ac078fb3fa070b0a690bb3b53905c1ad11b2741cec128dd5abc9ef1c69b1a0d187a1d4137a9d63ae56f49ba80a68d4caf26b580965ea920000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1b0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a915944ea389cf3106d000000000000000000000000000000000000000000004a915944ea4e2469e89900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000581867b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d950004f18d29757bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68596a6b774d57466c4d69316b4e7a526c4c54566c4e6a6374596d4a6d4e79316d5a54686d4d44686a4d6d56685a6d456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000000fc773e816074091cac89cd4c701d49027e7e128000000000000000000000000000000000000000000000000000009c02e8c8308000000000000000000000000000000000000000000000000000009aaac97315700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x2711dece01d7fdaccb7a73539c4cc6b8926df2864b0f21bd4d0db13acc2498ee",
      "signature": {
        "s": "0x71333723b0914df6d7284cedba152d7ed34662918424ce2e773e929085403f88",
        "r": "0x64bf2b5e60f7ba830a2b6a8124be15e5c872b8ca4cad4a6b6aca303095ff32c9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6ee89d226fb6b4298b44f71fa37b245265b1815392759f045efc5d97548f22ab",
      "signature": {
        "s": "0x5abc9ef1c69b1a0d187a1d4137a9d63ae56f49ba80a68d4caf26b580965ea920",
        "r": "0x2a6131154485ef5d4ac078fb3fa070b0a690bb3b53905c1ad11b2741cec128dd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "92374651313",
    "total": "323373744817313384785"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "92374651313",
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
            "amount": "27620540572834263947196"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "92374651"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhYjkwMWFlMi1kNzRlLTVlNjctYmJmNy1mZThmMDhjMmVhZmEifQ==",
    "nonce": 111024,
    "balances": {
      "current": "352136330146738294952045",
      "previous": "352136330146830761978009"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fc773e816074091cac89cd4c701d49027e7e128",
    "nonce": 46,
    "balances": {
      "current": "10721019331336",
      "previous": "10628644680023"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:12.160Z",
  "updated": "2022-05-04T08:56:12.225Z",
  "id": "62723fac7832e20011830c75"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000000000009c02e8c83080000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `10721019331336`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`