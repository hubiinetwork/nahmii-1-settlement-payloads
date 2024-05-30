# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8Bf63653841ac8405699EB6d80a8930A8E48435C`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000007ff30000000000000000000000000000000000000000000000000000000000007ff300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000007ff30000000000000000000000000000000000000000000000000000000000007ff3f9a3ad7420eb4155ca911345a101abf9ff0b83085258dd83058c3571a4b08787caa827aaac77471724bc4336ebb44bbf4581d315a2de7a499bedeefd8bf745e7568a9d10846a448d27cec6da131c9250d6cfa10e8d69ba3a328648b1dd09206c000000000000000000000000000000000000000000000000000000000000001c17f613b74f8600dbf0a19b65fefc90f05e97aff8faf6117363b5dd3a28bc2b305255f56c984bc299594b7f7cf892177a6c9fb6e1dc94dd2efb9e64213cef1b547c733186eb24be4774ba2ab1e9a6a5fe0976b9f4b1424d7df90e3e2d484e2ae1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000018f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cca3bed5000000000000000000000000000000000000000000000000002386f2cca43ee800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008052700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a444d354e324a6c4f43316c4f4755324c5455795a5463744f4463794d7931685a4455354d5451775a6a497a4d6a416966513d3d000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000008bf63653841ac8405699eb6d80a8930a8e48435c0000000000000000000000000000000000000000000000000000000000007ff3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf9a3ad7420eb4155ca911345a101abf9ff0b83085258dd83058c3571a4b08787",
      "signature": {
        "s": "0x568a9d10846a448d27cec6da131c9250d6cfa10e8d69ba3a328648b1dd09206c",
        "r": "0xcaa827aaac77471724bc4336ebb44bbf4581d315a2de7a499bedeefd8bf745e7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x17f613b74f8600dbf0a19b65fefc90f05e97aff8faf6117363b5dd3a28bc2b30",
      "signature": {
        "s": "0x7c733186eb24be4774ba2ab1e9a6a5fe0976b9f4b1424d7df90e3e2d484e2ae1",
        "r": "0x5255f56c984bc299594b7f7cf892177a6c9fb6e1dc94dd2efb9e64213cef1b54",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "32755",
    "total": "32755"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "32755",
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
            "amount": "525607"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "32"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZDM5N2JlOC1lOGU2LTUyZTctODcyMy1hZDU5MTQwZjIzMjAifQ==",
    "nonce": 399,
    "balances": {
      "current": "10000001558363861",
      "previous": "10000001558396648"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8bf63653841ac8405699eb6d80a8930a8e48435c",
    "nonce": 13,
    "balances": {
      "current": "32755",
      "previous": "0"
    }
  },
  "blockNumber": "10114500",
  "created": "2020-05-22T08:01:49.426Z",
  "updated": "2020-05-22T08:01:49.494Z",
  "id": "5ec786edb0c6090011d5a951"
}
```
* *stageAmount*: `32755`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000007ff300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000007ff30000000000000000000000000000000000000000000000000000000000007ff3f9a3ad7420eb4155ca911345a101abf9ff0b83085258dd83058c3571a4b08787caa827aaac77471724bc4336ebb44bbf4581d315a2de7a499bedeefd8bf745e7568a9d10846a448d27cec6da131c9250d6cfa10e8d69ba3a328648b1dd09206c000000000000000000000000000000000000000000000000000000000000001c17f613b74f8600dbf0a19b65fefc90f05e97aff8faf6117363b5dd3a28bc2b305255f56c984bc299594b7f7cf892177a6c9fb6e1dc94dd2efb9e64213cef1b547c733186eb24be4774ba2ab1e9a6a5fe0976b9f4b1424d7df90e3e2d484e2ae1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000018f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cca3bed5000000000000000000000000000000000000000000000000002386f2cca43ee800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008052700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a444d354e324a6c4f43316c4f4755324c5455795a5463744f4463794d7931685a4455354d5451775a6a497a4d6a416966513d3d000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000008bf63653841ac8405699eb6d80a8930a8e48435c0000000000000000000000000000000000000000000000000000000000007ff3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf9a3ad7420eb4155ca911345a101abf9ff0b83085258dd83058c3571a4b08787",
      "signature": {
        "s": "0x568a9d10846a448d27cec6da131c9250d6cfa10e8d69ba3a328648b1dd09206c",
        "r": "0xcaa827aaac77471724bc4336ebb44bbf4581d315a2de7a499bedeefd8bf745e7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x17f613b74f8600dbf0a19b65fefc90f05e97aff8faf6117363b5dd3a28bc2b30",
      "signature": {
        "s": "0x7c733186eb24be4774ba2ab1e9a6a5fe0976b9f4b1424d7df90e3e2d484e2ae1",
        "r": "0x5255f56c984bc299594b7f7cf892177a6c9fb6e1dc94dd2efb9e64213cef1b54",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "32755",
    "total": "32755"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "32755",
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
            "amount": "525607"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "32"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZDM5N2JlOC1lOGU2LTUyZTctODcyMy1hZDU5MTQwZjIzMjAifQ==",
    "nonce": 399,
    "balances": {
      "current": "10000001558363861",
      "previous": "10000001558396648"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8bf63653841ac8405699eb6d80a8930a8e48435c",
    "nonce": 13,
    "balances": {
      "current": "32755",
      "previous": "0"
    }
  },
  "blockNumber": "10114500",
  "created": "2020-05-22T08:01:49.426Z",
  "updated": "2020-05-22T08:01:49.494Z",
  "id": "5ec786edb0c6090011d5a951"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000007ff30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `32755`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``