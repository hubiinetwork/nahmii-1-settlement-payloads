# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0xfC7fc1DEB936D18aa5E771288C7C1aa773A4EFB2`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000936229fff80c7eff0000000000000000000000000000000000000000000000000000000ac905e9a60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000ac905e9a600000000000000000000000000000000000000000000001ed72c6bb9370807964e7482531550314c1667480bf0d7c394069c0554d894cdd7f06080b8a2d74d0e9af26a08346a195a50bb10c39176038abdf69f03975d391f7e7694f5f962d181358a1621fcddd1396201cf0ac12116c431e938ba8dfa0ac7c5820981be1bdf60000000000000000000000000000000000000000000000000000000000000001c6e422b44a1dc2fc09dd301fe4857d2e7782e452a7b836337782abeccb1bf6e3fd0ab20b54b64902a527f2c936a788737638f9cf3eca4fa726c77ccbafe73f4275eaafd393fc698884d852e7f9c36d55f7d3024539e9838450789e0c2d5e47253000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b34c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003d091a4d71c0e4b2635a000000000000000000000000000000000000000000003d091a4d71cbb07b1f6800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002c2d2680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dcc5f65390a16aa61f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a68685a6a55304e79316d4d3259334c545531596a67744f574d7a4f53316a596a67344d6a56694e7a5a684d32516966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000fc7fc1deb936d18aa5e771288c7c1aa773a4efb2000000000000000000000000000000000000000000000000936229fff80c7eff000000000000000000000000000000000000000000000000936229f52f06955900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x4e7482531550314c1667480bf0d7c394069c0554d894cdd7f06080b8a2d74d0e",
      "signature": {
        "s": "0x358a1621fcddd1396201cf0ac12116c431e938ba8dfa0ac7c5820981be1bdf60",
        "r": "0x9af26a08346a195a50bb10c39176038abdf69f03975d391f7e7694f5f962d181",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6e422b44a1dc2fc09dd301fe4857d2e7782e452a7b836337782abeccb1bf6e3f",
      "signature": {
        "s": "0x5eaafd393fc698884d852e7f9c36d55f7d3024539e9838450789e0c2d5e47253",
        "r": "0xd0ab20b54b64902a527f2c936a788737638f9cf3eca4fa726c77ccbafe73f427",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "46322280870",
    "total": "568907208271652718486"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "46322280870",
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
            "amount": "27684380791314718565919"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "46322280"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YjhhZjU0Ny1mM2Y3LTU1YjgtOWMzOS1jYjg4MjViNzZhM2QifQ==",
    "nonce": 111436,
    "balances": {
      "current": "288232271447803221402458",
      "previous": "288232271447849590005608"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfc7fc1deb936d18aa5e771288c7c1aa773a4efb2",
    "nonce": 45,
    "balances": {
      "current": "10620097050648018687",
      "previous": "10620097004325737817"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:17.891Z",
  "updated": "2022-05-04T08:58:17.956Z",
  "id": "62724029bbd75600116d06a9"
}
```
* *stageAmount*: `10620097050648018687`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000ac905e9a60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000ac905e9a600000000000000000000000000000000000000000000001ed72c6bb9370807964e7482531550314c1667480bf0d7c394069c0554d894cdd7f06080b8a2d74d0e9af26a08346a195a50bb10c39176038abdf69f03975d391f7e7694f5f962d181358a1621fcddd1396201cf0ac12116c431e938ba8dfa0ac7c5820981be1bdf60000000000000000000000000000000000000000000000000000000000000001c6e422b44a1dc2fc09dd301fe4857d2e7782e452a7b836337782abeccb1bf6e3fd0ab20b54b64902a527f2c936a788737638f9cf3eca4fa726c77ccbafe73f4275eaafd393fc698884d852e7f9c36d55f7d3024539e9838450789e0c2d5e47253000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b34c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003d091a4d71c0e4b2635a000000000000000000000000000000000000000000003d091a4d71cbb07b1f6800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002c2d2680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dcc5f65390a16aa61f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a68685a6a55304e79316d4d3259334c545531596a67744f574d7a4f53316a596a67344d6a56694e7a5a684d32516966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000fc7fc1deb936d18aa5e771288c7c1aa773a4efb2000000000000000000000000000000000000000000000000936229fff80c7eff000000000000000000000000000000000000000000000000936229f52f06955900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x4e7482531550314c1667480bf0d7c394069c0554d894cdd7f06080b8a2d74d0e",
      "signature": {
        "s": "0x358a1621fcddd1396201cf0ac12116c431e938ba8dfa0ac7c5820981be1bdf60",
        "r": "0x9af26a08346a195a50bb10c39176038abdf69f03975d391f7e7694f5f962d181",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6e422b44a1dc2fc09dd301fe4857d2e7782e452a7b836337782abeccb1bf6e3f",
      "signature": {
        "s": "0x5eaafd393fc698884d852e7f9c36d55f7d3024539e9838450789e0c2d5e47253",
        "r": "0xd0ab20b54b64902a527f2c936a788737638f9cf3eca4fa726c77ccbafe73f427",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "46322280870",
    "total": "568907208271652718486"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "46322280870",
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
            "amount": "27684380791314718565919"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "46322280"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YjhhZjU0Ny1mM2Y3LTU1YjgtOWMzOS1jYjg4MjViNzZhM2QifQ==",
    "nonce": 111436,
    "balances": {
      "current": "288232271447803221402458",
      "previous": "288232271447849590005608"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfc7fc1deb936d18aa5e771288c7c1aa773a4efb2",
    "nonce": 45,
    "balances": {
      "current": "10620097050648018687",
      "previous": "10620097004325737817"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:17.891Z",
  "updated": "2022-05-04T08:58:17.956Z",
  "id": "62724029bbd75600116d06a9"
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
0x0f200f9b000000000000000000000000000000000000000000000000936229fff80c7eff0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `10620097050648018687`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`