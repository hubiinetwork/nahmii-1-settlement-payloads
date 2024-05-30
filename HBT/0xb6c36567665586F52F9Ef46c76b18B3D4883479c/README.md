# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb6c36567665586F52F9Ef46c76b18B3D4883479c`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000f23c50d000000000000000000000000000000000000000000000000000000000f23c50d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000f23c50d000000000000000000000000000000000000000000000000000000000f23c50d71c762bd8368e56dfa3f7abfa08c3f0fbc36009ad2dff451d770735ed9c7efa8df425092aaf023376c249d61898f0c0202109588fed592e4fe31e36f777e179b012223234da14112fe54efd572aef7c08bb8fa1be81608e4c943bb3502d5f219000000000000000000000000000000000000000000000000000000000000001cc9310e1430322931f95eb8a8f8f3777b4258cf8caa6b6d3653ab984db2074447fc26bcbbddfba5f28917da98892d0ca93e5bba19a8cd01495b9c62ce904f364a5aaa249b09282bcc4a434d3560bd7c37a4aaeecf6542df1c16f05ac32e09dadf000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56600000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000147400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e319495baaf33000000000000000000000000000000000000000000000000002e3194a4e2547200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000003e032000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003925ecbf6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d5459334e544a6c4f53316a4d5455314c5455325a6a41745957566a5979307a4e474d31596a55304d7a4532597a596966513d3d0000000000000000000000000000000000000000000000000000000000000011000000000000000000000000b6c36567665586f52f9ef46c76b18b3d4883479c000000000000000000000000000000000000000000000000000000000f23c50d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x71c762bd8368e56dfa3f7abfa08c3f0fbc36009ad2dff451d770735ed9c7efa8",
      "signature": {
        "s": "0x012223234da14112fe54efd572aef7c08bb8fa1be81608e4c943bb3502d5f219",
        "r": "0xdf425092aaf023376c249d61898f0c0202109588fed592e4fe31e36f777e179b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc9310e1430322931f95eb8a8f8f3777b4258cf8caa6b6d3653ab984db2074447",
      "signature": {
        "s": "0x5aaa249b09282bcc4a434d3560bd7c37a4aaeecf6542df1c16f05ac32e09dadf",
        "r": "0xfc26bcbbddfba5f28917da98892d0ca93e5bba19a8cd01495b9c62ce904f364a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "254002445",
    "total": "254002445"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "254002445",
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
            "amount": "15340588022"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "254002"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMTY3NTJlOS1jMTU1LTU2ZjAtYWVjYy0zNGM1YjU0MzE2YzYifQ==",
    "nonce": 5236,
    "balances": {
      "current": "13002363165650739",
      "previous": "13002363419907186"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6c36567665586f52f9ef46c76b18b3d4883479c",
    "nonce": 17,
    "balances": {
      "current": "254002445",
      "previous": "0"
    }
  },
  "blockNumber": "10114656",
  "created": "2020-05-22T08:39:34.813Z",
  "updated": "2020-05-22T08:39:34.886Z",
  "id": "5ec78fc6e5756b00111b8628"
}
```
* *stageAmount*: `254002445`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000f23c50d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000f23c50d000000000000000000000000000000000000000000000000000000000f23c50d71c762bd8368e56dfa3f7abfa08c3f0fbc36009ad2dff451d770735ed9c7efa8df425092aaf023376c249d61898f0c0202109588fed592e4fe31e36f777e179b012223234da14112fe54efd572aef7c08bb8fa1be81608e4c943bb3502d5f219000000000000000000000000000000000000000000000000000000000000001cc9310e1430322931f95eb8a8f8f3777b4258cf8caa6b6d3653ab984db2074447fc26bcbbddfba5f28917da98892d0ca93e5bba19a8cd01495b9c62ce904f364a5aaa249b09282bcc4a434d3560bd7c37a4aaeecf6542df1c16f05ac32e09dadf000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56600000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000147400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e319495baaf33000000000000000000000000000000000000000000000000002e3194a4e2547200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000003e032000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003925ecbf6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d5459334e544a6c4f53316a4d5455314c5455325a6a41745957566a5979307a4e474d31596a55304d7a4532597a596966513d3d0000000000000000000000000000000000000000000000000000000000000011000000000000000000000000b6c36567665586f52f9ef46c76b18b3d4883479c000000000000000000000000000000000000000000000000000000000f23c50d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x71c762bd8368e56dfa3f7abfa08c3f0fbc36009ad2dff451d770735ed9c7efa8",
      "signature": {
        "s": "0x012223234da14112fe54efd572aef7c08bb8fa1be81608e4c943bb3502d5f219",
        "r": "0xdf425092aaf023376c249d61898f0c0202109588fed592e4fe31e36f777e179b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc9310e1430322931f95eb8a8f8f3777b4258cf8caa6b6d3653ab984db2074447",
      "signature": {
        "s": "0x5aaa249b09282bcc4a434d3560bd7c37a4aaeecf6542df1c16f05ac32e09dadf",
        "r": "0xfc26bcbbddfba5f28917da98892d0ca93e5bba19a8cd01495b9c62ce904f364a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "254002445",
    "total": "254002445"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "254002445",
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
            "amount": "15340588022"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "254002"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMTY3NTJlOS1jMTU1LTU2ZjAtYWVjYy0zNGM1YjU0MzE2YzYifQ==",
    "nonce": 5236,
    "balances": {
      "current": "13002363165650739",
      "previous": "13002363419907186"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6c36567665586f52f9ef46c76b18b3d4883479c",
    "nonce": 17,
    "balances": {
      "current": "254002445",
      "previous": "0"
    }
  },
  "blockNumber": "10114656",
  "created": "2020-05-22T08:39:34.813Z",
  "updated": "2020-05-22T08:39:34.886Z",
  "id": "5ec78fc6e5756b00111b8628"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000f23c50d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `254002445`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`