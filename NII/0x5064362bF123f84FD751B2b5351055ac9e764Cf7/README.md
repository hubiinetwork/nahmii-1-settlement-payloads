# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5064362bF123f84FD751B2b5351055ac9e764Cf7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000016ac6dd042d804c1b5d00000000000000000000000000000000000000000000000899dcf8456ffe2be80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000899dcf8456ffe2be80000000000000000000000000000000000000000000000f15a6bd4dc5e0193c53b6629a438f52522102da5c38749bd443297bf8fec3f81fd43f658e6973bcfc073a4610bc846e6cd0c61452d4bc1dc3d7129d7892321df303781388613d94c643b6c0c2c1838ce863011f35514eac9dd325d156f3e44507319dd9f023c5ed7dc000000000000000000000000000000000000000000000000000000000000001bde5981e4d22964001555d900a856703de6c3edddab1dd649a3d05729c73dcf3a79f73150d2d15cd3efa2f743a483f70539f665582a4d0967343539bf6f7d8a7a4daac6e1c383e696a23227d4d2ad0f0fbb58bc47d6fa9538ba26e42c168bf186000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af7b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000056048ba880696fe47ed400000000000000000000000000000000000000000000560d27b925fcc49afc2f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000233ad4de4b851730000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d6625d4ce6a5e187100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a6b354e7a4e69597930794e5445784c5456685a57557459574e6b5a6930334d544e6d4e5449324f5749305954456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005064362bf123f84fd751b2b5351055ac9e764cf700000000000000000000000000000000000000000000016ac6dd042d804c1b5d0000000000000000000000000000000000000000000001622d000be8104def7500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3b6629a438f52522102da5c38749bd443297bf8fec3f81fd43f658e6973bcfc0",
      "signature": {
        "s": "0x3b6c0c2c1838ce863011f35514eac9dd325d156f3e44507319dd9f023c5ed7dc",
        "r": "0x73a4610bc846e6cd0c61452d4bc1dc3d7129d7892321df303781388613d94c64",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xde5981e4d22964001555d900a856703de6c3edddab1dd649a3d05729c73dcf3a",
      "signature": {
        "s": "0x4daac6e1c383e696a23227d4d2ad0f0fbb58bc47d6fa9538ba26e42c168bf186",
        "r": "0x79f73150d2d15cd3efa2f743a483f70539f665582a4d0967343539bf6f7d8a7a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "158660961949471091688",
    "total": "4452180857092858549189"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949471091688",
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
            "amount": "27566523552064130352912"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949471091"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMzk5NzNiYy0yNTExLTVhZWUtYWNkZi03MTNmNTI2OWI0YTEifQ==",
    "nonce": 110459,
    "balances": {
      "current": "406207367937642023124692",
      "previous": "406366187560553443687471"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5064362bf123f84fd751b2b5351055ac9e764cf7",
    "nonce": 46,
    "balances": {
      "current": "6692050968865692982109",
      "previous": "6533390006916221890421"
    }
  },
  "blockNumber": "14709967",
  "created": "2022-05-04T08:53:23.396Z",
  "updated": "2022-05-04T08:53:23.611Z",
  "id": "62723f037832e20011830bbb"
}
```
* *stageAmount*: `6692050968865692982109`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000899dcf8456ffe2be80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000899dcf8456ffe2be80000000000000000000000000000000000000000000000f15a6bd4dc5e0193c53b6629a438f52522102da5c38749bd443297bf8fec3f81fd43f658e6973bcfc073a4610bc846e6cd0c61452d4bc1dc3d7129d7892321df303781388613d94c643b6c0c2c1838ce863011f35514eac9dd325d156f3e44507319dd9f023c5ed7dc000000000000000000000000000000000000000000000000000000000000001bde5981e4d22964001555d900a856703de6c3edddab1dd649a3d05729c73dcf3a79f73150d2d15cd3efa2f743a483f70539f665582a4d0967343539bf6f7d8a7a4daac6e1c383e696a23227d4d2ad0f0fbb58bc47d6fa9538ba26e42c168bf186000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af7b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000056048ba880696fe47ed400000000000000000000000000000000000000000000560d27b925fcc49afc2f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000233ad4de4b851730000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d6625d4ce6a5e187100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a6b354e7a4e69597930794e5445784c5456685a57557459574e6b5a6930334d544e6d4e5449324f5749305954456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005064362bf123f84fd751b2b5351055ac9e764cf700000000000000000000000000000000000000000000016ac6dd042d804c1b5d0000000000000000000000000000000000000000000001622d000be8104def7500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3b6629a438f52522102da5c38749bd443297bf8fec3f81fd43f658e6973bcfc0",
      "signature": {
        "s": "0x3b6c0c2c1838ce863011f35514eac9dd325d156f3e44507319dd9f023c5ed7dc",
        "r": "0x73a4610bc846e6cd0c61452d4bc1dc3d7129d7892321df303781388613d94c64",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xde5981e4d22964001555d900a856703de6c3edddab1dd649a3d05729c73dcf3a",
      "signature": {
        "s": "0x4daac6e1c383e696a23227d4d2ad0f0fbb58bc47d6fa9538ba26e42c168bf186",
        "r": "0x79f73150d2d15cd3efa2f743a483f70539f665582a4d0967343539bf6f7d8a7a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "158660961949471091688",
    "total": "4452180857092858549189"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949471091688",
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
            "amount": "27566523552064130352912"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949471091"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMzk5NzNiYy0yNTExLTVhZWUtYWNkZi03MTNmNTI2OWI0YTEifQ==",
    "nonce": 110459,
    "balances": {
      "current": "406207367937642023124692",
      "previous": "406366187560553443687471"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5064362bf123f84fd751b2b5351055ac9e764cf7",
    "nonce": 46,
    "balances": {
      "current": "6692050968865692982109",
      "previous": "6533390006916221890421"
    }
  },
  "blockNumber": "14709967",
  "created": "2022-05-04T08:53:23.396Z",
  "updated": "2022-05-04T08:53:23.611Z",
  "id": "62723f037832e20011830bbb"
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
0x0f200f9b00000000000000000000000000000000000000000000016ac6dd042d804c1b5d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6692050968865692982109`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`