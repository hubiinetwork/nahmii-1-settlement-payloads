# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x722907C29c3ea0Bc9B502cD9d8Bb7128dc1Ce5B1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000022c458950000000000000000000000000000000000000000000000000000000022c45895000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000022c458950000000000000000000000000000000000000000000000000000000022c458955c29c9055590eab84a74b0e355c5cae59dbf87e8da4010306db6450657604844e03e38a1cecd03f18deb5d0dcf1119a5a33eac4d6fc1e6b23cdacdf25c7675da1e429ef85e3c7c6d022b06f322d63dcf1fbebfcc3056102b8c83356d67e92e81000000000000000000000000000000000000000000000000000000000000001becc6d51ca2f007f6bee17b0776c5480b29d785699a71c4ee357c1e64a063875c13b44c9fa29556b991394932aee2f4bd8a954c8a728f50a93b60043942d1dfbc1fae895afd6cd025e66787f1c3d2d9f962fb75d803f935d75e39acaa7ea3993f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a567e000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017ba00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b12ffa509f0000000000000000000000000000000000000000000000000002e1b132272490200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000008e67d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000953dce527000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931593251304d6a4d334e4330344e4467324c5455354e7a41744f575a6b5a533033596d5978595749334d3259324e57516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000722907c29c3ea0bc9b502cd9d8bb7128dc1ce5b10000000000000000000000000000000000000000000000000000000022c45895000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5c29c9055590eab84a74b0e355c5cae59dbf87e8da4010306db6450657604844",
      "signature": {
        "s": "0x1e429ef85e3c7c6d022b06f322d63dcf1fbebfcc3056102b8c83356d67e92e81",
        "r": "0xe03e38a1cecd03f18deb5d0dcf1119a5a33eac4d6fc1e6b23cdacdf25c7675da",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xecc6d51ca2f007f6bee17b0776c5480b29d785699a71c4ee357c1e64a063875c",
      "signature": {
        "s": "0x1fae895afd6cd025e66787f1c3d2d9f962fb75d803f935d75e39acaa7ea3993f",
        "r": "0x13b44c9fa29556b991394932aee2f4bd8a954c8a728f50a93b60043942d1dfbc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "583293077",
    "total": "583293077"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "583293077",
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
            "amount": "40061691175"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "583293"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1Y2Q0MjM3NC04NDg2LTU5NzAtOWZkZS03YmYxYWI3M2Y2NWQifQ==",
    "nonce": 6074,
    "balances": {
      "current": "12977617341057520",
      "previous": "12977617924933890"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x722907c29c3ea0bc9b502cd9d8bb7128dc1ce5b1",
    "nonce": 22,
    "balances": {
      "current": "583293077",
      "previous": "0"
    }
  },
  "blockNumber": "10114686",
  "created": "2020-05-22T08:46:12.666Z",
  "updated": "2020-05-22T08:46:12.724Z",
  "id": "5ec79154e5756b00111b8738"
}
```
* *stageAmount*: `583293077`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000022c45895000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000022c458950000000000000000000000000000000000000000000000000000000022c458955c29c9055590eab84a74b0e355c5cae59dbf87e8da4010306db6450657604844e03e38a1cecd03f18deb5d0dcf1119a5a33eac4d6fc1e6b23cdacdf25c7675da1e429ef85e3c7c6d022b06f322d63dcf1fbebfcc3056102b8c83356d67e92e81000000000000000000000000000000000000000000000000000000000000001becc6d51ca2f007f6bee17b0776c5480b29d785699a71c4ee357c1e64a063875c13b44c9fa29556b991394932aee2f4bd8a954c8a728f50a93b60043942d1dfbc1fae895afd6cd025e66787f1c3d2d9f962fb75d803f935d75e39acaa7ea3993f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a567e000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017ba00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b12ffa509f0000000000000000000000000000000000000000000000000002e1b132272490200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000008e67d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000953dce527000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931593251304d6a4d334e4330344e4467324c5455354e7a41744f575a6b5a533033596d5978595749334d3259324e57516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000722907c29c3ea0bc9b502cd9d8bb7128dc1ce5b10000000000000000000000000000000000000000000000000000000022c45895000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5c29c9055590eab84a74b0e355c5cae59dbf87e8da4010306db6450657604844",
      "signature": {
        "s": "0x1e429ef85e3c7c6d022b06f322d63dcf1fbebfcc3056102b8c83356d67e92e81",
        "r": "0xe03e38a1cecd03f18deb5d0dcf1119a5a33eac4d6fc1e6b23cdacdf25c7675da",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xecc6d51ca2f007f6bee17b0776c5480b29d785699a71c4ee357c1e64a063875c",
      "signature": {
        "s": "0x1fae895afd6cd025e66787f1c3d2d9f962fb75d803f935d75e39acaa7ea3993f",
        "r": "0x13b44c9fa29556b991394932aee2f4bd8a954c8a728f50a93b60043942d1dfbc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "583293077",
    "total": "583293077"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "583293077",
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
            "amount": "40061691175"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "583293"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1Y2Q0MjM3NC04NDg2LTU5NzAtOWZkZS03YmYxYWI3M2Y2NWQifQ==",
    "nonce": 6074,
    "balances": {
      "current": "12977617341057520",
      "previous": "12977617924933890"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x722907c29c3ea0bc9b502cd9d8bb7128dc1ce5b1",
    "nonce": 22,
    "balances": {
      "current": "583293077",
      "previous": "0"
    }
  },
  "blockNumber": "10114686",
  "created": "2020-05-22T08:46:12.666Z",
  "updated": "2020-05-22T08:46:12.724Z",
  "id": "5ec79154e5756b00111b8738"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000022c45895000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `583293077`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`