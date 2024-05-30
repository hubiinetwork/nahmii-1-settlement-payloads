# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9e228615BB1304073A3c953d491f407f10FB722b`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000012238b08f017f5b54f0000000000000000000000000000000000000000000000006e17d936abf9da320000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000006e17d936abf9da3200000000000000000000000000000000000000000000000c1152310b040c1942865805c38a0d0cbe046c5f6091a653ac5c91ed6362652c680c3c97d439fdfc33e5e820efa7412e23f2af279bbd6b739f971bd4d6890e2728c72facfef9e996a806602f87e412884b5dd166eb7bac20d746faefeaf9a6ff9408c9b3e7a8206504000000000000000000000000000000000000000000000000000000000000001ca15fc9820e0f4b6ea018a3ca0d7fb73d3cd0452d9439d9859dfde7a655ab4d91bcf2a290c8587511e572350a80c3d4f72cc1cbc88a13fe5a875c5f5062b5c4891746e6d249f43eb046f3bc4e2ba31790882d60f2cd6e7f4db1c12aed1a0d743a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b66e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030bd3e47f509c0eaf98b0000000000000000000000000000000000000000000030bdac7bfd511ebad64200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001c2f10b1d602850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfeb025a1549fcdf3d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a57566d4f5755314d69316d4d574e6a4c54557a4e5459744f47526b5a43316a593251315a6a49324d474e684d6a556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009e228615bb1304073a3c953d491f407f10fb722b000000000000000000000000000000000000000000000012238b08f017f5b54f000000000000000000000000000000000000000000000011b5732fb96bfbdb1d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x865805c38a0d0cbe046c5f6091a653ac5c91ed6362652c680c3c97d439fdfc33",
      "signature": {
        "s": "0x06602f87e412884b5dd166eb7bac20d746faefeaf9a6ff9408c9b3e7a8206504",
        "r": "0xe5e820efa7412e23f2af279bbd6b739f971bd4d6890e2728c72facfef9e996a8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa15fc9820e0f4b6ea018a3ca0d7fb73d3cd0452d9439d9859dfde7a655ab4d91",
      "signature": {
        "s": "0x1746e6d249f43eb046f3bc4e2ba31790882d60f2cd6e7f4db1c12aed1a0d743a",
        "r": "0xbcf2a290c8587511e572350a80c3d4f72cc1cbc88a13fe5a875c5f5062b5c489",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7933048097473157682",
    "total": "222609042854631971138"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7933048097473157682",
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
            "amount": "27742390539381804687165"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7933048097473157"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZWVmOWU1Mi1mMWNjLTUzNTYtOGRkZC1jY2Q1ZjI2MGNhMjUifQ==",
    "nonce": 112238,
    "balances": {
      "current": "230164513632650013637003",
      "previous": "230172454613795584267842"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9e228615bb1304073a3c953d491f407f10fb722b",
    "nonce": 46,
    "balances": {
      "current": "334602543967149339983",
      "previous": "326669495869676182301"
    }
  },
  "blockNumber": "14709989",
  "created": "2022-05-04T09:02:43.315Z",
  "updated": "2022-05-04T09:02:43.370Z",
  "id": "62724133bbd75600116d07ab"
}
```
* *stageAmount*: `334602543967149339983`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000006e17d936abf9da320000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000006e17d936abf9da3200000000000000000000000000000000000000000000000c1152310b040c1942865805c38a0d0cbe046c5f6091a653ac5c91ed6362652c680c3c97d439fdfc33e5e820efa7412e23f2af279bbd6b739f971bd4d6890e2728c72facfef9e996a806602f87e412884b5dd166eb7bac20d746faefeaf9a6ff9408c9b3e7a8206504000000000000000000000000000000000000000000000000000000000000001ca15fc9820e0f4b6ea018a3ca0d7fb73d3cd0452d9439d9859dfde7a655ab4d91bcf2a290c8587511e572350a80c3d4f72cc1cbc88a13fe5a875c5f5062b5c4891746e6d249f43eb046f3bc4e2ba31790882d60f2cd6e7f4db1c12aed1a0d743a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b66e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030bd3e47f509c0eaf98b0000000000000000000000000000000000000000000030bdac7bfd511ebad64200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001c2f10b1d602850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfeb025a1549fcdf3d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a57566d4f5755314d69316d4d574e6a4c54557a4e5459744f47526b5a43316a593251315a6a49324d474e684d6a556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009e228615bb1304073a3c953d491f407f10fb722b000000000000000000000000000000000000000000000012238b08f017f5b54f000000000000000000000000000000000000000000000011b5732fb96bfbdb1d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x865805c38a0d0cbe046c5f6091a653ac5c91ed6362652c680c3c97d439fdfc33",
      "signature": {
        "s": "0x06602f87e412884b5dd166eb7bac20d746faefeaf9a6ff9408c9b3e7a8206504",
        "r": "0xe5e820efa7412e23f2af279bbd6b739f971bd4d6890e2728c72facfef9e996a8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa15fc9820e0f4b6ea018a3ca0d7fb73d3cd0452d9439d9859dfde7a655ab4d91",
      "signature": {
        "s": "0x1746e6d249f43eb046f3bc4e2ba31790882d60f2cd6e7f4db1c12aed1a0d743a",
        "r": "0xbcf2a290c8587511e572350a80c3d4f72cc1cbc88a13fe5a875c5f5062b5c489",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7933048097473157682",
    "total": "222609042854631971138"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7933048097473157682",
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
            "amount": "27742390539381804687165"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7933048097473157"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZWVmOWU1Mi1mMWNjLTUzNTYtOGRkZC1jY2Q1ZjI2MGNhMjUifQ==",
    "nonce": 112238,
    "balances": {
      "current": "230164513632650013637003",
      "previous": "230172454613795584267842"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9e228615bb1304073a3c953d491f407f10fb722b",
    "nonce": 46,
    "balances": {
      "current": "334602543967149339983",
      "previous": "326669495869676182301"
    }
  },
  "blockNumber": "14709989",
  "created": "2022-05-04T09:02:43.315Z",
  "updated": "2022-05-04T09:02:43.370Z",
  "id": "62724133bbd75600116d07ab"
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
0x0f200f9b000000000000000000000000000000000000000000000012238b08f017f5b54f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `334602543967149339983`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`