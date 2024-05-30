# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x598c7326Cc9C7167Ea1977FC4efe3cf84f6263A7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000000000000000000000000000000000000000005c4f4d6381360eb188b01deaff929e34525ed0c93093fb6762018bd3ffd12fdf6924bd5e4087d4e9dd9c4a1802b1ee18f765295dc814b4763ffdbe5228635444005b66c916f4b83949fdb63479a94b4ad878c4250dbd9688d7eb952e328744f0b2000000000000000000000000000000000000000000000000000000000000001c36294ee0f9244be9f4197cf47d102d61eeece76ce1d9109358eebd49d85481d32131d03c5216da48bf0586b3c2a3daaed6d6c8b3d63cf78d9a3c7ad0e79633a954eb5548bd8f3428ea375e2b6e082498c6a1544fc95f6f2477aed9c442b09aef000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000168b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b90ef81ce29000000000000000000000000000000000000000000000000002e1b90ef81ce8600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000933a7bce1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f4441774f5749774e5330785a544e694c5455345a446b74596a526d4e5331694d47466a4d54686c4d446b344d6a456966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000598c7326cc9c7167ea1977fc4efe3cf84f6263a7000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f4d6381360eb188b01deaff929e34525ed0c93093fb6762018bd3ffd12fdf69",
      "signature": {
        "s": "0x5b66c916f4b83949fdb63479a94b4ad878c4250dbd9688d7eb952e328744f0b2",
        "r": "0x24bd5e4087d4e9dd9c4a1802b1ee18f765295dc814b4763ffdbe522863544400",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x36294ee0f9244be9f4197cf47d102d61eeece76ce1d9109358eebd49d85481d3",
      "signature": {
        "s": "0x54eb5548bd8f3428ea375e2b6e082498c6a1544fc95f6f2477aed9c442b09aef",
        "r": "0x2131d03c5216da48bf0586b3c2a3daaed6d6c8b3d63cf78d9a3c7ad0e79633a9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "92",
    "total": "92"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "92",
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
            "amount": "39521336545"
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
    "data": "eyJyZWYiOiIxODAwOWIwNS0xZTNiLTU4ZDktYjRmNS1iMGFjMThlMDk4MjEifQ==",
    "nonce": 5771,
    "balances": {
      "current": "12978158236192297",
      "previous": "12978158236192390"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x598c7326cc9c7167ea1977fc4efe3cf84f6263a7",
    "nonce": 21,
    "balances": {
      "current": "92",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:45.676Z",
  "updated": "2020-05-22T08:43:45.741Z",
  "id": "5ec790c1e5756b00111b86d5"
}
```
* *stageAmount*: `92`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000000000000000000000000000000000000000005c4f4d6381360eb188b01deaff929e34525ed0c93093fb6762018bd3ffd12fdf6924bd5e4087d4e9dd9c4a1802b1ee18f765295dc814b4763ffdbe5228635444005b66c916f4b83949fdb63479a94b4ad878c4250dbd9688d7eb952e328744f0b2000000000000000000000000000000000000000000000000000000000000001c36294ee0f9244be9f4197cf47d102d61eeece76ce1d9109358eebd49d85481d32131d03c5216da48bf0586b3c2a3daaed6d6c8b3d63cf78d9a3c7ad0e79633a954eb5548bd8f3428ea375e2b6e082498c6a1544fc95f6f2477aed9c442b09aef000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000168b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b90ef81ce29000000000000000000000000000000000000000000000000002e1b90ef81ce8600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000933a7bce1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f4441774f5749774e5330785a544e694c5455345a446b74596a526d4e5331694d47466a4d54686c4d446b344d6a456966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000598c7326cc9c7167ea1977fc4efe3cf84f6263a7000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f4d6381360eb188b01deaff929e34525ed0c93093fb6762018bd3ffd12fdf69",
      "signature": {
        "s": "0x5b66c916f4b83949fdb63479a94b4ad878c4250dbd9688d7eb952e328744f0b2",
        "r": "0x24bd5e4087d4e9dd9c4a1802b1ee18f765295dc814b4763ffdbe522863544400",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x36294ee0f9244be9f4197cf47d102d61eeece76ce1d9109358eebd49d85481d3",
      "signature": {
        "s": "0x54eb5548bd8f3428ea375e2b6e082498c6a1544fc95f6f2477aed9c442b09aef",
        "r": "0x2131d03c5216da48bf0586b3c2a3daaed6d6c8b3d63cf78d9a3c7ad0e79633a9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "92",
    "total": "92"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "92",
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
            "amount": "39521336545"
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
    "data": "eyJyZWYiOiIxODAwOWIwNS0xZTNiLTU4ZDktYjRmNS1iMGFjMThlMDk4MjEifQ==",
    "nonce": 5771,
    "balances": {
      "current": "12978158236192297",
      "previous": "12978158236192390"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x598c7326cc9c7167ea1977fc4efe3cf84f6263a7",
    "nonce": 21,
    "balances": {
      "current": "92",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:45.676Z",
  "updated": "2020-05-22T08:43:45.741Z",
  "id": "5ec790c1e5756b00111b86d5"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `92`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`