# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5715Ced744626a35D2343Acac1D09e2ec629fC3C`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000b6b14ab000000000000000000000000000000000000000000000000000000000b6b14ab000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000b6b14ab000000000000000000000000000000000000000000000000000000000b6b14ab75ac45e4d1fadecc815280f44b7bb5bca0e406d3405bcf3e69be5af5bf45ce9e5b749bb38cf6d96752c1b60262f33459ce2e58f235c96c3f470212e96d741b2340ab081ebf34116dde66e94a056e1a9a3c403d7ca6834d6c8ff619e61af7e7e9000000000000000000000000000000000000000000000000000000000000001c0ea6e82aabb9ad02736f69ae59476ba23684135d4963daf3fc2aa2610b1940c396ae23d0c562669f919d1a709e31d13197f04b34fe30b6f20acbe043558c0b5947650953987d57968731c3f7b53644ab5bce76c2119057f2f2f9bf6ea9f0826a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56860000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000184100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad63d3cbe9c000000000000000000000000000000000000000000000000002e1ad648aabf9600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002ec4f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096366d82f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d574931596a4d7a597930784f444d354c54566b4e7a63744f4455334e7931685a5449794e6d49775a6a4d324d32456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005715ced744626a35d2343acac1d09e2ec629fc3c000000000000000000000000000000000000000000000000000000000b6b14ab000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x75ac45e4d1fadecc815280f44b7bb5bca0e406d3405bcf3e69be5af5bf45ce9e",
      "signature": {
        "s": "0x40ab081ebf34116dde66e94a056e1a9a3c403d7ca6834d6c8ff619e61af7e7e9",
        "r": "0x5b749bb38cf6d96752c1b60262f33459ce2e58f235c96c3f470212e96d741b23",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0ea6e82aabb9ad02736f69ae59476ba23684135d4963daf3fc2aa2610b1940c3",
      "signature": {
        "s": "0x47650953987d57968731c3f7b53644ab5bce76c2119057f2f2f9bf6ea9f0826a",
        "r": "0x96ae23d0c562669f919d1a709e31d13197f04b34fe30b6f20acbe043558c0b59",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "191567019",
    "total": "191567019"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "191567019",
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
            "amount": "40322390063"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "191567"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0MWI1YjMzYy0xODM5LTVkNzctODU3Ny1hZTIyNmIwZjM2M2EifQ==",
    "nonce": 6209,
    "balances": {
      "current": "12977356381404828",
      "previous": "12977356573163414"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5715ced744626a35d2343acac1d09e2ec629fc3c",
    "nonce": 22,
    "balances": {
      "current": "191567019",
      "previous": "0"
    }
  },
  "blockNumber": "10114694",
  "created": "2020-05-22T08:47:21.811Z",
  "updated": "2020-05-22T08:47:21.884Z",
  "id": "5ec79199e5756b00111b8767"
}
```
* *stageAmount*: `191567019`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000b6b14ab000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000b6b14ab000000000000000000000000000000000000000000000000000000000b6b14ab75ac45e4d1fadecc815280f44b7bb5bca0e406d3405bcf3e69be5af5bf45ce9e5b749bb38cf6d96752c1b60262f33459ce2e58f235c96c3f470212e96d741b2340ab081ebf34116dde66e94a056e1a9a3c403d7ca6834d6c8ff619e61af7e7e9000000000000000000000000000000000000000000000000000000000000001c0ea6e82aabb9ad02736f69ae59476ba23684135d4963daf3fc2aa2610b1940c396ae23d0c562669f919d1a709e31d13197f04b34fe30b6f20acbe043558c0b5947650953987d57968731c3f7b53644ab5bce76c2119057f2f2f9bf6ea9f0826a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56860000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000184100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad63d3cbe9c000000000000000000000000000000000000000000000000002e1ad648aabf9600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002ec4f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096366d82f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d574931596a4d7a597930784f444d354c54566b4e7a63744f4455334e7931685a5449794e6d49775a6a4d324d32456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005715ced744626a35d2343acac1d09e2ec629fc3c000000000000000000000000000000000000000000000000000000000b6b14ab000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x75ac45e4d1fadecc815280f44b7bb5bca0e406d3405bcf3e69be5af5bf45ce9e",
      "signature": {
        "s": "0x40ab081ebf34116dde66e94a056e1a9a3c403d7ca6834d6c8ff619e61af7e7e9",
        "r": "0x5b749bb38cf6d96752c1b60262f33459ce2e58f235c96c3f470212e96d741b23",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0ea6e82aabb9ad02736f69ae59476ba23684135d4963daf3fc2aa2610b1940c3",
      "signature": {
        "s": "0x47650953987d57968731c3f7b53644ab5bce76c2119057f2f2f9bf6ea9f0826a",
        "r": "0x96ae23d0c562669f919d1a709e31d13197f04b34fe30b6f20acbe043558c0b59",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "191567019",
    "total": "191567019"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "191567019",
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
            "amount": "40322390063"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "191567"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0MWI1YjMzYy0xODM5LTVkNzctODU3Ny1hZTIyNmIwZjM2M2EifQ==",
    "nonce": 6209,
    "balances": {
      "current": "12977356381404828",
      "previous": "12977356573163414"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5715ced744626a35d2343acac1d09e2ec629fc3c",
    "nonce": 22,
    "balances": {
      "current": "191567019",
      "previous": "0"
    }
  },
  "blockNumber": "10114694",
  "created": "2020-05-22T08:47:21.811Z",
  "updated": "2020-05-22T08:47:21.884Z",
  "id": "5ec79199e5756b00111b8767"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000b6b14ab000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `191567019`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`