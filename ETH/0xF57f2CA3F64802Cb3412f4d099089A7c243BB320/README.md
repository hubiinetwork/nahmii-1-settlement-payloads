# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF57f2CA3F64802Cb3412f4d099089A7c243BB320`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000338c000000000000000000000000000000000000000000000000000000000000338c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000338c000000000000000000000000000000000000000000000000000000000000338ceab98895b062ffe13233c4d6cf7ba97a666d3c01aa5998980553621315518b99ad47062cabb5154035dadb167b8c986e69911b13eff795fc891a4861f482ae193c37a614a17e674f201be152839192302f70c2822ff80cb08b6ca4f643f13639000000000000000000000000000000000000000000000000000000000000001b4a58ea3787061f3963719d75d5c5b6430894638856f054b3ea824b73580ff8a52c4dfb4841983cd715f7c3262bbf9090703fc6376d67dca7b85e1cf75c1505761e92580d6a179bb13ea79e5851af1ca63f39687e87b88a5861f9ba0c652594b3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000087600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc8b6648000000000000000000000000000000000000000000000000002386f2bc8b99e100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c20af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d5451324d4463314f5331684e4749314c5455334f5445744f47597a5969307759574d335a5755324e6a466c4d32496966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000f57f2ca3f64802cb3412f4d099089a7c243bb320000000000000000000000000000000000000000000000000000000000000338c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeab98895b062ffe13233c4d6cf7ba97a666d3c01aa5998980553621315518b99",
      "signature": {
        "s": "0x3c37a614a17e674f201be152839192302f70c2822ff80cb08b6ca4f643f13639",
        "r": "0xad47062cabb5154035dadb167b8c986e69911b13eff795fc891a4861f482ae19",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4a58ea3787061f3963719d75d5c5b6430894638856f054b3ea824b73580ff8a5",
      "signature": {
        "s": "0x1e92580d6a179bb13ea79e5851af1ca63f39687e87b88a5861f9ba0c652594b3",
        "r": "0x2c4dfb4841983cd715f7c3262bbf9090703fc6376d67dca7b85e1cf75c150576",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "13196",
    "total": "13196"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13196",
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
            "amount": "794799"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "13"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMTQ2MDc1OS1hNGI1LTU3OTEtOGYzYi0wYWM3ZWU2NjFlM2IifQ==",
    "nonce": 2166,
    "balances": {
      "current": "10000001288332872",
      "previous": "10000001288346081"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf57f2ca3f64802cb3412f4d099089a7c243bb320",
    "nonce": 13,
    "balances": {
      "current": "13196",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:46.054Z",
  "updated": "2020-05-22T08:14:46.122Z",
  "id": "5ec789f6e5756b00111b8234"
}
```
* *stageAmount*: `13196`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000338c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000338c000000000000000000000000000000000000000000000000000000000000338ceab98895b062ffe13233c4d6cf7ba97a666d3c01aa5998980553621315518b99ad47062cabb5154035dadb167b8c986e69911b13eff795fc891a4861f482ae193c37a614a17e674f201be152839192302f70c2822ff80cb08b6ca4f643f13639000000000000000000000000000000000000000000000000000000000000001b4a58ea3787061f3963719d75d5c5b6430894638856f054b3ea824b73580ff8a52c4dfb4841983cd715f7c3262bbf9090703fc6376d67dca7b85e1cf75c1505761e92580d6a179bb13ea79e5851af1ca63f39687e87b88a5861f9ba0c652594b3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000087600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc8b6648000000000000000000000000000000000000000000000000002386f2bc8b99e100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c20af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d5451324d4463314f5331684e4749314c5455334f5445744f47597a5969307759574d335a5755324e6a466c4d32496966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000f57f2ca3f64802cb3412f4d099089a7c243bb320000000000000000000000000000000000000000000000000000000000000338c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeab98895b062ffe13233c4d6cf7ba97a666d3c01aa5998980553621315518b99",
      "signature": {
        "s": "0x3c37a614a17e674f201be152839192302f70c2822ff80cb08b6ca4f643f13639",
        "r": "0xad47062cabb5154035dadb167b8c986e69911b13eff795fc891a4861f482ae19",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4a58ea3787061f3963719d75d5c5b6430894638856f054b3ea824b73580ff8a5",
      "signature": {
        "s": "0x1e92580d6a179bb13ea79e5851af1ca63f39687e87b88a5861f9ba0c652594b3",
        "r": "0x2c4dfb4841983cd715f7c3262bbf9090703fc6376d67dca7b85e1cf75c150576",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "13196",
    "total": "13196"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13196",
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
            "amount": "794799"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "13"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMTQ2MDc1OS1hNGI1LTU3OTEtOGYzYi0wYWM3ZWU2NjFlM2IifQ==",
    "nonce": 2166,
    "balances": {
      "current": "10000001288332872",
      "previous": "10000001288346081"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf57f2ca3f64802cb3412f4d099089a7c243bb320",
    "nonce": 13,
    "balances": {
      "current": "13196",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:46.054Z",
  "updated": "2020-05-22T08:14:46.122Z",
  "id": "5ec789f6e5756b00111b8234"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000338c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13196`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``