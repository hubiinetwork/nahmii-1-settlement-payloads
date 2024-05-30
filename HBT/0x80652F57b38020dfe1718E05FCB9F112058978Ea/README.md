# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x80652F57b38020dfe1718E05FCB9F112058978Ea`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000002fcaf141500000000000000000000000000000000000000000000000000000002fcaf1415000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002fcaf141500000000000000000000000000000000000000000000000000000002fcaf141519d0e84e53a0601f63a2967d3d262d7393b3ae15485aa7463900f21203f54bd7fe0309a00b1a7c4a28cbeeb2f2506a1042509d213efc5b3c35b5e8f9de68697e4ee1b8cd2bc7b499d70618f092b97a389201e2987bef38377ad0f2cf784c2730000000000000000000000000000000000000000000000000000000000000001baf4971899ed64706d95a40fc571fc8a0fa34c3d41dccf475a611b29448270fb3952b2d312f7acae89bcb4ea843d70d9bba31c3949f734028289503f26990351a0cebf079e29e2f07f3e2d2201cb2c1aec9302b2f940e6fa98ec8396730d5c51b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b9b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e153bf41f9166000000000000000000000000000000000000000000000000002e153ef19267cd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000c3c252000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ad23646d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b596d51334e32553059533077593245314c5455344e446b7459546b355a43316c595755324d4745795a4463345954496966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000080652f57b38020dfe1718e05fcb9f112058978ea00000000000000000000000000000000000000000000000000000002fcaf1415000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x19d0e84e53a0601f63a2967d3d262d7393b3ae15485aa7463900f21203f54bd7",
      "signature": {
        "s": "0x4ee1b8cd2bc7b499d70618f092b97a389201e2987bef38377ad0f2cf784c2730",
        "r": "0xfe0309a00b1a7c4a28cbeeb2f2506a1042509d213efc5b3c35b5e8f9de68697e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaf4971899ed64706d95a40fc571fc8a0fa34c3d41dccf475a611b29448270fb3",
      "signature": {
        "s": "0x0cebf079e29e2f07f3e2d2201cb2c1aec9302b2f940e6fa98ec8396730d5c51b",
        "r": "0x952b2d312f7acae89bcb4ea843d70d9bba31c3949f734028289503f26990351a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "12829266965",
    "total": "12829266965"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12829266965",
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
            "amount": "46476445400"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "12829266"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkYmQ3N2U0YS0wY2E1LTU4NDktYTk5ZC1lYWU2MGEyZDc4YTIifQ==",
    "nonce": 7067,
    "balances": {
      "current": "12971196171653478",
      "previous": "12971209013749709"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x80652f57b38020dfe1718e05fcb9f112058978ea",
    "nonce": 22,
    "balances": {
      "current": "12829266965",
      "previous": "0"
    }
  },
  "blockNumber": "10114729",
  "created": "2020-05-22T08:53:50.400Z",
  "updated": "2020-05-22T08:53:50.458Z",
  "id": "5ec7931ee5756b00111b886e"
}
```
* *stageAmount*: `12829266965`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000002fcaf1415000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002fcaf141500000000000000000000000000000000000000000000000000000002fcaf141519d0e84e53a0601f63a2967d3d262d7393b3ae15485aa7463900f21203f54bd7fe0309a00b1a7c4a28cbeeb2f2506a1042509d213efc5b3c35b5e8f9de68697e4ee1b8cd2bc7b499d70618f092b97a389201e2987bef38377ad0f2cf784c2730000000000000000000000000000000000000000000000000000000000000001baf4971899ed64706d95a40fc571fc8a0fa34c3d41dccf475a611b29448270fb3952b2d312f7acae89bcb4ea843d70d9bba31c3949f734028289503f26990351a0cebf079e29e2f07f3e2d2201cb2c1aec9302b2f940e6fa98ec8396730d5c51b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b9b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e153bf41f9166000000000000000000000000000000000000000000000000002e153ef19267cd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000c3c252000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ad23646d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b596d51334e32553059533077593245314c5455344e446b7459546b355a43316c595755324d4745795a4463345954496966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000080652f57b38020dfe1718e05fcb9f112058978ea00000000000000000000000000000000000000000000000000000002fcaf1415000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x19d0e84e53a0601f63a2967d3d262d7393b3ae15485aa7463900f21203f54bd7",
      "signature": {
        "s": "0x4ee1b8cd2bc7b499d70618f092b97a389201e2987bef38377ad0f2cf784c2730",
        "r": "0xfe0309a00b1a7c4a28cbeeb2f2506a1042509d213efc5b3c35b5e8f9de68697e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaf4971899ed64706d95a40fc571fc8a0fa34c3d41dccf475a611b29448270fb3",
      "signature": {
        "s": "0x0cebf079e29e2f07f3e2d2201cb2c1aec9302b2f940e6fa98ec8396730d5c51b",
        "r": "0x952b2d312f7acae89bcb4ea843d70d9bba31c3949f734028289503f26990351a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "12829266965",
    "total": "12829266965"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12829266965",
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
            "amount": "46476445400"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "12829266"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkYmQ3N2U0YS0wY2E1LTU4NDktYTk5ZC1lYWU2MGEyZDc4YTIifQ==",
    "nonce": 7067,
    "balances": {
      "current": "12971196171653478",
      "previous": "12971209013749709"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x80652f57b38020dfe1718e05fcb9f112058978ea",
    "nonce": 22,
    "balances": {
      "current": "12829266965",
      "previous": "0"
    }
  },
  "blockNumber": "10114729",
  "created": "2020-05-22T08:53:50.400Z",
  "updated": "2020-05-22T08:53:50.458Z",
  "id": "5ec7931ee5756b00111b886e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000002fcaf1415000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `12829266965`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`