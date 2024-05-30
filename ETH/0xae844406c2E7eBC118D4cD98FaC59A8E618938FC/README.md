# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xae844406c2E7eBC118D4cD98FaC59A8E618938FC`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000024bb00000000000000000000000000000000000000000000000000000000000024bb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000024bb00000000000000000000000000000000000000000000000000000000000024bb49a7f02ac6a75a0fadd987ae8cc55c88586cb95fac98f46ba30855390ffc3f1191bd29d06c1bfb5886bea5e8ea658eb1f2922b319c9da8fa9cf2cf55f6e1850456099dbddfb6f62dd56ad203c9f584e9e09b476f57f01947c684ac6ee5c1a354000000000000000000000000000000000000000000000000000000000000001cfd2586c965d15f93ce3067dd83694790e9a746d11bb8e6f35d31592d02804eaae0908c5f32e3ca0da164d040abd2e1893e900649ac36fc6b672af6db09b4b8397e8a9874b83350ae65178b808893230cf500dbe8d7be6fcf9dbd6224fa60b985000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000008600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d24b039d000000000000000000000000000000000000000000000000002386f2d24b286100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006933900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a5759355a4759304f53316d5a6d55334c5455335a4749744f544d30596930354d32466c4f4445785a544d795a47456966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000ae844406c2e7ebc118d4cd98fac59a8e618938fc00000000000000000000000000000000000000000000000000000000000024bb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x49a7f02ac6a75a0fadd987ae8cc55c88586cb95fac98f46ba30855390ffc3f11",
      "signature": {
        "s": "0x56099dbddfb6f62dd56ad203c9f584e9e09b476f57f01947c684ac6ee5c1a354",
        "r": "0x91bd29d06c1bfb5886bea5e8ea658eb1f2922b319c9da8fa9cf2cf55f6e18504",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfd2586c965d15f93ce3067dd83694790e9a746d11bb8e6f35d31592d02804eaa",
      "signature": {
        "s": "0x7e8a9874b83350ae65178b808893230cf500dbe8d7be6fcf9dbd6224fa60b985",
        "r": "0xe0908c5f32e3ca0da164d040abd2e1893e900649ac36fc6b672af6db09b4b839",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9403",
    "total": "9403"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9403",
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
            "amount": "430905"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZWY5ZGY0OS1mZmU3LTU3ZGItOTM0Yi05M2FlODExZTMyZGEifQ==",
    "nonce": 134,
    "balances": {
      "current": "10000001653212061",
      "previous": "10000001653221473"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xae844406c2e7ebc118d4cd98fac59a8e618938fc",
    "nonce": 19,
    "balances": {
      "current": "9403",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:47.739Z",
  "updated": "2020-05-22T07:59:47.834Z",
  "id": "5ec78673b0c6090011d5a902"
}
```
* *stageAmount*: `9403`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000024bb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000024bb00000000000000000000000000000000000000000000000000000000000024bb49a7f02ac6a75a0fadd987ae8cc55c88586cb95fac98f46ba30855390ffc3f1191bd29d06c1bfb5886bea5e8ea658eb1f2922b319c9da8fa9cf2cf55f6e1850456099dbddfb6f62dd56ad203c9f584e9e09b476f57f01947c684ac6ee5c1a354000000000000000000000000000000000000000000000000000000000000001cfd2586c965d15f93ce3067dd83694790e9a746d11bb8e6f35d31592d02804eaae0908c5f32e3ca0da164d040abd2e1893e900649ac36fc6b672af6db09b4b8397e8a9874b83350ae65178b808893230cf500dbe8d7be6fcf9dbd6224fa60b985000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000008600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d24b039d000000000000000000000000000000000000000000000000002386f2d24b286100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006933900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a5759355a4759304f53316d5a6d55334c5455335a4749744f544d30596930354d32466c4f4445785a544d795a47456966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000ae844406c2e7ebc118d4cd98fac59a8e618938fc00000000000000000000000000000000000000000000000000000000000024bb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x49a7f02ac6a75a0fadd987ae8cc55c88586cb95fac98f46ba30855390ffc3f11",
      "signature": {
        "s": "0x56099dbddfb6f62dd56ad203c9f584e9e09b476f57f01947c684ac6ee5c1a354",
        "r": "0x91bd29d06c1bfb5886bea5e8ea658eb1f2922b319c9da8fa9cf2cf55f6e18504",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfd2586c965d15f93ce3067dd83694790e9a746d11bb8e6f35d31592d02804eaa",
      "signature": {
        "s": "0x7e8a9874b83350ae65178b808893230cf500dbe8d7be6fcf9dbd6224fa60b985",
        "r": "0xe0908c5f32e3ca0da164d040abd2e1893e900649ac36fc6b672af6db09b4b839",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9403",
    "total": "9403"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9403",
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
            "amount": "430905"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZWY5ZGY0OS1mZmU3LTU3ZGItOTM0Yi05M2FlODExZTMyZGEifQ==",
    "nonce": 134,
    "balances": {
      "current": "10000001653212061",
      "previous": "10000001653221473"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xae844406c2e7ebc118d4cd98fac59a8e618938fc",
    "nonce": 19,
    "balances": {
      "current": "9403",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:47.739Z",
  "updated": "2020-05-22T07:59:47.834Z",
  "id": "5ec78673b0c6090011d5a902"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000024bb0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9403`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``