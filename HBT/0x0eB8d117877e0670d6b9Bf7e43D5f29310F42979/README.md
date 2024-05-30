# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0eB8d117877e0670d6b9Bf7e43D5f29310F42979`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004ed52af6000000000000000000000000000000000000000000000000000000004ed52af6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed52af6000000000000000000000000000000000000000000000000000000004ed52af6523abb9f006a5f1497fdef3504ccf171b00a6c944e6f4030196ef29b2495293c26eab93f1373072943ff148ace73a220548c73730918db3352db101dd10b0570783b93d629f026a781309a23c299f0723199ae50f836fd5df6fbed4ae643e7b6000000000000000000000000000000000000000000000000000000000000001cf0daddae66aac570f45db9afa6a822ece5e8dc6cedba5e10326b14bd61496ef0344572b9dea507dfdb147e0dc8edcfe28c4dd9328da86e8fdfd4995f6ee65fba3f681cc6c8f916b284ce56a3a1ea87ca1845207f151036d1be35966a737977b5000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c2300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13a08c9a39ab000000000000000000000000000000000000000000000000002e13a0db83930200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e61000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3b6d2367000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a4441794e44566c4d79316a4e6a42684c5455315a6a4d744f47557a4f43316c5a5449304f575a684d6a6b775957496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000eb8d117877e0670d6b9bf7e43d5f29310f42979000000000000000000000000000000000000000000000000000000004ed52af6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x523abb9f006a5f1497fdef3504ccf171b00a6c944e6f4030196ef29b2495293c",
      "signature": {
        "s": "0x783b93d629f026a781309a23c299f0723199ae50f836fd5df6fbed4ae643e7b6",
        "r": "0x26eab93f1373072943ff148ace73a220548c73730918db3352db101dd10b0570",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf0daddae66aac570f45db9afa6a822ece5e8dc6cedba5e10326b14bd61496ef0",
      "signature": {
        "s": "0x3f681cc6c8f916b284ce56a3a1ea87ca1845207f151036d1be35966a737977b5",
        "r": "0x344572b9dea507dfdb147e0dc8edcfe28c4dd9328da86e8fdfd4995f6ee65fba",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322593014",
    "total": "1322593014"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322593014",
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
            "amount": "48241648487"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322593"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzZDAyNDVlMy1jNjBhLTU1ZjMtOGUzOC1lZTI0OWZhMjkwYWIifQ==",
    "nonce": 7203,
    "balances": {
      "current": "12969429203302827",
      "previous": "12969430527218434"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0eb8d117877e0670d6b9bf7e43d5f29310f42979",
    "nonce": 22,
    "balances": {
      "current": "1322593014",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:59.217Z",
  "updated": "2020-05-22T08:54:59.292Z",
  "id": "5ec79363005df800101bcba4"
}
```
* *stageAmount*: `1322593014`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004ed52af6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed52af6000000000000000000000000000000000000000000000000000000004ed52af6523abb9f006a5f1497fdef3504ccf171b00a6c944e6f4030196ef29b2495293c26eab93f1373072943ff148ace73a220548c73730918db3352db101dd10b0570783b93d629f026a781309a23c299f0723199ae50f836fd5df6fbed4ae643e7b6000000000000000000000000000000000000000000000000000000000000001cf0daddae66aac570f45db9afa6a822ece5e8dc6cedba5e10326b14bd61496ef0344572b9dea507dfdb147e0dc8edcfe28c4dd9328da86e8fdfd4995f6ee65fba3f681cc6c8f916b284ce56a3a1ea87ca1845207f151036d1be35966a737977b5000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c2300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13a08c9a39ab000000000000000000000000000000000000000000000000002e13a0db83930200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e61000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3b6d2367000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a4441794e44566c4d79316a4e6a42684c5455315a6a4d744f47557a4f43316c5a5449304f575a684d6a6b775957496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000eb8d117877e0670d6b9bf7e43d5f29310f42979000000000000000000000000000000000000000000000000000000004ed52af6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x523abb9f006a5f1497fdef3504ccf171b00a6c944e6f4030196ef29b2495293c",
      "signature": {
        "s": "0x783b93d629f026a781309a23c299f0723199ae50f836fd5df6fbed4ae643e7b6",
        "r": "0x26eab93f1373072943ff148ace73a220548c73730918db3352db101dd10b0570",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf0daddae66aac570f45db9afa6a822ece5e8dc6cedba5e10326b14bd61496ef0",
      "signature": {
        "s": "0x3f681cc6c8f916b284ce56a3a1ea87ca1845207f151036d1be35966a737977b5",
        "r": "0x344572b9dea507dfdb147e0dc8edcfe28c4dd9328da86e8fdfd4995f6ee65fba",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322593014",
    "total": "1322593014"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322593014",
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
            "amount": "48241648487"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322593"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzZDAyNDVlMy1jNjBhLTU1ZjMtOGUzOC1lZTI0OWZhMjkwYWIifQ==",
    "nonce": 7203,
    "balances": {
      "current": "12969429203302827",
      "previous": "12969430527218434"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0eb8d117877e0670d6b9bf7e43d5f29310f42979",
    "nonce": 22,
    "balances": {
      "current": "1322593014",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:59.217Z",
  "updated": "2020-05-22T08:54:59.292Z",
  "id": "5ec79363005df800101bcba4"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004ed52af6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1322593014`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`