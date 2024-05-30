# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5d66A9FB9d8fFA67faA21E83591e453755cFE6f6`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000adcda00000000000000000000000000000000000000000000000000000000000adcda000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000adcda00000000000000000000000000000000000000000000000000000000000adcdafca812683a5cee22d42f13b7b7b158de67be7d61f69a5ea84d2dbfc114e023e56ee7bd24d20a6ac2a0f4fbe38639d6fef10187a2e14f137d1e1b6fbf37e1484a37b89255c5381f8a9afb8a381b4c722884fbc621e5de115919c7aebba06731de000000000000000000000000000000000000000000000000000000000000001c6a7b4af20448ba29740908eb4009268763a44957026beb51438d30031a63636e89690feb062e5866728a66ebd05bbc3aa51752e3223f1bc51141ff01925d1a4778294163961138253d8d2ff38b8b1fb98b4ea57a2489ec0a0ef2663b3cdc071c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001c500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbe0ddb1000000000000000000000000000000000000000000000000002386f2cbebbd5200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002c70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000836f400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e7a49345a6d59305a43316c4f4452694c5455325a4463744f4449334e53316b4f5451795a444669596a6c6b4d6d556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000005d66a9fb9d8ffa67faa21e83591e453755cfe6f600000000000000000000000000000000000000000000000000000000000adcda000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfca812683a5cee22d42f13b7b7b158de67be7d61f69a5ea84d2dbfc114e023e5",
      "signature": {
        "s": "0x37b89255c5381f8a9afb8a381b4c722884fbc621e5de115919c7aebba06731de",
        "r": "0x6ee7bd24d20a6ac2a0f4fbe38639d6fef10187a2e14f137d1e1b6fbf37e1484a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a7b4af20448ba29740908eb4009268763a44957026beb51438d30031a63636e",
      "signature": {
        "s": "0x78294163961138253d8d2ff38b8b1fb98b4ea57a2489ec0a0ef2663b3cdc071c",
        "r": "0x89690feb062e5866728a66ebd05bbc3aa51752e3223f1bc51141ff01925d1a47",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "711898",
    "total": "711898"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "711898",
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
            "amount": "538356"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "711"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNzI4ZmY0ZC1lODRiLTU2ZDctODI3NS1kOTQyZDFiYjlkMmUifQ==",
    "nonce": 453,
    "balances": {
      "current": "10000001545592241",
      "previous": "10000001546304850"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5d66a9fb9d8ffa67faa21e83591e453755cfe6f6",
    "nonce": 20,
    "balances": {
      "current": "711898",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:07.795Z",
  "updated": "2020-05-22T08:02:07.867Z",
  "id": "5ec786ffb0c6090011d5a963"
}
```
* *stageAmount*: `711898`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000adcda000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000adcda00000000000000000000000000000000000000000000000000000000000adcdafca812683a5cee22d42f13b7b7b158de67be7d61f69a5ea84d2dbfc114e023e56ee7bd24d20a6ac2a0f4fbe38639d6fef10187a2e14f137d1e1b6fbf37e1484a37b89255c5381f8a9afb8a381b4c722884fbc621e5de115919c7aebba06731de000000000000000000000000000000000000000000000000000000000000001c6a7b4af20448ba29740908eb4009268763a44957026beb51438d30031a63636e89690feb062e5866728a66ebd05bbc3aa51752e3223f1bc51141ff01925d1a4778294163961138253d8d2ff38b8b1fb98b4ea57a2489ec0a0ef2663b3cdc071c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001c500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbe0ddb1000000000000000000000000000000000000000000000000002386f2cbebbd5200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002c70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000836f400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e7a49345a6d59305a43316c4f4452694c5455325a4463744f4449334e53316b4f5451795a444669596a6c6b4d6d556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000005d66a9fb9d8ffa67faa21e83591e453755cfe6f600000000000000000000000000000000000000000000000000000000000adcda000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfca812683a5cee22d42f13b7b7b158de67be7d61f69a5ea84d2dbfc114e023e5",
      "signature": {
        "s": "0x37b89255c5381f8a9afb8a381b4c722884fbc621e5de115919c7aebba06731de",
        "r": "0x6ee7bd24d20a6ac2a0f4fbe38639d6fef10187a2e14f137d1e1b6fbf37e1484a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a7b4af20448ba29740908eb4009268763a44957026beb51438d30031a63636e",
      "signature": {
        "s": "0x78294163961138253d8d2ff38b8b1fb98b4ea57a2489ec0a0ef2663b3cdc071c",
        "r": "0x89690feb062e5866728a66ebd05bbc3aa51752e3223f1bc51141ff01925d1a47",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "711898",
    "total": "711898"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "711898",
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
            "amount": "538356"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "711"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNzI4ZmY0ZC1lODRiLTU2ZDctODI3NS1kOTQyZDFiYjlkMmUifQ==",
    "nonce": 453,
    "balances": {
      "current": "10000001545592241",
      "previous": "10000001546304850"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5d66a9fb9d8ffa67faa21e83591e453755cfe6f6",
    "nonce": 20,
    "balances": {
      "current": "711898",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:07.795Z",
  "updated": "2020-05-22T08:02:07.867Z",
  "id": "5ec786ffb0c6090011d5a963"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000adcda0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `711898`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``