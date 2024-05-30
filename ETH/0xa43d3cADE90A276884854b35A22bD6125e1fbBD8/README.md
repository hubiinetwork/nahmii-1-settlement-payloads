# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa43d3cADE90A276884854b35A22bD6125e1fbBD8`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000004c5f7000000000000000000000000000000000000000000000000000000000004c5f70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000004c5f7000000000000000000000000000000000000000000000000000000000004c5f73f2fd61cf692ba78273da545c84f9c593efe5cc014883c40605047e2e8831090349cb09ba912a156115bf0d6fc51f19eab78a49a7ae377dae9162a439a785a716668278e08902f9d7d140b226fc19734e45cc86c24c5703f15a262cd1b3b210d000000000000000000000000000000000000000000000000000000000000001b02b7d8cfa747cc792ac12c61c31a31116e65bc2e56f5c8eb00aed17a81f045767983cc383f5299cac7b8e9cf2a92496a28588d1f02829da7bee32fea75aaeb10669a9e93106748940af4566ecb75c0ab19dccd76e131e9d42ec158bd935875d8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000008200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d259648e000000000000000000000000000000000000000000000000002386f2d25e2bbd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000138000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000068f8c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f57517a4d444979596930314d7a64694c5455314d574574596d466d5a5330785932466d4d6a59305a5445774e7a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000a43d3cade90a276884854b35a22bd6125e1fbbd8000000000000000000000000000000000000000000000000000000000004c5f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f2fd61cf692ba78273da545c84f9c593efe5cc014883c40605047e2e8831090",
      "signature": {
        "s": "0x6668278e08902f9d7d140b226fc19734e45cc86c24c5703f15a262cd1b3b210d",
        "r": "0x349cb09ba912a156115bf0d6fc51f19eab78a49a7ae377dae9162a439a785a71",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x02b7d8cfa747cc792ac12c61c31a31116e65bc2e56f5c8eb00aed17a81f04576",
      "signature": {
        "s": "0x669a9e93106748940af4566ecb75c0ab19dccd76e131e9d42ec158bd935875d8",
        "r": "0x7983cc383f5299cac7b8e9cf2a92496a28588d1f02829da7bee32fea75aaeb10",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "312823",
    "total": "312823"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "312823",
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
            "amount": "429964"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "312"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OWQzMDIyYi01MzdiLTU1MWEtYmFmZS0xY2FmMjY0ZTEwNzMifQ==",
    "nonce": 130,
    "balances": {
      "current": "10000001654154382",
      "previous": "10000001654467517"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa43d3cade90a276884854b35a22bd6125e1fbbd8",
    "nonce": 13,
    "balances": {
      "current": "312823",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:44.889Z",
  "updated": "2020-05-22T07:59:44.966Z",
  "id": "5ec78670005df800101bc23c"
}
```
* *stageAmount*: `312823`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000004c5f70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000004c5f7000000000000000000000000000000000000000000000000000000000004c5f73f2fd61cf692ba78273da545c84f9c593efe5cc014883c40605047e2e8831090349cb09ba912a156115bf0d6fc51f19eab78a49a7ae377dae9162a439a785a716668278e08902f9d7d140b226fc19734e45cc86c24c5703f15a262cd1b3b210d000000000000000000000000000000000000000000000000000000000000001b02b7d8cfa747cc792ac12c61c31a31116e65bc2e56f5c8eb00aed17a81f045767983cc383f5299cac7b8e9cf2a92496a28588d1f02829da7bee32fea75aaeb10669a9e93106748940af4566ecb75c0ab19dccd76e131e9d42ec158bd935875d8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000008200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d259648e000000000000000000000000000000000000000000000000002386f2d25e2bbd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000138000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000068f8c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f57517a4d444979596930314d7a64694c5455314d574574596d466d5a5330785932466d4d6a59305a5445774e7a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000a43d3cade90a276884854b35a22bd6125e1fbbd8000000000000000000000000000000000000000000000000000000000004c5f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f2fd61cf692ba78273da545c84f9c593efe5cc014883c40605047e2e8831090",
      "signature": {
        "s": "0x6668278e08902f9d7d140b226fc19734e45cc86c24c5703f15a262cd1b3b210d",
        "r": "0x349cb09ba912a156115bf0d6fc51f19eab78a49a7ae377dae9162a439a785a71",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x02b7d8cfa747cc792ac12c61c31a31116e65bc2e56f5c8eb00aed17a81f04576",
      "signature": {
        "s": "0x669a9e93106748940af4566ecb75c0ab19dccd76e131e9d42ec158bd935875d8",
        "r": "0x7983cc383f5299cac7b8e9cf2a92496a28588d1f02829da7bee32fea75aaeb10",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "312823",
    "total": "312823"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "312823",
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
            "amount": "429964"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "312"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OWQzMDIyYi01MzdiLTU1MWEtYmFmZS0xY2FmMjY0ZTEwNzMifQ==",
    "nonce": 130,
    "balances": {
      "current": "10000001654154382",
      "previous": "10000001654467517"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa43d3cade90a276884854b35a22bd6125e1fbbd8",
    "nonce": 13,
    "balances": {
      "current": "312823",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:44.889Z",
  "updated": "2020-05-22T07:59:44.966Z",
  "id": "5ec78670005df800101bc23c"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000004c5f70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `312823`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``