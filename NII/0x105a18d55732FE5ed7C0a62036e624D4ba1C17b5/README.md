# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x105a18d55732FE5ed7C0a62036e624D4ba1C17b5`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000125eef0692d227270000000000000000000000000000000000000000000000000000000b83c7b33e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000b83c7b33e0000000000000000000000000000000000000000000000000000010cbc6e4d9610466f9c6d144cf7153f9e7d2c1c69bc5d986d029ff14d69f12d3065cb05592bde2144867219f36a458e45d7f78402f7fcd804e6d007c899fe1c7ac000884ef44a90f7e990d4251a9bbc37f7ab2b129f33ea48c0ef0216befd4bcbe30169c4c8000000000000000000000000000000000000000000000000000000000000001cb56474dd84ac8cf0e60e1224e61dab896f3f9dc4bfd289e8a9314a5fde746b1db90b0b6c5f11006d8078448b918582111358ff177734c8b3356730c7a25014340d9d1737e33e4965435c72cca05e9266cf5511fbf8976d68356f572bc7528cf2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b729000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002f20e6e295c1d017251c000000000000000000000000000000000000000000002f20e6e295cd56d17a1100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002f2a1b70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e054768fa0ff4b987f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5954557a5a6a55355a5330304d4449324c5455334d474574595445334e79316d4e544269597a41315a4449335a54496966513d3d000000000000000000000000000000000000000000000000000000000000002a000000000000000000000000105a18d55732fe5ed7c0a62036e624d4ba1c17b5000000000000000000000000000000000000000000000000125eef0692d22727000000000000000000000000000000000000000000000000125eeefb0f0a73e900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x10466f9c6d144cf7153f9e7d2c1c69bc5d986d029ff14d69f12d3065cb05592b",
      "signature": {
        "s": "0x4a90f7e990d4251a9bbc37f7ab2b129f33ea48c0ef0216befd4bcbe30169c4c8",
        "r": "0xde2144867219f36a458e45d7f78402f7fcd804e6d007c899fe1c7ac000884ef4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb56474dd84ac8cf0e60e1224e61dab896f3f9dc4bfd289e8a9314a5fde746b1d",
      "signature": {
        "s": "0x0d9d1737e33e4965435c72cca05e9266cf5511fbf8976d68356f572bc7528cf2",
        "r": "0xb90b0b6c5f11006d8078448b918582111358ff177734c8b3356730c7a2501434",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "49455543102",
    "total": "1154212580758"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "49455543102",
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
            "amount": "27749989296727244118143"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "49455543"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjYTUzZjU5ZS00MDI2LTU3MGEtYTE3Ny1mNTBiYzA1ZDI3ZTIifQ==",
    "nonce": 112425,
    "balances": {
      "current": "222558157529865143133468",
      "previous": "222558157529914648132113"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x105a18d55732fe5ed7c0a62036e624d4ba1c17b5",
    "nonce": 42,
    "balances": {
      "current": "1323758152005592871",
      "previous": "1323758102550049769"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:43.856Z",
  "updated": "2022-05-04T09:03:43.943Z",
  "id": "6272416f3592fd001130b787"
}
```
* *stageAmount*: `1323758152005592871`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000b83c7b33e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000b83c7b33e0000000000000000000000000000000000000000000000000000010cbc6e4d9610466f9c6d144cf7153f9e7d2c1c69bc5d986d029ff14d69f12d3065cb05592bde2144867219f36a458e45d7f78402f7fcd804e6d007c899fe1c7ac000884ef44a90f7e990d4251a9bbc37f7ab2b129f33ea48c0ef0216befd4bcbe30169c4c8000000000000000000000000000000000000000000000000000000000000001cb56474dd84ac8cf0e60e1224e61dab896f3f9dc4bfd289e8a9314a5fde746b1db90b0b6c5f11006d8078448b918582111358ff177734c8b3356730c7a25014340d9d1737e33e4965435c72cca05e9266cf5511fbf8976d68356f572bc7528cf2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b729000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002f20e6e295c1d017251c000000000000000000000000000000000000000000002f20e6e295cd56d17a1100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002f2a1b70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e054768fa0ff4b987f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5954557a5a6a55355a5330304d4449324c5455334d474574595445334e79316d4e544269597a41315a4449335a54496966513d3d000000000000000000000000000000000000000000000000000000000000002a000000000000000000000000105a18d55732fe5ed7c0a62036e624d4ba1c17b5000000000000000000000000000000000000000000000000125eef0692d22727000000000000000000000000000000000000000000000000125eeefb0f0a73e900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x10466f9c6d144cf7153f9e7d2c1c69bc5d986d029ff14d69f12d3065cb05592b",
      "signature": {
        "s": "0x4a90f7e990d4251a9bbc37f7ab2b129f33ea48c0ef0216befd4bcbe30169c4c8",
        "r": "0xde2144867219f36a458e45d7f78402f7fcd804e6d007c899fe1c7ac000884ef4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb56474dd84ac8cf0e60e1224e61dab896f3f9dc4bfd289e8a9314a5fde746b1d",
      "signature": {
        "s": "0x0d9d1737e33e4965435c72cca05e9266cf5511fbf8976d68356f572bc7528cf2",
        "r": "0xb90b0b6c5f11006d8078448b918582111358ff177734c8b3356730c7a2501434",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "49455543102",
    "total": "1154212580758"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "49455543102",
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
            "amount": "27749989296727244118143"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "49455543"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjYTUzZjU5ZS00MDI2LTU3MGEtYTE3Ny1mNTBiYzA1ZDI3ZTIifQ==",
    "nonce": 112425,
    "balances": {
      "current": "222558157529865143133468",
      "previous": "222558157529914648132113"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x105a18d55732fe5ed7c0a62036e624d4ba1c17b5",
    "nonce": 42,
    "balances": {
      "current": "1323758152005592871",
      "previous": "1323758102550049769"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:43.856Z",
  "updated": "2022-05-04T09:03:43.943Z",
  "id": "6272416f3592fd001130b787"
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
0x0f200f9b000000000000000000000000000000000000000000000000125eef0692d227270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `1323758152005592871`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`