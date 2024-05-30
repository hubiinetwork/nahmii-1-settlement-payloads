# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF8F6203e4987934134D292FA0aa8b4235Ab31B83`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004ed5b5d7000000000000000000000000000000000000000000000000000000004ed5b5d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed5b5d7000000000000000000000000000000000000000000000000000000004ed5b5d7de34948729d0bc54b0f7cc79a59e468b912cd202d84917894d99f10ba266bd81736e47b58b53ed4df03a31eb05b7db6b6ffd56dfdbcbd6538f4d60e7fe7da0943ac004721a26e965f6ad50bb75ade9653d99f6955460ec1237d2a9a7ceb5acab000000000000000000000000000000000000000000000000000000000000001c57cd50414773ced65b4d5062f065db889ca2803c681a567f0f0e7cbf37e5ab51fc798242778ed8eeb6fa15bc6224c1e62a2c68e590b3d64c12849051cd3af0b54fdadf4ffd7498f0e4795e8f9944be0d7ebcc2ea2ba25cc03b7824f20e464100000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019ed00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e174326029a3a000000000000000000000000000000000000000000000000002e174374ec7e9500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e84000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4d6e510a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a59324d345a57526a4e5330304e574d334c5455784e474974595467304d7931684d54426d5a57566b596a45794d44456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000f8f6203e4987934134d292fa0aa8b4235ab31b83000000000000000000000000000000000000000000000000000000004ed5b5d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xde34948729d0bc54b0f7cc79a59e468b912cd202d84917894d99f10ba266bd81",
      "signature": {
        "s": "0x3ac004721a26e965f6ad50bb75ade9653d99f6955460ec1237d2a9a7ceb5acab",
        "r": "0x736e47b58b53ed4df03a31eb05b7db6b6ffd56dfdbcbd6538f4d60e7fe7da094",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x57cd50414773ced65b4d5062f065db889ca2803c681a567f0f0e7cbf37e5ab51",
      "signature": {
        "s": "0x4fdadf4ffd7498f0e4795e8f9944be0d7ebcc2ea2ba25cc03b7824f20e464100",
        "r": "0xfc798242778ed8eeb6fa15bc6224c1e62a2c68e590b3d64c12849051cd3af0b5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322628567",
    "total": "1322628567"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322628567",
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
            "amount": "44248748298"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322628"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzY2M4ZWRjNS00NWM3LTUxNGItYTg0My1hMTBmZWVkYjEyMDEifQ==",
    "nonce": 6637,
    "balances": {
      "current": "12973426096642618",
      "previous": "12973427420593813"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf8f6203e4987934134d292fa0aa8b4235ab31b83",
    "nonce": 22,
    "balances": {
      "current": "1322628567",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:43.504Z",
  "updated": "2020-05-22T08:50:43.582Z",
  "id": "5ec79263005df800101bcae7"
}
```
* *stageAmount*: `1322628567`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004ed5b5d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed5b5d7000000000000000000000000000000000000000000000000000000004ed5b5d7de34948729d0bc54b0f7cc79a59e468b912cd202d84917894d99f10ba266bd81736e47b58b53ed4df03a31eb05b7db6b6ffd56dfdbcbd6538f4d60e7fe7da0943ac004721a26e965f6ad50bb75ade9653d99f6955460ec1237d2a9a7ceb5acab000000000000000000000000000000000000000000000000000000000000001c57cd50414773ced65b4d5062f065db889ca2803c681a567f0f0e7cbf37e5ab51fc798242778ed8eeb6fa15bc6224c1e62a2c68e590b3d64c12849051cd3af0b54fdadf4ffd7498f0e4795e8f9944be0d7ebcc2ea2ba25cc03b7824f20e464100000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019ed00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e174326029a3a000000000000000000000000000000000000000000000000002e174374ec7e9500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e84000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4d6e510a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a59324d345a57526a4e5330304e574d334c5455784e474974595467304d7931684d54426d5a57566b596a45794d44456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000f8f6203e4987934134d292fa0aa8b4235ab31b83000000000000000000000000000000000000000000000000000000004ed5b5d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xde34948729d0bc54b0f7cc79a59e468b912cd202d84917894d99f10ba266bd81",
      "signature": {
        "s": "0x3ac004721a26e965f6ad50bb75ade9653d99f6955460ec1237d2a9a7ceb5acab",
        "r": "0x736e47b58b53ed4df03a31eb05b7db6b6ffd56dfdbcbd6538f4d60e7fe7da094",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x57cd50414773ced65b4d5062f065db889ca2803c681a567f0f0e7cbf37e5ab51",
      "signature": {
        "s": "0x4fdadf4ffd7498f0e4795e8f9944be0d7ebcc2ea2ba25cc03b7824f20e464100",
        "r": "0xfc798242778ed8eeb6fa15bc6224c1e62a2c68e590b3d64c12849051cd3af0b5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322628567",
    "total": "1322628567"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322628567",
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
            "amount": "44248748298"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322628"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzY2M4ZWRjNS00NWM3LTUxNGItYTg0My1hMTBmZWVkYjEyMDEifQ==",
    "nonce": 6637,
    "balances": {
      "current": "12973426096642618",
      "previous": "12973427420593813"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf8f6203e4987934134d292fa0aa8b4235ab31b83",
    "nonce": 22,
    "balances": {
      "current": "1322628567",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:43.504Z",
  "updated": "2020-05-22T08:50:43.582Z",
  "id": "5ec79263005df800101bcae7"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004ed5b5d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1322628567`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`