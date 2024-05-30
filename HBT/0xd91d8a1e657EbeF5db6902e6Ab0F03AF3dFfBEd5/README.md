# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd91d8a1e657EbeF5db6902e6Ab0F03AF3dFfBEd5`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000001a7d28f0000000000000000000000000000000000000000000000000000000001a7d28f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000001a7d28f0000000000000000000000000000000000000000000000000000000001a7d28feb5f931b8917fbcae063725eb2083e04b36f769907be9c7248e07e4f6daed5ede8e429ce013da1188b9610a8812898956601add2aecdd9131556a80dc90c51dc3aec79cd8ddc297686df62289318d9ac9569d2f8bdd5bce3803ef737e40700f4000000000000000000000000000000000000000000000000000000000000001ce27ff456959a4f97f4fb79fee76f9c97e75d48c7d9878d6d7c9b45e0ef5f7da045fb55c106e453fd7ef199db167eff6650209d48287ce620f22cc85931de567862df64fd54a2880c21fbdca9e8f567f3d265797fff3a1937409ada3c1cb43e56000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56880000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000187100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ab948a03393000000000000000000000000000000000000000000000000002e1ab94a4872a100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000006c7f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096ace93b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a44646c4e324d78597930314e7a63344c5455785a6a4574596a5a69596930304d444132597a526b597a4d785a6a636966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d91d8a1e657ebef5db6902e6ab0f03af3dffbed50000000000000000000000000000000000000000000000000000000001a7d28f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeb5f931b8917fbcae063725eb2083e04b36f769907be9c7248e07e4f6daed5ed",
      "signature": {
        "s": "0x3aec79cd8ddc297686df62289318d9ac9569d2f8bdd5bce3803ef737e40700f4",
        "r": "0xe8e429ce013da1188b9610a8812898956601add2aecdd9131556a80dc90c51dc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe27ff456959a4f97f4fb79fee76f9c97e75d48c7d9878d6d7c9b45e0ef5f7da0",
      "signature": {
        "s": "0x62df64fd54a2880c21fbdca9e8f567f3d265797fff3a1937409ada3c1cb43e56",
        "r": "0x45fb55c106e453fd7ef199db167eff6650209d48287ce620f22cc85931de5678",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "27775631",
    "total": "27775631"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27775631",
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
            "amount": "40446628786"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "27775"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZDdlN2MxYy01Nzc4LTUxZjEtYjZiYi00MDA2YzRkYzMxZjcifQ==",
    "nonce": 6257,
    "balances": {
      "current": "12977232018420627",
      "previous": "12977232046224033"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd91d8a1e657ebef5db6902e6ab0f03af3dffbed5",
    "nonce": 22,
    "balances": {
      "current": "27775631",
      "previous": "0"
    }
  },
  "blockNumber": "10114696",
  "created": "2020-05-22T08:47:40.694Z",
  "updated": "2020-05-22T08:47:40.846Z",
  "id": "5ec791acb0c6090011d5b0ed"
}
```
* *stageAmount*: `27775631`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000001a7d28f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000001a7d28f0000000000000000000000000000000000000000000000000000000001a7d28feb5f931b8917fbcae063725eb2083e04b36f769907be9c7248e07e4f6daed5ede8e429ce013da1188b9610a8812898956601add2aecdd9131556a80dc90c51dc3aec79cd8ddc297686df62289318d9ac9569d2f8bdd5bce3803ef737e40700f4000000000000000000000000000000000000000000000000000000000000001ce27ff456959a4f97f4fb79fee76f9c97e75d48c7d9878d6d7c9b45e0ef5f7da045fb55c106e453fd7ef199db167eff6650209d48287ce620f22cc85931de567862df64fd54a2880c21fbdca9e8f567f3d265797fff3a1937409ada3c1cb43e56000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56880000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000187100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ab948a03393000000000000000000000000000000000000000000000000002e1ab94a4872a100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000006c7f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096ace93b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a44646c4e324d78597930314e7a63344c5455785a6a4574596a5a69596930304d444132597a526b597a4d785a6a636966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d91d8a1e657ebef5db6902e6ab0f03af3dffbed50000000000000000000000000000000000000000000000000000000001a7d28f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeb5f931b8917fbcae063725eb2083e04b36f769907be9c7248e07e4f6daed5ed",
      "signature": {
        "s": "0x3aec79cd8ddc297686df62289318d9ac9569d2f8bdd5bce3803ef737e40700f4",
        "r": "0xe8e429ce013da1188b9610a8812898956601add2aecdd9131556a80dc90c51dc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe27ff456959a4f97f4fb79fee76f9c97e75d48c7d9878d6d7c9b45e0ef5f7da0",
      "signature": {
        "s": "0x62df64fd54a2880c21fbdca9e8f567f3d265797fff3a1937409ada3c1cb43e56",
        "r": "0x45fb55c106e453fd7ef199db167eff6650209d48287ce620f22cc85931de5678",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "27775631",
    "total": "27775631"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27775631",
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
            "amount": "40446628786"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "27775"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZDdlN2MxYy01Nzc4LTUxZjEtYjZiYi00MDA2YzRkYzMxZjcifQ==",
    "nonce": 6257,
    "balances": {
      "current": "12977232018420627",
      "previous": "12977232046224033"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd91d8a1e657ebef5db6902e6ab0f03af3dffbed5",
    "nonce": 22,
    "balances": {
      "current": "27775631",
      "previous": "0"
    }
  },
  "blockNumber": "10114696",
  "created": "2020-05-22T08:47:40.694Z",
  "updated": "2020-05-22T08:47:40.846Z",
  "id": "5ec791acb0c6090011d5b0ed"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000001a7d28f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `27775631`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`