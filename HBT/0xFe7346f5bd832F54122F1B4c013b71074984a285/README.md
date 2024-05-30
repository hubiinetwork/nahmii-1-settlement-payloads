# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFe7346f5bd832F54122F1B4c013b71074984a285`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000832e283000000000000000000000000000000000000000000000000000000000832e283000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000832e283000000000000000000000000000000000000000000000000000000000832e2833291ce6fc0d36fb9b2fcac8c25bb7e2e9d3915c56679fd75cd756a974122d99718ffa5a6e221ae5111682fb2c0c0b6ab96e328289f8da63a008223e801a74cfb06c06e4a136ba6291713ccd8be9aeefac2147596bbdb6fcfd98bc0a5a2af840f000000000000000000000000000000000000000000000000000000000000001b8ec0248bb87e88e13e31369e67f6e7f19779d83215d39eefd6f42b0de970cb1ca06f067e5434645a7d9ad0e60b81b7fad4ad7124f0a3aef1379200223577928f0c1a7469557b1ceb8236791c55c4886a964652c300d69a226ad65a035dab2182000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001aba00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1619f912041a000000000000000000000000000000000000000000000000002e161a0146ffed00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000021950000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a996e8e3c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d6a6b334d6d4a685a6930794d7a4a694c5455794e6a49744f4441324f5330784d6d4a6d5a54417a4e4449344e6a456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fe7346f5bd832f54122f1b4c013b71074984a285000000000000000000000000000000000000000000000000000000000832e283000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3291ce6fc0d36fb9b2fcac8c25bb7e2e9d3915c56679fd75cd756a974122d997",
      "signature": {
        "s": "0x06c06e4a136ba6291713ccd8be9aeefac2147596bbdb6fcfd98bc0a5a2af840f",
        "r": "0x18ffa5a6e221ae5111682fb2c0c0b6ab96e328289f8da63a008223e801a74cfb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8ec0248bb87e88e13e31369e67f6e7f19779d83215d39eefd6f42b0de970cb1c",
      "signature": {
        "s": "0x0c1a7469557b1ceb8236791c55c4886a964652c300d69a226ad65a035dab2182",
        "r": "0xa06f067e5434645a7d9ad0e60b81b7fad4ad7124f0a3aef1379200223577928f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "137552515",
    "total": "137552515"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "137552515",
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
            "amount": "45523832380"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "137552"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMjk3MmJhZi0yMzJiLTUyNjItODA2OS0xMmJmZTAzNDI4NjEifQ==",
    "nonce": 6842,
    "balances": {
      "current": "12972149737391130",
      "previous": "12972149875081197"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe7346f5bd832f54122f1b4c013b71074984a285",
    "nonce": 22,
    "balances": {
      "current": "137552515",
      "previous": "0"
    }
  },
  "blockNumber": "10114717",
  "created": "2020-05-22T08:52:04.135Z",
  "updated": "2020-05-22T08:52:04.241Z",
  "id": "5ec792b4e5756b00111b8828"
}
```
* *stageAmount*: `137552515`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000832e283000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000832e283000000000000000000000000000000000000000000000000000000000832e2833291ce6fc0d36fb9b2fcac8c25bb7e2e9d3915c56679fd75cd756a974122d99718ffa5a6e221ae5111682fb2c0c0b6ab96e328289f8da63a008223e801a74cfb06c06e4a136ba6291713ccd8be9aeefac2147596bbdb6fcfd98bc0a5a2af840f000000000000000000000000000000000000000000000000000000000000001b8ec0248bb87e88e13e31369e67f6e7f19779d83215d39eefd6f42b0de970cb1ca06f067e5434645a7d9ad0e60b81b7fad4ad7124f0a3aef1379200223577928f0c1a7469557b1ceb8236791c55c4886a964652c300d69a226ad65a035dab2182000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001aba00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1619f912041a000000000000000000000000000000000000000000000000002e161a0146ffed00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000021950000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a996e8e3c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d6a6b334d6d4a685a6930794d7a4a694c5455794e6a49744f4441324f5330784d6d4a6d5a54417a4e4449344e6a456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fe7346f5bd832f54122f1b4c013b71074984a285000000000000000000000000000000000000000000000000000000000832e283000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3291ce6fc0d36fb9b2fcac8c25bb7e2e9d3915c56679fd75cd756a974122d997",
      "signature": {
        "s": "0x06c06e4a136ba6291713ccd8be9aeefac2147596bbdb6fcfd98bc0a5a2af840f",
        "r": "0x18ffa5a6e221ae5111682fb2c0c0b6ab96e328289f8da63a008223e801a74cfb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8ec0248bb87e88e13e31369e67f6e7f19779d83215d39eefd6f42b0de970cb1c",
      "signature": {
        "s": "0x0c1a7469557b1ceb8236791c55c4886a964652c300d69a226ad65a035dab2182",
        "r": "0xa06f067e5434645a7d9ad0e60b81b7fad4ad7124f0a3aef1379200223577928f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "137552515",
    "total": "137552515"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "137552515",
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
            "amount": "45523832380"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "137552"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMjk3MmJhZi0yMzJiLTUyNjItODA2OS0xMmJmZTAzNDI4NjEifQ==",
    "nonce": 6842,
    "balances": {
      "current": "12972149737391130",
      "previous": "12972149875081197"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe7346f5bd832f54122f1b4c013b71074984a285",
    "nonce": 22,
    "balances": {
      "current": "137552515",
      "previous": "0"
    }
  },
  "blockNumber": "10114717",
  "created": "2020-05-22T08:52:04.135Z",
  "updated": "2020-05-22T08:52:04.241Z",
  "id": "5ec792b4e5756b00111b8828"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000832e283000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `137552515`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`