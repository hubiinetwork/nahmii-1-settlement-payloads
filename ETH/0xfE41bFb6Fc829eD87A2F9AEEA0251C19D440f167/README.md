# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xfE41bFb6Fc829eD87A2F9AEEA0251C19D440f167`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000479200000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000479200000000000000000000000000000000000000000000000000000000000047923b412417c1e0aad4544869792d93a306c4fa32eb59482649af340f4f0d2a3cb17b2622ef46080c4faea2ecb16b0454ebfcd59e791c3f3ad8af1ee4741af3ae2a10dbe5b8e55e20168e68365d77da7b674d969977e9555cf7ab72ba81dfd60c09000000000000000000000000000000000000000000000000000000000000001b59ea049c6b169b717c15a81048df42f1123e4d157246f2d161e5acff798db1ca3edc2cc3ba411ed96bf61111e8f83c6570b37ded6bd172566894f7318096da8a3186f261b238cbfa571f40cb44ac672d540fea50aa430543e3ecd94acef211bf000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f0000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007eb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c392e5d5000000000000000000000000000000000000000000000000002386f2c3932d7900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a54a900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493159575a684e544a694e6930354f545a684c5455785a5751745954466c4d6930324f54677a4d474e6b5a54566d4f54676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000fe41bfb6fc829ed87a2f9aeea0251c19d440f1670000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3b412417c1e0aad4544869792d93a306c4fa32eb59482649af340f4f0d2a3cb1",
      "signature": {
        "s": "0x10dbe5b8e55e20168e68365d77da7b674d969977e9555cf7ab72ba81dfd60c09",
        "r": "0x7b2622ef46080c4faea2ecb16b0454ebfcd59e791c3f3ad8af1ee4741af3ae2a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x59ea049c6b169b717c15a81048df42f1123e4d157246f2d161e5acff798db1ca",
      "signature": {
        "s": "0x3186f261b238cbfa571f40cb44ac672d540fea50aa430543e3ecd94acef211bf",
        "r": "0x3edc2cc3ba411ed96bf61111e8f83c6570b37ded6bd172566894f7318096da8a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18322",
    "total": "18322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18322",
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
            "amount": "677033"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1YWZhNTJiNi05OTZhLTUxZWQtYTFlMi02OTgzMGNkZTVmOTgifQ==",
    "nonce": 2027,
    "balances": {
      "current": "10000001406264789",
      "previous": "10000001406283129"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe41bfb6fc829ed87a2f9aeea0251c19d440f167",
    "nonce": 20,
    "balances": {
      "current": "18322",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:13:52.234Z",
  "updated": "2020-05-22T08:13:52.303Z",
  "id": "5ec789c0005df800101bc4cb"
}
```
* *stageAmount*: `18322`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000479200000000000000000000000000000000000000000000000000000000000047923b412417c1e0aad4544869792d93a306c4fa32eb59482649af340f4f0d2a3cb17b2622ef46080c4faea2ecb16b0454ebfcd59e791c3f3ad8af1ee4741af3ae2a10dbe5b8e55e20168e68365d77da7b674d969977e9555cf7ab72ba81dfd60c09000000000000000000000000000000000000000000000000000000000000001b59ea049c6b169b717c15a81048df42f1123e4d157246f2d161e5acff798db1ca3edc2cc3ba411ed96bf61111e8f83c6570b37ded6bd172566894f7318096da8a3186f261b238cbfa571f40cb44ac672d540fea50aa430543e3ecd94acef211bf000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f0000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007eb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c392e5d5000000000000000000000000000000000000000000000000002386f2c3932d7900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a54a900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493159575a684e544a694e6930354f545a684c5455785a5751745954466c4d6930324f54677a4d474e6b5a54566d4f54676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000fe41bfb6fc829ed87a2f9aeea0251c19d440f1670000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3b412417c1e0aad4544869792d93a306c4fa32eb59482649af340f4f0d2a3cb1",
      "signature": {
        "s": "0x10dbe5b8e55e20168e68365d77da7b674d969977e9555cf7ab72ba81dfd60c09",
        "r": "0x7b2622ef46080c4faea2ecb16b0454ebfcd59e791c3f3ad8af1ee4741af3ae2a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x59ea049c6b169b717c15a81048df42f1123e4d157246f2d161e5acff798db1ca",
      "signature": {
        "s": "0x3186f261b238cbfa571f40cb44ac672d540fea50aa430543e3ecd94acef211bf",
        "r": "0x3edc2cc3ba411ed96bf61111e8f83c6570b37ded6bd172566894f7318096da8a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18322",
    "total": "18322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18322",
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
            "amount": "677033"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1YWZhNTJiNi05OTZhLTUxZWQtYTFlMi02OTgzMGNkZTVmOTgifQ==",
    "nonce": 2027,
    "balances": {
      "current": "10000001406264789",
      "previous": "10000001406283129"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe41bfb6fc829ed87a2f9aeea0251c19d440f167",
    "nonce": 20,
    "balances": {
      "current": "18322",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:13:52.234Z",
  "updated": "2020-05-22T08:13:52.303Z",
  "id": "5ec789c0005df800101bc4cb"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18322`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``