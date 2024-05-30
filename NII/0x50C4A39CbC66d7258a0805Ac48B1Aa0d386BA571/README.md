# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x50C4A39CbC66d7258a0805Ac48B1Aa0d386BA571`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000261770d24117dcdabc000000000000000000000000000000000000000000000000e73214f2cf9ef7040000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf9ef70400000000000000000000000000000000000000000000001957930097241c1683b28318cfcd8c1a67300c887f5c507c9dce9572f1422e032b2acb11bf9803850aacb1b14298061a7f41f17a3f1229de3a3109406ff9bdaf33878d01645ad9a1f861a0535e91ecc908ba8d0891c14af16f3a11fa96b89a3b0b8d1d01c27925d3a3000000000000000000000000000000000000000000000000000000000000001b5367e2a8b4190e328730b6f1380b66c1c4c5abfb141e984baa6c04adc5db0f0404b88b1780a134c396a464edd2b0148463cf2c01afc0a04af8ee8eb1ea8bbdf7615125e5c21ca4f04213b83821bae336c8823bc5964e8b4a30068197c2a11f64000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adb7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096632e081d3b4baabc13000000000000000000000000000000000000000000009664157561d12a57f04300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3d2c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ec0c63c2e3cea9f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a54497a5a574e6a4e6930794e3249784c5456694e575574595751304e4330774f575132595456694e7a466c596a676966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000050c4a39cbc66d7258a0805ac48b1aa0d386ba5710000000000000000000000000000000000000000000000261770d24117dcdabc000000000000000000000000000000000000000000000025303ebd4e483de3b800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb28318cfcd8c1a67300c887f5c507c9dce9572f1422e032b2acb11bf9803850a",
      "signature": {
        "s": "0x61a0535e91ecc908ba8d0891c14af16f3a11fa96b89a3b0b8d1d01c27925d3a3",
        "r": "0xacb1b14298061a7f41f17a3f1229de3a3109406ff9bdaf33878d01645ad9a1f8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5367e2a8b4190e328730b6f1380b66c1c4c5abfb141e984baa6c04adc5db0f04",
      "signature": {
        "s": "0x615125e5c21ca4f04213b83821bae336c8823bc5964e8b4a30068197c2a11f64",
        "r": "0x04b88b1780a134c396a464edd2b0148463cf2c01afc0a04af8ee8eb1ea8bbdf7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16659401004694828804",
    "total": "467478989994760869507"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694828804",
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
            "amount": "27262850076450376034803"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694828"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZTIzZWNjNi0yN2IxLTViNWUtYWQ0NC0wOWQ2YTViNzFlYjgifQ==",
    "nonce": 110007,
    "balances": {
      "current": "710184517027010095791123",
      "previous": "710201193087415795314755"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x50c4a39cbc66d7258a0805ac48b1aa0d386ba571",
    "nonce": 46,
    "balances": {
      "current": "702665355838241954492",
      "previous": "686005954833547125688"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:51:04.230Z",
  "updated": "2022-05-04T08:51:04.328Z",
  "id": "62723e787832e20011830b2a"
}
```
* *stageAmount*: `702665355838241954492`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000e73214f2cf9ef7040000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf9ef70400000000000000000000000000000000000000000000001957930097241c1683b28318cfcd8c1a67300c887f5c507c9dce9572f1422e032b2acb11bf9803850aacb1b14298061a7f41f17a3f1229de3a3109406ff9bdaf33878d01645ad9a1f861a0535e91ecc908ba8d0891c14af16f3a11fa96b89a3b0b8d1d01c27925d3a3000000000000000000000000000000000000000000000000000000000000001b5367e2a8b4190e328730b6f1380b66c1c4c5abfb141e984baa6c04adc5db0f0404b88b1780a134c396a464edd2b0148463cf2c01afc0a04af8ee8eb1ea8bbdf7615125e5c21ca4f04213b83821bae336c8823bc5964e8b4a30068197c2a11f64000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adb7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096632e081d3b4baabc13000000000000000000000000000000000000000000009664157561d12a57f04300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3d2c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ec0c63c2e3cea9f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a54497a5a574e6a4e6930794e3249784c5456694e575574595751304e4330774f575132595456694e7a466c596a676966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000050c4a39cbc66d7258a0805ac48b1aa0d386ba5710000000000000000000000000000000000000000000000261770d24117dcdabc000000000000000000000000000000000000000000000025303ebd4e483de3b800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb28318cfcd8c1a67300c887f5c507c9dce9572f1422e032b2acb11bf9803850a",
      "signature": {
        "s": "0x61a0535e91ecc908ba8d0891c14af16f3a11fa96b89a3b0b8d1d01c27925d3a3",
        "r": "0xacb1b14298061a7f41f17a3f1229de3a3109406ff9bdaf33878d01645ad9a1f8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5367e2a8b4190e328730b6f1380b66c1c4c5abfb141e984baa6c04adc5db0f04",
      "signature": {
        "s": "0x615125e5c21ca4f04213b83821bae336c8823bc5964e8b4a30068197c2a11f64",
        "r": "0x04b88b1780a134c396a464edd2b0148463cf2c01afc0a04af8ee8eb1ea8bbdf7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16659401004694828804",
    "total": "467478989994760869507"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694828804",
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
            "amount": "27262850076450376034803"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694828"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZTIzZWNjNi0yN2IxLTViNWUtYWQ0NC0wOWQ2YTViNzFlYjgifQ==",
    "nonce": 110007,
    "balances": {
      "current": "710184517027010095791123",
      "previous": "710201193087415795314755"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x50c4a39cbc66d7258a0805ac48b1aa0d386ba571",
    "nonce": 46,
    "balances": {
      "current": "702665355838241954492",
      "previous": "686005954833547125688"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:51:04.230Z",
  "updated": "2022-05-04T08:51:04.328Z",
  "id": "62723e787832e20011830b2a"
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
0x0f200f9b0000000000000000000000000000000000000000000000261770d24117dcdabc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `702665355838241954492`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`