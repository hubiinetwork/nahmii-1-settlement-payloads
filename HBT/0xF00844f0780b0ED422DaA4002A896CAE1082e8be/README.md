# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF00844f0780b0ED422DaA4002A896CAE1082e8be`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000084994f000000000000000000000000000000000000000000000000000000000084994f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000084994f000000000000000000000000000000000000000000000000000000000084994f022161a97247ce21d8c68a7e22eec731a439d27e6d2e99703853db6e8141f5248247cc9dc33e59c4bc827c37561ea27e7c3802db4b0bc984c1dc31064a8ffed570c2a62a54031d5951f4045611de1bc945f2afe5098d4801a965110c398de3414000000000000000000000000000000000000000000000000000000000000001c131cb54fcb796d3b8e3226b6309da60c4543d46ab6fb4e2bc72ade0ba5bfce023654b3d02cac660c2a34887fadf97995ccba0f28e522e3b8f4f3bf77db0af0905c01d7e26fc072d9a9a375f4955b52ef735f23cc3259e4b1309cfe1d2e0542cd000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001acc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e161636c5433a000000000000000000000000000000000000000000000000002e16163f10f74900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000021f1f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9a64a87c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4f5749324e6a67314e53307a4d5463314c5455344d6d4574596a64694d69316b4e5463315a5451325a544978596d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000f00844f0780b0ed422daa4002a896cae1082e8be00000000000000000000000000000000000000000000000000000000084994f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x22161a97247ce21d8c68a7e22eec731a439d27e6d2e99703853db6e8141f5248",
      "signature": {
        "s": "0x0c2a62a54031d5951f4045611de1bc945f2afe5098d4801a965110c398de3414",
        "r": "0x247cc9dc33e59c4bc827c37561ea27e7c3802db4b0bc984c1dc31064a8ffed57",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x131cb54fcb796d3b8e3226b6309da60c4543d46ab6fb4e2bc72ade0ba5bfce02",
      "signature": {
        "s": "0x5c01d7e26fc072d9a9a375f4955b52ef735f23cc3259e4b1309cfe1d2e0542cd",
        "r": "0x3654b3d02cac660c2a34887fadf97995ccba0f28e522e3b8f4f3bf77db0af090",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "139039984",
    "total": "139039984"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "139039984",
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
            "amount": "45539960956"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "139039"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjOWI2Njg1NS0zMTc1LTU4MmEtYjdiMi1kNTc1ZTQ2ZTIxYmMifQ==",
    "nonce": 6860,
    "balances": {
      "current": "12972133592679226",
      "previous": "12972133731858249"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf00844f0780b0ed422daa4002a896cae1082e8be",
    "nonce": 22,
    "balances": {
      "current": "139039984",
      "previous": "0"
    }
  },
  "blockNumber": "10114717",
  "created": "2020-05-22T08:52:10.753Z",
  "updated": "2020-05-22T08:52:11.818Z",
  "id": "5ec792ba005df800101bcb35"
}
```
* *stageAmount*: `139039984`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000084994f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000084994f000000000000000000000000000000000000000000000000000000000084994f022161a97247ce21d8c68a7e22eec731a439d27e6d2e99703853db6e8141f5248247cc9dc33e59c4bc827c37561ea27e7c3802db4b0bc984c1dc31064a8ffed570c2a62a54031d5951f4045611de1bc945f2afe5098d4801a965110c398de3414000000000000000000000000000000000000000000000000000000000000001c131cb54fcb796d3b8e3226b6309da60c4543d46ab6fb4e2bc72ade0ba5bfce023654b3d02cac660c2a34887fadf97995ccba0f28e522e3b8f4f3bf77db0af0905c01d7e26fc072d9a9a375f4955b52ef735f23cc3259e4b1309cfe1d2e0542cd000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001acc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e161636c5433a000000000000000000000000000000000000000000000000002e16163f10f74900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000021f1f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9a64a87c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4f5749324e6a67314e53307a4d5463314c5455344d6d4574596a64694d69316b4e5463315a5451325a544978596d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000f00844f0780b0ed422daa4002a896cae1082e8be00000000000000000000000000000000000000000000000000000000084994f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x22161a97247ce21d8c68a7e22eec731a439d27e6d2e99703853db6e8141f5248",
      "signature": {
        "s": "0x0c2a62a54031d5951f4045611de1bc945f2afe5098d4801a965110c398de3414",
        "r": "0x247cc9dc33e59c4bc827c37561ea27e7c3802db4b0bc984c1dc31064a8ffed57",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x131cb54fcb796d3b8e3226b6309da60c4543d46ab6fb4e2bc72ade0ba5bfce02",
      "signature": {
        "s": "0x5c01d7e26fc072d9a9a375f4955b52ef735f23cc3259e4b1309cfe1d2e0542cd",
        "r": "0x3654b3d02cac660c2a34887fadf97995ccba0f28e522e3b8f4f3bf77db0af090",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "139039984",
    "total": "139039984"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "139039984",
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
            "amount": "45539960956"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "139039"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjOWI2Njg1NS0zMTc1LTU4MmEtYjdiMi1kNTc1ZTQ2ZTIxYmMifQ==",
    "nonce": 6860,
    "balances": {
      "current": "12972133592679226",
      "previous": "12972133731858249"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf00844f0780b0ed422daa4002a896cae1082e8be",
    "nonce": 22,
    "balances": {
      "current": "139039984",
      "previous": "0"
    }
  },
  "blockNumber": "10114717",
  "created": "2020-05-22T08:52:10.753Z",
  "updated": "2020-05-22T08:52:11.818Z",
  "id": "5ec792ba005df800101bcb35"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000084994f0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `139039984`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`