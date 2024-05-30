# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAd802B8d261F17CbeeB154188F9645eEB83ee149`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000ba1a494d00000000000000000000000000000000000000000000000000000000ba1a494d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ba1a494d00000000000000000000000000000000000000000000000000000000ba1a494dd4437b152fd0569aa5dc8c3e3270ced6b207523ab10d828e707c52e5039487d5a8c034cd8d808fecf976655c9b7f5f27328375c4c216e514f8b417e16de992b9612d7494f7ee9ea0d9be959d837aa7bd5263f7df9c836d6109e3697274f9b607000000000000000000000000000000000000000000000000000000000000001be08ff89045834679ff8ca6851f152b8f3411d745614b75c6389050a66d47434c7c315805829c9f195dd50524c48792ab8530fe0ce19000b991d5f81b5e349b0c128adb008bd2dc8af14e6d972b57e42dbe33a477c53de31d297e3c191c7ea87e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5662000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014ba00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2379b1d6f328000000000000000000000000000000000000000000000000002e237a6c20e0e100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002fa46c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000072dd5b060000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695954426c597a6b334d4330355a54466b4c5456685a5455744f4749785a6930795a474d314e546b354d6a6c6d4f544d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000ad802b8d261f17cbeeb154188f9645eeb83ee14900000000000000000000000000000000000000000000000000000000ba1a494d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd4437b152fd0569aa5dc8c3e3270ced6b207523ab10d828e707c52e5039487d5",
      "signature": {
        "s": "0x612d7494f7ee9ea0d9be959d837aa7bd5263f7df9c836d6109e3697274f9b607",
        "r": "0xa8c034cd8d808fecf976655c9b7f5f27328375c4c216e514f8b417e16de992b9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe08ff89045834679ff8ca6851f152b8f3411d745614b75c6389050a66d47434c",
      "signature": {
        "s": "0x128adb008bd2dc8af14e6d972b57e42dbe33a477c53de31d297e3c191c7ea87e",
        "r": "0x7c315805829c9f195dd50524c48792ab8530fe0ce19000b991d5f81b5e349b0c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3122284877",
    "total": "3122284877"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3122284877",
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
            "amount": "30833750112"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3122284"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYTBlYzk3MC05ZTFkLTVhZTUtOGIxZi0yZGM1NTk5MjlmOTMifQ==",
    "nonce": 5306,
    "balances": {
      "current": "12986854510359336",
      "previous": "12986857635766497"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xad802b8d261f17cbeeb154188f9645eeb83ee149",
    "nonce": 22,
    "balances": {
      "current": "3122284877",
      "previous": "0"
    }
  },
  "blockNumber": "10114658",
  "created": "2020-05-22T08:40:03.478Z",
  "updated": "2020-05-22T08:40:03.550Z",
  "id": "5ec78fe3005df800101bc924"
}
```
* *stageAmount*: `3122284877`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000ba1a494d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ba1a494d00000000000000000000000000000000000000000000000000000000ba1a494dd4437b152fd0569aa5dc8c3e3270ced6b207523ab10d828e707c52e5039487d5a8c034cd8d808fecf976655c9b7f5f27328375c4c216e514f8b417e16de992b9612d7494f7ee9ea0d9be959d837aa7bd5263f7df9c836d6109e3697274f9b607000000000000000000000000000000000000000000000000000000000000001be08ff89045834679ff8ca6851f152b8f3411d745614b75c6389050a66d47434c7c315805829c9f195dd50524c48792ab8530fe0ce19000b991d5f81b5e349b0c128adb008bd2dc8af14e6d972b57e42dbe33a477c53de31d297e3c191c7ea87e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5662000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014ba00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2379b1d6f328000000000000000000000000000000000000000000000000002e237a6c20e0e100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002fa46c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000072dd5b060000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695954426c597a6b334d4330355a54466b4c5456685a5455744f4749785a6930795a474d314e546b354d6a6c6d4f544d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000ad802b8d261f17cbeeb154188f9645eeb83ee14900000000000000000000000000000000000000000000000000000000ba1a494d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd4437b152fd0569aa5dc8c3e3270ced6b207523ab10d828e707c52e5039487d5",
      "signature": {
        "s": "0x612d7494f7ee9ea0d9be959d837aa7bd5263f7df9c836d6109e3697274f9b607",
        "r": "0xa8c034cd8d808fecf976655c9b7f5f27328375c4c216e514f8b417e16de992b9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe08ff89045834679ff8ca6851f152b8f3411d745614b75c6389050a66d47434c",
      "signature": {
        "s": "0x128adb008bd2dc8af14e6d972b57e42dbe33a477c53de31d297e3c191c7ea87e",
        "r": "0x7c315805829c9f195dd50524c48792ab8530fe0ce19000b991d5f81b5e349b0c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3122284877",
    "total": "3122284877"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3122284877",
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
            "amount": "30833750112"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3122284"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYTBlYzk3MC05ZTFkLTVhZTUtOGIxZi0yZGM1NTk5MjlmOTMifQ==",
    "nonce": 5306,
    "balances": {
      "current": "12986854510359336",
      "previous": "12986857635766497"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xad802b8d261f17cbeeb154188f9645eeb83ee149",
    "nonce": 22,
    "balances": {
      "current": "3122284877",
      "previous": "0"
    }
  },
  "blockNumber": "10114658",
  "created": "2020-05-22T08:40:03.478Z",
  "updated": "2020-05-22T08:40:03.550Z",
  "id": "5ec78fe3005df800101bc924"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000ba1a494d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3122284877`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`