# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1FE7915ceaFe123A283ed1A8d23424c0246138cA`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001d05ab4d650488fc70000000000000000000000000000000000000000000000000b026285779a17490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b026285779a174900000000000000000000000000000000000000000000000134ee9e811a205849e736cc52c3a6b8afb87f7f4dc8a295533a1bf34ea0b2f58158cb2efb107f90798f14a712acc087ba5e52404f1ba84c888d41ea2a942abe50688c43212bc162315fc1ab03d0e4d032542e47b6d0befac96eaae3adcb823ce4d190e13d7ae70120000000000000000000000000000000000000000000000000000000000000001c2ab84dbb2b214a30e7ee85248f436cc520292c77adbc257b6b0ecf50296749acef23d3ddee61f844ca4ac7215c99b9ed94fdf5cb4142c5d03029db7be318ad2434aa85e1b284c66955a6cbd9e34476dc1471d2f8d8058c5da678824f397cfb4e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac2f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a9473f382b7470d8bc3000000000000000000000000000000000000000000009a947ef8b6be6a09d6c800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002d181ab6233bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d990a14b555cc3110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d6a41774f546b304e6930305932497a4c5455315a5445744f4456685a43316c4e7a41795a6a67314e444134596a636966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001fe7915ceafe123a283ed1a8d23424c0246138ca000000000000000000000000000000000000000000000001d05ab4d650488fc7000000000000000000000000000000000000000000000001c5585250d8ae787e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe736cc52c3a6b8afb87f7f4dc8a295533a1bf34ea0b2f58158cb2efb107f9079",
      "signature": {
        "s": "0x5fc1ab03d0e4d032542e47b6d0befac96eaae3adcb823ce4d190e13d7ae70120",
        "r": "0x8f14a712acc087ba5e52404f1ba84c888d41ea2a942abe50688c43212bc16231",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2ab84dbb2b214a30e7ee85248f436cc520292c77adbc257b6b0ecf50296749ac",
      "signature": {
        "s": "0x34aa85e1b284c66955a6cbd9e34476dc1471d2f8d8058c5da678824f397cfb4e",
        "r": "0xef23d3ddee61f844ca4ac7215c99b9ed94fdf5cb4142c5d03029db7be318ad24",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "793304809747388233",
    "total": "22260904285465237577"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "793304809747388233",
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
            "amount": "27243071460443101643537"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "793304809747388"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMjAwOTk0Ni00Y2IzLTU1ZTEtODVhZC1lNzAyZjg1NDA4YjcifQ==",
    "nonce": 109615,
    "balances": {
      "current": "729982911650291761646531",
      "previous": "729983705748406318782152"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1fe7915ceafe123a283ed1a8d23424c0246138ca",
    "nonce": 46,
    "balances": {
      "current": "33460255214065455047",
      "previous": "32666950404318066814"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:59.944Z",
  "updated": "2022-05-04T08:49:00.013Z",
  "id": "62723dfb7832e20011830aa7"
}
```
* *stageAmount*: `33460255214065455047`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000b026285779a17490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b026285779a174900000000000000000000000000000000000000000000000134ee9e811a205849e736cc52c3a6b8afb87f7f4dc8a295533a1bf34ea0b2f58158cb2efb107f90798f14a712acc087ba5e52404f1ba84c888d41ea2a942abe50688c43212bc162315fc1ab03d0e4d032542e47b6d0befac96eaae3adcb823ce4d190e13d7ae70120000000000000000000000000000000000000000000000000000000000000001c2ab84dbb2b214a30e7ee85248f436cc520292c77adbc257b6b0ecf50296749acef23d3ddee61f844ca4ac7215c99b9ed94fdf5cb4142c5d03029db7be318ad2434aa85e1b284c66955a6cbd9e34476dc1471d2f8d8058c5da678824f397cfb4e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac2f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a9473f382b7470d8bc3000000000000000000000000000000000000000000009a947ef8b6be6a09d6c800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002d181ab6233bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d990a14b555cc3110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d6a41774f546b304e6930305932497a4c5455315a5445744f4456685a43316c4e7a41795a6a67314e444134596a636966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001fe7915ceafe123a283ed1a8d23424c0246138ca000000000000000000000000000000000000000000000001d05ab4d650488fc7000000000000000000000000000000000000000000000001c5585250d8ae787e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe736cc52c3a6b8afb87f7f4dc8a295533a1bf34ea0b2f58158cb2efb107f9079",
      "signature": {
        "s": "0x5fc1ab03d0e4d032542e47b6d0befac96eaae3adcb823ce4d190e13d7ae70120",
        "r": "0x8f14a712acc087ba5e52404f1ba84c888d41ea2a942abe50688c43212bc16231",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2ab84dbb2b214a30e7ee85248f436cc520292c77adbc257b6b0ecf50296749ac",
      "signature": {
        "s": "0x34aa85e1b284c66955a6cbd9e34476dc1471d2f8d8058c5da678824f397cfb4e",
        "r": "0xef23d3ddee61f844ca4ac7215c99b9ed94fdf5cb4142c5d03029db7be318ad24",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "793304809747388233",
    "total": "22260904285465237577"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "793304809747388233",
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
            "amount": "27243071460443101643537"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "793304809747388"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMjAwOTk0Ni00Y2IzLTU1ZTEtODVhZC1lNzAyZjg1NDA4YjcifQ==",
    "nonce": 109615,
    "balances": {
      "current": "729982911650291761646531",
      "previous": "729983705748406318782152"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1fe7915ceafe123a283ed1a8d23424c0246138ca",
    "nonce": 46,
    "balances": {
      "current": "33460255214065455047",
      "previous": "32666950404318066814"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:59.944Z",
  "updated": "2022-05-04T08:49:00.013Z",
  "id": "62723dfb7832e20011830aa7"
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
0x0f200f9b000000000000000000000000000000000000000000000001d05ab4d650488fc70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `33460255214065455047`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`