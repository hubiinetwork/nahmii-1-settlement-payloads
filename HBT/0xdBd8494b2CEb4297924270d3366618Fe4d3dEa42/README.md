# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdBd8494b2CEb4297924270d3366618Fe4d3dEa42`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000002d873d8e000000000000000000000000000000000000000000000000000000002d873d8e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002d873d8e000000000000000000000000000000000000000000000000000000002d873d8ec108f7512045c988d10f813a7a6b4dda93be6cf5d05e8dc7889a6a3d60c182edfc835a88ba24878141265a141fd20c8b6069edc9d6b06b632d950c1fd2b165257ebe4ce79ce36d05df811f03d9aacf3097a135f7e7125864f59a9c53b537a069000000000000000000000000000000000000000000000000000000000000001c31e09c332d34d78da60624c2ce1bcd350768243c1e5f77872b13dfcb9945ada2d4e0b565e6de6d066f8160581676d4c529474f63d315e0c2c4f808e5cae58e570dd6273e58b6a48f51c36c3beaf4d7b48bde4efe48090c8d2b58480a077f02cb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a567a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000177a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1c3ee34f89000000000000000000000000000000000000000000000000002e1b1c6c7634d400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000ba7bd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009517f7c9e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e4756684e544e684d5330794e5452694c54566b4d7a4174596a6b7a4d693031596a4d354e324d354f5463794f57456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dbd8494b2ceb4297924270d3366618fe4d3dea42000000000000000000000000000000000000000000000000000000002d873d8e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc108f7512045c988d10f813a7a6b4dda93be6cf5d05e8dc7889a6a3d60c182ed",
      "signature": {
        "s": "0x7ebe4ce79ce36d05df811f03d9aacf3097a135f7e7125864f59a9c53b537a069",
        "r": "0xfc835a88ba24878141265a141fd20c8b6069edc9d6b06b632d950c1fd2b16525",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x31e09c332d34d78da60624c2ce1bcd350768243c1e5f77872b13dfcb9945ada2",
      "signature": {
        "s": "0x0dd6273e58b6a48f51c36c3beaf4d7b48bde4efe48090c8d2b58480a077f02cb",
        "r": "0xd4e0b565e6de6d066f8160581676d4c529474f63d315e0c2c4f808e5cae58e57",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "763837838",
    "total": "763837838"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "763837838",
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
            "amount": "40022015134"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "763837"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNGVhNTNhMS0yNTRiLTVkMzAtYjkzMi01YjM5N2M5OTcyOWEifQ==",
    "nonce": 6010,
    "balances": {
      "current": "12977657056808841",
      "previous": "12977657821410516"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdbd8494b2ceb4297924270d3366618fe4d3dea42",
    "nonce": 22,
    "balances": {
      "current": "763837838",
      "previous": "0"
    }
  },
  "blockNumber": "10114682",
  "created": "2020-05-22T08:45:41.079Z",
  "updated": "2020-05-22T08:45:42.145Z",
  "id": "5ec79135005df800101bca15"
}
```
* *stageAmount*: `763837838`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000002d873d8e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002d873d8e000000000000000000000000000000000000000000000000000000002d873d8ec108f7512045c988d10f813a7a6b4dda93be6cf5d05e8dc7889a6a3d60c182edfc835a88ba24878141265a141fd20c8b6069edc9d6b06b632d950c1fd2b165257ebe4ce79ce36d05df811f03d9aacf3097a135f7e7125864f59a9c53b537a069000000000000000000000000000000000000000000000000000000000000001c31e09c332d34d78da60624c2ce1bcd350768243c1e5f77872b13dfcb9945ada2d4e0b565e6de6d066f8160581676d4c529474f63d315e0c2c4f808e5cae58e570dd6273e58b6a48f51c36c3beaf4d7b48bde4efe48090c8d2b58480a077f02cb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a567a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000177a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1c3ee34f89000000000000000000000000000000000000000000000000002e1b1c6c7634d400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000ba7bd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009517f7c9e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e4756684e544e684d5330794e5452694c54566b4d7a4174596a6b7a4d693031596a4d354e324d354f5463794f57456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dbd8494b2ceb4297924270d3366618fe4d3dea42000000000000000000000000000000000000000000000000000000002d873d8e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc108f7512045c988d10f813a7a6b4dda93be6cf5d05e8dc7889a6a3d60c182ed",
      "signature": {
        "s": "0x7ebe4ce79ce36d05df811f03d9aacf3097a135f7e7125864f59a9c53b537a069",
        "r": "0xfc835a88ba24878141265a141fd20c8b6069edc9d6b06b632d950c1fd2b16525",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x31e09c332d34d78da60624c2ce1bcd350768243c1e5f77872b13dfcb9945ada2",
      "signature": {
        "s": "0x0dd6273e58b6a48f51c36c3beaf4d7b48bde4efe48090c8d2b58480a077f02cb",
        "r": "0xd4e0b565e6de6d066f8160581676d4c529474f63d315e0c2c4f808e5cae58e57",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "763837838",
    "total": "763837838"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "763837838",
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
            "amount": "40022015134"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "763837"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNGVhNTNhMS0yNTRiLTVkMzAtYjkzMi01YjM5N2M5OTcyOWEifQ==",
    "nonce": 6010,
    "balances": {
      "current": "12977657056808841",
      "previous": "12977657821410516"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdbd8494b2ceb4297924270d3366618fe4d3dea42",
    "nonce": 22,
    "balances": {
      "current": "763837838",
      "previous": "0"
    }
  },
  "blockNumber": "10114682",
  "created": "2020-05-22T08:45:41.079Z",
  "updated": "2020-05-22T08:45:42.145Z",
  "id": "5ec79135005df800101bca15"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000002d873d8e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `763837838`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`