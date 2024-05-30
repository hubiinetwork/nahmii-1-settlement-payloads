# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xDcEB496c6a62E825923a3C3e02b834CaC3e5C275`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000c514faa800000000000000000000000000000000000000000000000000000000c514faa8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000c514faa800000000000000000000000000000000000000000000000000000000c514faa8a7dac7eacf285cb128c9d694554607f647fadb946fc676ffe8f71d7274cf531017f53eb49639cc3105ecb8f0981007742b3fbe0d00eb84ac829592bfbb9f022945bb63c3cec12f5e81dfa3cbaa9ae71fd9b74c53d767643c2cb78ea7022a99b5000000000000000000000000000000000000000000000000000000000000001b332b758468b18f4c8d5180dbdb83b6994145f081644173e86ba2a6c11da26b782b80318bdb79d668e40613a318b111ace71528e688fe3992d0779c0e63f914be642be2439dec3793c542b779445d6d94aab7d95857445762590568b5b85d1d7f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c1b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13a37c02f81b000000000000000000000000000000000000000000000000002e13a4414a66b900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003273f6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3aacf842000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a6a466a4f475a694e7930774e44646c4c5455794d5759744f474d324e433078595452684d5449795a54453459546b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dceb496c6a62e825923a3c3e02b834cac3e5c27500000000000000000000000000000000000000000000000000000000c514faa8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa7dac7eacf285cb128c9d694554607f647fadb946fc676ffe8f71d7274cf5310",
      "signature": {
        "s": "0x45bb63c3cec12f5e81dfa3cbaa9ae71fd9b74c53d767643c2cb78ea7022a99b5",
        "r": "0x17f53eb49639cc3105ecb8f0981007742b3fbe0d00eb84ac829592bfbb9f0229",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x332b758468b18f4c8d5180dbdb83b6994145f081644173e86ba2a6c11da26b78",
      "signature": {
        "s": "0x642be2439dec3793c542b779445d6d94aab7d95857445762590568b5b85d1d7f",
        "r": "0x2b80318bdb79d668e40613a318b111ace71528e688fe3992d0779c0e63f914be",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3306486440",
    "total": "3306486440"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3306486440",
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
            "amount": "48229054530"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3306486"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwZjFjOGZiNy0wNDdlLTUyMWYtOGM2NC0xYTRhMTIyZTE4YTkifQ==",
    "nonce": 7195,
    "balances": {
      "current": "12969441809856539",
      "previous": "12969445119649465"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdceb496c6a62e825923a3c3e02b834cac3e5c275",
    "nonce": 22,
    "balances": {
      "current": "3306486440",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:55.671Z",
  "updated": "2020-05-22T08:54:55.757Z",
  "id": "5ec7935fe5756b00111b889a"
}
```
* *stageAmount*: `3306486440`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000c514faa8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000c514faa800000000000000000000000000000000000000000000000000000000c514faa8a7dac7eacf285cb128c9d694554607f647fadb946fc676ffe8f71d7274cf531017f53eb49639cc3105ecb8f0981007742b3fbe0d00eb84ac829592bfbb9f022945bb63c3cec12f5e81dfa3cbaa9ae71fd9b74c53d767643c2cb78ea7022a99b5000000000000000000000000000000000000000000000000000000000000001b332b758468b18f4c8d5180dbdb83b6994145f081644173e86ba2a6c11da26b782b80318bdb79d668e40613a318b111ace71528e688fe3992d0779c0e63f914be642be2439dec3793c542b779445d6d94aab7d95857445762590568b5b85d1d7f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c1b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13a37c02f81b000000000000000000000000000000000000000000000000002e13a4414a66b900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003273f6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3aacf842000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a6a466a4f475a694e7930774e44646c4c5455794d5759744f474d324e433078595452684d5449795a54453459546b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dceb496c6a62e825923a3c3e02b834cac3e5c27500000000000000000000000000000000000000000000000000000000c514faa8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa7dac7eacf285cb128c9d694554607f647fadb946fc676ffe8f71d7274cf5310",
      "signature": {
        "s": "0x45bb63c3cec12f5e81dfa3cbaa9ae71fd9b74c53d767643c2cb78ea7022a99b5",
        "r": "0x17f53eb49639cc3105ecb8f0981007742b3fbe0d00eb84ac829592bfbb9f0229",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x332b758468b18f4c8d5180dbdb83b6994145f081644173e86ba2a6c11da26b78",
      "signature": {
        "s": "0x642be2439dec3793c542b779445d6d94aab7d95857445762590568b5b85d1d7f",
        "r": "0x2b80318bdb79d668e40613a318b111ace71528e688fe3992d0779c0e63f914be",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3306486440",
    "total": "3306486440"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3306486440",
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
            "amount": "48229054530"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3306486"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwZjFjOGZiNy0wNDdlLTUyMWYtOGM2NC0xYTRhMTIyZTE4YTkifQ==",
    "nonce": 7195,
    "balances": {
      "current": "12969441809856539",
      "previous": "12969445119649465"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdceb496c6a62e825923a3c3e02b834cac3e5c275",
    "nonce": 22,
    "balances": {
      "current": "3306486440",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:55.671Z",
  "updated": "2020-05-22T08:54:55.757Z",
  "id": "5ec7935fe5756b00111b889a"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000c514faa8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3306486440`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`