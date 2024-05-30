# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC178204eDaC25F3b51846D70a37b800cEa33d467`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000018d561680000000000000000000000000000000000000000000000000000000018d56168000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000018d561680000000000000000000000000000000000000000000000000000000018d561689a62220ac10f81275e6876e98f377a30cda8ebf9c75a801022445836a2b1969003d1bfbdf1f8402ee46c2c5203de2d899b054170537dfb0cd5bee506e3b72c542c2ec981b64f177a5103241166fd2d0df71f822dd1a1fd86f20acfe740e35c0c000000000000000000000000000000000000000000000000000000000000001c807b0a8b7a001fadf4d4e2147d257b78eeb82baf908a219dee3c87a798327f9784c14c33fc3c6d1e6bf7af4b120b6c9e82ca8ebd144278b9d27abbcead973ede52ca0d2fd21b378feec684bd449bcf7a94e71781e6cb048ad2f43c4dcec8f991000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5680000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017cb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b10cb89df07000000000000000000000000000000000000000000000000002e1b10e4659bec00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000065b7d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009546d2974000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d4759795a6a4d315a4330314d7a4d304c5455334d6a4574596a63344f5330314d444e6d4e7a4a6b4e6a646d4f54556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c178204edac25f3b51846d70a37b800cea33d4670000000000000000000000000000000000000000000000000000000018d56168000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9a62220ac10f81275e6876e98f377a30cda8ebf9c75a801022445836a2b19690",
      "signature": {
        "s": "0x2c2ec981b64f177a5103241166fd2d0df71f822dd1a1fd86f20acfe740e35c0c",
        "r": "0x03d1bfbdf1f8402ee46c2c5203de2d899b054170537dfb0cd5bee506e3b72c54",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x807b0a8b7a001fadf4d4e2147d257b78eeb82baf908a219dee3c87a798327f97",
      "signature": {
        "s": "0x52ca0d2fd21b378feec684bd449bcf7a94e71781e6cb048ad2f43c4dcec8f991",
        "r": "0x84c14c33fc3c6d1e6bf7af4b120b6c9e82ca8ebd144278b9d27abbcead973ede",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "416637288",
    "total": "416637288"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "416637288",
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
            "amount": "40071145844"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "416637"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMGYyZjM1ZC01MzM0LTU3MjEtYjc4OS01MDNmNzJkNjdmOTUifQ==",
    "nonce": 6091,
    "balances": {
      "current": "12977607876927239",
      "previous": "12977608293981164"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc178204edac25f3b51846d70a37b800cea33d467",
    "nonce": 22,
    "balances": {
      "current": "416637288",
      "previous": "0"
    }
  },
  "blockNumber": "10114688",
  "created": "2020-05-22T08:46:22.141Z",
  "updated": "2020-05-22T08:46:22.212Z",
  "id": "5ec7915eb0c6090011d5b0b4"
}
```
* *stageAmount*: `416637288`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000018d56168000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000018d561680000000000000000000000000000000000000000000000000000000018d561689a62220ac10f81275e6876e98f377a30cda8ebf9c75a801022445836a2b1969003d1bfbdf1f8402ee46c2c5203de2d899b054170537dfb0cd5bee506e3b72c542c2ec981b64f177a5103241166fd2d0df71f822dd1a1fd86f20acfe740e35c0c000000000000000000000000000000000000000000000000000000000000001c807b0a8b7a001fadf4d4e2147d257b78eeb82baf908a219dee3c87a798327f9784c14c33fc3c6d1e6bf7af4b120b6c9e82ca8ebd144278b9d27abbcead973ede52ca0d2fd21b378feec684bd449bcf7a94e71781e6cb048ad2f43c4dcec8f991000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5680000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017cb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b10cb89df07000000000000000000000000000000000000000000000000002e1b10e4659bec00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000065b7d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009546d2974000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d4759795a6a4d315a4330314d7a4d304c5455334d6a4574596a63344f5330314d444e6d4e7a4a6b4e6a646d4f54556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c178204edac25f3b51846d70a37b800cea33d4670000000000000000000000000000000000000000000000000000000018d56168000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9a62220ac10f81275e6876e98f377a30cda8ebf9c75a801022445836a2b19690",
      "signature": {
        "s": "0x2c2ec981b64f177a5103241166fd2d0df71f822dd1a1fd86f20acfe740e35c0c",
        "r": "0x03d1bfbdf1f8402ee46c2c5203de2d899b054170537dfb0cd5bee506e3b72c54",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x807b0a8b7a001fadf4d4e2147d257b78eeb82baf908a219dee3c87a798327f97",
      "signature": {
        "s": "0x52ca0d2fd21b378feec684bd449bcf7a94e71781e6cb048ad2f43c4dcec8f991",
        "r": "0x84c14c33fc3c6d1e6bf7af4b120b6c9e82ca8ebd144278b9d27abbcead973ede",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "416637288",
    "total": "416637288"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "416637288",
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
            "amount": "40071145844"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "416637"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMGYyZjM1ZC01MzM0LTU3MjEtYjc4OS01MDNmNzJkNjdmOTUifQ==",
    "nonce": 6091,
    "balances": {
      "current": "12977607876927239",
      "previous": "12977608293981164"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc178204edac25f3b51846d70a37b800cea33d467",
    "nonce": 22,
    "balances": {
      "current": "416637288",
      "previous": "0"
    }
  },
  "blockNumber": "10114688",
  "created": "2020-05-22T08:46:22.141Z",
  "updated": "2020-05-22T08:46:22.212Z",
  "id": "5ec7915eb0c6090011d5b0b4"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000018d56168000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `416637288`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`