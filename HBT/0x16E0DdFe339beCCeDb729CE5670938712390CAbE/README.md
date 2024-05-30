# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x16E0DdFe339beCCeDb729CE5670938712390CAbE`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000037a158910000000000000000000000000000000000000000000000000000000037a15891000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000037a158910000000000000000000000000000000000000000000000000000000037a15891c1445986ec479a4e637bcf7c0dac727ce1ce22ee224e0ea458c552c284e7079d74ac7f6b590db0c5cb722cb0ef6adcb4990cda3e9a4a863b82cd61a00ae48b5b2216ff3fdde9dec58aa60062e733403cf7aedbac530a71737f2f39940e685b5d000000000000000000000000000000000000000000000000000000000000001bfccd1049080dfc46786fd6fe20902554253a9475a6b4030a35335c05028bbd4b04b1e60fda26f4dac0079a3236dd13c2f1b9061fd483a22b0cf351ea9b182c441c949efeb4f7307b42128e7fba7fb6966fb4adca8f948cf74a21a0db297e41a2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000159200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d5ef53b194d000000000000000000000000000000000000000000000000002e1d5f2ceaafa600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000e3dc8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd7ee3f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f4445324d6a6c6d4f4330345a5745794c54566b4d7a4574596d5a695a4331684e7a466a59544a6c4e7a6c6b5a6a596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000016e0ddfe339beccedb729ce5670938712390cabe0000000000000000000000000000000000000000000000000000000037a15891000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc1445986ec479a4e637bcf7c0dac727ce1ce22ee224e0ea458c552c284e7079d",
      "signature": {
        "s": "0x2216ff3fdde9dec58aa60062e733403cf7aedbac530a71737f2f39940e685b5d",
        "r": "0x74ac7f6b590db0c5cb722cb0ef6adcb4990cda3e9a4a863b82cd61a00ae48b5b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfccd1049080dfc46786fd6fe20902554253a9475a6b4030a35335c05028bbd4b",
      "signature": {
        "s": "0x1c949efeb4f7307b42128e7fba7fb6966fb4adca8f948cf74a21a0db297e41a2",
        "r": "0x04b1e60fda26f4dac0079a3236dd13c2f1b9061fd483a22b0cf351ea9b182c44",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "933320849",
    "total": "933320849"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "933320849",
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
            "amount": "37538948087"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "933320"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmODE2MjlmOC04ZWEyLTVkMzEtYmZiZC1hNzFjYTJlNzlkZjYifQ==",
    "nonce": 5522,
    "balances": {
      "current": "12980142607112525",
      "previous": "12980143541366694"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x16e0ddfe339beccedb729ce5670938712390cabe",
    "nonce": 22,
    "balances": {
      "current": "933320849",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:50.502Z",
  "updated": "2020-05-22T08:41:50.574Z",
  "id": "5ec7904eb0c6090011d5aff5"
}
```
* *stageAmount*: `933320849`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000037a15891000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000037a158910000000000000000000000000000000000000000000000000000000037a15891c1445986ec479a4e637bcf7c0dac727ce1ce22ee224e0ea458c552c284e7079d74ac7f6b590db0c5cb722cb0ef6adcb4990cda3e9a4a863b82cd61a00ae48b5b2216ff3fdde9dec58aa60062e733403cf7aedbac530a71737f2f39940e685b5d000000000000000000000000000000000000000000000000000000000000001bfccd1049080dfc46786fd6fe20902554253a9475a6b4030a35335c05028bbd4b04b1e60fda26f4dac0079a3236dd13c2f1b9061fd483a22b0cf351ea9b182c441c949efeb4f7307b42128e7fba7fb6966fb4adca8f948cf74a21a0db297e41a2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a566a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000159200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d5ef53b194d000000000000000000000000000000000000000000000000002e1d5f2ceaafa600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000e3dc8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd7ee3f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f4445324d6a6c6d4f4330345a5745794c54566b4d7a4574596d5a695a4331684e7a466a59544a6c4e7a6c6b5a6a596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000016e0ddfe339beccedb729ce5670938712390cabe0000000000000000000000000000000000000000000000000000000037a15891000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc1445986ec479a4e637bcf7c0dac727ce1ce22ee224e0ea458c552c284e7079d",
      "signature": {
        "s": "0x2216ff3fdde9dec58aa60062e733403cf7aedbac530a71737f2f39940e685b5d",
        "r": "0x74ac7f6b590db0c5cb722cb0ef6adcb4990cda3e9a4a863b82cd61a00ae48b5b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfccd1049080dfc46786fd6fe20902554253a9475a6b4030a35335c05028bbd4b",
      "signature": {
        "s": "0x1c949efeb4f7307b42128e7fba7fb6966fb4adca8f948cf74a21a0db297e41a2",
        "r": "0x04b1e60fda26f4dac0079a3236dd13c2f1b9061fd483a22b0cf351ea9b182c44",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "933320849",
    "total": "933320849"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "933320849",
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
            "amount": "37538948087"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "933320"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmODE2MjlmOC04ZWEyLTVkMzEtYmZiZC1hNzFjYTJlNzlkZjYifQ==",
    "nonce": 5522,
    "balances": {
      "current": "12980142607112525",
      "previous": "12980143541366694"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x16e0ddfe339beccedb729ce5670938712390cabe",
    "nonce": 22,
    "balances": {
      "current": "933320849",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:50.502Z",
  "updated": "2020-05-22T08:41:50.574Z",
  "id": "5ec7904eb0c6090011d5aff5"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000037a15891000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `933320849`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`