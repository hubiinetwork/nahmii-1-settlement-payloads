# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1E94417d938f2275742aA4ABCF1603c9028efA97`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000002000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000291b855b4728a2f8a2d53a296f72198a8fcd996470ae6ce877a60cead08ed0eba8a177e69d36eea984e3e01d066a9ba487d625f19e32fb31d0b1a165f10a574d94bbabeceb54f756958cc72fc61830c9eb74f9b5a7b437b96c31f5f38c8b69c17000000000000000000000000000000000000000000000000000000000000001b5d52ea948e17b95f861f346baf7dc80181a906f9c7da460c6d11f72bfcd4d13d8fa7357487e6a3e7e0f6e756de1682e6c0a350e4b66f84e44673b7cea91aa00511d5a6e7f5cbb65d246a5ea8954b2b9402753120bdd722382be54777eb1339de000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56930000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000195a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e83f0d77ea000000000000000000000000000000000000000000000000002e17e83f0d77ed00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2335469b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5451795a6a4a694d793032597a466a4c5455334e6d5574595463794f53316c4f4467784d6a5a694d3245354d44496966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000001e94417d938f2275742aa4abcf1603c9028efa970000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91b855b4728a2f8a2d53a296f72198a8fcd996470ae6ce877a60cead08ed0eba",
      "signature": {
        "s": "0x4bbabeceb54f756958cc72fc61830c9eb74f9b5a7b437b96c31f5f38c8b69c17",
        "r": "0x8a177e69d36eea984e3e01d066a9ba487d625f19e32fb31d0b1a165f10a574d9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5d52ea948e17b95f861f346baf7dc80181a906f9c7da460c6d11f72bfcd4d13d",
      "signature": {
        "s": "0x11d5a6e7f5cbb65d246a5ea8954b2b9402753120bdd722382be54777eb1339de",
        "r": "0x8fa7357487e6a3e7e0f6e756de1682e6c0a350e4b66f84e44673b7cea91aa005",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2",
    "total": "2"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2",
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
            "amount": "43540367003"
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
    "data": "eyJyZWYiOiI3ZTQyZjJiMy02YzFjLTU3NmUtYTcyOS1lODgxMjZiM2E5MDIifQ==",
    "nonce": 6490,
    "balances": {
      "current": "12974135186388970",
      "previous": "12974135186388973"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1e94417d938f2275742aa4abcf1603c9028efa97",
    "nonce": 21,
    "balances": {
      "current": "2",
      "previous": "0"
    }
  },
  "blockNumber": "10114707",
  "created": "2020-05-22T08:49:30.661Z",
  "updated": "2020-05-22T08:49:30.730Z",
  "id": "5ec7921ae5756b00111b87bc"
}
```
* *stageAmount*: `2`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000002000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000291b855b4728a2f8a2d53a296f72198a8fcd996470ae6ce877a60cead08ed0eba8a177e69d36eea984e3e01d066a9ba487d625f19e32fb31d0b1a165f10a574d94bbabeceb54f756958cc72fc61830c9eb74f9b5a7b437b96c31f5f38c8b69c17000000000000000000000000000000000000000000000000000000000000001b5d52ea948e17b95f861f346baf7dc80181a906f9c7da460c6d11f72bfcd4d13d8fa7357487e6a3e7e0f6e756de1682e6c0a350e4b66f84e44673b7cea91aa00511d5a6e7f5cbb65d246a5ea8954b2b9402753120bdd722382be54777eb1339de000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56930000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000195a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e83f0d77ea000000000000000000000000000000000000000000000000002e17e83f0d77ed00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2335469b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5451795a6a4a694d793032597a466a4c5455334e6d5574595463794f53316c4f4467784d6a5a694d3245354d44496966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000001e94417d938f2275742aa4abcf1603c9028efa970000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91b855b4728a2f8a2d53a296f72198a8fcd996470ae6ce877a60cead08ed0eba",
      "signature": {
        "s": "0x4bbabeceb54f756958cc72fc61830c9eb74f9b5a7b437b96c31f5f38c8b69c17",
        "r": "0x8a177e69d36eea984e3e01d066a9ba487d625f19e32fb31d0b1a165f10a574d9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5d52ea948e17b95f861f346baf7dc80181a906f9c7da460c6d11f72bfcd4d13d",
      "signature": {
        "s": "0x11d5a6e7f5cbb65d246a5ea8954b2b9402753120bdd722382be54777eb1339de",
        "r": "0x8fa7357487e6a3e7e0f6e756de1682e6c0a350e4b66f84e44673b7cea91aa005",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2",
    "total": "2"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2",
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
            "amount": "43540367003"
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
    "data": "eyJyZWYiOiI3ZTQyZjJiMy02YzFjLTU3NmUtYTcyOS1lODgxMjZiM2E5MDIifQ==",
    "nonce": 6490,
    "balances": {
      "current": "12974135186388970",
      "previous": "12974135186388973"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1e94417d938f2275742aa4abcf1603c9028efa97",
    "nonce": 21,
    "balances": {
      "current": "2",
      "previous": "0"
    }
  },
  "blockNumber": "10114707",
  "created": "2020-05-22T08:49:30.661Z",
  "updated": "2020-05-22T08:49:30.730Z",
  "id": "5ec7921ae5756b00111b87bc"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`