# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFe48f0486aFC10bFE9FD91d6b495A0FE79d0a8E2`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000165ed7c600000000000000000000000000000000000000000000000000000000165ed7c6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000165ed7c600000000000000000000000000000000000000000000000000000000165ed7c6808457ddc8aca6aad819c7ffb7f05b41f41bdba59e6fffed7967434da686d1712c12c70d9310d120f464a5578036c07845494768076453bcb9c8541971b414635adfb993902c6c1c81807f046b5317f74154d0b75cc8fcd07415609f1c4c56fe000000000000000000000000000000000000000000000000000000000000001cdada411d72800596fa84b892fc4eb85cd77abf1c4a53ec050d1fac599a4263bf4e4ccf1e3bc3737e3cf7c73b5f56658b58269710fcacd7dbda1dea3148140757513b14928b8d2239a4058dd8c8189a0a6bffca789388373ce5d30789746c2a3f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001df100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b130bd03dd6000000000000000000000000000000000000000000000000002e0b132234cfae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005ba12000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6b610f9b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d54417a4f4459324e793078597a42694c54566d5a444174596d5268596930774e6a553559324d794f54417959546b6966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000fe48f0486afc10bfe9fd91d6b495a0fe79d0a8e200000000000000000000000000000000000000000000000000000000165ed7c6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x808457ddc8aca6aad819c7ffb7f05b41f41bdba59e6fffed7967434da686d171",
      "signature": {
        "s": "0x5adfb993902c6c1c81807f046b5317f74154d0b75cc8fcd07415609f1c4c56fe",
        "r": "0x2c12c70d9310d120f464a5578036c07845494768076453bcb9c8541971b41463",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdada411d72800596fa84b892fc4eb85cd77abf1c4a53ec050d1fac599a4263bf",
      "signature": {
        "s": "0x513b14928b8d2239a4058dd8c8189a0a6bffca789388373ce5d30789746c2a3f",
        "r": "0x4e4ccf1e3bc3737e3cf7c73b5f56658b58269710fcacd7dbda1dea3148140757",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "375314374",
    "total": "375314374"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "375314374",
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
            "amount": "57636097947"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "375314"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMTAzODY2Ny0xYzBiLTVmZDAtYmRhYi0wNjU5Y2MyOTAyYTkifQ==",
    "nonce": 7665,
    "balances": {
      "current": "12960025359171030",
      "previous": "12960025734860718"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe48f0486afc10bfe9fd91d6b495a0fe79d0a8e2",
    "nonce": 6,
    "balances": {
      "current": "375314374",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:34.578Z",
  "updated": "2020-05-22T08:58:35.649Z",
  "id": "5ec7943ae5756b00111b892e"
}
```
* *stageAmount*: `375314374`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000165ed7c6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000165ed7c600000000000000000000000000000000000000000000000000000000165ed7c6808457ddc8aca6aad819c7ffb7f05b41f41bdba59e6fffed7967434da686d1712c12c70d9310d120f464a5578036c07845494768076453bcb9c8541971b414635adfb993902c6c1c81807f046b5317f74154d0b75cc8fcd07415609f1c4c56fe000000000000000000000000000000000000000000000000000000000000001cdada411d72800596fa84b892fc4eb85cd77abf1c4a53ec050d1fac599a4263bf4e4ccf1e3bc3737e3cf7c73b5f56658b58269710fcacd7dbda1dea3148140757513b14928b8d2239a4058dd8c8189a0a6bffca789388373ce5d30789746c2a3f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001df100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b130bd03dd6000000000000000000000000000000000000000000000000002e0b132234cfae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005ba12000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6b610f9b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d54417a4f4459324e793078597a42694c54566d5a444174596d5268596930774e6a553559324d794f54417959546b6966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000fe48f0486afc10bfe9fd91d6b495a0fe79d0a8e200000000000000000000000000000000000000000000000000000000165ed7c6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x808457ddc8aca6aad819c7ffb7f05b41f41bdba59e6fffed7967434da686d171",
      "signature": {
        "s": "0x5adfb993902c6c1c81807f046b5317f74154d0b75cc8fcd07415609f1c4c56fe",
        "r": "0x2c12c70d9310d120f464a5578036c07845494768076453bcb9c8541971b41463",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdada411d72800596fa84b892fc4eb85cd77abf1c4a53ec050d1fac599a4263bf",
      "signature": {
        "s": "0x513b14928b8d2239a4058dd8c8189a0a6bffca789388373ce5d30789746c2a3f",
        "r": "0x4e4ccf1e3bc3737e3cf7c73b5f56658b58269710fcacd7dbda1dea3148140757",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "375314374",
    "total": "375314374"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "375314374",
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
            "amount": "57636097947"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "375314"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMTAzODY2Ny0xYzBiLTVmZDAtYmRhYi0wNjU5Y2MyOTAyYTkifQ==",
    "nonce": 7665,
    "balances": {
      "current": "12960025359171030",
      "previous": "12960025734860718"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe48f0486afc10bfe9fd91d6b495a0fe79d0a8e2",
    "nonce": 6,
    "balances": {
      "current": "375314374",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:34.578Z",
  "updated": "2020-05-22T08:58:35.649Z",
  "id": "5ec7943ae5756b00111b892e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000165ed7c6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `375314374`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`