# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFa9a024Ea56D130daD68EDCD9af89a677D635B9F`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000134c790000000000000000000000000000000000000000000000000000000000134c79000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000134c790000000000000000000000000000000000000000000000000000000000134c79aeb01b1e29a1c8957281270702eaa3a3969893ebe5dd41950e21554f83ee64c92dcc0b11df41735c6c3e8b5732cc73da29e67a0511b6ef27cbe9c2653b994854056ed660c92a7d596491e1d2688a6259b246bc0f65cbd687f886d9bcd0897f2f000000000000000000000000000000000000000000000000000000000000001b23883cd9a31adfd9ef1cdb251ef9ce77b42482f03efe078c9845f62a8e3224daab35fd8bcb2a3ff7473355edb5ed0e972b10fa1800ebb9e157155cb15e1570052c0e42ddd514be8c15458dfd6893e4668cda2a575c69fc2e463773c9a39f0b7f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000177c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1c1561b9cf000000000000000000000000000000000000000000000000002e1b1c15750b3800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000004f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009518a1a0b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934595441334d546b774f53316d4e6d466a4c5456694e445574596a4d334e6930304f444d30596a4d774e7a677a596d496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fa9a024ea56d130dad68edcd9af89a677d635b9f0000000000000000000000000000000000000000000000000000000000134c79000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xaeb01b1e29a1c8957281270702eaa3a3969893ebe5dd41950e21554f83ee64c9",
      "signature": {
        "s": "0x056ed660c92a7d596491e1d2688a6259b246bc0f65cbd687f886d9bcd0897f2f",
        "r": "0x2dcc0b11df41735c6c3e8b5732cc73da29e67a0511b6ef27cbe9c2653b994854",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x23883cd9a31adfd9ef1cdb251ef9ce77b42482f03efe078c9845f62a8e3224da",
      "signature": {
        "s": "0x2c0e42ddd514be8c15458dfd6893e4668cda2a575c69fc2e463773c9a39f0b7f",
        "r": "0xab35fd8bcb2a3ff7473355edb5ed0e972b10fa1800ebb9e157155cb15e157005",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1264761",
    "total": "1264761"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1264761",
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
            "amount": "40022710795"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1264"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YTA3MTkwOS1mNmFjLTViNDUtYjM3Ni00ODM0YjMwNzgzYmIifQ==",
    "nonce": 6012,
    "balances": {
      "current": "12977656360450511",
      "previous": "12977656361716536"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfa9a024ea56d130dad68edcd9af89a677d635b9f",
    "nonce": 22,
    "balances": {
      "current": "1264761",
      "previous": "0"
    }
  },
  "blockNumber": "10114682",
  "created": "2020-05-22T08:45:43.462Z",
  "updated": "2020-05-22T08:45:43.531Z",
  "id": "5ec79137b0c6090011d5b094"
}
```
* *stageAmount*: `1264761`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000134c79000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000134c790000000000000000000000000000000000000000000000000000000000134c79aeb01b1e29a1c8957281270702eaa3a3969893ebe5dd41950e21554f83ee64c92dcc0b11df41735c6c3e8b5732cc73da29e67a0511b6ef27cbe9c2653b994854056ed660c92a7d596491e1d2688a6259b246bc0f65cbd687f886d9bcd0897f2f000000000000000000000000000000000000000000000000000000000000001b23883cd9a31adfd9ef1cdb251ef9ce77b42482f03efe078c9845f62a8e3224daab35fd8bcb2a3ff7473355edb5ed0e972b10fa1800ebb9e157155cb15e1570052c0e42ddd514be8c15458dfd6893e4668cda2a575c69fc2e463773c9a39f0b7f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000177c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1c1561b9cf000000000000000000000000000000000000000000000000002e1b1c15750b3800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000004f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009518a1a0b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934595441334d546b774f53316d4e6d466a4c5456694e445574596a4d334e6930304f444d30596a4d774e7a677a596d496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fa9a024ea56d130dad68edcd9af89a677d635b9f0000000000000000000000000000000000000000000000000000000000134c79000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xaeb01b1e29a1c8957281270702eaa3a3969893ebe5dd41950e21554f83ee64c9",
      "signature": {
        "s": "0x056ed660c92a7d596491e1d2688a6259b246bc0f65cbd687f886d9bcd0897f2f",
        "r": "0x2dcc0b11df41735c6c3e8b5732cc73da29e67a0511b6ef27cbe9c2653b994854",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x23883cd9a31adfd9ef1cdb251ef9ce77b42482f03efe078c9845f62a8e3224da",
      "signature": {
        "s": "0x2c0e42ddd514be8c15458dfd6893e4668cda2a575c69fc2e463773c9a39f0b7f",
        "r": "0xab35fd8bcb2a3ff7473355edb5ed0e972b10fa1800ebb9e157155cb15e157005",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1264761",
    "total": "1264761"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1264761",
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
            "amount": "40022710795"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1264"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YTA3MTkwOS1mNmFjLTViNDUtYjM3Ni00ODM0YjMwNzgzYmIifQ==",
    "nonce": 6012,
    "balances": {
      "current": "12977656360450511",
      "previous": "12977656361716536"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfa9a024ea56d130dad68edcd9af89a677d635b9f",
    "nonce": 22,
    "balances": {
      "current": "1264761",
      "previous": "0"
    }
  },
  "blockNumber": "10114682",
  "created": "2020-05-22T08:45:43.462Z",
  "updated": "2020-05-22T08:45:43.531Z",
  "id": "5ec79137b0c6090011d5b094"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000134c79000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1264761`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`