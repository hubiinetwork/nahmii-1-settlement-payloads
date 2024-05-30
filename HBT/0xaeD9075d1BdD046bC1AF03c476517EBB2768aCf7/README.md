# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xaeD9075d1BdD046bC1AF03c476517EBB2768aCf7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000001b89b766500000000000000000000000000000000000000000000000000000001b89b7665000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001b89b766500000000000000000000000000000000000000000000000000000001b89b7665a4d556d8b89d111c762d659a3b037a40e49c429e8565e3e020fbbbf152736a09b705d078248adc13780c554519196c6c94ce03aded596056ebd25e1d949314f46d9980110d88ce314f6f8ce5afc97feaa165b38598cd564e1d511762aedb37d3000000000000000000000000000000000000000000000000000000000000001c7307ba68387d73345cdc8fe7e779d38f8e359ba8a008815596115529d33806da024915fd2031967935f43f8a12349e933377123e5a08e832930143c4b9f5c5172723cafbff949aa666e6c903a1a542ec0da07de0f954c4f6387ed1c5e565fb3c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c4d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1373e3add789000000000000000000000000000000000000000000000000002e13759cba199100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000070cba3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b46d90adc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e4445774e4449774e4330354f5445794c54557a5a6d4974596a6c6c4f433032597a63354d32493159544d355a546b6966513d3d0000000000000000000000000000000000000000000000000000000000000018000000000000000000000000aed9075d1bdd046bc1af03c476517ebb2768acf700000000000000000000000000000000000000000000000000000001b89b7665000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa4d556d8b89d111c762d659a3b037a40e49c429e8565e3e020fbbbf152736a09",
      "signature": {
        "s": "0x6d9980110d88ce314f6f8ce5afc97feaa165b38598cd564e1d511762aedb37d3",
        "r": "0xb705d078248adc13780c554519196c6c94ce03aded596056ebd25e1d949314f4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7307ba68387d73345cdc8fe7e779d38f8e359ba8a008815596115529d33806da",
      "signature": {
        "s": "0x2723cafbff949aa666e6c903a1a542ec0da07de0f954c4f6387ed1c5e565fb3c",
        "r": "0x024915fd2031967935f43f8a12349e933377123e5a08e832930143c4b9f5c517",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7392163429",
    "total": "7392163429"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7392163429",
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
            "amount": "48433269468"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "7392163"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNDEwNDIwNC05OTEyLTUzZmItYjllOC02Yzc5M2I1YTM5ZTkifQ==",
    "nonce": 7245,
    "balances": {
      "current": "12969237390677897",
      "previous": "12969244790233489"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaed9075d1bdd046bc1af03c476517ebb2768acf7",
    "nonce": 24,
    "balances": {
      "current": "7392163429",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:20.401Z",
  "updated": "2020-05-22T08:55:20.467Z",
  "id": "5ec79378005df800101bcbb9"
}
```
* *stageAmount*: `7392163429`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000001b89b7665000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001b89b766500000000000000000000000000000000000000000000000000000001b89b7665a4d556d8b89d111c762d659a3b037a40e49c429e8565e3e020fbbbf152736a09b705d078248adc13780c554519196c6c94ce03aded596056ebd25e1d949314f46d9980110d88ce314f6f8ce5afc97feaa165b38598cd564e1d511762aedb37d3000000000000000000000000000000000000000000000000000000000000001c7307ba68387d73345cdc8fe7e779d38f8e359ba8a008815596115529d33806da024915fd2031967935f43f8a12349e933377123e5a08e832930143c4b9f5c5172723cafbff949aa666e6c903a1a542ec0da07de0f954c4f6387ed1c5e565fb3c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c4d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1373e3add789000000000000000000000000000000000000000000000000002e13759cba199100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000070cba3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b46d90adc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e4445774e4449774e4330354f5445794c54557a5a6d4974596a6c6c4f433032597a63354d32493159544d355a546b6966513d3d0000000000000000000000000000000000000000000000000000000000000018000000000000000000000000aed9075d1bdd046bc1af03c476517ebb2768acf700000000000000000000000000000000000000000000000000000001b89b7665000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa4d556d8b89d111c762d659a3b037a40e49c429e8565e3e020fbbbf152736a09",
      "signature": {
        "s": "0x6d9980110d88ce314f6f8ce5afc97feaa165b38598cd564e1d511762aedb37d3",
        "r": "0xb705d078248adc13780c554519196c6c94ce03aded596056ebd25e1d949314f4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7307ba68387d73345cdc8fe7e779d38f8e359ba8a008815596115529d33806da",
      "signature": {
        "s": "0x2723cafbff949aa666e6c903a1a542ec0da07de0f954c4f6387ed1c5e565fb3c",
        "r": "0x024915fd2031967935f43f8a12349e933377123e5a08e832930143c4b9f5c517",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7392163429",
    "total": "7392163429"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7392163429",
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
            "amount": "48433269468"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "7392163"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNDEwNDIwNC05OTEyLTUzZmItYjllOC02Yzc5M2I1YTM5ZTkifQ==",
    "nonce": 7245,
    "balances": {
      "current": "12969237390677897",
      "previous": "12969244790233489"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaed9075d1bdd046bc1af03c476517ebb2768acf7",
    "nonce": 24,
    "balances": {
      "current": "7392163429",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:20.401Z",
  "updated": "2020-05-22T08:55:20.467Z",
  "id": "5ec79378005df800101bcbb9"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000001b89b7665000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7392163429`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`