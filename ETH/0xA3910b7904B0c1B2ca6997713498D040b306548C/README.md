# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA3910b7904B0c1B2ca6997713498D040b306548C`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000008e416000000000000000000000000000000000000000000000000000000000008e4160000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000008e416000000000000000000000000000000000000000000000000000000000008e41670a151c8555eb904660cbd7973c88e3f8db151f2af3f829f6e722fa01eca0e21bd3f0d93d27dd3a196f51b91f0f83c1653d395bc62556388b8734718fe9cb43e5fc37cbfb4db3a41dd77f781b26f3751a466ae81f5e934d24cfc6546f2414e8b000000000000000000000000000000000000000000000000000000000000001c69e651f3fb39bc0106df0db1489dcdeaefa4c62f662e80583a8ace54dfccff3694c17778a96a09bf137e7a875d72975c0519a5ee4d55cc4ac4260048380d7df903a98e25ab8c19f76d86b679ba172716f714aac71ac8682cfcc6ecb3803b3cdd000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ea000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006e500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c507e060000000000000000000000000000000000000000000000000002386f2c510c6bc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000024600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009f5b200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a544d795a546332596930304e6a4e684c5455324e6d5174596d4d7a4e43307a4e7a67324e6d566b4d4749334e47516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a3910b7904b0c1b2ca6997713498d040b306548c000000000000000000000000000000000000000000000000000000000008e416000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x70a151c8555eb904660cbd7973c88e3f8db151f2af3f829f6e722fa01eca0e21",
      "signature": {
        "s": "0x5fc37cbfb4db3a41dd77f781b26f3751a466ae81f5e934d24cfc6546f2414e8b",
        "r": "0xbd3f0d93d27dd3a196f51b91f0f83c1653d395bc62556388b8734718fe9cb43e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x69e651f3fb39bc0106df0db1489dcdeaefa4c62f662e80583a8ace54dfccff36",
      "signature": {
        "s": "0x03a98e25ab8c19f76d86b679ba172716f714aac71ac8682cfcc6ecb3803b3cdd",
        "r": "0x94c17778a96a09bf137e7a875d72975c0519a5ee4d55cc4ac4260048380d7df9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "582678",
    "total": "582678"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "582678",
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
            "amount": "652722"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "582"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTMyZTc2Yi00NjNhLTU2NmQtYmMzNC0zNzg2NmVkMGI3NGQifQ==",
    "nonce": 1765,
    "balances": {
      "current": "10000001430708320",
      "previous": "10000001431291580"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa3910b7904b0c1b2ca6997713498d040b306548c",
    "nonce": 20,
    "balances": {
      "current": "582678",
      "previous": "0"
    }
  },
  "blockNumber": "10114538",
  "created": "2020-05-22T08:11:51.906Z",
  "updated": "2020-05-22T08:11:51.969Z",
  "id": "5ec78947e5756b00111b81ab"
}
```
* *stageAmount*: `582678`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000008e4160000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000008e416000000000000000000000000000000000000000000000000000000000008e41670a151c8555eb904660cbd7973c88e3f8db151f2af3f829f6e722fa01eca0e21bd3f0d93d27dd3a196f51b91f0f83c1653d395bc62556388b8734718fe9cb43e5fc37cbfb4db3a41dd77f781b26f3751a466ae81f5e934d24cfc6546f2414e8b000000000000000000000000000000000000000000000000000000000000001c69e651f3fb39bc0106df0db1489dcdeaefa4c62f662e80583a8ace54dfccff3694c17778a96a09bf137e7a875d72975c0519a5ee4d55cc4ac4260048380d7df903a98e25ab8c19f76d86b679ba172716f714aac71ac8682cfcc6ecb3803b3cdd000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ea000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006e500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c507e060000000000000000000000000000000000000000000000000002386f2c510c6bc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000024600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009f5b200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a544d795a546332596930304e6a4e684c5455324e6d5174596d4d7a4e43307a4e7a67324e6d566b4d4749334e47516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a3910b7904b0c1b2ca6997713498d040b306548c000000000000000000000000000000000000000000000000000000000008e416000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x70a151c8555eb904660cbd7973c88e3f8db151f2af3f829f6e722fa01eca0e21",
      "signature": {
        "s": "0x5fc37cbfb4db3a41dd77f781b26f3751a466ae81f5e934d24cfc6546f2414e8b",
        "r": "0xbd3f0d93d27dd3a196f51b91f0f83c1653d395bc62556388b8734718fe9cb43e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x69e651f3fb39bc0106df0db1489dcdeaefa4c62f662e80583a8ace54dfccff36",
      "signature": {
        "s": "0x03a98e25ab8c19f76d86b679ba172716f714aac71ac8682cfcc6ecb3803b3cdd",
        "r": "0x94c17778a96a09bf137e7a875d72975c0519a5ee4d55cc4ac4260048380d7df9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "582678",
    "total": "582678"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "582678",
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
            "amount": "652722"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "582"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTMyZTc2Yi00NjNhLTU2NmQtYmMzNC0zNzg2NmVkMGI3NGQifQ==",
    "nonce": 1765,
    "balances": {
      "current": "10000001430708320",
      "previous": "10000001431291580"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa3910b7904b0c1b2ca6997713498d040b306548c",
    "nonce": 20,
    "balances": {
      "current": "582678",
      "previous": "0"
    }
  },
  "blockNumber": "10114538",
  "created": "2020-05-22T08:11:51.906Z",
  "updated": "2020-05-22T08:11:51.969Z",
  "id": "5ec78947e5756b00111b81ab"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000008e4160000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `582678`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``