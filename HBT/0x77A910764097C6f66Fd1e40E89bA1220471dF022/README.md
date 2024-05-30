# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x77A910764097C6f66Fd1e40E89bA1220471dF022`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000495011b000000000000000000000000000000000000000000000000000000000495011b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000495011b000000000000000000000000000000000000000000000000000000000495011b47760f500b75d2bf2807cebcae879492d875032bf24ba5305ab580ed8c129346fd28a0592644d65fceb14e107656c86dda48da84d2e2ea99c7b8e507bc5eb267671ccfffe0834be78710ed3c4583a07607bdbcf438623910b26a71de739753ff000000000000000000000000000000000000000000000000000000000000001b2a518984d767a4cf061255fad94d182e766fd38cb8d9f6f6302d1ebf0b163f8adfeaab2cc98d3525c797272c2467d5c46f0c622b7100c12d503e767ece730e7f5e666cdf9f57f5a80cff8ca1f76d289754ed176144c508d03c1c7d30552b3853000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56be00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e5300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0590b57b1b000000000000000000000000000000000000000000000000002e0b05954ba88000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000012c4a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ed3a910000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6d4a6a4e47566b4d79316d4f4456694c54557a5a6a6374596a59354f5330305a4459334d444e684d7a51794d47496966513d3d000000000000000000000000000000000000000000000000000000000000000700000000000000000000000077a910764097c6f66fd1e40e89ba1220471df022000000000000000000000000000000000000000000000000000000000495011b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x47760f500b75d2bf2807cebcae879492d875032bf24ba5305ab580ed8c129346",
      "signature": {
        "s": "0x671ccfffe0834be78710ed3c4583a07607bdbcf438623910b26a71de739753ff",
        "r": "0xfd28a0592644d65fceb14e107656c86dda48da84d2e2ea99c7b8e507bc5eb267",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2a518984d767a4cf061255fad94d182e766fd38cb8d9f6f6302d1ebf0b163f8a",
      "signature": {
        "s": "0x5e666cdf9f57f5a80cff8ca1f76d289754ed176144c508d03c1c7d30552b3853",
        "r": "0xdfeaab2cc98d3525c797272c2467d5c46f0c622b7100c12d503e767ece730e7f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "76874011",
    "total": "76874011"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76874011",
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
            "amount": "57693939984"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "76874"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ZmJjNGVkMy1mODViLTUzZjctYjY5OS00ZDY3MDNhMzQyMGIifQ==",
    "nonce": 7763,
    "balances": {
      "current": "12959967459244827",
      "previous": "12959967536195712"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x77a910764097c6f66fd1e40e89ba1220471df022",
    "nonce": 7,
    "balances": {
      "current": "76874011",
      "previous": "0"
    }
  },
  "blockNumber": "10114750",
  "created": "2020-05-22T08:59:26.909Z",
  "updated": "2020-05-22T08:59:27.979Z",
  "id": "5ec7946e005df800101bcc63"
}
```
* *stageAmount*: `76874011`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000495011b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000495011b000000000000000000000000000000000000000000000000000000000495011b47760f500b75d2bf2807cebcae879492d875032bf24ba5305ab580ed8c129346fd28a0592644d65fceb14e107656c86dda48da84d2e2ea99c7b8e507bc5eb267671ccfffe0834be78710ed3c4583a07607bdbcf438623910b26a71de739753ff000000000000000000000000000000000000000000000000000000000000001b2a518984d767a4cf061255fad94d182e766fd38cb8d9f6f6302d1ebf0b163f8adfeaab2cc98d3525c797272c2467d5c46f0c622b7100c12d503e767ece730e7f5e666cdf9f57f5a80cff8ca1f76d289754ed176144c508d03c1c7d30552b3853000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56be00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e5300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0590b57b1b000000000000000000000000000000000000000000000000002e0b05954ba88000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000012c4a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ed3a910000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6d4a6a4e47566b4d79316d4f4456694c54557a5a6a6374596a59354f5330305a4459334d444e684d7a51794d47496966513d3d000000000000000000000000000000000000000000000000000000000000000700000000000000000000000077a910764097c6f66fd1e40e89ba1220471df022000000000000000000000000000000000000000000000000000000000495011b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x47760f500b75d2bf2807cebcae879492d875032bf24ba5305ab580ed8c129346",
      "signature": {
        "s": "0x671ccfffe0834be78710ed3c4583a07607bdbcf438623910b26a71de739753ff",
        "r": "0xfd28a0592644d65fceb14e107656c86dda48da84d2e2ea99c7b8e507bc5eb267",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2a518984d767a4cf061255fad94d182e766fd38cb8d9f6f6302d1ebf0b163f8a",
      "signature": {
        "s": "0x5e666cdf9f57f5a80cff8ca1f76d289754ed176144c508d03c1c7d30552b3853",
        "r": "0xdfeaab2cc98d3525c797272c2467d5c46f0c622b7100c12d503e767ece730e7f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "76874011",
    "total": "76874011"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76874011",
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
            "amount": "57693939984"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "76874"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ZmJjNGVkMy1mODViLTUzZjctYjY5OS00ZDY3MDNhMzQyMGIifQ==",
    "nonce": 7763,
    "balances": {
      "current": "12959967459244827",
      "previous": "12959967536195712"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x77a910764097c6f66fd1e40e89ba1220471df022",
    "nonce": 7,
    "balances": {
      "current": "76874011",
      "previous": "0"
    }
  },
  "blockNumber": "10114750",
  "created": "2020-05-22T08:59:26.909Z",
  "updated": "2020-05-22T08:59:27.979Z",
  "id": "5ec7946e005df800101bcc63"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000495011b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `76874011`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`