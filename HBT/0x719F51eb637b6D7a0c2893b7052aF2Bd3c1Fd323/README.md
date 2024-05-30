# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x719F51eb637b6D7a0c2893b7052aF2Bd3c1Fd323`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000001a7d5920000000000000000000000000000000000000000000000000000000001a7d592000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000001a7d5920000000000000000000000000000000000000000000000000000000001a7d59255ddd1be8b16a481c6c5f90dbd4740f08240519df116d24b002915f15d63a254998bdd47529732bb4ab75df2db4565a4310c2379b9baa311668c89c0b960f3653b62b31e4631a13ddf5d6fbfa04de28fe2f4787814fb01ac992fb346782153f0000000000000000000000000000000000000000000000000000000000000001b0271fd26cefd3136693037f52066db48b5631ccf007c2b4103c1cd804dfe570f24686a6d8de5c940ce465f50e4c2936439eda3cbd4cd8c749b4da863577940fe0799bcaee6f74684e62067aa52ab3bcdae045fe1c7d5eaa68cd818f21e4a63fa000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a566a000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015b700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d4e05ff258a000000000000000000000000000000000000000000000000002e1d4e07a7679c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000006c80000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c1d39a05000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e3249344f5463315a6930334d54426c4c5456694d7a55744f4445794e4331694e6a67324d4449355a474934596a416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000719f51eb637b6d7a0c2893b7052af2bd3c1fd3230000000000000000000000000000000000000000000000000000000001a7d592000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x55ddd1be8b16a481c6c5f90dbd4740f08240519df116d24b002915f15d63a254",
      "signature": {
        "s": "0x3b62b31e4631a13ddf5d6fbfa04de28fe2f4787814fb01ac992fb346782153f0",
        "r": "0x998bdd47529732bb4ab75df2db4565a4310c2379b9baa311668c89c0b960f365",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0271fd26cefd3136693037f52066db48b5631ccf007c2b4103c1cd804dfe570f",
      "signature": {
        "s": "0x0799bcaee6f74684e62067aa52ab3bcdae045fe1c7d5eaa68cd818f21e4a63fa",
        "r": "0x24686a6d8de5c940ce465f50e4c2936439eda3cbd4cd8c749b4da863577940fe",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "27776402",
    "total": "27776402"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27776402",
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
            "amount": "37611608581"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "27776"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5N2I4OTc1Zi03MTBlLTViMzUtODEyNC1iNjg2MDI5ZGI4YjAifQ==",
    "nonce": 5559,
    "balances": {
      "current": "12980069873952138",
      "previous": "12980069901756316"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x719f51eb637b6d7a0c2893b7052af2bd3c1fd323",
    "nonce": 22,
    "balances": {
      "current": "27776402",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:42:06.889Z",
  "updated": "2020-05-22T08:42:06.953Z",
  "id": "5ec7905e005df800101bc97b"
}
```
* *stageAmount*: `27776402`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000001a7d592000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000001a7d5920000000000000000000000000000000000000000000000000000000001a7d59255ddd1be8b16a481c6c5f90dbd4740f08240519df116d24b002915f15d63a254998bdd47529732bb4ab75df2db4565a4310c2379b9baa311668c89c0b960f3653b62b31e4631a13ddf5d6fbfa04de28fe2f4787814fb01ac992fb346782153f0000000000000000000000000000000000000000000000000000000000000001b0271fd26cefd3136693037f52066db48b5631ccf007c2b4103c1cd804dfe570f24686a6d8de5c940ce465f50e4c2936439eda3cbd4cd8c749b4da863577940fe0799bcaee6f74684e62067aa52ab3bcdae045fe1c7d5eaa68cd818f21e4a63fa000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a566a000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015b700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d4e05ff258a000000000000000000000000000000000000000000000000002e1d4e07a7679c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000006c80000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c1d39a05000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e3249344f5463315a6930334d54426c4c5456694d7a55744f4445794e4331694e6a67324d4449355a474934596a416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000719f51eb637b6d7a0c2893b7052af2bd3c1fd3230000000000000000000000000000000000000000000000000000000001a7d592000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x55ddd1be8b16a481c6c5f90dbd4740f08240519df116d24b002915f15d63a254",
      "signature": {
        "s": "0x3b62b31e4631a13ddf5d6fbfa04de28fe2f4787814fb01ac992fb346782153f0",
        "r": "0x998bdd47529732bb4ab75df2db4565a4310c2379b9baa311668c89c0b960f365",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0271fd26cefd3136693037f52066db48b5631ccf007c2b4103c1cd804dfe570f",
      "signature": {
        "s": "0x0799bcaee6f74684e62067aa52ab3bcdae045fe1c7d5eaa68cd818f21e4a63fa",
        "r": "0x24686a6d8de5c940ce465f50e4c2936439eda3cbd4cd8c749b4da863577940fe",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "27776402",
    "total": "27776402"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27776402",
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
            "amount": "37611608581"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "27776"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5N2I4OTc1Zi03MTBlLTViMzUtODEyNC1iNjg2MDI5ZGI4YjAifQ==",
    "nonce": 5559,
    "balances": {
      "current": "12980069873952138",
      "previous": "12980069901756316"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x719f51eb637b6d7a0c2893b7052af2bd3c1fd323",
    "nonce": 22,
    "balances": {
      "current": "27776402",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:42:06.889Z",
  "updated": "2020-05-22T08:42:06.953Z",
  "id": "5ec7905e005df800101bc97b"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000001a7d592000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `27776402`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`