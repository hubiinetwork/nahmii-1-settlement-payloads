# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x118a4B5C5977e67A722652A08c76a85564A14992`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000479300000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000479300000000000000000000000000000000000000000000000000000000000047930ee683057e20e641934c23ecea6c61ef9ab00158ebe6bdeffc64ef9626332fc7a297e3e587452c06275d8e512964688cd80d3889a5138c49db0bfd8ee7aa8df653c319f0ce62fa66f14cdd72605af149a41d09eac0c199fb45b46d42695dadd0000000000000000000000000000000000000000000000000000000000000001c60175fb3f1f5c2552571a2c90ecb1af6f3c7b558c2e5796b184f1fd57360573fabe98548efe194fb9b54450e9740b4bd53bacca58bf6fde46b27c30bfd8730d059edc6c7045d3ceac297896c1b6673212d7507868d3fea20a518a1660e5b6209000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000078100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3eb2db9000000000000000000000000000000000000000000000000002386f2c3eb755e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a3e4100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a544e694e3249325a5330794e575a6d4c54566c4f4745744f544a6c5a6930305a474935595451335a544e6b5a44496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000118a4b5c5977e67a722652a08c76a85564a149920000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0ee683057e20e641934c23ecea6c61ef9ab00158ebe6bdeffc64ef9626332fc7",
      "signature": {
        "s": "0x53c319f0ce62fa66f14cdd72605af149a41d09eac0c199fb45b46d42695dadd0",
        "r": "0xa297e3e587452c06275d8e512964688cd80d3889a5138c49db0bfd8ee7aa8df6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x60175fb3f1f5c2552571a2c90ecb1af6f3c7b558c2e5796b184f1fd57360573f",
      "signature": {
        "s": "0x59edc6c7045d3ceac297896c1b6673212d7507868d3fea20a518a1660e5b6209",
        "r": "0xabe98548efe194fb9b54450e9740b4bd53bacca58bf6fde46b27c30bfd8730d0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "671297"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTNiN2I2ZS0yNWZmLTVlOGEtOTJlZi00ZGI5YTQ3ZTNkZDIifQ==",
    "nonce": 1921,
    "balances": {
      "current": "10000001412050361",
      "previous": "10000001412068702"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x118a4b5c5977e67a722652a08c76a85564a14992",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114542",
  "created": "2020-05-22T08:13:06.339Z",
  "updated": "2020-05-22T08:13:06.404Z",
  "id": "5ec78992b0c6090011d5ab4f"
}
```
* *stageAmount*: `18323`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000479300000000000000000000000000000000000000000000000000000000000047930ee683057e20e641934c23ecea6c61ef9ab00158ebe6bdeffc64ef9626332fc7a297e3e587452c06275d8e512964688cd80d3889a5138c49db0bfd8ee7aa8df653c319f0ce62fa66f14cdd72605af149a41d09eac0c199fb45b46d42695dadd0000000000000000000000000000000000000000000000000000000000000001c60175fb3f1f5c2552571a2c90ecb1af6f3c7b558c2e5796b184f1fd57360573fabe98548efe194fb9b54450e9740b4bd53bacca58bf6fde46b27c30bfd8730d059edc6c7045d3ceac297896c1b6673212d7507868d3fea20a518a1660e5b6209000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000078100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3eb2db9000000000000000000000000000000000000000000000000002386f2c3eb755e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a3e4100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a544e694e3249325a5330794e575a6d4c54566c4f4745744f544a6c5a6930305a474935595451335a544e6b5a44496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000118a4b5c5977e67a722652a08c76a85564a149920000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0ee683057e20e641934c23ecea6c61ef9ab00158ebe6bdeffc64ef9626332fc7",
      "signature": {
        "s": "0x53c319f0ce62fa66f14cdd72605af149a41d09eac0c199fb45b46d42695dadd0",
        "r": "0xa297e3e587452c06275d8e512964688cd80d3889a5138c49db0bfd8ee7aa8df6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x60175fb3f1f5c2552571a2c90ecb1af6f3c7b558c2e5796b184f1fd57360573f",
      "signature": {
        "s": "0x59edc6c7045d3ceac297896c1b6673212d7507868d3fea20a518a1660e5b6209",
        "r": "0xabe98548efe194fb9b54450e9740b4bd53bacca58bf6fde46b27c30bfd8730d0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "671297"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTNiN2I2ZS0yNWZmLTVlOGEtOTJlZi00ZGI5YTQ3ZTNkZDIifQ==",
    "nonce": 1921,
    "balances": {
      "current": "10000001412050361",
      "previous": "10000001412068702"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x118a4b5c5977e67a722652a08c76a85564a14992",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114542",
  "created": "2020-05-22T08:13:06.339Z",
  "updated": "2020-05-22T08:13:06.404Z",
  "id": "5ec78992b0c6090011d5ab4f"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18323`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``