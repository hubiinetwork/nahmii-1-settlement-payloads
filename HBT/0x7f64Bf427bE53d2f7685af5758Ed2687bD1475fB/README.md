# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7f64Bf427bE53d2f7685af5758Ed2687bD1475fB`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000001820000000000000000000000000000000000000000000000000000000000000182000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000182000000000000000000000000000000000000000000000000000000000000018248b3073f1466401beda1da14c3c7fb248d2e5a8ecee6a568924955e4b1ccaf2e8e2c8097e0fc53bea306f856602bc17970da2911ccee7ce1cc2eec2dfd66e835671dbfa2abb49285a0f7ce93385ad93368186f28679877110cd8b4df6a0856a6000000000000000000000000000000000000000000000000000000000000001bfd3951f3f1e09822832f36cdb17e754ad2adbededadb7f05dd6546c5cc508c02034d28479f0b917f1be7cffef0381e4a85ab6b62a9ea5963eed8ebfb4415c3ed3d612830ba61975a2dbd5648694e36bad8639d0cff2edeed745d010c2358fe88000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019de00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e174f4cf576ce000000000000000000000000000000000000000000000000002e174f4cf5785100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4a52b59c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a47457759544a694f53316c4f4749344c54557a4d6a6b744f4468694f5330794d6a55795a575933596d55354e44676966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000007f64bf427be53d2f7685af5758ed2687bd1475fb0000000000000000000000000000000000000000000000000000000000000182000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x48b3073f1466401beda1da14c3c7fb248d2e5a8ecee6a568924955e4b1ccaf2e",
      "signature": {
        "s": "0x671dbfa2abb49285a0f7ce93385ad93368186f28679877110cd8b4df6a0856a6",
        "r": "0x8e2c8097e0fc53bea306f856602bc17970da2911ccee7ce1cc2eec2dfd66e835",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfd3951f3f1e09822832f36cdb17e754ad2adbededadb7f05dd6546c5cc508c02",
      "signature": {
        "s": "0x3d612830ba61975a2dbd5648694e36bad8639d0cff2edeed745d010c2358fe88",
        "r": "0x034d28479f0b917f1be7cffef0381e4a85ab6b62a9ea5963eed8ebfb4415c3ed",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "386",
    "total": "386"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "386",
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
            "amount": "44196607388"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZGEwYTJiOS1lOGI4LTUzMjktODhiOS0yMjUyZWY3YmU5NDgifQ==",
    "nonce": 6622,
    "balances": {
      "current": "12973478289700558",
      "previous": "12973478289700945"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7f64bf427be53d2f7685af5758ed2687bd1475fb",
    "nonce": 21,
    "balances": {
      "current": "386",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:33.412Z",
  "updated": "2020-05-22T08:50:34.500Z",
  "id": "5ec79259e5756b00111b87e6"
}
```
* *stageAmount*: `386`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000182000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000182000000000000000000000000000000000000000000000000000000000000018248b3073f1466401beda1da14c3c7fb248d2e5a8ecee6a568924955e4b1ccaf2e8e2c8097e0fc53bea306f856602bc17970da2911ccee7ce1cc2eec2dfd66e835671dbfa2abb49285a0f7ce93385ad93368186f28679877110cd8b4df6a0856a6000000000000000000000000000000000000000000000000000000000000001bfd3951f3f1e09822832f36cdb17e754ad2adbededadb7f05dd6546c5cc508c02034d28479f0b917f1be7cffef0381e4a85ab6b62a9ea5963eed8ebfb4415c3ed3d612830ba61975a2dbd5648694e36bad8639d0cff2edeed745d010c2358fe88000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019de00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e174f4cf576ce000000000000000000000000000000000000000000000000002e174f4cf5785100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4a52b59c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a47457759544a694f53316c4f4749344c54557a4d6a6b744f4468694f5330794d6a55795a575933596d55354e44676966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000007f64bf427be53d2f7685af5758ed2687bd1475fb0000000000000000000000000000000000000000000000000000000000000182000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x48b3073f1466401beda1da14c3c7fb248d2e5a8ecee6a568924955e4b1ccaf2e",
      "signature": {
        "s": "0x671dbfa2abb49285a0f7ce93385ad93368186f28679877110cd8b4df6a0856a6",
        "r": "0x8e2c8097e0fc53bea306f856602bc17970da2911ccee7ce1cc2eec2dfd66e835",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfd3951f3f1e09822832f36cdb17e754ad2adbededadb7f05dd6546c5cc508c02",
      "signature": {
        "s": "0x3d612830ba61975a2dbd5648694e36bad8639d0cff2edeed745d010c2358fe88",
        "r": "0x034d28479f0b917f1be7cffef0381e4a85ab6b62a9ea5963eed8ebfb4415c3ed",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "386",
    "total": "386"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "386",
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
            "amount": "44196607388"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZGEwYTJiOS1lOGI4LTUzMjktODhiOS0yMjUyZWY3YmU5NDgifQ==",
    "nonce": 6622,
    "balances": {
      "current": "12973478289700558",
      "previous": "12973478289700945"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7f64bf427be53d2f7685af5758ed2687bd1475fb",
    "nonce": 21,
    "balances": {
      "current": "386",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:33.412Z",
  "updated": "2020-05-22T08:50:34.500Z",
  "id": "5ec79259e5756b00111b87e6"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000182000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `386`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`