# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc4351ca450725DA5324CB12d7adffe1bA856270F`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000003b999dc0000000000000000000000000000000000000000000000000000000003b999dc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000003b999dc0000000000000000000000000000000000000000000000000000000003b999dc835fc4beed50a6be25157292c11b24ddb43198102c7dc102326e7056cac46c832d6a5ab0a8f51f0ffe410ae0cad0e88e1396405b4627cd455bd8c052f35290210aba301ac3814d56eacda16a2de76dee4ef350ffedb004b5145098e0775cd78c000000000000000000000000000000000000000000000000000000000000001c07e04be3c3acc652a0693d65c1e4709cac4edbaad3a6d38b58682b268e2d9544ba952de7e2de65ef9bd027f36649de8123017afe8f70c03c64058cddaf8038676f68d9e366ca059ce14c45505f85fccff0e6144c19a62da022c5b17f40c96b44000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56880000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000187b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ab927cea2c9000000000000000000000000000000000000000000000000002e1ab92b8930c400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000f41f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096ad6f857000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a596d4d324e57526b4d69316d597a566d4c5456684d6d45745957526a5a6930324e4445324f4459315a4759785a544d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c4351ca450725da5324cb12d7adffe1ba856270f0000000000000000000000000000000000000000000000000000000003b999dc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x835fc4beed50a6be25157292c11b24ddb43198102c7dc102326e7056cac46c83",
      "signature": {
        "s": "0x0aba301ac3814d56eacda16a2de76dee4ef350ffedb004b5145098e0775cd78c",
        "r": "0x2d6a5ab0a8f51f0ffe410ae0cad0e88e1396405b4627cd455bd8c052f3529021",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x07e04be3c3acc652a0693d65c1e4709cac4edbaad3a6d38b58682b268e2d9544",
      "signature": {
        "s": "0x6f68d9e366ca059ce14c45505f85fccff0e6144c19a62da022c5b17f40c96b44",
        "r": "0xba952de7e2de65ef9bd027f36649de8123017afe8f70c03c64058cddaf803867",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "62495196",
    "total": "62495196"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "62495196",
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
            "amount": "40447178839"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "62495"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYmM2NWRkMi1mYzVmLTVhMmEtYWRjZi02NDE2ODY1ZGYxZTMifQ==",
    "nonce": 6267,
    "balances": {
      "current": "12977231467815625",
      "previous": "12977231530373316"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc4351ca450725da5324cb12d7adffe1ba856270f",
    "nonce": 22,
    "balances": {
      "current": "62495196",
      "previous": "0"
    }
  },
  "blockNumber": "10114696",
  "created": "2020-05-22T08:47:45.613Z",
  "updated": "2020-05-22T08:47:45.684Z",
  "id": "5ec791b1005df800101bca62"
}
```
* *stageAmount*: `62495196`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000003b999dc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000003b999dc0000000000000000000000000000000000000000000000000000000003b999dc835fc4beed50a6be25157292c11b24ddb43198102c7dc102326e7056cac46c832d6a5ab0a8f51f0ffe410ae0cad0e88e1396405b4627cd455bd8c052f35290210aba301ac3814d56eacda16a2de76dee4ef350ffedb004b5145098e0775cd78c000000000000000000000000000000000000000000000000000000000000001c07e04be3c3acc652a0693d65c1e4709cac4edbaad3a6d38b58682b268e2d9544ba952de7e2de65ef9bd027f36649de8123017afe8f70c03c64058cddaf8038676f68d9e366ca059ce14c45505f85fccff0e6144c19a62da022c5b17f40c96b44000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56880000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000187b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ab927cea2c9000000000000000000000000000000000000000000000000002e1ab92b8930c400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000f41f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096ad6f857000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a596d4d324e57526b4d69316d597a566d4c5456684d6d45745957526a5a6930324e4445324f4459315a4759785a544d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c4351ca450725da5324cb12d7adffe1ba856270f0000000000000000000000000000000000000000000000000000000003b999dc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x835fc4beed50a6be25157292c11b24ddb43198102c7dc102326e7056cac46c83",
      "signature": {
        "s": "0x0aba301ac3814d56eacda16a2de76dee4ef350ffedb004b5145098e0775cd78c",
        "r": "0x2d6a5ab0a8f51f0ffe410ae0cad0e88e1396405b4627cd455bd8c052f3529021",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x07e04be3c3acc652a0693d65c1e4709cac4edbaad3a6d38b58682b268e2d9544",
      "signature": {
        "s": "0x6f68d9e366ca059ce14c45505f85fccff0e6144c19a62da022c5b17f40c96b44",
        "r": "0xba952de7e2de65ef9bd027f36649de8123017afe8f70c03c64058cddaf803867",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "62495196",
    "total": "62495196"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "62495196",
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
            "amount": "40447178839"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "62495"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYmM2NWRkMi1mYzVmLTVhMmEtYWRjZi02NDE2ODY1ZGYxZTMifQ==",
    "nonce": 6267,
    "balances": {
      "current": "12977231467815625",
      "previous": "12977231530373316"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc4351ca450725da5324cb12d7adffe1ba856270f",
    "nonce": 22,
    "balances": {
      "current": "62495196",
      "previous": "0"
    }
  },
  "blockNumber": "10114696",
  "created": "2020-05-22T08:47:45.613Z",
  "updated": "2020-05-22T08:47:45.684Z",
  "id": "5ec791b1005df800101bca62"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000003b999dc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `62495196`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`