# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe6973EF1790959f7eb5d5B23263E9e68C847418e`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000028960000000000000000000000000000000000000000000000000000000000002896000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000028960000000000000000000000000000000000000000000000000000000000002896e081267246fba16fe0666c3174bc95b7b1e12ca9c1850676c00e185f1cce7ca153593155cee22a10812edf2ef3f7a4bd26adde3b2baf818b97a6023fecca9eca03849706ec725db23f756805839bc0425731c6d6bd83ed72e386e600d0704a94000000000000000000000000000000000000000000000000000000000000001cf22ebf54a59cf159e9bc5135a5109142e8e9ea220c35a423df1da3aad9846d99e1615d5a6a5a9065b994413bc7890cdc9d7fce36a2e8d3ac23ab026f8fc3e82a5af83d933565cd25008101aac04a166184c00a360968049515adc1b109a01ce1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56be00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e5500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0586d11e87000000000000000000000000000000000000000000000000002e0b0586d1472700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ed630b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6d526d5a47557a4e79316b4f44597a4c54557a596a41744f575a694d6930774e5441774f54497a4e6d4e684f544d6966513d3d0000000000000000000000000000000000000000000000000000000000000007000000000000000000000000e6973ef1790959f7eb5d5b23263e9e68c847418e0000000000000000000000000000000000000000000000000000000000002896000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe081267246fba16fe0666c3174bc95b7b1e12ca9c1850676c00e185f1cce7ca1",
      "signature": {
        "s": "0x03849706ec725db23f756805839bc0425731c6d6bd83ed72e386e600d0704a94",
        "r": "0x53593155cee22a10812edf2ef3f7a4bd26adde3b2baf818b97a6023fecca9eca",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf22ebf54a59cf159e9bc5135a5109142e8e9ea220c35a423df1da3aad9846d99",
      "signature": {
        "s": "0x5af83d933565cd25008101aac04a166184c00a360968049515adc1b109a01ce1",
        "r": "0xe1615d5a6a5a9065b994413bc7890cdc9d7fce36a2e8d3ac23ab026f8fc3e82a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10390",
    "total": "10390"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10390",
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
            "amount": "57694105778"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NmRmZGUzNy1kODYzLTUzYjAtOWZiMi0wNTAwOTIzNmNhOTMifQ==",
    "nonce": 7765,
    "balances": {
      "current": "12959967293283975",
      "previous": "12959967293294375"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe6973ef1790959f7eb5d5b23263e9e68c847418e",
    "nonce": 7,
    "balances": {
      "current": "10390",
      "previous": "0"
    }
  },
  "blockNumber": "10114750",
  "created": "2020-05-22T08:59:28.318Z",
  "updated": "2020-05-22T08:59:29.466Z",
  "id": "5ec79470b0c6090011d5b2f6"
}
```
* *stageAmount*: `10390`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000002896000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000028960000000000000000000000000000000000000000000000000000000000002896e081267246fba16fe0666c3174bc95b7b1e12ca9c1850676c00e185f1cce7ca153593155cee22a10812edf2ef3f7a4bd26adde3b2baf818b97a6023fecca9eca03849706ec725db23f756805839bc0425731c6d6bd83ed72e386e600d0704a94000000000000000000000000000000000000000000000000000000000000001cf22ebf54a59cf159e9bc5135a5109142e8e9ea220c35a423df1da3aad9846d99e1615d5a6a5a9065b994413bc7890cdc9d7fce36a2e8d3ac23ab026f8fc3e82a5af83d933565cd25008101aac04a166184c00a360968049515adc1b109a01ce1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56be00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e5500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0586d11e87000000000000000000000000000000000000000000000000002e0b0586d1472700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ed630b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6d526d5a47557a4e79316b4f44597a4c54557a596a41744f575a694d6930774e5441774f54497a4e6d4e684f544d6966513d3d0000000000000000000000000000000000000000000000000000000000000007000000000000000000000000e6973ef1790959f7eb5d5b23263e9e68c847418e0000000000000000000000000000000000000000000000000000000000002896000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe081267246fba16fe0666c3174bc95b7b1e12ca9c1850676c00e185f1cce7ca1",
      "signature": {
        "s": "0x03849706ec725db23f756805839bc0425731c6d6bd83ed72e386e600d0704a94",
        "r": "0x53593155cee22a10812edf2ef3f7a4bd26adde3b2baf818b97a6023fecca9eca",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf22ebf54a59cf159e9bc5135a5109142e8e9ea220c35a423df1da3aad9846d99",
      "signature": {
        "s": "0x5af83d933565cd25008101aac04a166184c00a360968049515adc1b109a01ce1",
        "r": "0xe1615d5a6a5a9065b994413bc7890cdc9d7fce36a2e8d3ac23ab026f8fc3e82a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10390",
    "total": "10390"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10390",
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
            "amount": "57694105778"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NmRmZGUzNy1kODYzLTUzYjAtOWZiMi0wNTAwOTIzNmNhOTMifQ==",
    "nonce": 7765,
    "balances": {
      "current": "12959967293283975",
      "previous": "12959967293294375"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe6973ef1790959f7eb5d5b23263e9e68c847418e",
    "nonce": 7,
    "balances": {
      "current": "10390",
      "previous": "0"
    }
  },
  "blockNumber": "10114750",
  "created": "2020-05-22T08:59:28.318Z",
  "updated": "2020-05-22T08:59:29.466Z",
  "id": "5ec79470b0c6090011d5b2f6"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000002896000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10390`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`