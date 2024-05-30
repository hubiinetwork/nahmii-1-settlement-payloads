# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2D0a564d8133E6ED752B7f36B74E105599ceAb0b`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000009000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000009f46d601aced9738c6b08f5d94bfde79b721089469854fc0bc4556f168d529feb37586cf8fa086ee19f465bf0c2f7d6662c2aab084a4b86be6ce6d97f12785645604f0e72661655ae1c0e7fcff74ffede7a0c6490b6912b53e076b3ddd5a7ef71000000000000000000000000000000000000000000000000000000000000001cdc32ddcbb272adba6a66d90cae11f5116f4da600b218cfe5d0e7982b9426bdf1850a1023c717c075c9e8e2cc80f274cc06500dc2030db0899455a1a268fe06064833e4f018490e3838e28ee90fc9ed01359bd1cf07717f44ef370d2304f293a4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7b92c3b000000000000000000000000000000000000000000000000002386f2c7b92c4500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009460100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d6a426d4e4449314e433030597a52684c5455315a6d45744f47517a5a43307a59546b3459546777596d4e6b4e6a556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002d0a564d8133e6ed752b7f36b74e105599ceab0b0000000000000000000000000000000000000000000000000000000000000009000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf46d601aced9738c6b08f5d94bfde79b721089469854fc0bc4556f168d529feb",
      "signature": {
        "s": "0x604f0e72661655ae1c0e7fcff74ffede7a0c6490b6912b53e076b3ddd5a7ef71",
        "r": "0x37586cf8fa086ee19f465bf0c2f7d6662c2aab084a4b86be6ce6d97f12785645",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdc32ddcbb272adba6a66d90cae11f5116f4da600b218cfe5d0e7982b9426bdf1",
      "signature": {
        "s": "0x4833e4f018490e3838e28ee90fc9ed01359bd1cf07717f44ef370d2304f293a4",
        "r": "0x850a1023c717c075c9e8e2cc80f274cc06500dc2030db0899455a1a268fe0606",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9",
    "total": "9"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9",
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
            "amount": "607745"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0MjBmNDI1NC00YzRhLTU1ZmEtOGQzZC0zYTk4YTgwYmNkNjUifQ==",
    "nonce": 1277,
    "balances": {
      "current": "10000001475882043",
      "previous": "10000001475882053"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d0a564d8133e6ed752b7f36b74e105599ceab0b",
    "nonce": 20,
    "balances": {
      "current": "9",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:10.101Z",
  "updated": "2020-05-22T08:08:10.171Z",
  "id": "5ec7886ab0c6090011d5aa73"
}
```
* *stageAmount*: `9`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000009000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000009f46d601aced9738c6b08f5d94bfde79b721089469854fc0bc4556f168d529feb37586cf8fa086ee19f465bf0c2f7d6662c2aab084a4b86be6ce6d97f12785645604f0e72661655ae1c0e7fcff74ffede7a0c6490b6912b53e076b3ddd5a7ef71000000000000000000000000000000000000000000000000000000000000001cdc32ddcbb272adba6a66d90cae11f5116f4da600b218cfe5d0e7982b9426bdf1850a1023c717c075c9e8e2cc80f274cc06500dc2030db0899455a1a268fe06064833e4f018490e3838e28ee90fc9ed01359bd1cf07717f44ef370d2304f293a4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7b92c3b000000000000000000000000000000000000000000000000002386f2c7b92c4500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009460100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d6a426d4e4449314e433030597a52684c5455315a6d45744f47517a5a43307a59546b3459546777596d4e6b4e6a556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002d0a564d8133e6ed752b7f36b74e105599ceab0b0000000000000000000000000000000000000000000000000000000000000009000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf46d601aced9738c6b08f5d94bfde79b721089469854fc0bc4556f168d529feb",
      "signature": {
        "s": "0x604f0e72661655ae1c0e7fcff74ffede7a0c6490b6912b53e076b3ddd5a7ef71",
        "r": "0x37586cf8fa086ee19f465bf0c2f7d6662c2aab084a4b86be6ce6d97f12785645",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdc32ddcbb272adba6a66d90cae11f5116f4da600b218cfe5d0e7982b9426bdf1",
      "signature": {
        "s": "0x4833e4f018490e3838e28ee90fc9ed01359bd1cf07717f44ef370d2304f293a4",
        "r": "0x850a1023c717c075c9e8e2cc80f274cc06500dc2030db0899455a1a268fe0606",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9",
    "total": "9"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9",
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
            "amount": "607745"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0MjBmNDI1NC00YzRhLTU1ZmEtOGQzZC0zYTk4YTgwYmNkNjUifQ==",
    "nonce": 1277,
    "balances": {
      "current": "10000001475882043",
      "previous": "10000001475882053"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d0a564d8133e6ed752b7f36b74e105599ceab0b",
    "nonce": 20,
    "balances": {
      "current": "9",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:10.101Z",
  "updated": "2020-05-22T08:08:10.171Z",
  "id": "5ec7886ab0c6090011d5aa73"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``