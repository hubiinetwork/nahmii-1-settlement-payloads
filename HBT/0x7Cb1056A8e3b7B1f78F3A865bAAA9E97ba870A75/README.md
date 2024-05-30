# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7Cb1056A8e3b7B1f78F3A865bAAA9E97ba870A75`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000022158e500000000000000000000000000000000000000000000000000000000022158e5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000022158e500000000000000000000000000000000000000000000000000000000022158e540624042afbdb57302eee0ae1297f19d7f7f8fadfd3b8a1153bf5a1d0eb8ff2ea125736a3993b118a008e9a8330970eaf09bd03ef058a033e4e3095c44b189313940584b5f2ee56f258609957ed61d7f6ab44e300404cd15f0eec73057dfc091000000000000000000000000000000000000000000000000000000000000001ca1459fde3528309486aaf94cf103a57f0764aa0b10b87b73931f325be9037370695ad9850bbc158aa30ff4fb416e927f51d6fd02bd6a00fec102b389c15d7677179436dc05eb4765256b2e1652b4de973324dae35a225475b4b042a0e8b7430d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001dd600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b161cb19ec1000000000000000000000000000000000000000000000000002e0b161ed3834100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000008b9b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6a985521000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e7a6b785a5463335a4330795a4459304c5455794d5749744f544e6b595331684f44526a4d6d55315a5745784f446b6966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000007cb1056a8e3b7b1f78f3a865baaa9e97ba870a7500000000000000000000000000000000000000000000000000000000022158e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x40624042afbdb57302eee0ae1297f19d7f7f8fadfd3b8a1153bf5a1d0eb8ff2e",
      "signature": {
        "s": "0x3940584b5f2ee56f258609957ed61d7f6ab44e300404cd15f0eec73057dfc091",
        "r": "0xa125736a3993b118a008e9a8330970eaf09bd03ef058a033e4e3095c44b18931",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa1459fde3528309486aaf94cf103a57f0764aa0b10b87b73931f325be9037370",
      "signature": {
        "s": "0x179436dc05eb4765256b2e1652b4de973324dae35a225475b4b042a0e8b7430d",
        "r": "0x695ad9850bbc158aa30ff4fb416e927f51d6fd02bd6a00fec102b389c15d7677",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "35739877",
    "total": "35739877"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "35739877",
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
            "amount": "57622943009"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "35739"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNzkxZTc3ZC0yZDY0LTUyMWItOTNkYS1hODRjMmU1ZWExODkifQ==",
    "nonce": 7638,
    "balances": {
      "current": "12960038527278785",
      "previous": "12960038563054401"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7cb1056a8e3b7b1f78f3a865baaa9e97ba870a75",
    "nonce": 6,
    "balances": {
      "current": "35739877",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:17.451Z",
  "updated": "2020-05-22T08:58:18.519Z",
  "id": "5ec79429b0c6090011d5b2c9"
}
```
* *stageAmount*: `35739877`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000022158e5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000022158e500000000000000000000000000000000000000000000000000000000022158e540624042afbdb57302eee0ae1297f19d7f7f8fadfd3b8a1153bf5a1d0eb8ff2ea125736a3993b118a008e9a8330970eaf09bd03ef058a033e4e3095c44b189313940584b5f2ee56f258609957ed61d7f6ab44e300404cd15f0eec73057dfc091000000000000000000000000000000000000000000000000000000000000001ca1459fde3528309486aaf94cf103a57f0764aa0b10b87b73931f325be9037370695ad9850bbc158aa30ff4fb416e927f51d6fd02bd6a00fec102b389c15d7677179436dc05eb4765256b2e1652b4de973324dae35a225475b4b042a0e8b7430d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001dd600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b161cb19ec1000000000000000000000000000000000000000000000000002e0b161ed3834100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000008b9b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6a985521000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e7a6b785a5463335a4330795a4459304c5455794d5749744f544e6b595331684f44526a4d6d55315a5745784f446b6966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000007cb1056a8e3b7b1f78f3a865baaa9e97ba870a7500000000000000000000000000000000000000000000000000000000022158e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x40624042afbdb57302eee0ae1297f19d7f7f8fadfd3b8a1153bf5a1d0eb8ff2e",
      "signature": {
        "s": "0x3940584b5f2ee56f258609957ed61d7f6ab44e300404cd15f0eec73057dfc091",
        "r": "0xa125736a3993b118a008e9a8330970eaf09bd03ef058a033e4e3095c44b18931",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa1459fde3528309486aaf94cf103a57f0764aa0b10b87b73931f325be9037370",
      "signature": {
        "s": "0x179436dc05eb4765256b2e1652b4de973324dae35a225475b4b042a0e8b7430d",
        "r": "0x695ad9850bbc158aa30ff4fb416e927f51d6fd02bd6a00fec102b389c15d7677",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "35739877",
    "total": "35739877"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "35739877",
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
            "amount": "57622943009"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "35739"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNzkxZTc3ZC0yZDY0LTUyMWItOTNkYS1hODRjMmU1ZWExODkifQ==",
    "nonce": 7638,
    "balances": {
      "current": "12960038527278785",
      "previous": "12960038563054401"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7cb1056a8e3b7b1f78f3a865baaa9e97ba870a75",
    "nonce": 6,
    "balances": {
      "current": "35739877",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:17.451Z",
  "updated": "2020-05-22T08:58:18.519Z",
  "id": "5ec79429b0c6090011d5b2c9"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000022158e5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `35739877`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`