# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x15BCE97936E98517E7a581d047cdA19E2a857146`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000004a350000000000000000000000000000000000000000000000000000000000004a3500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004a350000000000000000000000000000000000000000000000000000000000004a358661ef7864f2da0f92088780df078001be66045825216c465bf9f66c2053d6a588b5ebecd6fb936c149761c1fd272a1588724ffbcce1cc634f204a4bd477b4aa5e7105a3b2250ca0387bf260eb5cc8783ee8d6e7b00b846eb15533c3771b85a5000000000000000000000000000000000000000000000000000000000000001bd8ca0d23b43358386bb8353fe2de5208d8d95d32968e950b610a7320258026d2d32e9ef9d45cb0308e4af2c392dee259ce578405166017b7855026d94e3855cc6fb1780b4ec12e643a5a0b0f864258d0adbf1ac999b7d31b9d05bfccaa1974a4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000061a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c61c164d000000000000000000000000000000000000000000000000002386f2c61c609400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009af4a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d6a4d774e575a6c4f43316b5a544a6c4c5455344f5449744f475a6b4d4330324d57457a4d7a6b355a6d49354e7a456966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000015bce97936e98517e7a581d047cda19e2a8571460000000000000000000000000000000000000000000000000000000000004a35000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8661ef7864f2da0f92088780df078001be66045825216c465bf9f66c2053d6a5",
      "signature": {
        "s": "0x5e7105a3b2250ca0387bf260eb5cc8783ee8d6e7b00b846eb15533c3771b85a5",
        "r": "0x88b5ebecd6fb936c149761c1fd272a1588724ffbcce1cc634f204a4bd477b4aa",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd8ca0d23b43358386bb8353fe2de5208d8d95d32968e950b610a7320258026d2",
      "signature": {
        "s": "0x6fb1780b4ec12e643a5a0b0f864258d0adbf1ac999b7d31b9d05bfccaa1974a4",
        "r": "0xd32e9ef9d45cb0308e4af2c392dee259ce578405166017b7855026d94e3855cc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18997",
    "total": "18997"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18997",
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
            "amount": "634698"
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
    "data": "eyJyZWYiOiIzMjMwNWZlOC1kZTJlLTU4OTItOGZkMC02MWEzMzk5ZmI5NzEifQ==",
    "nonce": 1562,
    "balances": {
      "current": "10000001448810061",
      "previous": "10000001448829076"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x15bce97936e98517e7a581d047cda19e2a857146",
    "nonce": 20,
    "balances": {
      "current": "18997",
      "previous": "0"
    }
  },
  "blockNumber": "10114533",
  "created": "2020-05-22T08:10:32.363Z",
  "updated": "2020-05-22T08:10:32.434Z",
  "id": "5ec788f8e5756b00111b8161"
}
```
* *stageAmount*: `18997`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004a3500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004a350000000000000000000000000000000000000000000000000000000000004a358661ef7864f2da0f92088780df078001be66045825216c465bf9f66c2053d6a588b5ebecd6fb936c149761c1fd272a1588724ffbcce1cc634f204a4bd477b4aa5e7105a3b2250ca0387bf260eb5cc8783ee8d6e7b00b846eb15533c3771b85a5000000000000000000000000000000000000000000000000000000000000001bd8ca0d23b43358386bb8353fe2de5208d8d95d32968e950b610a7320258026d2d32e9ef9d45cb0308e4af2c392dee259ce578405166017b7855026d94e3855cc6fb1780b4ec12e643a5a0b0f864258d0adbf1ac999b7d31b9d05bfccaa1974a4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000061a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c61c164d000000000000000000000000000000000000000000000000002386f2c61c609400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009af4a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d6a4d774e575a6c4f43316b5a544a6c4c5455344f5449744f475a6b4d4330324d57457a4d7a6b355a6d49354e7a456966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000015bce97936e98517e7a581d047cda19e2a8571460000000000000000000000000000000000000000000000000000000000004a35000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8661ef7864f2da0f92088780df078001be66045825216c465bf9f66c2053d6a5",
      "signature": {
        "s": "0x5e7105a3b2250ca0387bf260eb5cc8783ee8d6e7b00b846eb15533c3771b85a5",
        "r": "0x88b5ebecd6fb936c149761c1fd272a1588724ffbcce1cc634f204a4bd477b4aa",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd8ca0d23b43358386bb8353fe2de5208d8d95d32968e950b610a7320258026d2",
      "signature": {
        "s": "0x6fb1780b4ec12e643a5a0b0f864258d0adbf1ac999b7d31b9d05bfccaa1974a4",
        "r": "0xd32e9ef9d45cb0308e4af2c392dee259ce578405166017b7855026d94e3855cc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18997",
    "total": "18997"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18997",
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
            "amount": "634698"
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
    "data": "eyJyZWYiOiIzMjMwNWZlOC1kZTJlLTU4OTItOGZkMC02MWEzMzk5ZmI5NzEifQ==",
    "nonce": 1562,
    "balances": {
      "current": "10000001448810061",
      "previous": "10000001448829076"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x15bce97936e98517e7a581d047cda19e2a857146",
    "nonce": 20,
    "balances": {
      "current": "18997",
      "previous": "0"
    }
  },
  "blockNumber": "10114533",
  "created": "2020-05-22T08:10:32.363Z",
  "updated": "2020-05-22T08:10:32.434Z",
  "id": "5ec788f8e5756b00111b8161"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000004a350000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18997`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``