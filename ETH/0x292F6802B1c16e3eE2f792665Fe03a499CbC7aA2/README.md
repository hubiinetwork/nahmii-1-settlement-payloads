# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x292F6802B1c16e3eE2f792665Fe03a499CbC7aA2`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000fd80000000000000000000000000000000000000000000000000000000000000fd800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000fd80000000000000000000000000000000000000000000000000000000000000fd8b0fbb5b93d3ea4e967ae59e93c26a41a36fd9e024f3a36df529f35e79e7d6686b0a59742e012d114c5dd69f6f08bc27ae8e1b0c44759a4c86b01c0b648f4d3a65f9da39151e0654862c4bd946c2be8dea25d4b27971ce27e8b60e636d5e551ab000000000000000000000000000000000000000000000000000000000000001ceb65e78ede235c26323dd7ec91d290514069d078c6819430af09ecd3d65a92275c03b03a06a4ec9743c8f70cd6b63486aa416398e0b1eb30dc6d8bc4abbd3d805a02abf7fd77774672c70ab00b8d5f7c72c062b6311384587aaebe23781aae84000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55da000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004c000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7ec5b93000000000000000000000000000000000000000000000000002386f2c7ec6b6f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000938f900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a4455344e544533597931684e6a686a4c54553059545574595752684f53316c4d546c6a4e7a6777596d55795a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000292f6802b1c16e3ee2f792665fe03a499cbc7aa20000000000000000000000000000000000000000000000000000000000000fd8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb0fbb5b93d3ea4e967ae59e93c26a41a36fd9e024f3a36df529f35e79e7d6686",
      "signature": {
        "s": "0x5f9da39151e0654862c4bd946c2be8dea25d4b27971ce27e8b60e636d5e551ab",
        "r": "0xb0a59742e012d114c5dd69f6f08bc27ae8e1b0c44759a4c86b01c0b648f4d3a6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xeb65e78ede235c26323dd7ec91d290514069d078c6819430af09ecd3d65a9227",
      "signature": {
        "s": "0x5a02abf7fd77774672c70ab00b8d5f7c72c062b6311384587aaebe23781aae84",
        "r": "0x5c03b03a06a4ec9743c8f70cd6b63486aa416398e0b1eb30dc6d8bc4abbd3d80",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4056",
    "total": "4056"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4056",
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
            "amount": "604409"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZDU4NTE3Yy1hNjhjLTU0YTUtYWRhOS1lMTljNzgwYmUyZjMifQ==",
    "nonce": 1216,
    "balances": {
      "current": "10000001479236499",
      "previous": "10000001479240559"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x292f6802b1c16e3ee2f792665fe03a499cbc7aa2",
    "nonce": 14,
    "balances": {
      "current": "4056",
      "previous": "0"
    }
  },
  "blockNumber": "10114522",
  "created": "2020-05-22T08:07:40.137Z",
  "updated": "2020-05-22T08:07:40.204Z",
  "id": "5ec7884c005df800101bc3b5"
}
```
* *stageAmount*: `4056`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000fd800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000fd80000000000000000000000000000000000000000000000000000000000000fd8b0fbb5b93d3ea4e967ae59e93c26a41a36fd9e024f3a36df529f35e79e7d6686b0a59742e012d114c5dd69f6f08bc27ae8e1b0c44759a4c86b01c0b648f4d3a65f9da39151e0654862c4bd946c2be8dea25d4b27971ce27e8b60e636d5e551ab000000000000000000000000000000000000000000000000000000000000001ceb65e78ede235c26323dd7ec91d290514069d078c6819430af09ecd3d65a92275c03b03a06a4ec9743c8f70cd6b63486aa416398e0b1eb30dc6d8bc4abbd3d805a02abf7fd77774672c70ab00b8d5f7c72c062b6311384587aaebe23781aae84000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55da000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004c000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7ec5b93000000000000000000000000000000000000000000000000002386f2c7ec6b6f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000938f900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a4455344e544533597931684e6a686a4c54553059545574595752684f53316c4d546c6a4e7a6777596d55795a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000292f6802b1c16e3ee2f792665fe03a499cbc7aa20000000000000000000000000000000000000000000000000000000000000fd8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb0fbb5b93d3ea4e967ae59e93c26a41a36fd9e024f3a36df529f35e79e7d6686",
      "signature": {
        "s": "0x5f9da39151e0654862c4bd946c2be8dea25d4b27971ce27e8b60e636d5e551ab",
        "r": "0xb0a59742e012d114c5dd69f6f08bc27ae8e1b0c44759a4c86b01c0b648f4d3a6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xeb65e78ede235c26323dd7ec91d290514069d078c6819430af09ecd3d65a9227",
      "signature": {
        "s": "0x5a02abf7fd77774672c70ab00b8d5f7c72c062b6311384587aaebe23781aae84",
        "r": "0x5c03b03a06a4ec9743c8f70cd6b63486aa416398e0b1eb30dc6d8bc4abbd3d80",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4056",
    "total": "4056"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4056",
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
            "amount": "604409"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZDU4NTE3Yy1hNjhjLTU0YTUtYWRhOS1lMTljNzgwYmUyZjMifQ==",
    "nonce": 1216,
    "balances": {
      "current": "10000001479236499",
      "previous": "10000001479240559"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x292f6802b1c16e3ee2f792665fe03a499cbc7aa2",
    "nonce": 14,
    "balances": {
      "current": "4056",
      "previous": "0"
    }
  },
  "blockNumber": "10114522",
  "created": "2020-05-22T08:07:40.137Z",
  "updated": "2020-05-22T08:07:40.204Z",
  "id": "5ec7884c005df800101bc3b5"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000fd80000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4056`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``