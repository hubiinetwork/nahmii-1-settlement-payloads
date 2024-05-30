# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8E2f57403d6616d8f772f1C3927Ea7813765d3ee`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000061750000000000000000000000000000000000000000000000000000000000006175000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000061750000000000000000000000000000000000000000000000000000000000006175039a49c101ff8b8e416c04c68a4c378b0b4b242e7677ca3052edc3af287a92b68a6bdcb2592c6bfcd5b7d9572e03397ee2e5a22ac3f0046b74a98cb2069cf8158598db3cd22ebd74557a00016abd6d083d56a7ea1dde57252d3cb9387dd9782bf000000000000000000000000000000000000000000000000000000000000001ba6975869f032525bb25cae0450d999a5665d7968ba178f6954e0228f398a3f855d37059037b004218f49dd662001de8c31e20ca87ce776250bfbb9ba9ae2544f3862956b63c582c61df019231ef3d8788402a7abbd67f0a3ad59a94a836eb048000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000048e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c80c9445000000000000000000000000000000000000000000000000002386f2c812ad2400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000018f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000930c900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d54686c4d5459774e43316a4d6a5a684c5455354e7a4d744f44686a4e43316c595451784d4755344d6d5935596d496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000008e2f57403d6616d8f772f1c3927ea7813765d3ee0000000000000000000000000000000000000000000000000000000000061750000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x39a49c101ff8b8e416c04c68a4c378b0b4b242e7677ca3052edc3af287a92b68",
      "signature": {
        "s": "0x598db3cd22ebd74557a00016abd6d083d56a7ea1dde57252d3cb9387dd9782bf",
        "r": "0xa6bdcb2592c6bfcd5b7d9572e03397ee2e5a22ac3f0046b74a98cb2069cf8158",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa6975869f032525bb25cae0450d999a5665d7968ba178f6954e0228f398a3f85",
      "signature": {
        "s": "0x3862956b63c582c61df019231ef3d8788402a7abbd67f0a3ad59a94a836eb048",
        "r": "0x5d37059037b004218f49dd662001de8c31e20ca87ce776250bfbb9ba9ae2544f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "399184",
    "total": "399184"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "399184",
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
            "amount": "602313"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "399"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMThlMTYwNC1jMjZhLTU5NzMtODhjNC1lYTQxMGU4MmY5YmIifQ==",
    "nonce": 1166,
    "balances": {
      "current": "10000001481348165",
      "previous": "10000001481747748"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8e2f57403d6616d8f772f1c3927ea7813765d3ee",
    "nonce": 20,
    "balances": {
      "current": "399184",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:14.702Z",
  "updated": "2020-05-22T08:07:14.771Z",
  "id": "5ec78832005df800101bc3a6"
}
```
* *stageAmount*: `399184`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000006175000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000061750000000000000000000000000000000000000000000000000000000000006175039a49c101ff8b8e416c04c68a4c378b0b4b242e7677ca3052edc3af287a92b68a6bdcb2592c6bfcd5b7d9572e03397ee2e5a22ac3f0046b74a98cb2069cf8158598db3cd22ebd74557a00016abd6d083d56a7ea1dde57252d3cb9387dd9782bf000000000000000000000000000000000000000000000000000000000000001ba6975869f032525bb25cae0450d999a5665d7968ba178f6954e0228f398a3f855d37059037b004218f49dd662001de8c31e20ca87ce776250bfbb9ba9ae2544f3862956b63c582c61df019231ef3d8788402a7abbd67f0a3ad59a94a836eb048000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000048e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c80c9445000000000000000000000000000000000000000000000000002386f2c812ad2400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000018f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000930c900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d54686c4d5459774e43316a4d6a5a684c5455354e7a4d744f44686a4e43316c595451784d4755344d6d5935596d496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000008e2f57403d6616d8f772f1c3927ea7813765d3ee0000000000000000000000000000000000000000000000000000000000061750000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x39a49c101ff8b8e416c04c68a4c378b0b4b242e7677ca3052edc3af287a92b68",
      "signature": {
        "s": "0x598db3cd22ebd74557a00016abd6d083d56a7ea1dde57252d3cb9387dd9782bf",
        "r": "0xa6bdcb2592c6bfcd5b7d9572e03397ee2e5a22ac3f0046b74a98cb2069cf8158",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa6975869f032525bb25cae0450d999a5665d7968ba178f6954e0228f398a3f85",
      "signature": {
        "s": "0x3862956b63c582c61df019231ef3d8788402a7abbd67f0a3ad59a94a836eb048",
        "r": "0x5d37059037b004218f49dd662001de8c31e20ca87ce776250bfbb9ba9ae2544f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "399184",
    "total": "399184"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "399184",
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
            "amount": "602313"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "399"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMThlMTYwNC1jMjZhLTU5NzMtODhjNC1lYTQxMGU4MmY5YmIifQ==",
    "nonce": 1166,
    "balances": {
      "current": "10000001481348165",
      "previous": "10000001481747748"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8e2f57403d6616d8f772f1c3927ea7813765d3ee",
    "nonce": 20,
    "balances": {
      "current": "399184",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:14.702Z",
  "updated": "2020-05-22T08:07:14.771Z",
  "id": "5ec78832005df800101bc3a6"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000617500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `399184`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``