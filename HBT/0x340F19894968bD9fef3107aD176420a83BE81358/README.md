# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x340F19894968bD9fef3107aD176420a83BE81358`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001ae6fa9b000000000000000000000000000000000000000000000000000000001ae6fa9b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001ae6fa9b000000000000000000000000000000000000000000000000000000001ae6fa9b749e4349a3bd6fd5836c7f3a323656fd0af2e3d40df4eac69a91fbd80f1359eb68f591d22bbce3b865b6845affc75d8ab0554f1540eb7c1d578711c8e8f0de5a1e136cf34bbb34b451a1f45889664fb5cc6cd56ac746d92b46816530afed7f41000000000000000000000000000000000000000000000000000000000000001ce94851561d1d82faf4d4325b3efe0eb17a4ce7edc48a7c193ad644773912be005f40ce0dd75ad6d0b34027b4ff9cc15c6f88db001f87a7a89b2145f0e5d973e44af3b91f11298512e42f37ecd34ef05a0f6738e050f31a27638154cf1dc9e03f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a6c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1689342dd7f0000000000000000000000000000000000000000000000000002e16894f1bb59c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000006e311000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a7cfc35e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a51304e6a41304d69316d4d7a457a4c5455315a6d5574596d526b5a4330774f544e6b4e7a63795a54466a4d54596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000340f19894968bd9fef3107ad176420a83be81358000000000000000000000000000000000000000000000000000000001ae6fa9b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x749e4349a3bd6fd5836c7f3a323656fd0af2e3d40df4eac69a91fbd80f1359eb",
      "signature": {
        "s": "0x1e136cf34bbb34b451a1f45889664fb5cc6cd56ac746d92b46816530afed7f41",
        "r": "0x68f591d22bbce3b865b6845affc75d8ab0554f1540eb7c1d578711c8e8f0de5a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe94851561d1d82faf4d4325b3efe0eb17a4ce7edc48a7c193ad644773912be00",
      "signature": {
        "s": "0x4af3b91f11298512e42f37ecd34ef05a0f6738e050f31a27638154cf1dc9e03f",
        "r": "0x5f40ce0dd75ad6d0b34027b4ff9cc15c6f88db001f87a7a89b2145f0e5d973e4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "451345051",
    "total": "451345051"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "451345051",
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
            "amount": "45046576617"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "451345"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NjQ0NjA0Mi1mMzEzLTU1ZmUtYmRkZC0wOTNkNzcyZTFjMTYifQ==",
    "nonce": 6764,
    "balances": {
      "current": "12972627470440432",
      "previous": "12972627922236828"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x340f19894968bd9fef3107ad176420a83be81358",
    "nonce": 22,
    "balances": {
      "current": "451345051",
      "previous": "0"
    }
  },
  "blockNumber": "10114715",
  "created": "2020-05-22T08:51:32.419Z",
  "updated": "2020-05-22T08:51:32.487Z",
  "id": "5ec79294b0c6090011d5b198"
}
```
* *stageAmount*: `451345051`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001ae6fa9b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001ae6fa9b000000000000000000000000000000000000000000000000000000001ae6fa9b749e4349a3bd6fd5836c7f3a323656fd0af2e3d40df4eac69a91fbd80f1359eb68f591d22bbce3b865b6845affc75d8ab0554f1540eb7c1d578711c8e8f0de5a1e136cf34bbb34b451a1f45889664fb5cc6cd56ac746d92b46816530afed7f41000000000000000000000000000000000000000000000000000000000000001ce94851561d1d82faf4d4325b3efe0eb17a4ce7edc48a7c193ad644773912be005f40ce0dd75ad6d0b34027b4ff9cc15c6f88db001f87a7a89b2145f0e5d973e44af3b91f11298512e42f37ecd34ef05a0f6738e050f31a27638154cf1dc9e03f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a6c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1689342dd7f0000000000000000000000000000000000000000000000000002e16894f1bb59c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000006e311000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a7cfc35e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a51304e6a41304d69316d4d7a457a4c5455315a6d5574596d526b5a4330774f544e6b4e7a63795a54466a4d54596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000340f19894968bd9fef3107ad176420a83be81358000000000000000000000000000000000000000000000000000000001ae6fa9b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x749e4349a3bd6fd5836c7f3a323656fd0af2e3d40df4eac69a91fbd80f1359eb",
      "signature": {
        "s": "0x1e136cf34bbb34b451a1f45889664fb5cc6cd56ac746d92b46816530afed7f41",
        "r": "0x68f591d22bbce3b865b6845affc75d8ab0554f1540eb7c1d578711c8e8f0de5a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe94851561d1d82faf4d4325b3efe0eb17a4ce7edc48a7c193ad644773912be00",
      "signature": {
        "s": "0x4af3b91f11298512e42f37ecd34ef05a0f6738e050f31a27638154cf1dc9e03f",
        "r": "0x5f40ce0dd75ad6d0b34027b4ff9cc15c6f88db001f87a7a89b2145f0e5d973e4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "451345051",
    "total": "451345051"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "451345051",
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
            "amount": "45046576617"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "451345"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NjQ0NjA0Mi1mMzEzLTU1ZmUtYmRkZC0wOTNkNzcyZTFjMTYifQ==",
    "nonce": 6764,
    "balances": {
      "current": "12972627470440432",
      "previous": "12972627922236828"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x340f19894968bd9fef3107ad176420a83be81358",
    "nonce": 22,
    "balances": {
      "current": "451345051",
      "previous": "0"
    }
  },
  "blockNumber": "10114715",
  "created": "2020-05-22T08:51:32.419Z",
  "updated": "2020-05-22T08:51:32.487Z",
  "id": "5ec79294b0c6090011d5b198"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000001ae6fa9b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `451345051`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`