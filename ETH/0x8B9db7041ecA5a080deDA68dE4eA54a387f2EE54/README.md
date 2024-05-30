# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8B9db7041ecA5a080deDA68dE4eA54a387f2EE54`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000479300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000479344dcb54a60fbd4cae4da4525f83d6d4c2e9afca3364fab8fc302860918f9557018e084f60c5b24547c5230c419789b7ac097206799702801745339af88c7464d3527680245d98fb6385c03a5a24b8d51776575476da916d141d4b23bf480a94b000000000000000000000000000000000000000000000000000000000000001c3e9a550aba0f332993ed13be1c51d7de81f47648c69facf2fb62bd4bba4572828e5b7401ce6a97356c92fc988f8a92d8254e7ed5934bcc097d4a8aab7844082f61144eee1c5e4188ad33364b48721f738b318bf252214e9c3704c8ec70f2d5a3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000044a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c85dea72000000000000000000000000000000000000000000000000002386f2c85e321700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000012000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000091c0d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6a566a4d6a6b77597930794d7a45354c54566d4e446b74596a64685a43316c4d6d4d314f574a6b4d446b7a596d496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000008b9db7041eca5a080deda68de4ea54a387f2ee540000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x44dcb54a60fbd4cae4da4525f83d6d4c2e9afca3364fab8fc302860918f95570",
      "signature": {
        "s": "0x3527680245d98fb6385c03a5a24b8d51776575476da916d141d4b23bf480a94b",
        "r": "0x18e084f60c5b24547c5230c419789b7ac097206799702801745339af88c7464d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3e9a550aba0f332993ed13be1c51d7de81f47648c69facf2fb62bd4bba457282",
      "signature": {
        "s": "0x61144eee1c5e4188ad33364b48721f738b318bf252214e9c3704c8ec70f2d5a3",
        "r": "0x8e5b7401ce6a97356c92fc988f8a92d8254e7ed5934bcc097d4a8aab7844082f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
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
            "amount": "597005"
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
    "data": "eyJyZWYiOiIxMjVjMjkwYy0yMzE5LTVmNDktYjdhZC1lMmM1OWJkMDkzYmIifQ==",
    "nonce": 1098,
    "balances": {
      "current": "10000001486678642",
      "previous": "10000001486696983"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8b9db7041eca5a080deda68de4ea54a387f2ee54",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114519",
  "created": "2020-05-22T08:06:48.893Z",
  "updated": "2020-05-22T08:06:49.553Z",
  "id": "5ec78818b0c6090011d5aa38"
}
```
* *stageAmount*: `18323`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000479300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000479344dcb54a60fbd4cae4da4525f83d6d4c2e9afca3364fab8fc302860918f9557018e084f60c5b24547c5230c419789b7ac097206799702801745339af88c7464d3527680245d98fb6385c03a5a24b8d51776575476da916d141d4b23bf480a94b000000000000000000000000000000000000000000000000000000000000001c3e9a550aba0f332993ed13be1c51d7de81f47648c69facf2fb62bd4bba4572828e5b7401ce6a97356c92fc988f8a92d8254e7ed5934bcc097d4a8aab7844082f61144eee1c5e4188ad33364b48721f738b318bf252214e9c3704c8ec70f2d5a3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000044a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c85dea72000000000000000000000000000000000000000000000000002386f2c85e321700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000012000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000091c0d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6a566a4d6a6b77597930794d7a45354c54566d4e446b74596a64685a43316c4d6d4d314f574a6b4d446b7a596d496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000008b9db7041eca5a080deda68de4ea54a387f2ee540000000000000000000000000000000000000000000000000000000000004793000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x44dcb54a60fbd4cae4da4525f83d6d4c2e9afca3364fab8fc302860918f95570",
      "signature": {
        "s": "0x3527680245d98fb6385c03a5a24b8d51776575476da916d141d4b23bf480a94b",
        "r": "0x18e084f60c5b24547c5230c419789b7ac097206799702801745339af88c7464d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3e9a550aba0f332993ed13be1c51d7de81f47648c69facf2fb62bd4bba457282",
      "signature": {
        "s": "0x61144eee1c5e4188ad33364b48721f738b318bf252214e9c3704c8ec70f2d5a3",
        "r": "0x8e5b7401ce6a97356c92fc988f8a92d8254e7ed5934bcc097d4a8aab7844082f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18323",
    "total": "18323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18323",
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
            "amount": "597005"
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
    "data": "eyJyZWYiOiIxMjVjMjkwYy0yMzE5LTVmNDktYjdhZC1lMmM1OWJkMDkzYmIifQ==",
    "nonce": 1098,
    "balances": {
      "current": "10000001486678642",
      "previous": "10000001486696983"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8b9db7041eca5a080deda68de4ea54a387f2ee54",
    "nonce": 20,
    "balances": {
      "current": "18323",
      "previous": "0"
    }
  },
  "blockNumber": "10114519",
  "created": "2020-05-22T08:06:48.893Z",
  "updated": "2020-05-22T08:06:49.553Z",
  "id": "5ec78818b0c6090011d5aa38"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047930000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18323`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``