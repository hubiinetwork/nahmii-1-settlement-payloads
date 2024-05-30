# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x53347f2A083c7d8B225266787947eA5d5b43E964`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de0b6b3a7642531000000000000000000000000000000000000000000000038cd09e81a332bb7500000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000038cd09e81a332bb750000000000000000000000000000000000000000000000038cd09e81a332bb75081ae06c7b0e5f994c7370a35cbe0eecc7db738ca8e3db926ec154d5f074a088468f8558cfa4ece8dd1e91ba1dbd9c26538fa9cc93c5c851b11cb948a382c9c420c27bd1ba55eb2083326708b393b1aff14e8c7fe5a2ec175d4b2287109ea24ba000000000000000000000000000000000000000000000000000000000000001cf6c36aacb863e8d6d5a9cb11c332623069c6ba6508d2629f60dd4f2187ade4e5c78e880a9cf0e4270672edd8bb6aeb75fa2eb44e5fe8b20b0ad86f06c81285fa4c791dac8bba654db5067ec32f4d34a7e0fc523cdc8cf2430557b0417960ed9b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e2de740000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000053347f2a083c7d8b225266787947ea5d5b43e9640000000000000000000000000000000000000000000000000de0b6b3a7642531000000000000000000000000000000000000000000000038e9752050f3b37d3300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000e8a81831923a0b20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000e8a81831923a0b20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e7a63314f4755354e7930354e4746684c5451784e5751744f4459784d79316c4f5749314d5464694f5759304f54596966513d3d00000000000000000000000000000000000000000000000000000000000000cd000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000a77d10229f8df892489f00000000000000000000000000000000000000000000a7444318b773c566914f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x81ae06c7b0e5f994c7370a35cbe0eecc7db738ca8e3db926ec154d5f074a0884",
      "signature": {
        "s": "0x0c27bd1ba55eb2083326708b393b1aff14e8c7fe5a2ec175d4b2287109ea24ba",
        "r": "0x68f8558cfa4ece8dd1e91ba1dbd9c26538fa9cc93c5c851b11cb948a382c9c42",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf6c36aacb863e8d6d5a9cb11c332623069c6ba6508d2629f60dd4f2187ade4e5",
      "signature": {
        "s": "0x4c791dac8bba654db5067ec32f4d34a7e0fc523cdc8cf2430557b0417960ed9b",
        "r": "0xc78e880a9cf0e4270672edd8bb6aeb75fa2eb44e5fe8b20b0ad86f06c81285fa",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1047792263379525810000",
    "total": "1047792263379525810000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1047792263379525810000",
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
            "amount": "1047792263379525810"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1047792263379525810"
      }
    },
    "wallet": "0x53347f2a083c7d8b225266787947ea5d5b43e964",
    "data": "eyJyZWYiOiIyNzc1OGU5Ny05NGFhLTQxNWQtODYxMy1lOWI1MTdiOWY0OTYifQ==",
    "nonce": 12,
    "balances": {
      "current": "1000000000000009521",
      "previous": "1049840055642905345331"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 205,
    "balances": {
      "current": "790942208315530369190047",
      "previous": "789894416052150843380047"
    }
  },
  "blockNumber": "14868084",
  "created": "2022-05-29T18:46:52.631Z",
  "updated": "2022-05-29T18:46:52.759Z",
  "id": "6293bf9c3592fd001130b8a6"
}
```
* *stageAmount*: `1000000000000009521`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000038cd09e81a332bb7500000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000038cd09e81a332bb750000000000000000000000000000000000000000000000038cd09e81a332bb75081ae06c7b0e5f994c7370a35cbe0eecc7db738ca8e3db926ec154d5f074a088468f8558cfa4ece8dd1e91ba1dbd9c26538fa9cc93c5c851b11cb948a382c9c420c27bd1ba55eb2083326708b393b1aff14e8c7fe5a2ec175d4b2287109ea24ba000000000000000000000000000000000000000000000000000000000000001cf6c36aacb863e8d6d5a9cb11c332623069c6ba6508d2629f60dd4f2187ade4e5c78e880a9cf0e4270672edd8bb6aeb75fa2eb44e5fe8b20b0ad86f06c81285fa4c791dac8bba654db5067ec32f4d34a7e0fc523cdc8cf2430557b0417960ed9b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e2de740000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000053347f2a083c7d8b225266787947ea5d5b43e9640000000000000000000000000000000000000000000000000de0b6b3a7642531000000000000000000000000000000000000000000000038e9752050f3b37d3300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000e8a81831923a0b20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000e8a81831923a0b20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e7a63314f4755354e7930354e4746684c5451784e5751744f4459784d79316c4f5749314d5464694f5759304f54596966513d3d00000000000000000000000000000000000000000000000000000000000000cd000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000a77d10229f8df892489f00000000000000000000000000000000000000000000a7444318b773c566914f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x81ae06c7b0e5f994c7370a35cbe0eecc7db738ca8e3db926ec154d5f074a0884",
      "signature": {
        "s": "0x0c27bd1ba55eb2083326708b393b1aff14e8c7fe5a2ec175d4b2287109ea24ba",
        "r": "0x68f8558cfa4ece8dd1e91ba1dbd9c26538fa9cc93c5c851b11cb948a382c9c42",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf6c36aacb863e8d6d5a9cb11c332623069c6ba6508d2629f60dd4f2187ade4e5",
      "signature": {
        "s": "0x4c791dac8bba654db5067ec32f4d34a7e0fc523cdc8cf2430557b0417960ed9b",
        "r": "0xc78e880a9cf0e4270672edd8bb6aeb75fa2eb44e5fe8b20b0ad86f06c81285fa",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1047792263379525810000",
    "total": "1047792263379525810000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1047792263379525810000",
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
            "amount": "1047792263379525810"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1047792263379525810"
      }
    },
    "wallet": "0x53347f2a083c7d8b225266787947ea5d5b43e964",
    "data": "eyJyZWYiOiIyNzc1OGU5Ny05NGFhLTQxNWQtODYxMy1lOWI1MTdiOWY0OTYifQ==",
    "nonce": 12,
    "balances": {
      "current": "1000000000000009521",
      "previous": "1049840055642905345331"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 205,
    "balances": {
      "current": "790942208315530369190047",
      "previous": "789894416052150843380047"
    }
  },
  "blockNumber": "14868084",
  "created": "2022-05-29T18:46:52.631Z",
  "updated": "2022-05-29T18:46:52.759Z",
  "id": "6293bf9c3592fd001130b8a6"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de0b6b3a76425310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000000000000009521`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`