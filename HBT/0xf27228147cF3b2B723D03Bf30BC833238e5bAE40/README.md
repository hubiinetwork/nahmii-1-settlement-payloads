# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf27228147cF3b2B723D03Bf30BC833238e5bAE40`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000424787fb00000000000000000000000000000000000000000000000000000000424787fb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000424787fb00000000000000000000000000000000000000000000000000000000424787fb583d8a75f0fc5ba182b6bb493973d69e05f64fb14bbe15af914656888509188076061a7a915767938295fff9146cb57f8ec5b7efcfdfeec7e38ec23e08355e9715042f49200ed16ecb7bd4163474ffeeed6383010eab935428719543830ac254000000000000000000000000000000000000000000000000000000000000001bac5ac9b94957f9f239ade2be4776429fc5257fab52b7433cfe1a9f7533e1d1530d0a09e4145dbba5a9cb006e642a5e561ca060aca6e54e9397c0479fc91ee3614e071813552a27482bba4bf6f140f80b8b17dd31047b3210a8295c00fabafb64000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e3600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b05eed75137000000000000000000000000000000000000000000000000002e0b06312fd0e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000010f7b0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ebb963c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f574d31596d4534596930344e6d59304c54557a596d5974596a566a4d43316b595449305a44633359324e6a4e6a496966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000f27228147cf3b2b723d03bf30bc833238e5bae4000000000000000000000000000000000000000000000000000000000424787fb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x583d8a75f0fc5ba182b6bb493973d69e05f64fb14bbe15af9146568885091880",
      "signature": {
        "s": "0x15042f49200ed16ecb7bd4163474ffeeed6383010eab935428719543830ac254",
        "r": "0x76061a7a915767938295fff9146cb57f8ec5b7efcfdfeec7e38ec23e08355e97",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xac5ac9b94957f9f239ade2be4776429fc5257fab52b7433cfe1a9f7533e1d153",
      "signature": {
        "s": "0x4e071813552a27482bba4bf6f140f80b8b17dd31047b3210a8295c00fabafb64",
        "r": "0x0d0a09e4145dbba5a9cb006e642a5e561ca060aca6e54e9397c0479fc91ee361",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1111984123",
    "total": "1111984123"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1111984123",
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
            "amount": "57692362300"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1111984"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4OWM1YmE4Yi04NmY0LTUzYmYtYjVjMC1kYTI0ZDc3Y2NjNjIifQ==",
    "nonce": 7734,
    "balances": {
      "current": "12959969038520631",
      "previous": "12959970151616738"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf27228147cf3b2b723d03bf30bc833238e5bae40",
    "nonce": 13,
    "balances": {
      "current": "1111984123",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:09.599Z",
  "updated": "2020-05-22T08:59:09.669Z",
  "id": "5ec7945db0c6090011d5b2ef"
}
```
* *stageAmount*: `1111984123`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000424787fb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000424787fb00000000000000000000000000000000000000000000000000000000424787fb583d8a75f0fc5ba182b6bb493973d69e05f64fb14bbe15af914656888509188076061a7a915767938295fff9146cb57f8ec5b7efcfdfeec7e38ec23e08355e9715042f49200ed16ecb7bd4163474ffeeed6383010eab935428719543830ac254000000000000000000000000000000000000000000000000000000000000001bac5ac9b94957f9f239ade2be4776429fc5257fab52b7433cfe1a9f7533e1d1530d0a09e4145dbba5a9cb006e642a5e561ca060aca6e54e9397c0479fc91ee3614e071813552a27482bba4bf6f140f80b8b17dd31047b3210a8295c00fabafb64000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e3600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b05eed75137000000000000000000000000000000000000000000000000002e0b06312fd0e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000010f7b0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ebb963c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f574d31596d4534596930344e6d59304c54557a596d5974596a566a4d43316b595449305a44633359324e6a4e6a496966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000f27228147cf3b2b723d03bf30bc833238e5bae4000000000000000000000000000000000000000000000000000000000424787fb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x583d8a75f0fc5ba182b6bb493973d69e05f64fb14bbe15af9146568885091880",
      "signature": {
        "s": "0x15042f49200ed16ecb7bd4163474ffeeed6383010eab935428719543830ac254",
        "r": "0x76061a7a915767938295fff9146cb57f8ec5b7efcfdfeec7e38ec23e08355e97",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xac5ac9b94957f9f239ade2be4776429fc5257fab52b7433cfe1a9f7533e1d153",
      "signature": {
        "s": "0x4e071813552a27482bba4bf6f140f80b8b17dd31047b3210a8295c00fabafb64",
        "r": "0x0d0a09e4145dbba5a9cb006e642a5e561ca060aca6e54e9397c0479fc91ee361",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1111984123",
    "total": "1111984123"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1111984123",
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
            "amount": "57692362300"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1111984"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4OWM1YmE4Yi04NmY0LTUzYmYtYjVjMC1kYTI0ZDc3Y2NjNjIifQ==",
    "nonce": 7734,
    "balances": {
      "current": "12959969038520631",
      "previous": "12959970151616738"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf27228147cf3b2b723d03bf30bc833238e5bae40",
    "nonce": 13,
    "balances": {
      "current": "1111984123",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:09.599Z",
  "updated": "2020-05-22T08:59:09.669Z",
  "id": "5ec7945db0c6090011d5b2ef"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000424787fb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1111984123`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`