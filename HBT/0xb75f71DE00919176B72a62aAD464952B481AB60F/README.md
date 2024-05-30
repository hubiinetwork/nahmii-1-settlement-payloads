# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb75f71DE00919176B72a62aAD464952B481AB60F`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004ed523ee000000000000000000000000000000000000000000000000000000004ed523ee000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed523ee000000000000000000000000000000000000000000000000000000004ed523eefbbc0f8be3e4a99bcf712516b16b1d094d3b92ab63cf5488a5e747234a6c586d11ffe29d6df0754778acd457e87b260b0884ab74fdd1fa563862065a1b23289d1afb6ec8dcd6b2472937fa32f85803d5b4d7b86d4309a37b624a908cc650a0e3000000000000000000000000000000000000000000000000000000000000001c27a09ee78234dc6ff75b9f861a66b500684558daba6ef61583d0751e23bcd8436552cf00a0f8da79c06270d74cf69171665f7674525e60dca866bf2cfade74d70ae2d47d50c60b48784cd36efec44bed75e10dd1b6b889ecf5d1e5c004f9474f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c3d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e137f2e18b145000000000000000000000000000000000000000000000000002e137f7d02039200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e5f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b43f5d5be000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a47566b595751304e693078596a55334c54566b4e6a49744f44517a4d79316b4e4759305a6a6b774d4467784d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b75f71de00919176b72a62aad464952b481ab60f000000000000000000000000000000000000000000000000000000004ed523ee000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfbbc0f8be3e4a99bcf712516b16b1d094d3b92ab63cf5488a5e747234a6c586d",
      "signature": {
        "s": "0x1afb6ec8dcd6b2472937fa32f85803d5b4d7b86d4309a37b624a908cc650a0e3",
        "r": "0x11ffe29d6df0754778acd457e87b260b0884ab74fdd1fa563862065a1b23289d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x27a09ee78234dc6ff75b9f861a66b500684558daba6ef61583d0751e23bcd843",
      "signature": {
        "s": "0x0ae2d47d50c60b48784cd36efec44bed75e10dd1b6b889ecf5d1e5c004f9474f",
        "r": "0x6552cf00a0f8da79c06270d74cf69171665f7674525e60dca866bf2cfade74d7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322591214",
    "total": "1322591214"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322591214",
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
            "amount": "48384824766"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322591"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZGVkYWQ0Ni0xYjU3LTVkNjItODQzMy1kNGY0ZjkwMDgxMmUifQ==",
    "nonce": 7229,
    "balances": {
      "current": "12969285883834693",
      "previous": "12969287207748498"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb75f71de00919176b72a62aad464952b481ab60f",
    "nonce": 22,
    "balances": {
      "current": "1322591214",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:13.164Z",
  "updated": "2020-05-22T08:55:13.222Z",
  "id": "5ec79371b0c6090011d5b237"
}
```
* *stageAmount*: `1322591214`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004ed523ee000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed523ee000000000000000000000000000000000000000000000000000000004ed523eefbbc0f8be3e4a99bcf712516b16b1d094d3b92ab63cf5488a5e747234a6c586d11ffe29d6df0754778acd457e87b260b0884ab74fdd1fa563862065a1b23289d1afb6ec8dcd6b2472937fa32f85803d5b4d7b86d4309a37b624a908cc650a0e3000000000000000000000000000000000000000000000000000000000000001c27a09ee78234dc6ff75b9f861a66b500684558daba6ef61583d0751e23bcd8436552cf00a0f8da79c06270d74cf69171665f7674525e60dca866bf2cfade74d70ae2d47d50c60b48784cd36efec44bed75e10dd1b6b889ecf5d1e5c004f9474f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c3d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e137f2e18b145000000000000000000000000000000000000000000000000002e137f7d02039200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e5f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b43f5d5be000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a47566b595751304e693078596a55334c54566b4e6a49744f44517a4d79316b4e4759305a6a6b774d4467784d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b75f71de00919176b72a62aad464952b481ab60f000000000000000000000000000000000000000000000000000000004ed523ee000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfbbc0f8be3e4a99bcf712516b16b1d094d3b92ab63cf5488a5e747234a6c586d",
      "signature": {
        "s": "0x1afb6ec8dcd6b2472937fa32f85803d5b4d7b86d4309a37b624a908cc650a0e3",
        "r": "0x11ffe29d6df0754778acd457e87b260b0884ab74fdd1fa563862065a1b23289d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x27a09ee78234dc6ff75b9f861a66b500684558daba6ef61583d0751e23bcd843",
      "signature": {
        "s": "0x0ae2d47d50c60b48784cd36efec44bed75e10dd1b6b889ecf5d1e5c004f9474f",
        "r": "0x6552cf00a0f8da79c06270d74cf69171665f7674525e60dca866bf2cfade74d7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322591214",
    "total": "1322591214"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322591214",
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
            "amount": "48384824766"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322591"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZGVkYWQ0Ni0xYjU3LTVkNjItODQzMy1kNGY0ZjkwMDgxMmUifQ==",
    "nonce": 7229,
    "balances": {
      "current": "12969285883834693",
      "previous": "12969287207748498"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb75f71de00919176b72a62aad464952b481ab60f",
    "nonce": 22,
    "balances": {
      "current": "1322591214",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:13.164Z",
  "updated": "2020-05-22T08:55:13.222Z",
  "id": "5ec79371b0c6090011d5b237"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004ed523ee000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1322591214`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`