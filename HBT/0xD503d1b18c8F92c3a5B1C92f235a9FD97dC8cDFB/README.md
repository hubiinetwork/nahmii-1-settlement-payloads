# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD503d1b18c8F92c3a5B1C92f235a9FD97dC8cDFB`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000247e29f400000000000000000000000000000000000000000000000000000000247e29f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000247e29f400000000000000000000000000000000000000000000000000000000247e29f41dab597fbb1232e0376f654b59b1b0e2d163043771b09222ae45aa4ebe2ca547e8da846aa7c33085929e33d2ae397ea56710f6405388012c0d1d49851b19f404034d206fca412506ef50210394bf6ab5aa561b270afadf32c7f2fa89a64bfdfa000000000000000000000000000000000000000000000000000000000000001c69055e26c23551adf9c1414395e0dd37e311dbe91489b5c8ce444a24fe20a8719d9845ec2c2e451c0b948a1476059b298a515122add55a99d562ed9deda8ba606345e0321799ed14de07cb1910f1fa42b3b9840065ce607e42bc9b822f113192000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c0700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13b02df952df000000000000000000000000000000000000000000000000002e13b05280d46b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000095798000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b376dcf8a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68597a466c4d6a4d305a43316d4e5467314c5455315a6d4d7459574e6b5953316b4e6d4979596a4d7a4d4759344d6a636966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000d503d1b18c8f92c3a5b1c92f235a9fd97dc8cdfb00000000000000000000000000000000000000000000000000000000247e29f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1dab597fbb1232e0376f654b59b1b0e2d163043771b09222ae45aa4ebe2ca547",
      "signature": {
        "s": "0x034d206fca412506ef50210394bf6ab5aa561b270afadf32c7f2fa89a64bfdfa",
        "r": "0xe8da846aa7c33085929e33d2ae397ea56710f6405388012c0d1d49851b19f404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x69055e26c23551adf9c1414395e0dd37e311dbe91489b5c8ce444a24fe20a871",
      "signature": {
        "s": "0x6345e0321799ed14de07cb1910f1fa42b3b9840065ce607e42bc9b822f113192",
        "r": "0x9d9845ec2c2e451c0b948a1476059b298a515122add55a99d562ed9deda8ba60",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "612248052",
    "total": "612248052"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "612248052",
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
            "amount": "48174583690"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "612248"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhYzFlMjM0ZC1mNTg1LTU1ZmMtYWNkYS1kNmIyYjMzMGY4MjcifQ==",
    "nonce": 7175,
    "balances": {
      "current": "12969496335176415",
      "previous": "12969496948036715"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd503d1b18c8f92c3a5b1c92f235a9fd97dc8cdfb",
    "nonce": 10,
    "balances": {
      "current": "612248052",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:45.892Z",
  "updated": "2020-05-22T08:54:45.960Z",
  "id": "5ec79355e5756b00111b8893"
}
```
* *stageAmount*: `612248052`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000247e29f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000247e29f400000000000000000000000000000000000000000000000000000000247e29f41dab597fbb1232e0376f654b59b1b0e2d163043771b09222ae45aa4ebe2ca547e8da846aa7c33085929e33d2ae397ea56710f6405388012c0d1d49851b19f404034d206fca412506ef50210394bf6ab5aa561b270afadf32c7f2fa89a64bfdfa000000000000000000000000000000000000000000000000000000000000001c69055e26c23551adf9c1414395e0dd37e311dbe91489b5c8ce444a24fe20a8719d9845ec2c2e451c0b948a1476059b298a515122add55a99d562ed9deda8ba606345e0321799ed14de07cb1910f1fa42b3b9840065ce607e42bc9b822f113192000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c0700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13b02df952df000000000000000000000000000000000000000000000000002e13b05280d46b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000095798000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b376dcf8a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68597a466c4d6a4d305a43316d4e5467314c5455315a6d4d7459574e6b5953316b4e6d4979596a4d7a4d4759344d6a636966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000d503d1b18c8f92c3a5b1c92f235a9fd97dc8cdfb00000000000000000000000000000000000000000000000000000000247e29f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1dab597fbb1232e0376f654b59b1b0e2d163043771b09222ae45aa4ebe2ca547",
      "signature": {
        "s": "0x034d206fca412506ef50210394bf6ab5aa561b270afadf32c7f2fa89a64bfdfa",
        "r": "0xe8da846aa7c33085929e33d2ae397ea56710f6405388012c0d1d49851b19f404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x69055e26c23551adf9c1414395e0dd37e311dbe91489b5c8ce444a24fe20a871",
      "signature": {
        "s": "0x6345e0321799ed14de07cb1910f1fa42b3b9840065ce607e42bc9b822f113192",
        "r": "0x9d9845ec2c2e451c0b948a1476059b298a515122add55a99d562ed9deda8ba60",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "612248052",
    "total": "612248052"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "612248052",
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
            "amount": "48174583690"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "612248"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhYzFlMjM0ZC1mNTg1LTU1ZmMtYWNkYS1kNmIyYjMzMGY4MjcifQ==",
    "nonce": 7175,
    "balances": {
      "current": "12969496335176415",
      "previous": "12969496948036715"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd503d1b18c8f92c3a5b1c92f235a9fd97dc8cdfb",
    "nonce": 10,
    "balances": {
      "current": "612248052",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:45.892Z",
  "updated": "2020-05-22T08:54:45.960Z",
  "id": "5ec79355e5756b00111b8893"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000247e29f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `612248052`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`