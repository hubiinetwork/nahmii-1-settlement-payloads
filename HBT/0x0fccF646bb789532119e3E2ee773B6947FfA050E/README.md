# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0fccF646bb789532119e3E2ee773B6947FfA050E`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000052c7637c0000000000000000000000000000000000000000000000000000000052c7637c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c7637c0000000000000000000000000000000000000000000000000000000052c7637c05f6ac9ce87ab6bdb098c34bfca04b453bfbc78fcbbbf137333b386e5a014cdf67c2311db3271fab49f2538c4111c50b486491fbf8f3dd6bca7c7874017a651f41e40045bffe5519db61ad446a835ec60d1cabd819d7ac568a920e0608a53d7f000000000000000000000000000000000000000000000000000000000000001bb9d0cc9bca159682f1e91c24a698cfa12a90ed0070487bae6455825901c515b9054f1e5844bc540bc1646b9531f3279d1777ae81571acc2f45e5f3033553b2b40a6d0dc29124f38f246e0fa7451eb8de369f06c17aa6f915d89b7d7383d3fb61000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56790000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000174a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b27f8aafc3c000000000000000000000000000000000000000000000000002e1b284b8790b600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094e7fcc95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977595467314d7a5a6b4f5330784e7a6b344c5455334d6a45744f546b355969316a59545a6d5957566a4d4755354e6a676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000fccf646bb789532119e3e2ee773b6947ffa050e0000000000000000000000000000000000000000000000000000000052c7637c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x05f6ac9ce87ab6bdb098c34bfca04b453bfbc78fcbbbf137333b386e5a014cdf",
      "signature": {
        "s": "0x41e40045bffe5519db61ad446a835ec60d1cabd819d7ac568a920e0608a53d7f",
        "r": "0x67c2311db3271fab49f2538c4111c50b486491fbf8f3dd6bca7c7874017a651f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb9d0cc9bca159682f1e91c24a698cfa12a90ed0070487bae6455825901c515b9",
      "signature": {
        "s": "0x0a6d0dc29124f38f246e0fa7451eb8de369f06c17aa6f915d89b7d7383d3fb61",
        "r": "0x054f1e5844bc540bc1646b9531f3279d1777ae81571acc2f45e5f3033553b2b4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388798844",
    "total": "1388798844"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388798844",
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
            "amount": "39971703957"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388798"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYTg1MzZkOS0xNzk4LTU3MjEtOTk5Yi1jYTZmYWVjMGU5NjgifQ==",
    "nonce": 5962,
    "balances": {
      "current": "12977707418319932",
      "previous": "12977708808507574"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fccf646bb789532119e3e2ee773b6947ffa050e",
    "nonce": 22,
    "balances": {
      "current": "1388798844",
      "previous": "0"
    }
  },
  "blockNumber": "10114681",
  "created": "2020-05-22T08:45:23.086Z",
  "updated": "2020-05-22T08:45:23.161Z",
  "id": "5ec79123b0c6090011d5b081"
}
```
* *stageAmount*: `1388798844`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000052c7637c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c7637c0000000000000000000000000000000000000000000000000000000052c7637c05f6ac9ce87ab6bdb098c34bfca04b453bfbc78fcbbbf137333b386e5a014cdf67c2311db3271fab49f2538c4111c50b486491fbf8f3dd6bca7c7874017a651f41e40045bffe5519db61ad446a835ec60d1cabd819d7ac568a920e0608a53d7f000000000000000000000000000000000000000000000000000000000000001bb9d0cc9bca159682f1e91c24a698cfa12a90ed0070487bae6455825901c515b9054f1e5844bc540bc1646b9531f3279d1777ae81571acc2f45e5f3033553b2b40a6d0dc29124f38f246e0fa7451eb8de369f06c17aa6f915d89b7d7383d3fb61000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56790000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000174a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b27f8aafc3c000000000000000000000000000000000000000000000000002e1b284b8790b600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094e7fcc95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977595467314d7a5a6b4f5330784e7a6b344c5455334d6a45744f546b355969316a59545a6d5957566a4d4755354e6a676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000fccf646bb789532119e3e2ee773b6947ffa050e0000000000000000000000000000000000000000000000000000000052c7637c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x05f6ac9ce87ab6bdb098c34bfca04b453bfbc78fcbbbf137333b386e5a014cdf",
      "signature": {
        "s": "0x41e40045bffe5519db61ad446a835ec60d1cabd819d7ac568a920e0608a53d7f",
        "r": "0x67c2311db3271fab49f2538c4111c50b486491fbf8f3dd6bca7c7874017a651f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb9d0cc9bca159682f1e91c24a698cfa12a90ed0070487bae6455825901c515b9",
      "signature": {
        "s": "0x0a6d0dc29124f38f246e0fa7451eb8de369f06c17aa6f915d89b7d7383d3fb61",
        "r": "0x054f1e5844bc540bc1646b9531f3279d1777ae81571acc2f45e5f3033553b2b4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388798844",
    "total": "1388798844"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388798844",
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
            "amount": "39971703957"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388798"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYTg1MzZkOS0xNzk4LTU3MjEtOTk5Yi1jYTZmYWVjMGU5NjgifQ==",
    "nonce": 5962,
    "balances": {
      "current": "12977707418319932",
      "previous": "12977708808507574"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fccf646bb789532119e3e2ee773b6947ffa050e",
    "nonce": 22,
    "balances": {
      "current": "1388798844",
      "previous": "0"
    }
  },
  "blockNumber": "10114681",
  "created": "2020-05-22T08:45:23.086Z",
  "updated": "2020-05-22T08:45:23.161Z",
  "id": "5ec79123b0c6090011d5b081"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000052c7637c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1388798844`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`