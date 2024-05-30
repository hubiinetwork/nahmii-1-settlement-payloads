# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFBf7731253485701F79E5FC705A758eAd19c7aA8`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000763fad1700000000000000000000000000000000000000000000000000000000763fad17000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000763fad1700000000000000000000000000000000000000000000000000000000763fad17f7d37b6535b014a95c15ada15654617f2bc23f3952602cd0b6b7794cb03bba2647ac4a0b53b7a5c4287f268f550f346d34dc08df7576ba830f329363dce8755c75370ca310d3cb33e3bd2b8e27845d8fabbf13fd8232a2a60fa5da9a41165c37000000000000000000000000000000000000000000000000000000000000001c6d54e9bba5d8d01af168b33dee8aef4dc69f734c62a1e20350d8fc647be6f4b60698613a0f3eb6f3c0e87481bbcaa3ba3069ab2a07b31787e434dd196b26060d25fc37763a1d321659db4a14c3c7e6e629c4105bd5f97e6902aa323163006e8f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c7600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1360577381a4000000000000000000000000000000000000000000000000002e1360cdd1744700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e458c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4bd8d83a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596a466d4e57466d4e693034595441304c54566d4e7a4d745954426c4d53316c4f5449334d7a6378596a6b324e44416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fbf7731253485701f79e5fc705a758ead19c7aa800000000000000000000000000000000000000000000000000000000763fad17000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf7d37b6535b014a95c15ada15654617f2bc23f3952602cd0b6b7794cb03bba26",
      "signature": {
        "s": "0x75370ca310d3cb33e3bd2b8e27845d8fabbf13fd8232a2a60fa5da9a41165c37",
        "r": "0x47ac4a0b53b7a5c4287f268f550f346d34dc08df7576ba830f329363dce8755c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6d54e9bba5d8d01af168b33dee8aef4dc69f734c62a1e20350d8fc647be6f4b6",
      "signature": {
        "s": "0x25fc37763a1d321659db4a14c3c7e6e629c4105bd5f97e6902aa323163006e8f",
        "r": "0x0698613a0f3eb6f3c0e87481bbcaa3ba3069ab2a07b31787e434dd196b26060d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1983884567",
    "total": "1983884567"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1983884567",
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
            "amount": "48517142586"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1983884"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YjFmNWFmNi04YTA0LTVmNzMtYTBlMS1lOTI3MzcxYjk2NDAifQ==",
    "nonce": 7286,
    "balances": {
      "current": "12969153433665956",
      "previous": "12969155419534407"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfbf7731253485701f79e5fc705a758ead19c7aa8",
    "nonce": 22,
    "balances": {
      "current": "1983884567",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:40.878Z",
  "updated": "2020-05-22T08:55:40.961Z",
  "id": "5ec7938cb0c6090011d5b24b"
}
```
* *stageAmount*: `1983884567`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000763fad17000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000763fad1700000000000000000000000000000000000000000000000000000000763fad17f7d37b6535b014a95c15ada15654617f2bc23f3952602cd0b6b7794cb03bba2647ac4a0b53b7a5c4287f268f550f346d34dc08df7576ba830f329363dce8755c75370ca310d3cb33e3bd2b8e27845d8fabbf13fd8232a2a60fa5da9a41165c37000000000000000000000000000000000000000000000000000000000000001c6d54e9bba5d8d01af168b33dee8aef4dc69f734c62a1e20350d8fc647be6f4b60698613a0f3eb6f3c0e87481bbcaa3ba3069ab2a07b31787e434dd196b26060d25fc37763a1d321659db4a14c3c7e6e629c4105bd5f97e6902aa323163006e8f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c7600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1360577381a4000000000000000000000000000000000000000000000000002e1360cdd1744700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e458c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4bd8d83a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596a466d4e57466d4e693034595441304c54566d4e7a4d745954426c4d53316c4f5449334d7a6378596a6b324e44416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000fbf7731253485701f79e5fc705a758ead19c7aa800000000000000000000000000000000000000000000000000000000763fad17000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf7d37b6535b014a95c15ada15654617f2bc23f3952602cd0b6b7794cb03bba26",
      "signature": {
        "s": "0x75370ca310d3cb33e3bd2b8e27845d8fabbf13fd8232a2a60fa5da9a41165c37",
        "r": "0x47ac4a0b53b7a5c4287f268f550f346d34dc08df7576ba830f329363dce8755c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6d54e9bba5d8d01af168b33dee8aef4dc69f734c62a1e20350d8fc647be6f4b6",
      "signature": {
        "s": "0x25fc37763a1d321659db4a14c3c7e6e629c4105bd5f97e6902aa323163006e8f",
        "r": "0x0698613a0f3eb6f3c0e87481bbcaa3ba3069ab2a07b31787e434dd196b26060d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1983884567",
    "total": "1983884567"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1983884567",
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
            "amount": "48517142586"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1983884"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YjFmNWFmNi04YTA0LTVmNzMtYTBlMS1lOTI3MzcxYjk2NDAifQ==",
    "nonce": 7286,
    "balances": {
      "current": "12969153433665956",
      "previous": "12969155419534407"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfbf7731253485701f79e5fc705a758ead19c7aa8",
    "nonce": 22,
    "balances": {
      "current": "1983884567",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:40.878Z",
  "updated": "2020-05-22T08:55:40.961Z",
  "id": "5ec7938cb0c6090011d5b24b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000763fad17000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1983884567`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`