# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8768f846C2d7C1C76c2719062C39fc07fEd0C9D8`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000019de2cada000000000000000000000000000000000000000000000000000000019de2cada000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000019de2cada000000000000000000000000000000000000000000000000000000019de2cada02b1984ed650b98c323eb1e2c9868ac17204ac5c9bf198204f781a33436233b71149d2609798706105d18112dab0d13951d3ff7139712a9d75a0ce2bc25a97fc4ff5623b854464e6d752efcf6991c6c1a3f73177ecac201ca2146d24733dc4bc000000000000000000000000000000000000000000000000000000000000001bd57ba4b19bb33bf6c105aace21bd922907939bb136c3424b29adc9935b314103b93d858f7ad9d94c2f77a5ce7ace31fa3d542c4030f96361ff4cdf6bfd501af32e2741d803e73584bc595176a36e4486d523934e140fb83da21491031839313c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1809b1951e42000000000000000000000000000000000000000000000000002e180b4fe1dd8900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000069f46d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1aa7754b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e445a6b4d545a6d4e4330324e6a646d4c5456694e4755744f546b775a6930785a6d4579597a67344f575a6a4f54596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000008768f846c2d7c1c76c2719062c39fc07fed0c9d8000000000000000000000000000000000000000000000000000000019de2cada000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x02b1984ed650b98c323eb1e2c9868ac17204ac5c9bf198204f781a33436233b7",
      "signature": {
        "s": "0x4ff5623b854464e6d752efcf6991c6c1a3f73177ecac201ca2146d24733dc4bc",
        "r": "0x1149d2609798706105d18112dab0d13951d3ff7139712a9d75a0ce2bc25a97fc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd57ba4b19bb33bf6c105aace21bd922907939bb136c3424b29adc9935b314103",
      "signature": {
        "s": "0x2e2741d803e73584bc595176a36e4486d523934e140fb83da21491031839313c",
        "r": "0xb93d858f7ad9d94c2f77a5ce7ace31fa3d542c4030f96361ff4cdf6bfd501af3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6943853274",
    "total": "6943853274"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6943853274",
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
            "amount": "43396855115"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6943853"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNDZkMTZmNC02NjdmLTViNGUtOTkwZi0xZmEyYzg4OWZjOTYifQ==",
    "nonce": 6447,
    "balances": {
      "current": "12974278841802306",
      "previous": "12974285792599433"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8768f846c2d7c1c76c2719062c39fc07fed0c9d8",
    "nonce": 22,
    "balances": {
      "current": "6943853274",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:14.313Z",
  "updated": "2020-05-22T08:49:14.383Z",
  "id": "5ec7920ab0c6090011d5b12e"
}
```
* *stageAmount*: `6943853274`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000019de2cada000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000019de2cada000000000000000000000000000000000000000000000000000000019de2cada02b1984ed650b98c323eb1e2c9868ac17204ac5c9bf198204f781a33436233b71149d2609798706105d18112dab0d13951d3ff7139712a9d75a0ce2bc25a97fc4ff5623b854464e6d752efcf6991c6c1a3f73177ecac201ca2146d24733dc4bc000000000000000000000000000000000000000000000000000000000000001bd57ba4b19bb33bf6c105aace21bd922907939bb136c3424b29adc9935b314103b93d858f7ad9d94c2f77a5ce7ace31fa3d542c4030f96361ff4cdf6bfd501af32e2741d803e73584bc595176a36e4486d523934e140fb83da21491031839313c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1809b1951e42000000000000000000000000000000000000000000000000002e180b4fe1dd8900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000069f46d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1aa7754b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e445a6b4d545a6d4e4330324e6a646d4c5456694e4755744f546b775a6930785a6d4579597a67344f575a6a4f54596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000008768f846c2d7c1c76c2719062c39fc07fed0c9d8000000000000000000000000000000000000000000000000000000019de2cada000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x02b1984ed650b98c323eb1e2c9868ac17204ac5c9bf198204f781a33436233b7",
      "signature": {
        "s": "0x4ff5623b854464e6d752efcf6991c6c1a3f73177ecac201ca2146d24733dc4bc",
        "r": "0x1149d2609798706105d18112dab0d13951d3ff7139712a9d75a0ce2bc25a97fc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd57ba4b19bb33bf6c105aace21bd922907939bb136c3424b29adc9935b314103",
      "signature": {
        "s": "0x2e2741d803e73584bc595176a36e4486d523934e140fb83da21491031839313c",
        "r": "0xb93d858f7ad9d94c2f77a5ce7ace31fa3d542c4030f96361ff4cdf6bfd501af3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6943853274",
    "total": "6943853274"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6943853274",
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
            "amount": "43396855115"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6943853"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNDZkMTZmNC02NjdmLTViNGUtOTkwZi0xZmEyYzg4OWZjOTYifQ==",
    "nonce": 6447,
    "balances": {
      "current": "12974278841802306",
      "previous": "12974285792599433"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8768f846c2d7c1c76c2719062c39fc07fed0c9d8",
    "nonce": 22,
    "balances": {
      "current": "6943853274",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:14.313Z",
  "updated": "2020-05-22T08:49:14.383Z",
  "id": "5ec7920ab0c6090011d5b12e"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000019de2cada000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6943853274`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`