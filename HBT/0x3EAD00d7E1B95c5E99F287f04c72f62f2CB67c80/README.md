# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3EAD00d7E1B95c5E99F287f04c72f62f2CB67c80`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000188df69c20000000000000000000000000000000000000000000000000000000188df69c2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000188df69c20000000000000000000000000000000000000000000000000000000188df69c270a4ab3c15e7035f5b04e64b3e799f8f1da08a9e73cba32e4b6912bd5205224c60cacaaa4bd62db643ee3116840617bdcfdcce10ac506eb1e787497db3b3004a210eb1b68cf5387a8dd3b9299461dcd8898115ebbdc91192e65a285c5d17a7cb000000000000000000000000000000000000000000000000000000000000001cc45c8d6d236502b80acc03e8747afb3e1b60f96a3205ffecfa3d697148ff4a2a47e1bb7521e9adc361c37632fa36a62192688a0c7a5c341544f2988fbea6e68b45a49b3f1e4e97f3cc97794c509f8a8a51fe27780048afe5c98f82f30b13b212000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000169e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b7ce8f4e339000000000000000000000000000000000000000000000000002e1b7e7238e04900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064934e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000938c6d2d1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a546732596d4d774d79307a597a4d304c5455335a6a51744f5456694e43303359544d77593255784e7a45774f47516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003ead00d7e1b95c5e99f287f04c72f62f2cb67c800000000000000000000000000000000000000000000000000000000188df69c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x70a4ab3c15e7035f5b04e64b3e799f8f1da08a9e73cba32e4b6912bd5205224c",
      "signature": {
        "s": "0x210eb1b68cf5387a8dd3b9299461dcd8898115ebbdc91192e65a285c5d17a7cb",
        "r": "0x60cacaaa4bd62db643ee3116840617bdcfdcce10ac506eb1e787497db3b3004a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc45c8d6d236502b80acc03e8747afb3e1b60f96a3205ffecfa3d697148ff4a2a",
      "signature": {
        "s": "0x45a49b3f1e4e97f3cc97794c509f8a8a51fe27780048afe5c98f82f30b13b212",
        "r": "0x47e1bb7521e9adc361c37632fa36a62192688a0c7a5c341544f2988fbea6e68b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6591310274",
    "total": "6591310274"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6591310274",
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
            "amount": "39607259857"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6591310"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZTg2YmMwMy0zYzM0LTU3ZjQtOTViNC03YTMwY2UxNzEwOGQifQ==",
    "nonce": 5790,
    "balances": {
      "current": "12978072226947897",
      "previous": "12978078824849481"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ead00d7e1b95c5e99f287f04c72f62f2cb67c80",
    "nonce": 22,
    "balances": {
      "current": "6591310274",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:55.282Z",
  "updated": "2020-05-22T08:43:55.352Z",
  "id": "5ec790cbb0c6090011d5b04a"
}
```
* *stageAmount*: `6591310274`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000188df69c2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000188df69c20000000000000000000000000000000000000000000000000000000188df69c270a4ab3c15e7035f5b04e64b3e799f8f1da08a9e73cba32e4b6912bd5205224c60cacaaa4bd62db643ee3116840617bdcfdcce10ac506eb1e787497db3b3004a210eb1b68cf5387a8dd3b9299461dcd8898115ebbdc91192e65a285c5d17a7cb000000000000000000000000000000000000000000000000000000000000001cc45c8d6d236502b80acc03e8747afb3e1b60f96a3205ffecfa3d697148ff4a2a47e1bb7521e9adc361c37632fa36a62192688a0c7a5c341544f2988fbea6e68b45a49b3f1e4e97f3cc97794c509f8a8a51fe27780048afe5c98f82f30b13b212000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000169e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b7ce8f4e339000000000000000000000000000000000000000000000000002e1b7e7238e04900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064934e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000938c6d2d1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a546732596d4d774d79307a597a4d304c5455335a6a51744f5456694e43303359544d77593255784e7a45774f47516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003ead00d7e1b95c5e99f287f04c72f62f2cb67c800000000000000000000000000000000000000000000000000000000188df69c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x70a4ab3c15e7035f5b04e64b3e799f8f1da08a9e73cba32e4b6912bd5205224c",
      "signature": {
        "s": "0x210eb1b68cf5387a8dd3b9299461dcd8898115ebbdc91192e65a285c5d17a7cb",
        "r": "0x60cacaaa4bd62db643ee3116840617bdcfdcce10ac506eb1e787497db3b3004a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc45c8d6d236502b80acc03e8747afb3e1b60f96a3205ffecfa3d697148ff4a2a",
      "signature": {
        "s": "0x45a49b3f1e4e97f3cc97794c509f8a8a51fe27780048afe5c98f82f30b13b212",
        "r": "0x47e1bb7521e9adc361c37632fa36a62192688a0c7a5c341544f2988fbea6e68b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6591310274",
    "total": "6591310274"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6591310274",
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
            "amount": "39607259857"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6591310"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZTg2YmMwMy0zYzM0LTU3ZjQtOTViNC03YTMwY2UxNzEwOGQifQ==",
    "nonce": 5790,
    "balances": {
      "current": "12978072226947897",
      "previous": "12978078824849481"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ead00d7e1b95c5e99f287f04c72f62f2cb67c80",
    "nonce": 22,
    "balances": {
      "current": "6591310274",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:55.282Z",
  "updated": "2020-05-22T08:43:55.352Z",
  "id": "5ec790cbb0c6090011d5b04a"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000188df69c2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6591310274`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`