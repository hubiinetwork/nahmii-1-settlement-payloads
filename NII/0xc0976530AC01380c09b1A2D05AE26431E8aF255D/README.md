# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc0976530AC01380c09b1A2D05AE26431E8aF255D`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000e07e89b5333b90cc000000000000000000000000000000000000000000000000e07e89b5333b90cc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e07e89b5333b90cc000000000000000000000000000000000000000000000000e07e89b5333b90cc5926e67f2683c601edb51f3d909fef383bca91c385fade21cfd5c4ccc03de834568dce67f061568952fddffa3641d2d1a0bd0b5b79441a3c3ef12ea9c9168b784091a5d7c4c069c9ba65621f04ec6a7853ff0734d591a6c607108197294a2226000000000000000000000000000000000000000000000000000000000000001c6f95252c2bc38c417bae9f02230198ec4c682bf76229d97df798f66e46961a2b96973bdafdd8654615d80301e6231a63e0a8ce1ace0b5e9e190d01c5283616d91b18be9b9b5767915b0673013adda1237de218ae9b473377c59d89a7b9527e7c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bd3847000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000121cf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002300d6f6d0378f1bddee000000000000000000000000000000000000000000002301b7aed261eeae46ad00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003978752c56d7f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003598f38fc1b5879eb680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5455344e6a42694d7931685a6a686b4c5456694d6a4174596a59335a69303259574a6d597a63334d44417a5a6a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000c0976530ac01380c09b1a2d05ae26431e8af255d000000000000000000000000000000000000000000000000e07e89b5333b90cc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5926e67f2683c601edb51f3d909fef383bca91c385fade21cfd5c4ccc03de834",
      "signature": {
        "s": "0x4091a5d7c4c069c9ba65621f04ec6a7853ff0734d591a6c607108197294a2226",
        "r": "0x568dce67f061568952fddffa3641d2d1a0bd0b5b79441a3c3ef12ea9c9168b78",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6f95252c2bc38c417bae9f02230198ec4c682bf76229d97df798f66e46961a2b",
      "signature": {
        "s": "0x1b18be9b9b5767915b0673013adda1237de218ae9b473377c59d89a7b9527e7c",
        "r": "0x96973bdafdd8654615d80301e6231a63e0a8ce1ace0b5e9e190d01c5283616d9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16176518322903027916",
    "total": "16176518322903027916"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16176518322903027916",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "15819179946909583928168"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16176518322903027"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZTU4NjBiMy1hZjhkLTViMjAtYjY3Zi02YWJmYzc3MDAzZjMifQ==",
    "nonce": 74191,
    "balances": {
      "current": "165298316697343012625902",
      "previous": "165314509392184238556845"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc0976530ac01380c09b1a2d05ae26431e8af255d",
    "nonce": 1,
    "balances": {
      "current": "16176518322903027916",
      "previous": "0"
    }
  },
  "blockNumber": "12400711",
  "created": "2021-05-09T14:37:16.253Z",
  "updated": "2021-05-09T14:37:16.340Z",
  "id": "6097f39c0f95a80011b4b473"
}
```
* *stageAmount*: `16176518322903027916`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000e07e89b5333b90cc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e07e89b5333b90cc000000000000000000000000000000000000000000000000e07e89b5333b90cc5926e67f2683c601edb51f3d909fef383bca91c385fade21cfd5c4ccc03de834568dce67f061568952fddffa3641d2d1a0bd0b5b79441a3c3ef12ea9c9168b784091a5d7c4c069c9ba65621f04ec6a7853ff0734d591a6c607108197294a2226000000000000000000000000000000000000000000000000000000000000001c6f95252c2bc38c417bae9f02230198ec4c682bf76229d97df798f66e46961a2b96973bdafdd8654615d80301e6231a63e0a8ce1ace0b5e9e190d01c5283616d91b18be9b9b5767915b0673013adda1237de218ae9b473377c59d89a7b9527e7c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bd3847000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000121cf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002300d6f6d0378f1bddee000000000000000000000000000000000000000000002301b7aed261eeae46ad00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003978752c56d7f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003598f38fc1b5879eb680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5455344e6a42694d7931685a6a686b4c5456694d6a4174596a59335a69303259574a6d597a63334d44417a5a6a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000c0976530ac01380c09b1a2d05ae26431e8af255d000000000000000000000000000000000000000000000000e07e89b5333b90cc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5926e67f2683c601edb51f3d909fef383bca91c385fade21cfd5c4ccc03de834",
      "signature": {
        "s": "0x4091a5d7c4c069c9ba65621f04ec6a7853ff0734d591a6c607108197294a2226",
        "r": "0x568dce67f061568952fddffa3641d2d1a0bd0b5b79441a3c3ef12ea9c9168b78",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6f95252c2bc38c417bae9f02230198ec4c682bf76229d97df798f66e46961a2b",
      "signature": {
        "s": "0x1b18be9b9b5767915b0673013adda1237de218ae9b473377c59d89a7b9527e7c",
        "r": "0x96973bdafdd8654615d80301e6231a63e0a8ce1ace0b5e9e190d01c5283616d9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16176518322903027916",
    "total": "16176518322903027916"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16176518322903027916",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "15819179946909583928168"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16176518322903027"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZTU4NjBiMy1hZjhkLTViMjAtYjY3Zi02YWJmYzc3MDAzZjMifQ==",
    "nonce": 74191,
    "balances": {
      "current": "165298316697343012625902",
      "previous": "165314509392184238556845"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc0976530ac01380c09b1a2d05ae26431e8af255d",
    "nonce": 1,
    "balances": {
      "current": "16176518322903027916",
      "previous": "0"
    }
  },
  "blockNumber": "12400711",
  "created": "2021-05-09T14:37:16.253Z",
  "updated": "2021-05-09T14:37:16.340Z",
  "id": "6097f39c0f95a80011b4b473"
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
0x0f200f9b000000000000000000000000000000000000000000000000e07e89b5333b90cc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `16176518322903027916`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`