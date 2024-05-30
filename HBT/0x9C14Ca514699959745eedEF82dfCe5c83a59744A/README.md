# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9C14Ca514699959745eedEF82dfCe5c83a59744A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000ae1d943600000000000000000000000000000000000000000000000000000000ae1d9436000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ae1d943600000000000000000000000000000000000000000000000000000000ae1d9436c98d89796f76597c5aa5ea806cdcb3ac92ce148545edad25407332672823b8cfddb16d38d8905670adae89d71ad2cf9a68053c821effbff55d8384a2a3896a825043f39540494b302f60bbd73bf7980874be6214ec200d1033d88a91be2d4739000000000000000000000000000000000000000000000000000000000000001b79b8e7522e1cc2ef1dc27ae9a7e6a4cdf64709c675968ea38e7317e259e4b592e4a7b419afc29920b30dd0684fa8c46470fb15a1ef5d8a417689e0919b76c24c6a770760db678fa3e89dd95ad78a7511289370dba392fadedc15a84c27eaebb3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a9d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1637c459097a000000000000000000000000000000000000000000000000002e163872a3308600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002c92d6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a91cfec65000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f5759774d6a68694d5330354d574d7a4c5455305a6a4d744f54566b4e53316d597a677a4e475a684d544d784d6d456966513d3d000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000009c14ca514699959745eedef82dfce5c83a59744a00000000000000000000000000000000000000000000000000000000ae1d9436000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc98d89796f76597c5aa5ea806cdcb3ac92ce148545edad25407332672823b8cf",
      "signature": {
        "s": "0x5043f39540494b302f60bbd73bf7980874be6214ec200d1033d88a91be2d4739",
        "r": "0xddb16d38d8905670adae89d71ad2cf9a68053c821effbff55d8384a2a3896a82",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x79b8e7522e1cc2ef1dc27ae9a7e6a4cdf64709c675968ea38e7317e259e4b592",
      "signature": {
        "s": "0x6a770760db678fa3e89dd95ad78a7511289370dba392fadedc15a84c27eaebb3",
        "r": "0xe4a7b419afc29920b30dd0684fa8c46470fb15a1ef5d8a417689e0919b76c24c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2921174070",
    "total": "2921174070"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2921174070",
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
            "amount": "45395995749"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2921174"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlOWYwMjhiMS05MWMzLTU0ZjMtOTVkNS1mYzgzNGZhMTMxMmEifQ==",
    "nonce": 6813,
    "balances": {
      "current": "12972277701871994",
      "previous": "12972280625967238"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c14ca514699959745eedef82dfce5c83a59744a",
    "nonce": 13,
    "balances": {
      "current": "2921174070",
      "previous": "0"
    }
  },
  "blockNumber": "10114716",
  "created": "2020-05-22T08:51:51.637Z",
  "updated": "2020-05-22T08:51:51.702Z",
  "id": "5ec792a7b0c6090011d5b1ac"
}
```
* *stageAmount*: `2921174070`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000ae1d9436000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ae1d943600000000000000000000000000000000000000000000000000000000ae1d9436c98d89796f76597c5aa5ea806cdcb3ac92ce148545edad25407332672823b8cfddb16d38d8905670adae89d71ad2cf9a68053c821effbff55d8384a2a3896a825043f39540494b302f60bbd73bf7980874be6214ec200d1033d88a91be2d4739000000000000000000000000000000000000000000000000000000000000001b79b8e7522e1cc2ef1dc27ae9a7e6a4cdf64709c675968ea38e7317e259e4b592e4a7b419afc29920b30dd0684fa8c46470fb15a1ef5d8a417689e0919b76c24c6a770760db678fa3e89dd95ad78a7511289370dba392fadedc15a84c27eaebb3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a9d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1637c459097a000000000000000000000000000000000000000000000000002e163872a3308600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002c92d6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a91cfec65000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f5759774d6a68694d5330354d574d7a4c5455305a6a4d744f54566b4e53316d597a677a4e475a684d544d784d6d456966513d3d000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000009c14ca514699959745eedef82dfce5c83a59744a00000000000000000000000000000000000000000000000000000000ae1d9436000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc98d89796f76597c5aa5ea806cdcb3ac92ce148545edad25407332672823b8cf",
      "signature": {
        "s": "0x5043f39540494b302f60bbd73bf7980874be6214ec200d1033d88a91be2d4739",
        "r": "0xddb16d38d8905670adae89d71ad2cf9a68053c821effbff55d8384a2a3896a82",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x79b8e7522e1cc2ef1dc27ae9a7e6a4cdf64709c675968ea38e7317e259e4b592",
      "signature": {
        "s": "0x6a770760db678fa3e89dd95ad78a7511289370dba392fadedc15a84c27eaebb3",
        "r": "0xe4a7b419afc29920b30dd0684fa8c46470fb15a1ef5d8a417689e0919b76c24c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2921174070",
    "total": "2921174070"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2921174070",
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
            "amount": "45395995749"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2921174"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlOWYwMjhiMS05MWMzLTU0ZjMtOTVkNS1mYzgzNGZhMTMxMmEifQ==",
    "nonce": 6813,
    "balances": {
      "current": "12972277701871994",
      "previous": "12972280625967238"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c14ca514699959745eedef82dfce5c83a59744a",
    "nonce": 13,
    "balances": {
      "current": "2921174070",
      "previous": "0"
    }
  },
  "blockNumber": "10114716",
  "created": "2020-05-22T08:51:51.637Z",
  "updated": "2020-05-22T08:51:51.702Z",
  "id": "5ec792a7b0c6090011d5b1ac"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000ae1d9436000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2921174070`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`