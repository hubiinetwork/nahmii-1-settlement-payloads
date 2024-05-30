# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5C868bfa7DDa94E95a06780B163579EB712Bf37c`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000745000b66cde5fb000000000000000000000000000000000000000000000000002c1f491d42f0b20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000002c1f491d42f0b200000000000000000000000000000000000000000000000004d61cb242a37fbb11426db28b4308edf3788d4b07cc54a03e05606aea70d82212620973b82055da9e28e23717de7c6349e7cc5cd24cc7f4ae1a7555d7704103948bedfd8794d6ff03579c4b7304c5ad9956fcdd9434b1bd63040247ef254c3c0845ed7c98312aa2000000000000000000000000000000000000000000000000000000000000001b4c99377041da2acbcd2b480dc35fe09e090ad1099b8b903b06f083f8528724ef584263df413b23f0d7c014eb4161a4562291a1bb106f56a947509a602e139b5c56afb9168680960f69a966ea5f6d936e409dc4ab9e860a7eaf1d432cdd5823f7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abae000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009cd40b757b04164a1233000000000000000000000000000000000000000000009cd40ba1a598cb6359a900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000b4b97d656c40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4465c541133e8983c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6d59794f5467324f4330354d57466d4c5456684d3255744f4451794e69316d4f57566c4d3245314d4749344d57516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005c868bfa7dda94e95a06780b163579eb712bf37c0000000000000000000000000000000000000000000000000745000b66cde5fb0000000000000000000000000000000000000000000000000718e0c2498af54900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x11426db28b4308edf3788d4b07cc54a03e05606aea70d82212620973b82055da",
      "signature": {
        "s": "0x03579c4b7304c5ad9956fcdd9434b1bd63040247ef254c3c0845ed7c98312aa2",
        "r": "0x9e28e23717de7c6349e7cc5cd24cc7f4ae1a7555d7704103948bedfd8794d6ff",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4c99377041da2acbcd2b480dc35fe09e090ad1099b8b903b06f083f8528724ef",
      "signature": {
        "s": "0x56afb9168680960f69a966ea5f6d936e409dc4ab9e860a7eaf1d432cdd5823f7",
        "r": "0x584263df413b23f0d7c014eb4161a4562291a1bb106f56a947509a602e139b5c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "12419297859268786",
    "total": "348497573115559867"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12419297859268786",
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
            "amount": "27232464272508672579644"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12419297859268"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZmYyOTg2OC05MWFmLTVhM2UtODQyNi1mOWVlM2E1MGI4MWQifQ==",
    "nonce": 109486,
    "balances": {
      "current": "740600706772655254671923",
      "previous": "740600719204372411799977"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c868bfa7dda94e95a06780b163579eb712bf37c",
    "nonce": 46,
    "balances": {
      "current": "523824980627940859",
      "previous": "511405682768672073"
    }
  },
  "blockNumber": "14709941",
  "created": "2022-05-04T08:48:21.647Z",
  "updated": "2022-05-04T08:48:21.764Z",
  "id": "62723dd53592fd001130b3a7"
}
```
* *stageAmount*: `523824980627940859`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000002c1f491d42f0b20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000002c1f491d42f0b200000000000000000000000000000000000000000000000004d61cb242a37fbb11426db28b4308edf3788d4b07cc54a03e05606aea70d82212620973b82055da9e28e23717de7c6349e7cc5cd24cc7f4ae1a7555d7704103948bedfd8794d6ff03579c4b7304c5ad9956fcdd9434b1bd63040247ef254c3c0845ed7c98312aa2000000000000000000000000000000000000000000000000000000000000001b4c99377041da2acbcd2b480dc35fe09e090ad1099b8b903b06f083f8528724ef584263df413b23f0d7c014eb4161a4562291a1bb106f56a947509a602e139b5c56afb9168680960f69a966ea5f6d936e409dc4ab9e860a7eaf1d432cdd5823f7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abae000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009cd40b757b04164a1233000000000000000000000000000000000000000000009cd40ba1a598cb6359a900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000b4b97d656c40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4465c541133e8983c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6d59794f5467324f4330354d57466d4c5456684d3255744f4451794e69316d4f57566c4d3245314d4749344d57516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005c868bfa7dda94e95a06780b163579eb712bf37c0000000000000000000000000000000000000000000000000745000b66cde5fb0000000000000000000000000000000000000000000000000718e0c2498af54900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x11426db28b4308edf3788d4b07cc54a03e05606aea70d82212620973b82055da",
      "signature": {
        "s": "0x03579c4b7304c5ad9956fcdd9434b1bd63040247ef254c3c0845ed7c98312aa2",
        "r": "0x9e28e23717de7c6349e7cc5cd24cc7f4ae1a7555d7704103948bedfd8794d6ff",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4c99377041da2acbcd2b480dc35fe09e090ad1099b8b903b06f083f8528724ef",
      "signature": {
        "s": "0x56afb9168680960f69a966ea5f6d936e409dc4ab9e860a7eaf1d432cdd5823f7",
        "r": "0x584263df413b23f0d7c014eb4161a4562291a1bb106f56a947509a602e139b5c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "12419297859268786",
    "total": "348497573115559867"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12419297859268786",
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
            "amount": "27232464272508672579644"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12419297859268"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZmYyOTg2OC05MWFmLTVhM2UtODQyNi1mOWVlM2E1MGI4MWQifQ==",
    "nonce": 109486,
    "balances": {
      "current": "740600706772655254671923",
      "previous": "740600719204372411799977"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c868bfa7dda94e95a06780b163579eb712bf37c",
    "nonce": 46,
    "balances": {
      "current": "523824980627940859",
      "previous": "511405682768672073"
    }
  },
  "blockNumber": "14709941",
  "created": "2022-05-04T08:48:21.647Z",
  "updated": "2022-05-04T08:48:21.764Z",
  "id": "62723dd53592fd001130b3a7"
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
0x0f200f9b0000000000000000000000000000000000000000000000000745000b66cde5fb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `523824980627940859`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`