# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAcA332351B6C8207F1cb0FA9eca6B75EB546FF9A`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000002a8c5959000000000000000000000000000000000000000000000000000000002a8c5959000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002a8c5959000000000000000000000000000000000000000000000000000000002a8c59597167e1415b4db15ee8fc2c0619cbdc931d8aa75da55942be544b2042ddeeac44dad735f2d7c0fa4b50f50e577208057163e7824923c6b85f94f8c6254afc6fda4812189e76a3b97da859de8e9ae72778094c79f843b378d1400fbfc0829e93a8000000000000000000000000000000000000000000000000000000000000001b664571ed1555acbb5c4e8f49d9bdeef76c7bde945b081e7550fe1f6f5a62141ed3d131aca32c5b983028d985ced9c16b97c9ec2dbc07a06c0f2d383de1c50e252624e648ec31a76cc7d02386ce59e1bb7ea2db1df3a6387d0144ac71b1344315000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56790000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000176c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1ee35125b1000000000000000000000000000000000000000000000000002e1b1f0de8637a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000ae470000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000950d27e79000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d445268596d4d79597931684d3249304c54557a597a457459544a6d5953307a4d574d7a4f57566d4d574e695a6a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000aca332351b6c8207f1cb0fa9eca6b75eb546ff9a000000000000000000000000000000000000000000000000000000002a8c5959000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7167e1415b4db15ee8fc2c0619cbdc931d8aa75da55942be544b2042ddeeac44",
      "signature": {
        "s": "0x4812189e76a3b97da859de8e9ae72778094c79f843b378d1400fbfc0829e93a8",
        "r": "0xdad735f2d7c0fa4b50f50e577208057163e7824923c6b85f94f8c6254afc6fda",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x664571ed1555acbb5c4e8f49d9bdeef76c7bde945b081e7550fe1f6f5a62141e",
      "signature": {
        "s": "0x2624e648ec31a76cc7d02386ce59e1bb7ea2db1df3a6387d0144ac71b1344315",
        "r": "0xd3d131aca32c5b983028d985ced9c16b97c9ec2dbc07a06c0f2d383de1c50e25",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "713840985",
    "total": "713840985"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "713840985",
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
            "amount": "40010677881"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "713840"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDRhYmMyYy1hM2I0LTUzYzEtYTJmYS0zMWMzOWVmMWNiZjgifQ==",
    "nonce": 5996,
    "balances": {
      "current": "12977668405405105",
      "previous": "12977669119959930"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaca332351b6c8207f1cb0fa9eca6b75eb546ff9a",
    "nonce": 22,
    "balances": {
      "current": "713840985",
      "previous": "0"
    }
  },
  "blockNumber": "10114681",
  "created": "2020-05-22T08:45:35.391Z",
  "updated": "2020-05-22T08:45:35.454Z",
  "id": "5ec7912fe5756b00111b8721"
}
```
* *stageAmount*: `713840985`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000002a8c5959000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002a8c5959000000000000000000000000000000000000000000000000000000002a8c59597167e1415b4db15ee8fc2c0619cbdc931d8aa75da55942be544b2042ddeeac44dad735f2d7c0fa4b50f50e577208057163e7824923c6b85f94f8c6254afc6fda4812189e76a3b97da859de8e9ae72778094c79f843b378d1400fbfc0829e93a8000000000000000000000000000000000000000000000000000000000000001b664571ed1555acbb5c4e8f49d9bdeef76c7bde945b081e7550fe1f6f5a62141ed3d131aca32c5b983028d985ced9c16b97c9ec2dbc07a06c0f2d383de1c50e252624e648ec31a76cc7d02386ce59e1bb7ea2db1df3a6387d0144ac71b1344315000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56790000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000176c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1ee35125b1000000000000000000000000000000000000000000000000002e1b1f0de8637a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000ae470000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000950d27e79000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d445268596d4d79597931684d3249304c54557a597a457459544a6d5953307a4d574d7a4f57566d4d574e695a6a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000aca332351b6c8207f1cb0fa9eca6b75eb546ff9a000000000000000000000000000000000000000000000000000000002a8c5959000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7167e1415b4db15ee8fc2c0619cbdc931d8aa75da55942be544b2042ddeeac44",
      "signature": {
        "s": "0x4812189e76a3b97da859de8e9ae72778094c79f843b378d1400fbfc0829e93a8",
        "r": "0xdad735f2d7c0fa4b50f50e577208057163e7824923c6b85f94f8c6254afc6fda",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x664571ed1555acbb5c4e8f49d9bdeef76c7bde945b081e7550fe1f6f5a62141e",
      "signature": {
        "s": "0x2624e648ec31a76cc7d02386ce59e1bb7ea2db1df3a6387d0144ac71b1344315",
        "r": "0xd3d131aca32c5b983028d985ced9c16b97c9ec2dbc07a06c0f2d383de1c50e25",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "713840985",
    "total": "713840985"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "713840985",
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
            "amount": "40010677881"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "713840"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDRhYmMyYy1hM2I0LTUzYzEtYTJmYS0zMWMzOWVmMWNiZjgifQ==",
    "nonce": 5996,
    "balances": {
      "current": "12977668405405105",
      "previous": "12977669119959930"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaca332351b6c8207f1cb0fa9eca6b75eb546ff9a",
    "nonce": 22,
    "balances": {
      "current": "713840985",
      "previous": "0"
    }
  },
  "blockNumber": "10114681",
  "created": "2020-05-22T08:45:35.391Z",
  "updated": "2020-05-22T08:45:35.454Z",
  "id": "5ec7912fe5756b00111b8721"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000002a8c5959000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `713840985`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`