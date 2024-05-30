# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0f63f47a2ac52a42e3de279b48F0F4C1473c0c7c`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000009daab0ea000000000000000000000000000000000000000000000000000000009daab0ea000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009daab0ea000000000000000000000000000000000000000000000000000000009daab0ea8b47a3d991f7ea08b94a51b36121406a5c721abdf7b75ac5b04ffe58e7daec6a4813fb9179d7484eb90a35a793dc7243790582e13fbe6d8471673e7f174f5f086eea54a5c63d37d733c706c24129ceb189f8097e2b7653b1b7096e5c06fb743a000000000000000000000000000000000000000000000000000000000000001b7c0f83ddaade397f6066eefc33dccd77ff9389988e99e33942eab8e46262c2dfe85b05316ea8f7231cbb3744e7a86c0c153f70fc2a414f253c7cf2716395bf980cbd4edcd904f7d1582f92fe5e475f7409443ba1d56bb4fd4ea1e938e1ced786000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56aa00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bb000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15079e3793c4000000000000000000000000000000000000000000000000002e15083c0aa18700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000285cd9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000adf98b6d2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e324a6a5a6a42695a69316b4e44426a4c5455355a4759744f44426d4f4330354e3251794d574d344f4451344d44676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000f63f47a2ac52a42e3de279b48f0f4c1473c0c7c000000000000000000000000000000000000000000000000000000009daab0ea000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8b47a3d991f7ea08b94a51b36121406a5c721abdf7b75ac5b04ffe58e7daec6a",
      "signature": {
        "s": "0x6eea54a5c63d37d733c706c24129ceb189f8097e2b7653b1b7096e5c06fb743a",
        "r": "0x4813fb9179d7484eb90a35a793dc7243790582e13fbe6d8471673e7f174f5f08",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7c0f83ddaade397f6066eefc33dccd77ff9389988e99e33942eab8e46262c2df",
      "signature": {
        "s": "0x0cbd4edcd904f7d1582f92fe5e475f7409443ba1d56bb4fd4ea1e938e1ced786",
        "r": "0xe85b05316ea8f7231cbb3744e7a86c0c153f70fc2a414f253c7cf2716395bf98",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2645209322",
    "total": "2645209322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2645209322",
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
            "amount": "46701000402"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2645209"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmN2JjZjBiZi1kNDBjLTU5ZGYtODBmOC05N2QyMWM4ODQ4MDgifQ==",
    "nonce": 7088,
    "balances": {
      "current": "12970971392086980",
      "previous": "12970974039941511"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0f63f47a2ac52a42e3de279b48f0f4c1473c0c7c",
    "nonce": 22,
    "balances": {
      "current": "2645209322",
      "previous": "0"
    }
  },
  "blockNumber": "10114730",
  "created": "2020-05-22T08:54:11.652Z",
  "updated": "2020-05-22T08:54:11.732Z",
  "id": "5ec79333b0c6090011d5b210"
}
```
* *stageAmount*: `2645209322`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000009daab0ea000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009daab0ea000000000000000000000000000000000000000000000000000000009daab0ea8b47a3d991f7ea08b94a51b36121406a5c721abdf7b75ac5b04ffe58e7daec6a4813fb9179d7484eb90a35a793dc7243790582e13fbe6d8471673e7f174f5f086eea54a5c63d37d733c706c24129ceb189f8097e2b7653b1b7096e5c06fb743a000000000000000000000000000000000000000000000000000000000000001b7c0f83ddaade397f6066eefc33dccd77ff9389988e99e33942eab8e46262c2dfe85b05316ea8f7231cbb3744e7a86c0c153f70fc2a414f253c7cf2716395bf980cbd4edcd904f7d1582f92fe5e475f7409443ba1d56bb4fd4ea1e938e1ced786000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56aa00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bb000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15079e3793c4000000000000000000000000000000000000000000000000002e15083c0aa18700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000285cd9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000adf98b6d2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e324a6a5a6a42695a69316b4e44426a4c5455355a4759744f44426d4f4330354e3251794d574d344f4451344d44676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000f63f47a2ac52a42e3de279b48f0f4c1473c0c7c000000000000000000000000000000000000000000000000000000009daab0ea000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8b47a3d991f7ea08b94a51b36121406a5c721abdf7b75ac5b04ffe58e7daec6a",
      "signature": {
        "s": "0x6eea54a5c63d37d733c706c24129ceb189f8097e2b7653b1b7096e5c06fb743a",
        "r": "0x4813fb9179d7484eb90a35a793dc7243790582e13fbe6d8471673e7f174f5f08",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7c0f83ddaade397f6066eefc33dccd77ff9389988e99e33942eab8e46262c2df",
      "signature": {
        "s": "0x0cbd4edcd904f7d1582f92fe5e475f7409443ba1d56bb4fd4ea1e938e1ced786",
        "r": "0xe85b05316ea8f7231cbb3744e7a86c0c153f70fc2a414f253c7cf2716395bf98",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2645209322",
    "total": "2645209322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2645209322",
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
            "amount": "46701000402"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2645209"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmN2JjZjBiZi1kNDBjLTU5ZGYtODBmOC05N2QyMWM4ODQ4MDgifQ==",
    "nonce": 7088,
    "balances": {
      "current": "12970971392086980",
      "previous": "12970974039941511"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0f63f47a2ac52a42e3de279b48f0f4c1473c0c7c",
    "nonce": 22,
    "balances": {
      "current": "2645209322",
      "previous": "0"
    }
  },
  "blockNumber": "10114730",
  "created": "2020-05-22T08:54:11.652Z",
  "updated": "2020-05-22T08:54:11.732Z",
  "id": "5ec79333b0c6090011d5b210"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000009daab0ea000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2645209322`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`