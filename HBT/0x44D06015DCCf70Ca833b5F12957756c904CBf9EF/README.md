# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x44D06015DCCf70Ca833b5F12957756c904CBf9EF`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000017a685be0000000000000000000000000000000000000000000000000000000017a685be000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000017a685be0000000000000000000000000000000000000000000000000000000017a685be5aa09f693d5f06d7a3a7c56b1e5bafa25dc8436d33501bdcbb257aaaf147e2e2dd43bd63f803a7b0a121e0bfa6a0c0bc3aaf1ae803b314f16c98769d03fc451852a5e05b4669b92138cf192956f9b4aeac5845b5a35bcc4d1f1b3e3c853eaee7000000000000000000000000000000000000000000000000000000000000001c157aaa51bcbfd660731c23dda36b809028391c093c7b87fa5e6423dbf8602d61c6e8c25b29feb3ba5908b215ab443f779c34cbf2cec98924b1e78a5507ab69216e21a8d7f35642f2a94467b852cbd09184897d437bd92e71bf2ae3fad9a46153000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019c700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1774e3c21a7f000000000000000000000000000000000000000000000000002e1774fb6eae3200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000060df5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a40b5bbe2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934595446685954426b4f5330774e44426c4c5455314d4755744f57526c5a43316c59546c6b4e4455325a474979596d556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000044d06015dccf70ca833b5f12957756c904cbf9ef0000000000000000000000000000000000000000000000000000000017a685be000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5aa09f693d5f06d7a3a7c56b1e5bafa25dc8436d33501bdcbb257aaaf147e2e2",
      "signature": {
        "s": "0x52a5e05b4669b92138cf192956f9b4aeac5845b5a35bcc4d1f1b3e3c853eaee7",
        "r": "0xdd43bd63f803a7b0a121e0bfa6a0c0bc3aaf1ae803b314f16c98769d03fc4518",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x157aaa51bcbfd660731c23dda36b809028391c093c7b87fa5e6423dbf8602d61",
      "signature": {
        "s": "0x6e21a8d7f35642f2a94467b852cbd09184897d437bd92e71bf2ae3fad9a46153",
        "r": "0xc6e8c25b29feb3ba5908b215ab443f779c34cbf2cec98924b1e78a5507ab6921",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "396789182",
    "total": "396789182"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "396789182",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "44035324898"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "396789"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YTFhYTBkOS0wNDBlLTU1MGUtOWRlZC1lYTlkNDU2ZGIyYmUifQ==",
    "nonce": 6599,
    "balances": {
      "current": "12973639733484159",
      "previous": "12973640130670130"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x44d06015dccf70ca833b5f12957756c904cbf9ef",
    "nonce": 22,
    "balances": {
      "current": "396789182",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:26.833Z",
  "updated": "2020-05-22T08:50:26.909Z",
  "id": "5ec79252005df800101bcad7"
}
```
* *stageAmount*: `396789182`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000017a685be000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000017a685be0000000000000000000000000000000000000000000000000000000017a685be5aa09f693d5f06d7a3a7c56b1e5bafa25dc8436d33501bdcbb257aaaf147e2e2dd43bd63f803a7b0a121e0bfa6a0c0bc3aaf1ae803b314f16c98769d03fc451852a5e05b4669b92138cf192956f9b4aeac5845b5a35bcc4d1f1b3e3c853eaee7000000000000000000000000000000000000000000000000000000000000001c157aaa51bcbfd660731c23dda36b809028391c093c7b87fa5e6423dbf8602d61c6e8c25b29feb3ba5908b215ab443f779c34cbf2cec98924b1e78a5507ab69216e21a8d7f35642f2a94467b852cbd09184897d437bd92e71bf2ae3fad9a46153000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019c700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1774e3c21a7f000000000000000000000000000000000000000000000000002e1774fb6eae3200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000060df5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a40b5bbe2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934595446685954426b4f5330774e44426c4c5455314d4755744f57526c5a43316c59546c6b4e4455325a474979596d556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000044d06015dccf70ca833b5f12957756c904cbf9ef0000000000000000000000000000000000000000000000000000000017a685be000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5aa09f693d5f06d7a3a7c56b1e5bafa25dc8436d33501bdcbb257aaaf147e2e2",
      "signature": {
        "s": "0x52a5e05b4669b92138cf192956f9b4aeac5845b5a35bcc4d1f1b3e3c853eaee7",
        "r": "0xdd43bd63f803a7b0a121e0bfa6a0c0bc3aaf1ae803b314f16c98769d03fc4518",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x157aaa51bcbfd660731c23dda36b809028391c093c7b87fa5e6423dbf8602d61",
      "signature": {
        "s": "0x6e21a8d7f35642f2a94467b852cbd09184897d437bd92e71bf2ae3fad9a46153",
        "r": "0xc6e8c25b29feb3ba5908b215ab443f779c34cbf2cec98924b1e78a5507ab6921",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "396789182",
    "total": "396789182"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "396789182",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "44035324898"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "396789"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YTFhYTBkOS0wNDBlLTU1MGUtOWRlZC1lYTlkNDU2ZGIyYmUifQ==",
    "nonce": 6599,
    "balances": {
      "current": "12973639733484159",
      "previous": "12973640130670130"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x44d06015dccf70ca833b5f12957756c904cbf9ef",
    "nonce": 22,
    "balances": {
      "current": "396789182",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:26.833Z",
  "updated": "2020-05-22T08:50:26.909Z",
  "id": "5ec79252005df800101bcad7"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000017a685be000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `396789182`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`