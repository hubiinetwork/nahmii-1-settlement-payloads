# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x30170d0Cc0Ed9e2A1Aaab80ac596dF4c2E1Fe6C9`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000004e1dc943c18ff1c7aa3caac568b261e22b1d421974fba367ac0c9afefcc9cc6f1582584e88ba1d11ea75052b4b2e465f78e305f107b2d685fda1756c8f82fe556775126be4a5e09edd9f91055c5b285914a6f6ab5e83db3ebe93bc73c2f795c59000000000000000000000000000000000000000000000000000000000000001c0e95fd6fc90b36addea69dc7b260956d1485f8d042f0cbcfcbc0de34139daf18f17a3efa0081eac15cbbfb9135984d6e793ae46696048532db3eed4e195936236fb4dea20208d69409e79494b2d9f01c49e958344719a90a0d5765785e57d05a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000084100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bd96e236000000000000000000000000000000000000000000000000002386f2bd96e23b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000bdc4d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d57526b4f5745795979303359324a6c4c5456694e3251744f54453259533077596d5535595449784d6a4d355a6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000030170d0cc0ed9e2a1aaab80ac596df4c2e1fe6c90000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe1dc943c18ff1c7aa3caac568b261e22b1d421974fba367ac0c9afefcc9cc6f1",
      "signature": {
        "s": "0x775126be4a5e09edd9f91055c5b285914a6f6ab5e83db3ebe93bc73c2f795c59",
        "r": "0x582584e88ba1d11ea75052b4b2e465f78e305f107b2d685fda1756c8f82fe556",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0e95fd6fc90b36addea69dc7b260956d1485f8d042f0cbcfcbc0de34139daf18",
      "signature": {
        "s": "0x6fb4dea20208d69409e79494b2d9f01c49e958344719a90a0d5765785e57d05a",
        "r": "0xf17a3efa0081eac15cbbfb9135984d6e793ae46696048532db3eed4e19593623",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4",
    "total": "4"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4",
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
            "amount": "777293"
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
    "data": "eyJyZWYiOiJlMWRkOWEyYy03Y2JlLTViN2QtOTE2YS0wYmU5YTIxMjM5ZjkifQ==",
    "nonce": 2113,
    "balances": {
      "current": "10000001305862710",
      "previous": "10000001305862715"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x30170d0cc0ed9e2a1aaab80ac596df4c2e1fe6c9",
    "nonce": 4,
    "balances": {
      "current": "4",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:29.119Z",
  "updated": "2020-05-22T08:14:29.188Z",
  "id": "5ec789e5005df800101bc4df"
}
```
* *stageAmount*: `4`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000004e1dc943c18ff1c7aa3caac568b261e22b1d421974fba367ac0c9afefcc9cc6f1582584e88ba1d11ea75052b4b2e465f78e305f107b2d685fda1756c8f82fe556775126be4a5e09edd9f91055c5b285914a6f6ab5e83db3ebe93bc73c2f795c59000000000000000000000000000000000000000000000000000000000000001c0e95fd6fc90b36addea69dc7b260956d1485f8d042f0cbcfcbc0de34139daf18f17a3efa0081eac15cbbfb9135984d6e793ae46696048532db3eed4e195936236fb4dea20208d69409e79494b2d9f01c49e958344719a90a0d5765785e57d05a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000084100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bd96e236000000000000000000000000000000000000000000000000002386f2bd96e23b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000bdc4d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d57526b4f5745795979303359324a6c4c5456694e3251744f54453259533077596d5535595449784d6a4d355a6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000030170d0cc0ed9e2a1aaab80ac596df4c2e1fe6c90000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe1dc943c18ff1c7aa3caac568b261e22b1d421974fba367ac0c9afefcc9cc6f1",
      "signature": {
        "s": "0x775126be4a5e09edd9f91055c5b285914a6f6ab5e83db3ebe93bc73c2f795c59",
        "r": "0x582584e88ba1d11ea75052b4b2e465f78e305f107b2d685fda1756c8f82fe556",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0e95fd6fc90b36addea69dc7b260956d1485f8d042f0cbcfcbc0de34139daf18",
      "signature": {
        "s": "0x6fb4dea20208d69409e79494b2d9f01c49e958344719a90a0d5765785e57d05a",
        "r": "0xf17a3efa0081eac15cbbfb9135984d6e793ae46696048532db3eed4e19593623",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4",
    "total": "4"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4",
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
            "amount": "777293"
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
    "data": "eyJyZWYiOiJlMWRkOWEyYy03Y2JlLTViN2QtOTE2YS0wYmU5YTIxMjM5ZjkifQ==",
    "nonce": 2113,
    "balances": {
      "current": "10000001305862710",
      "previous": "10000001305862715"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x30170d0cc0ed9e2a1aaab80ac596df4c2e1fe6c9",
    "nonce": 4,
    "balances": {
      "current": "4",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:29.119Z",
  "updated": "2020-05-22T08:14:29.188Z",
  "id": "5ec789e5005df800101bc4df"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``