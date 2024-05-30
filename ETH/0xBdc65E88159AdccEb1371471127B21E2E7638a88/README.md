# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xBdc65E88159AdccEb1371471127B21E2E7638a88`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000070bc00000000000000000000000000000000000000000000000000000000000070bc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000070bc00000000000000000000000000000000000000000000000000000000000070bcc38f8e5a4368f27c629b93f457c1149d425082cf3706a7b60b18061391e897c783a7f0a8ebbadc03cb1018acfc04c97400cc3d09e96af705e5bcb755c4fec542453d953f19c71d2c4a294dd2ac2a3ea1752db34e636e8425e7d7b166b7c07ac7000000000000000000000000000000000000000000000000000000000000001c40eb4fd929daf867e88b0e3d7c44d2fd3eb1eebb35f47809773a7719b4e081fb06a8d0945ec835f2f769ce8d3447db7c243af4dc161c682de55e61f2d1bea627721945bf4f7836d43693288b5ef355047cc5d5006a866582e62294803265d46d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000026e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb0cc8f4000000000000000000000000000000000000000000000000002386f2cb0d39cc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086ce600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a6b334f544d305953307959575a6a4c54566c4e6a59744f446b315a53316a4d546c6a4f4455304e47597a4f44516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000bdc65e88159adcceb1371471127b21e2e7638a8800000000000000000000000000000000000000000000000000000000000070bc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc38f8e5a4368f27c629b93f457c1149d425082cf3706a7b60b18061391e897c7",
      "signature": {
        "s": "0x453d953f19c71d2c4a294dd2ac2a3ea1752db34e636e8425e7d7b166b7c07ac7",
        "r": "0x83a7f0a8ebbadc03cb1018acfc04c97400cc3d09e96af705e5bcb755c4fec542",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x40eb4fd929daf867e88b0e3d7c44d2fd3eb1eebb35f47809773a7719b4e081fb",
      "signature": {
        "s": "0x721945bf4f7836d43693288b5ef355047cc5d5006a866582e62294803265d46d",
        "r": "0x06a8d0945ec835f2f769ce8d3447db7c243af4dc161c682de55e61f2d1bea627",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "28860",
    "total": "28860"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "28860",
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
            "amount": "552166"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "28"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZjk3OTM0YS0yYWZjLTVlNjYtODk1ZS1jMTljODU0NGYzODQifQ==",
    "nonce": 622,
    "balances": {
      "current": "10000001531693300",
      "previous": "10000001531722188"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbdc65e88159adcceb1371471127b21e2e7638a88",
    "nonce": 20,
    "balances": {
      "current": "28860",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:26.676Z",
  "updated": "2020-05-22T08:03:26.750Z",
  "id": "5ec7874e005df800101bc2e2"
}
```
* *stageAmount*: `28860`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000070bc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000070bc00000000000000000000000000000000000000000000000000000000000070bcc38f8e5a4368f27c629b93f457c1149d425082cf3706a7b60b18061391e897c783a7f0a8ebbadc03cb1018acfc04c97400cc3d09e96af705e5bcb755c4fec542453d953f19c71d2c4a294dd2ac2a3ea1752db34e636e8425e7d7b166b7c07ac7000000000000000000000000000000000000000000000000000000000000001c40eb4fd929daf867e88b0e3d7c44d2fd3eb1eebb35f47809773a7719b4e081fb06a8d0945ec835f2f769ce8d3447db7c243af4dc161c682de55e61f2d1bea627721945bf4f7836d43693288b5ef355047cc5d5006a866582e62294803265d46d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000026e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb0cc8f4000000000000000000000000000000000000000000000000002386f2cb0d39cc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086ce600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a6b334f544d305953307959575a6a4c54566c4e6a59744f446b315a53316a4d546c6a4f4455304e47597a4f44516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000bdc65e88159adcceb1371471127b21e2e7638a8800000000000000000000000000000000000000000000000000000000000070bc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc38f8e5a4368f27c629b93f457c1149d425082cf3706a7b60b18061391e897c7",
      "signature": {
        "s": "0x453d953f19c71d2c4a294dd2ac2a3ea1752db34e636e8425e7d7b166b7c07ac7",
        "r": "0x83a7f0a8ebbadc03cb1018acfc04c97400cc3d09e96af705e5bcb755c4fec542",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x40eb4fd929daf867e88b0e3d7c44d2fd3eb1eebb35f47809773a7719b4e081fb",
      "signature": {
        "s": "0x721945bf4f7836d43693288b5ef355047cc5d5006a866582e62294803265d46d",
        "r": "0x06a8d0945ec835f2f769ce8d3447db7c243af4dc161c682de55e61f2d1bea627",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "28860",
    "total": "28860"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "28860",
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
            "amount": "552166"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "28"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZjk3OTM0YS0yYWZjLTVlNjYtODk1ZS1jMTljODU0NGYzODQifQ==",
    "nonce": 622,
    "balances": {
      "current": "10000001531693300",
      "previous": "10000001531722188"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbdc65e88159adcceb1371471127b21e2e7638a88",
    "nonce": 20,
    "balances": {
      "current": "28860",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:26.676Z",
  "updated": "2020-05-22T08:03:26.750Z",
  "id": "5ec7874e005df800101bc2e2"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000070bc0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `28860`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``