# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3eAF8Bea59069be3c9626c9f8352F6F054d8925a`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000615800000000000000000000000000000000000000000000000000000000000061580000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000615800000000000000000000000000000000000000000000000000000000000061584c39c05f517dc0c5a2a34041ad0dc40cc35d1a5c305e25fa324662f9c8bc2802ae10427e1ef87822b95173aedbb7811e0325d6cf8e765ff4715178bf12b8b4c068e718f06061822a4fb0bb33cf78c9d939460b8f15ae97bb893a5f3df9cd1168000000000000000000000000000000000000000000000000000000000000001cd0a1476140562724a075cac4cb64470fb37db9adf4235927b20240d094d066f221aa3be1e7958dbaa54aad85ef7ddf8f7f548ac9620433c593f310e987861a234dfa83697f283694a52dcbe1106bfc6064b1389d0a982034a6b50c6c4fa97c0e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004aa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7fe7ed5000000000000000000000000000000000000000000000000002386f2c7fee04500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009345f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d3249314f4751325a43307a4e6a4a6b4c5455304d6a55744f574d335a6930784f4745314e6a4d79597a67324f444d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000003eaf8bea59069be3c9626c9f8352f6f054d8925a0000000000000000000000000000000000000000000000000000000000006158000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4c39c05f517dc0c5a2a34041ad0dc40cc35d1a5c305e25fa324662f9c8bc2802",
      "signature": {
        "s": "0x68e718f06061822a4fb0bb33cf78c9d939460b8f15ae97bb893a5f3df9cd1168",
        "r": "0xae10427e1ef87822b95173aedbb7811e0325d6cf8e765ff4715178bf12b8b4c0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd0a1476140562724a075cac4cb64470fb37db9adf4235927b20240d094d066f2",
      "signature": {
        "s": "0x4dfa83697f283694a52dcbe1106bfc6064b1389d0a982034a6b50c6c4fa97c0e",
        "r": "0x21aa3be1e7958dbaa54aad85ef7ddf8f7f548ac9620433c593f310e987861a23",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "24920",
    "total": "24920"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24920",
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
            "amount": "603231"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "24"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5M2I1OGQ2ZC0zNjJkLTU0MjUtOWM3Zi0xOGE1NjMyYzg2ODMifQ==",
    "nonce": 1194,
    "balances": {
      "current": "10000001480425173",
      "previous": "10000001480450117"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3eaf8bea59069be3c9626c9f8352f6f054d8925a",
    "nonce": 20,
    "balances": {
      "current": "24920",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:31.810Z",
  "updated": "2020-05-22T08:07:31.887Z",
  "id": "5ec78843e5756b00111b80f7"
}
```
* *stageAmount*: `24920`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000061580000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000615800000000000000000000000000000000000000000000000000000000000061584c39c05f517dc0c5a2a34041ad0dc40cc35d1a5c305e25fa324662f9c8bc2802ae10427e1ef87822b95173aedbb7811e0325d6cf8e765ff4715178bf12b8b4c068e718f06061822a4fb0bb33cf78c9d939460b8f15ae97bb893a5f3df9cd1168000000000000000000000000000000000000000000000000000000000000001cd0a1476140562724a075cac4cb64470fb37db9adf4235927b20240d094d066f221aa3be1e7958dbaa54aad85ef7ddf8f7f548ac9620433c593f310e987861a234dfa83697f283694a52dcbe1106bfc6064b1389d0a982034a6b50c6c4fa97c0e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004aa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7fe7ed5000000000000000000000000000000000000000000000000002386f2c7fee04500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009345f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d3249314f4751325a43307a4e6a4a6b4c5455304d6a55744f574d335a6930784f4745314e6a4d79597a67324f444d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000003eaf8bea59069be3c9626c9f8352f6f054d8925a0000000000000000000000000000000000000000000000000000000000006158000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4c39c05f517dc0c5a2a34041ad0dc40cc35d1a5c305e25fa324662f9c8bc2802",
      "signature": {
        "s": "0x68e718f06061822a4fb0bb33cf78c9d939460b8f15ae97bb893a5f3df9cd1168",
        "r": "0xae10427e1ef87822b95173aedbb7811e0325d6cf8e765ff4715178bf12b8b4c0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd0a1476140562724a075cac4cb64470fb37db9adf4235927b20240d094d066f2",
      "signature": {
        "s": "0x4dfa83697f283694a52dcbe1106bfc6064b1389d0a982034a6b50c6c4fa97c0e",
        "r": "0x21aa3be1e7958dbaa54aad85ef7ddf8f7f548ac9620433c593f310e987861a23",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "24920",
    "total": "24920"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24920",
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
            "amount": "603231"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "24"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5M2I1OGQ2ZC0zNjJkLTU0MjUtOWM3Zi0xOGE1NjMyYzg2ODMifQ==",
    "nonce": 1194,
    "balances": {
      "current": "10000001480425173",
      "previous": "10000001480450117"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3eaf8bea59069be3c9626c9f8352f6f054d8925a",
    "nonce": 20,
    "balances": {
      "current": "24920",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:31.810Z",
  "updated": "2020-05-22T08:07:31.887Z",
  "id": "5ec78843e5756b00111b80f7"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000061580000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `24920`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``