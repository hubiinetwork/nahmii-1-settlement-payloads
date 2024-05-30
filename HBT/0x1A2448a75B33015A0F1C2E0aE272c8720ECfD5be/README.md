# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1A2448a75B33015A0F1C2E0aE272c8720ECfD5be`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000a600000000000000000000000000000000000000000000000000000000000000a6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000a600000000000000000000000000000000000000000000000000000000000000a6013274a83f63ab67dfc2342fdadbf7357c687e6537bf52a8f2d405898e549a2a30078738efe9757e8a946ee804fd4afcf7238eb9b247502a94853dd7145ad2883815676cc7aafb54acad1d5842faf94400dbaee983447b890d132de5780f2872000000000000000000000000000000000000000000000000000000000000001ce343ebafcbbe64f83ebfadb9a55ab6183ce7a50d3466675201176a288e8e7ca883ed5deecb8acc63a24c3a46714c0b139ea24f7b8e716653e2d0ad8d57ee3c1432f456fadc0178369e97bc1901140d79b3a79bbcab38079d7391146c14b6fd82000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a7c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e164236da71da000000000000000000000000000000000000000000000000002e164236da728100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a8f23ef26000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a6d49304d7a67785a6931695a474a6b4c5456684e575174596d56685a53316b4e546c6a4d5455774e7a6c69596d456966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000001a2448a75b33015a0f1c2e0ae272c8720ecfd5be00000000000000000000000000000000000000000000000000000000000000a6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x013274a83f63ab67dfc2342fdadbf7357c687e6537bf52a8f2d405898e549a2a",
      "signature": {
        "s": "0x3815676cc7aafb54acad1d5842faf94400dbaee983447b890d132de5780f2872",
        "r": "0x30078738efe9757e8a946ee804fd4afcf7238eb9b247502a94853dd7145ad288",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe343ebafcbbe64f83ebfadb9a55ab6183ce7a50d3466675201176a288e8e7ca8",
      "signature": {
        "s": "0x32f456fadc0178369e97bc1901140d79b3a79bbcab38079d7391146c14b6fd82",
        "r": "0x83ed5deecb8acc63a24c3a46714c0b139ea24f7b8e716653e2d0ad8d57ee3c14",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "166",
    "total": "166"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "166",
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
            "amount": "45351169830"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZmI0MzgxZi1iZGJkLTVhNWQtYmVhZS1kNTljMTUwNzliYmEifQ==",
    "nonce": 6780,
    "balances": {
      "current": "12972322572628442",
      "previous": "12972322572628609"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1a2448a75b33015a0f1c2e0ae272c8720ecfd5be",
    "nonce": 21,
    "balances": {
      "current": "166",
      "previous": "0"
    }
  },
  "blockNumber": "10114715",
  "created": "2020-05-22T08:51:36.399Z",
  "updated": "2020-05-22T08:51:37.545Z",
  "id": "5ec79298e5756b00111b8813"
}
```
* *stageAmount*: `166`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000a6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000a600000000000000000000000000000000000000000000000000000000000000a6013274a83f63ab67dfc2342fdadbf7357c687e6537bf52a8f2d405898e549a2a30078738efe9757e8a946ee804fd4afcf7238eb9b247502a94853dd7145ad2883815676cc7aafb54acad1d5842faf94400dbaee983447b890d132de5780f2872000000000000000000000000000000000000000000000000000000000000001ce343ebafcbbe64f83ebfadb9a55ab6183ce7a50d3466675201176a288e8e7ca883ed5deecb8acc63a24c3a46714c0b139ea24f7b8e716653e2d0ad8d57ee3c1432f456fadc0178369e97bc1901140d79b3a79bbcab38079d7391146c14b6fd82000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a7c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e164236da71da000000000000000000000000000000000000000000000000002e164236da728100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a8f23ef26000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a6d49304d7a67785a6931695a474a6b4c5456684e575174596d56685a53316b4e546c6a4d5455774e7a6c69596d456966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000001a2448a75b33015a0f1c2e0ae272c8720ecfd5be00000000000000000000000000000000000000000000000000000000000000a6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x013274a83f63ab67dfc2342fdadbf7357c687e6537bf52a8f2d405898e549a2a",
      "signature": {
        "s": "0x3815676cc7aafb54acad1d5842faf94400dbaee983447b890d132de5780f2872",
        "r": "0x30078738efe9757e8a946ee804fd4afcf7238eb9b247502a94853dd7145ad288",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe343ebafcbbe64f83ebfadb9a55ab6183ce7a50d3466675201176a288e8e7ca8",
      "signature": {
        "s": "0x32f456fadc0178369e97bc1901140d79b3a79bbcab38079d7391146c14b6fd82",
        "r": "0x83ed5deecb8acc63a24c3a46714c0b139ea24f7b8e716653e2d0ad8d57ee3c14",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "166",
    "total": "166"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "166",
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
            "amount": "45351169830"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZmI0MzgxZi1iZGJkLTVhNWQtYmVhZS1kNTljMTUwNzliYmEifQ==",
    "nonce": 6780,
    "balances": {
      "current": "12972322572628442",
      "previous": "12972322572628609"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1a2448a75b33015a0f1c2e0ae272c8720ecfd5be",
    "nonce": 21,
    "balances": {
      "current": "166",
      "previous": "0"
    }
  },
  "blockNumber": "10114715",
  "created": "2020-05-22T08:51:36.399Z",
  "updated": "2020-05-22T08:51:37.545Z",
  "id": "5ec79298e5756b00111b8813"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000a6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `166`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`