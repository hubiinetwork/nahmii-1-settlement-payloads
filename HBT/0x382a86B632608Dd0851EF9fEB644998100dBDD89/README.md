# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x382a86B632608Dd0851EF9fEB644998100dBDD89`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000056c7d3000000000000000000000000000000000000000000000000000000000056c7d3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000056c7d3000000000000000000000000000000000000000000000000000000000056c7d37c61fcc24fbb192858bdd8a9ef4f51fad66c0be55a9565607ebb7843dbf3c6d5f187b1a9dc2a8c76bb98bb50b437d3734d0740d3af2c7edd97b0e2cf670c28f75e4ef37d237d0c4508a8a4e922eb4e2aeb0b3fc7faf802b231bed26687ec78b1000000000000000000000000000000000000000000000000000000000000001b4967bc1667cf80cb9e635939722bd291db06713cf67c5de364af1815dde7e27a08439e2c2b49cd0efbabee845567198f898804a8aeffdbedb690fcfd42e8c03843d09d504d3aa35063d320b867994c67b766c5efbd1b547195e21f37f0c9d63c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ac800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1616c0e0a6d2000000000000000000000000000000000000000000000000002e1616c13784dc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000001637000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9a41568e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a517759546c6c4e7930795a4445304c5455774e4745744f546c684e6930304d6a4e6c4f54426b4e54566d4f47596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000382a86b632608dd0851ef9feb644998100dbdd89000000000000000000000000000000000000000000000000000000000056c7d3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c61fcc24fbb192858bdd8a9ef4f51fad66c0be55a9565607ebb7843dbf3c6d5",
      "signature": {
        "s": "0x5e4ef37d237d0c4508a8a4e922eb4e2aeb0b3fc7faf802b231bed26687ec78b1",
        "r": "0xf187b1a9dc2a8c76bb98bb50b437d3734d0740d3af2c7edd97b0e2cf670c28f7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4967bc1667cf80cb9e635939722bd291db06713cf67c5de364af1815dde7e27a",
      "signature": {
        "s": "0x43d09d504d3aa35063d320b867994c67b766c5efbd1b547195e21f37f0c9d63c",
        "r": "0x08439e2c2b49cd0efbabee845567198f898804a8aeffdbedb690fcfd42e8c038",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5687251",
    "total": "5687251"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5687251",
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
            "amount": "45537646222"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5687"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMzQwYTllNy0yZDE0LTUwNGEtOTlhNi00MjNlOTBkNTVmOGYifQ==",
    "nonce": 6856,
    "balances": {
      "current": "12972135909730002",
      "previous": "12972135915422940"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x382a86b632608dd0851ef9feb644998100dbdd89",
    "nonce": 22,
    "balances": {
      "current": "5687251",
      "previous": "0"
    }
  },
  "blockNumber": "10114717",
  "created": "2020-05-22T08:52:07.952Z",
  "updated": "2020-05-22T08:52:09.024Z",
  "id": "5ec792b7005df800101bcb34"
}
```
* *stageAmount*: `5687251`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000056c7d3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000056c7d3000000000000000000000000000000000000000000000000000000000056c7d37c61fcc24fbb192858bdd8a9ef4f51fad66c0be55a9565607ebb7843dbf3c6d5f187b1a9dc2a8c76bb98bb50b437d3734d0740d3af2c7edd97b0e2cf670c28f75e4ef37d237d0c4508a8a4e922eb4e2aeb0b3fc7faf802b231bed26687ec78b1000000000000000000000000000000000000000000000000000000000000001b4967bc1667cf80cb9e635939722bd291db06713cf67c5de364af1815dde7e27a08439e2c2b49cd0efbabee845567198f898804a8aeffdbedb690fcfd42e8c03843d09d504d3aa35063d320b867994c67b766c5efbd1b547195e21f37f0c9d63c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ac800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1616c0e0a6d2000000000000000000000000000000000000000000000000002e1616c13784dc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000001637000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9a41568e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a517759546c6c4e7930795a4445304c5455774e4745744f546c684e6930304d6a4e6c4f54426b4e54566d4f47596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000382a86b632608dd0851ef9feb644998100dbdd89000000000000000000000000000000000000000000000000000000000056c7d3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c61fcc24fbb192858bdd8a9ef4f51fad66c0be55a9565607ebb7843dbf3c6d5",
      "signature": {
        "s": "0x5e4ef37d237d0c4508a8a4e922eb4e2aeb0b3fc7faf802b231bed26687ec78b1",
        "r": "0xf187b1a9dc2a8c76bb98bb50b437d3734d0740d3af2c7edd97b0e2cf670c28f7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4967bc1667cf80cb9e635939722bd291db06713cf67c5de364af1815dde7e27a",
      "signature": {
        "s": "0x43d09d504d3aa35063d320b867994c67b766c5efbd1b547195e21f37f0c9d63c",
        "r": "0x08439e2c2b49cd0efbabee845567198f898804a8aeffdbedb690fcfd42e8c038",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5687251",
    "total": "5687251"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5687251",
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
            "amount": "45537646222"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5687"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMzQwYTllNy0yZDE0LTUwNGEtOTlhNi00MjNlOTBkNTVmOGYifQ==",
    "nonce": 6856,
    "balances": {
      "current": "12972135909730002",
      "previous": "12972135915422940"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x382a86b632608dd0851ef9feb644998100dbdd89",
    "nonce": 22,
    "balances": {
      "current": "5687251",
      "previous": "0"
    }
  },
  "blockNumber": "10114717",
  "created": "2020-05-22T08:52:07.952Z",
  "updated": "2020-05-22T08:52:09.024Z",
  "id": "5ec792b7005df800101bcb34"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000056c7d3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5687251`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`