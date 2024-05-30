# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdD82F45F6450797ebd3C58993dF6D38E02291A03`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000b8cbb23000000000000000000000000000000000000000000000000000000000b8cbb23000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000b8cbb23000000000000000000000000000000000000000000000000000000000b8cbb23de6ecfad6a4adbf0d7d73957ff1488c390bbb6369499df3bcf11be73d4ab5bd43c03b6371802c59abe2fb8dfe2972aeb55075990771b415aa52bcc3cfbdb9b900703e435472db23b74c79ac94c5c014ddf15a81ed40df1ad16361ce447fc1ebe000000000000000000000000000000000000000000000000000000000000001b8b383da79e3345ee75cc5d8e7660fe66857fd182f8054d9d6595970b8346fad438c1ea14be337cc2e145df804c0cb1aacb3d7be13f4c6dbdfb4fe81294b420c80256ace08bd820fd7334b2dcbd8d1d5185efcf824ba4ec1cb8919605985ce4ad000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569e00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ae100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e160fcb5ed1b6000000000000000000000000000000000000000000000000002e160fd6ee81c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002f4ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9c08f2bc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6a4e6b4e6d526a4e793031597a67784c5455775a446b74595449344d7930304e5441785a4449344d54526c597a636966513d3d0000000000000000000000000000000000000000000000000000000000000007000000000000000000000000dd82f45f6450797ebd3c58993df6d38e02291a03000000000000000000000000000000000000000000000000000000000b8cbb23000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xde6ecfad6a4adbf0d7d73957ff1488c390bbb6369499df3bcf11be73d4ab5bd4",
      "signature": {
        "s": "0x0703e435472db23b74c79ac94c5c014ddf15a81ed40df1ad16361ce447fc1ebe",
        "r": "0x3c03b6371802c59abe2fb8dfe2972aeb55075990771b415aa52bcc3cfbdb9b90",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8b383da79e3345ee75cc5d8e7660fe66857fd182f8054d9d6595970b8346fad4",
      "signature": {
        "s": "0x0256ace08bd820fd7334b2dcbd8d1d5185efcf824ba4ec1cb8919605985ce4ad",
        "r": "0x38c1ea14be337cc2e145df804c0cb1aacb3d7be13f4c6dbdfb4fe81294b420c8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "193772323",
    "total": "193772323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "193772323",
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
            "amount": "45567505084"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "193772"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzZjNkNmRjNy01YzgxLTUwZDktYTI4My00NTAxZDI4MTRlYzcifQ==",
    "nonce": 6881,
    "balances": {
      "current": "12972106020999606",
      "previous": "12972106214965701"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdd82f45f6450797ebd3c58993df6d38e02291a03",
    "nonce": 7,
    "balances": {
      "current": "193772323",
      "previous": "0"
    }
  },
  "blockNumber": "10114718",
  "created": "2020-05-22T08:52:19.829Z",
  "updated": "2020-05-22T08:52:20.919Z",
  "id": "5ec792c3005df800101bcb3b"
}
```
* *stageAmount*: `193772323`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000b8cbb23000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000b8cbb23000000000000000000000000000000000000000000000000000000000b8cbb23de6ecfad6a4adbf0d7d73957ff1488c390bbb6369499df3bcf11be73d4ab5bd43c03b6371802c59abe2fb8dfe2972aeb55075990771b415aa52bcc3cfbdb9b900703e435472db23b74c79ac94c5c014ddf15a81ed40df1ad16361ce447fc1ebe000000000000000000000000000000000000000000000000000000000000001b8b383da79e3345ee75cc5d8e7660fe66857fd182f8054d9d6595970b8346fad438c1ea14be337cc2e145df804c0cb1aacb3d7be13f4c6dbdfb4fe81294b420c80256ace08bd820fd7334b2dcbd8d1d5185efcf824ba4ec1cb8919605985ce4ad000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569e00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ae100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e160fcb5ed1b6000000000000000000000000000000000000000000000000002e160fd6ee81c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002f4ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9c08f2bc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6a4e6b4e6d526a4e793031597a67784c5455775a446b74595449344d7930304e5441785a4449344d54526c597a636966513d3d0000000000000000000000000000000000000000000000000000000000000007000000000000000000000000dd82f45f6450797ebd3c58993df6d38e02291a03000000000000000000000000000000000000000000000000000000000b8cbb23000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xde6ecfad6a4adbf0d7d73957ff1488c390bbb6369499df3bcf11be73d4ab5bd4",
      "signature": {
        "s": "0x0703e435472db23b74c79ac94c5c014ddf15a81ed40df1ad16361ce447fc1ebe",
        "r": "0x3c03b6371802c59abe2fb8dfe2972aeb55075990771b415aa52bcc3cfbdb9b90",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8b383da79e3345ee75cc5d8e7660fe66857fd182f8054d9d6595970b8346fad4",
      "signature": {
        "s": "0x0256ace08bd820fd7334b2dcbd8d1d5185efcf824ba4ec1cb8919605985ce4ad",
        "r": "0x38c1ea14be337cc2e145df804c0cb1aacb3d7be13f4c6dbdfb4fe81294b420c8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "193772323",
    "total": "193772323"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "193772323",
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
            "amount": "45567505084"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "193772"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzZjNkNmRjNy01YzgxLTUwZDktYTI4My00NTAxZDI4MTRlYzcifQ==",
    "nonce": 6881,
    "balances": {
      "current": "12972106020999606",
      "previous": "12972106214965701"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdd82f45f6450797ebd3c58993df6d38e02291a03",
    "nonce": 7,
    "balances": {
      "current": "193772323",
      "previous": "0"
    }
  },
  "blockNumber": "10114718",
  "created": "2020-05-22T08:52:19.829Z",
  "updated": "2020-05-22T08:52:20.919Z",
  "id": "5ec792c3005df800101bcb3b"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000b8cbb23000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `193772323`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`