# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4E141C3F4333b9DC3E1a698929dD875ad54CcC68`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000261770d233f2d8e7b9000000000000000000000000000000000000000000000000e73214f2cf9ee37e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf9ee37e0000000000000000000000000000000000000000000000195793009724189cc40f445e945fe7d2061e15f41b295bd9c51c62a804d757c6cc3e76fa066d3b4e4df327cd6f595cdb27efcbd04bd66ebacd259e50ffe0b3be917caa7f2a4a42a863528ab9796604b44c973b0724bba87b03b22ca6f9c760dd3bc83fd00b510d1b3f000000000000000000000000000000000000000000000000000000000000001cc6538fe473c0affba6277215b62d7fd3b0ea9e65677152f563b50032c6e80658204fb8a692d2d35e8074a4d41be539a5255c6aa355bbb8ae8051813519addcc66f211d72addda4b107004415286b96eb285d9a0f2f1a1b7cfe7af68d4a2a0cc9000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adbf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000965f90530acf4631480a00000000000000000000000000000000000000000000966077c04f6524de68af00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3d270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ecf9224f254884f80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a5441324d54646a4e693079596a4e6c4c5455354e5755744f445a6a4d6930314e32597a596a426d4e7a417a4f44416966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004e141c3f4333b9dc3e1a698929dd875ad54ccc680000000000000000000000000000000000000000000000261770d233f2d8e7b9000000000000000000000000000000000000000000000025303ebd41233a043b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f445e945fe7d2061e15f41b295bd9c51c62a804d757c6cc3e76fa066d3b4e4d",
      "signature": {
        "s": "0x528ab9796604b44c973b0724bba87b03b22ca6f9c760dd3bc83fd00b510d1b3f",
        "r": "0xf327cd6f595cdb27efcbd04bd66ebacd259e50ffe0b3be917caa7f2a4a42a863",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc6538fe473c0affba6277215b62d7fd3b0ea9e65677152f563b50032c6e80658",
      "signature": {
        "s": "0x6f211d72addda4b107004415286b96eb285d9a0f2f1a1b7cfe7af68d4a2a0cc9",
        "r": "0x204fb8a692d2d35e8074a4d41be539a5255c6aa355bbb8ae8051813519addcc6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16659401004694823806",
    "total": "467478989994760641732"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694823806",
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
            "amount": "27262916714054482953464"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694823"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxZTA2MTdjNi0yYjNlLTU5NWUtODZjMi01N2YzYjBmNzAzODAifQ==",
    "nonce": 110015,
    "balances": {
      "current": "710117812785299070208010",
      "previous": "710134488845704769726639"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4e141c3f4333b9dc3e1a698929dd875ad54ccc68",
    "nonce": 46,
    "balances": {
      "current": "702665355781786363833",
      "previous": "686005954777091540027"
    }
  },
  "blockNumber": "14709959",
  "created": "2022-05-04T08:51:07.612Z",
  "updated": "2022-05-04T08:51:07.685Z",
  "id": "62723e7bbbd75600116d04d7"
}
```
* *stageAmount*: `702665355781786363833`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000e73214f2cf9ee37e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf9ee37e0000000000000000000000000000000000000000000000195793009724189cc40f445e945fe7d2061e15f41b295bd9c51c62a804d757c6cc3e76fa066d3b4e4df327cd6f595cdb27efcbd04bd66ebacd259e50ffe0b3be917caa7f2a4a42a863528ab9796604b44c973b0724bba87b03b22ca6f9c760dd3bc83fd00b510d1b3f000000000000000000000000000000000000000000000000000000000000001cc6538fe473c0affba6277215b62d7fd3b0ea9e65677152f563b50032c6e80658204fb8a692d2d35e8074a4d41be539a5255c6aa355bbb8ae8051813519addcc66f211d72addda4b107004415286b96eb285d9a0f2f1a1b7cfe7af68d4a2a0cc9000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adbf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000965f90530acf4631480a00000000000000000000000000000000000000000000966077c04f6524de68af00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3d270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ecf9224f254884f80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a5441324d54646a4e693079596a4e6c4c5455354e5755744f445a6a4d6930314e32597a596a426d4e7a417a4f44416966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004e141c3f4333b9dc3e1a698929dd875ad54ccc680000000000000000000000000000000000000000000000261770d233f2d8e7b9000000000000000000000000000000000000000000000025303ebd41233a043b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f445e945fe7d2061e15f41b295bd9c51c62a804d757c6cc3e76fa066d3b4e4d",
      "signature": {
        "s": "0x528ab9796604b44c973b0724bba87b03b22ca6f9c760dd3bc83fd00b510d1b3f",
        "r": "0xf327cd6f595cdb27efcbd04bd66ebacd259e50ffe0b3be917caa7f2a4a42a863",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc6538fe473c0affba6277215b62d7fd3b0ea9e65677152f563b50032c6e80658",
      "signature": {
        "s": "0x6f211d72addda4b107004415286b96eb285d9a0f2f1a1b7cfe7af68d4a2a0cc9",
        "r": "0x204fb8a692d2d35e8074a4d41be539a5255c6aa355bbb8ae8051813519addcc6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16659401004694823806",
    "total": "467478989994760641732"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694823806",
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
            "amount": "27262916714054482953464"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694823"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxZTA2MTdjNi0yYjNlLTU5NWUtODZjMi01N2YzYjBmNzAzODAifQ==",
    "nonce": 110015,
    "balances": {
      "current": "710117812785299070208010",
      "previous": "710134488845704769726639"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4e141c3f4333b9dc3e1a698929dd875ad54ccc68",
    "nonce": 46,
    "balances": {
      "current": "702665355781786363833",
      "previous": "686005954777091540027"
    }
  },
  "blockNumber": "14709959",
  "created": "2022-05-04T08:51:07.612Z",
  "updated": "2022-05-04T08:51:07.685Z",
  "id": "62723e7bbbd75600116d04d7"
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
0x0f200f9b0000000000000000000000000000000000000000000000261770d233f2d8e7b90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `702665355781786363833`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`