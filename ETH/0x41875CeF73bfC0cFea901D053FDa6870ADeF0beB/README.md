# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x41875CeF73bfC0cFea901D053FDa6870ADeF0beB`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000046790c70406a94e3913ee45dbf056c8f4068ce6e520a03fd20bfce7f1f41b2c669ad1236b094221bc052597298775ef5d35821f59c2e37614a152e577ac743861604bd8092281988a67ab452f91af1b04d3898d38e188c4652f5cea274d7e35695000000000000000000000000000000000000000000000000000000000000001c3051d2213cd94769272a60b446925a617daea13fdbcb0a2a84bc52644c5199010f165b4afae3222b75d8da35a894bad25c228c2dc5eca0d03937e4ccf0035a966ab22b0772bcf54f6f6df237911112e96d7dd20f3689ff242cafeb9c9c04d3e1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000e700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cde0a96d000000000000000000000000000000000000000000000000002386f2cde0a9b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b42a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e7a49774e475a6b4f4330324e6d4d314c5456694f5749745957566a4d6931694e4745774e324532596d526a5a44496966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000041875cef73bfc0cfea901d053fda6870adef0beb0000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x790c70406a94e3913ee45dbf056c8f4068ce6e520a03fd20bfce7f1f41b2c669",
      "signature": {
        "s": "0x04bd8092281988a67ab452f91af1b04d3898d38e188c4652f5cea274d7e35695",
        "r": "0xad1236b094221bc052597298775ef5d35821f59c2e37614a152e577ac7438616",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3051d2213cd94769272a60b446925a617daea13fdbcb0a2a84bc52644c519901",
      "signature": {
        "s": "0x6ab22b0772bcf54f6f6df237911112e96d7dd20f3689ff242cafeb9c9c04d3e1",
        "r": "0x0f165b4afae3222b75d8da35a894bad25c228c2dc5eca0d03937e4ccf0035a96",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "70",
    "total": "70"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "70",
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
            "amount": "504874"
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
    "data": "eyJyZWYiOiI3NzIwNGZkOC02NmM1LTViOWItYWVjMi1iNGEwN2E2YmRjZDIifQ==",
    "nonce": 231,
    "balances": {
      "current": "10000001579133293",
      "previous": "10000001579133364"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x41875cef73bfc0cfea901d053fda6870adef0beb",
    "nonce": 20,
    "balances": {
      "current": "70",
      "previous": "0"
    }
  },
  "blockNumber": "10114493",
  "created": "2020-05-22T08:00:32.740Z",
  "updated": "2020-05-22T08:00:32.808Z",
  "id": "5ec786a0005df800101bc25e"
}
```
* *stageAmount*: `70`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000046790c70406a94e3913ee45dbf056c8f4068ce6e520a03fd20bfce7f1f41b2c669ad1236b094221bc052597298775ef5d35821f59c2e37614a152e577ac743861604bd8092281988a67ab452f91af1b04d3898d38e188c4652f5cea274d7e35695000000000000000000000000000000000000000000000000000000000000001c3051d2213cd94769272a60b446925a617daea13fdbcb0a2a84bc52644c5199010f165b4afae3222b75d8da35a894bad25c228c2dc5eca0d03937e4ccf0035a966ab22b0772bcf54f6f6df237911112e96d7dd20f3689ff242cafeb9c9c04d3e1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000e700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cde0a96d000000000000000000000000000000000000000000000000002386f2cde0a9b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b42a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e7a49774e475a6b4f4330324e6d4d314c5456694f5749745957566a4d6931694e4745774e324532596d526a5a44496966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000041875cef73bfc0cfea901d053fda6870adef0beb0000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x790c70406a94e3913ee45dbf056c8f4068ce6e520a03fd20bfce7f1f41b2c669",
      "signature": {
        "s": "0x04bd8092281988a67ab452f91af1b04d3898d38e188c4652f5cea274d7e35695",
        "r": "0xad1236b094221bc052597298775ef5d35821f59c2e37614a152e577ac7438616",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3051d2213cd94769272a60b446925a617daea13fdbcb0a2a84bc52644c519901",
      "signature": {
        "s": "0x6ab22b0772bcf54f6f6df237911112e96d7dd20f3689ff242cafeb9c9c04d3e1",
        "r": "0x0f165b4afae3222b75d8da35a894bad25c228c2dc5eca0d03937e4ccf0035a96",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "70",
    "total": "70"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "70",
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
            "amount": "504874"
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
    "data": "eyJyZWYiOiI3NzIwNGZkOC02NmM1LTViOWItYWVjMi1iNGEwN2E2YmRjZDIifQ==",
    "nonce": 231,
    "balances": {
      "current": "10000001579133293",
      "previous": "10000001579133364"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x41875cef73bfc0cfea901d053fda6870adef0beb",
    "nonce": 20,
    "balances": {
      "current": "70",
      "previous": "0"
    }
  },
  "blockNumber": "10114493",
  "created": "2020-05-22T08:00:32.740Z",
  "updated": "2020-05-22T08:00:32.808Z",
  "id": "5ec786a0005df800101bc25e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `70`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``