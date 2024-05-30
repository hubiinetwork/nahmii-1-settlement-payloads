# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xfC20588B7A8F4fF347831574b7eb46649489707c`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001ca10000000000000000000000000000000000000000000000000000000000001ca100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001ca10000000000000000000000000000000000000000000000000000000000001ca1cf7765fa5314ed230b6ca5bbfe2cf07e8e64872996d9a08a0c20734babd3b0eaf2c542171d2da1345ed7a6910ac2e7e5b449f95ff4449ae56ea6277abd1fb8595034499ac7920c1d4ca922723ac05e8aedc5e6e85ea67c397fd8d7f337d0989c000000000000000000000000000000000000000000000000000000000000001b244c571f3fcbadc4df02cfe5fb86b609cb71d1e8132bab0d68cde73392f454df9ef40734326c4bc1ff77a84fed76b0d0577552dc9f060b3c258cd2e4f86a7b9426fcf7be1754d9b666c738d6f9434e7911add6909d56d772545ab9455acb50aa000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000060b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c658882e000000000000000000000000000000000000000000000000002386f2c658a4d600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000007000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099fd900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d475579597a6c685a5330355a6d55784c5456684d6a497459574d794f53316d5a6a6b784f5745344e5445774d54676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000fc20588b7a8f4ff347831574b7eb46649489707c0000000000000000000000000000000000000000000000000000000000001ca1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcf7765fa5314ed230b6ca5bbfe2cf07e8e64872996d9a08a0c20734babd3b0ea",
      "signature": {
        "s": "0x5034499ac7920c1d4ca922723ac05e8aedc5e6e85ea67c397fd8d7f337d0989c",
        "r": "0xf2c542171d2da1345ed7a6910ac2e7e5b449f95ff4449ae56ea6277abd1fb859",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x244c571f3fcbadc4df02cfe5fb86b609cb71d1e8132bab0d68cde73392f454df",
      "signature": {
        "s": "0x26fcf7be1754d9b666c738d6f9434e7911add6909d56d772545ab9455acb50aa",
        "r": "0x9ef40734326c4bc1ff77a84fed76b0d0577552dc9f060b3c258cd2e4f86a7b94",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7329",
    "total": "7329"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7329",
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
            "amount": "630745"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "7"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3MGUyYzlhZS05ZmUxLTVhMjItYWMyOS1mZjkxOWE4NTEwMTgifQ==",
    "nonce": 1547,
    "balances": {
      "current": "10000001452771374",
      "previous": "10000001452778710"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfc20588b7a8f4ff347831574b7eb46649489707c",
    "nonce": 20,
    "balances": {
      "current": "7329",
      "previous": "0"
    }
  },
  "blockNumber": "10114532",
  "created": "2020-05-22T08:10:24.527Z",
  "updated": "2020-05-22T08:10:24.600Z",
  "id": "5ec788f0b0c6090011d5aad3"
}
```
* *stageAmount*: `7329`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000001ca100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001ca10000000000000000000000000000000000000000000000000000000000001ca1cf7765fa5314ed230b6ca5bbfe2cf07e8e64872996d9a08a0c20734babd3b0eaf2c542171d2da1345ed7a6910ac2e7e5b449f95ff4449ae56ea6277abd1fb8595034499ac7920c1d4ca922723ac05e8aedc5e6e85ea67c397fd8d7f337d0989c000000000000000000000000000000000000000000000000000000000000001b244c571f3fcbadc4df02cfe5fb86b609cb71d1e8132bab0d68cde73392f454df9ef40734326c4bc1ff77a84fed76b0d0577552dc9f060b3c258cd2e4f86a7b9426fcf7be1754d9b666c738d6f9434e7911add6909d56d772545ab9455acb50aa000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000060b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c658882e000000000000000000000000000000000000000000000000002386f2c658a4d600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000007000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099fd900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d475579597a6c685a5330355a6d55784c5456684d6a497459574d794f53316d5a6a6b784f5745344e5445774d54676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000fc20588b7a8f4ff347831574b7eb46649489707c0000000000000000000000000000000000000000000000000000000000001ca1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcf7765fa5314ed230b6ca5bbfe2cf07e8e64872996d9a08a0c20734babd3b0ea",
      "signature": {
        "s": "0x5034499ac7920c1d4ca922723ac05e8aedc5e6e85ea67c397fd8d7f337d0989c",
        "r": "0xf2c542171d2da1345ed7a6910ac2e7e5b449f95ff4449ae56ea6277abd1fb859",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x244c571f3fcbadc4df02cfe5fb86b609cb71d1e8132bab0d68cde73392f454df",
      "signature": {
        "s": "0x26fcf7be1754d9b666c738d6f9434e7911add6909d56d772545ab9455acb50aa",
        "r": "0x9ef40734326c4bc1ff77a84fed76b0d0577552dc9f060b3c258cd2e4f86a7b94",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7329",
    "total": "7329"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7329",
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
            "amount": "630745"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "7"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3MGUyYzlhZS05ZmUxLTVhMjItYWMyOS1mZjkxOWE4NTEwMTgifQ==",
    "nonce": 1547,
    "balances": {
      "current": "10000001452771374",
      "previous": "10000001452778710"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfc20588b7a8f4ff347831574b7eb46649489707c",
    "nonce": 20,
    "balances": {
      "current": "7329",
      "previous": "0"
    }
  },
  "blockNumber": "10114532",
  "created": "2020-05-22T08:10:24.527Z",
  "updated": "2020-05-22T08:10:24.600Z",
  "id": "5ec788f0b0c6090011d5aad3"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000001ca10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7329`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``