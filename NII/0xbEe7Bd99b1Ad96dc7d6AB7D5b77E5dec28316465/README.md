# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbEe7Bd99b1Ad96dc7d6AB7D5b77E5dec28316465`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000b7f38068b8577d4f00000000000000000000000000000000000000000000000005d48bfb41085a440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000005d48bfb41085a44000000000000000000000000000000000000000000000000a39a5081c6dbf1c10c7b9c84f6bec74dacdc74ac5ea2e8ed603d4a11382320126013595ddf33ce7d262501ec990ba1eb2af59d41908e1a63b6bccfa821d66fed35655004a4f804a85fa9e61083481e1f77e8c6484b8626a533371b15d95486fbce74baa20a37c14f000000000000000000000000000000000000000000000000000000000000001c9376f346df96fe10c70b6923a4bd29be83276d34f29613cb3fe10780d4961e42d8f74432492b94f444bf8e71c43bda986f288632fe3da6ad8062c261d301d0fd496d2c91352964df807fc90c4dd600583cc7a6917d1891f814bcf59ac1e1c9d3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b464000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039af0d021b688fc8b4c40000000000000000000000000000000000000000000039af12d8257b5ce9e62900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000017e178c18d7210000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dda16770ce5a678e3a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d545a6c4e4445304f43316c4f5745344c5455784e474d744f44677a5953307a4d7a45334d44466d4e7a63345a44416966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000bee7bd99b1ad96dc7d6ab7d5b77e5dec28316465000000000000000000000000000000000000000000000000b7f38068b8577d4f000000000000000000000000000000000000000000000000b21ef46d774f230b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c7b9c84f6bec74dacdc74ac5ea2e8ed603d4a11382320126013595ddf33ce7d",
      "signature": {
        "s": "0x5fa9e61083481e1f77e8c6484b8626a533371b15d95486fbce74baa20a37c14f",
        "r": "0x262501ec990ba1eb2af59d41908e1a63b6bccfa821d66fed35655004a4f804a8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9376f346df96fe10c70b6923a4bd29be83276d34f29613cb3fe10780d4961e42",
      "signature": {
        "s": "0x496d2c91352964df807fc90c4dd600583cc7a6917d1891f814bcf59ac1e1c9d3",
        "r": "0xd8f74432492b94f444bf8e71c43bda986f288632fe3da6ad8062c261d301d0fd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "420114576496417348",
    "total": "11788823492913000897"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "420114576496417348",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27700193243232326880826"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "420114576496417"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMTZlNDE0OC1lOWE4LTUxNGMtODgzYS0zMzE3MDFmNzc4ZDAifQ==",
    "nonce": 111716,
    "balances": {
      "current": "272404007078277298042052",
      "previous": "272404427612968370955817"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbee7bd99b1ad96dc7d6ab7d5b77e5dec28316465",
    "nonce": 36,
    "balances": {
      "current": "13255079315539197263",
      "previous": "12834964739042779915"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:47.150Z",
  "updated": "2022-05-04T08:59:47.220Z",
  "id": "627240833592fd001130b68c"
}
```
* *stageAmount*: `13255079315539197263`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000005d48bfb41085a440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000005d48bfb41085a44000000000000000000000000000000000000000000000000a39a5081c6dbf1c10c7b9c84f6bec74dacdc74ac5ea2e8ed603d4a11382320126013595ddf33ce7d262501ec990ba1eb2af59d41908e1a63b6bccfa821d66fed35655004a4f804a85fa9e61083481e1f77e8c6484b8626a533371b15d95486fbce74baa20a37c14f000000000000000000000000000000000000000000000000000000000000001c9376f346df96fe10c70b6923a4bd29be83276d34f29613cb3fe10780d4961e42d8f74432492b94f444bf8e71c43bda986f288632fe3da6ad8062c261d301d0fd496d2c91352964df807fc90c4dd600583cc7a6917d1891f814bcf59ac1e1c9d3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b464000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039af0d021b688fc8b4c40000000000000000000000000000000000000000000039af12d8257b5ce9e62900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000017e178c18d7210000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dda16770ce5a678e3a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d545a6c4e4445304f43316c4f5745344c5455784e474d744f44677a5953307a4d7a45334d44466d4e7a63345a44416966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000bee7bd99b1ad96dc7d6ab7d5b77e5dec28316465000000000000000000000000000000000000000000000000b7f38068b8577d4f000000000000000000000000000000000000000000000000b21ef46d774f230b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c7b9c84f6bec74dacdc74ac5ea2e8ed603d4a11382320126013595ddf33ce7d",
      "signature": {
        "s": "0x5fa9e61083481e1f77e8c6484b8626a533371b15d95486fbce74baa20a37c14f",
        "r": "0x262501ec990ba1eb2af59d41908e1a63b6bccfa821d66fed35655004a4f804a8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9376f346df96fe10c70b6923a4bd29be83276d34f29613cb3fe10780d4961e42",
      "signature": {
        "s": "0x496d2c91352964df807fc90c4dd600583cc7a6917d1891f814bcf59ac1e1c9d3",
        "r": "0xd8f74432492b94f444bf8e71c43bda986f288632fe3da6ad8062c261d301d0fd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "420114576496417348",
    "total": "11788823492913000897"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "420114576496417348",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27700193243232326880826"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "420114576496417"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMTZlNDE0OC1lOWE4LTUxNGMtODgzYS0zMzE3MDFmNzc4ZDAifQ==",
    "nonce": 111716,
    "balances": {
      "current": "272404007078277298042052",
      "previous": "272404427612968370955817"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbee7bd99b1ad96dc7d6ab7d5b77e5dec28316465",
    "nonce": 36,
    "balances": {
      "current": "13255079315539197263",
      "previous": "12834964739042779915"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:47.150Z",
  "updated": "2022-05-04T08:59:47.220Z",
  "id": "627240833592fd001130b68c"
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
0x0f200f9b000000000000000000000000000000000000000000000000b7f38068b8577d4f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13255079315539197263`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`