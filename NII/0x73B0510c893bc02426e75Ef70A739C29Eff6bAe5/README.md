# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x73B0510c893bc02426e75Ef70A739C29Eff6bAe5`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001ed7cbb65172399890000000000000000000000000000000000000000000000001d91d94c249b7ea30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001d91d94c249b7ea3000000000000000000000000000000000000000000000001ed7cbb6517239989ed479235382cced3efce010edb6a8af594ac44f0d3227229dc7d9eaa0f462abec5a59e2db13061436769116cb3ec946b5659394117edd90ed0f3c52a25a57c62238beb521e7b5b3720807b0283b6baf8d8c000ec970d14a31382fce50baaf77b000000000000000000000000000000000000000000000000000000000000001c1a80a00f643a6b3b9480cb5805ad1ec1eb07842991dfe987d2d8279e8b84e9b9089a172d515894d2ecf1eaab1ffb8e11e7c3348fe43e0929c3509611fe4594b15ea960600a6b0e2adfe7e622cd4c7e26eb67be0e92f85300e5142ee39ac429bb000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b4f7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000035f375963ffeec3bcea10000000000000000000000000000000000000000000035f3932fab2cad8cb48f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000791e19cb5674b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005de95ca857c1be91a100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b595445784d44517a4e6930345a6d55794c5456684f445174596d59354d693168597a517a4d324d335a6a686a4d47516966513d3d000000000000000000000000000000000000000000000000000000000000001100000000000000000000000073b0510c893bc02426e75ef70a739c29eff6bae5000000000000000000000000000000000000000000000001ed7cbb6517239989000000000000000000000000000000000000000000000001cfeae218f2881ae600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xed479235382cced3efce010edb6a8af594ac44f0d3227229dc7d9eaa0f462abe",
      "signature": {
        "s": "0x238beb521e7b5b3720807b0283b6baf8d8c000ec970d14a31382fce50baaf77b",
        "r": "0xc5a59e2db13061436769116cb3ec946b5659394117edd90ed0f3c52a25a57c62",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1a80a00f643a6b3b9480cb5805ad1ec1eb07842991dfe987d2d8279e8b84e9b9",
      "signature": {
        "s": "0x5ea960600a6b0e2adfe7e622cd4c7e26eb67be0e92f85300e5142ee39ac429bb",
        "r": "0x089a172d515894d2ecf1eaab1ffb8e11e7c3348fe43e0929c3509611fe4594b1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2130723019777867427",
    "total": "35559502800664893833"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2130723019777867427",
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
            "amount": "27717803184936784042512"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2130723019777867"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkYTExMDQzNi04ZmUyLTVhODQtYmY5Mi1hYzQzM2M3ZjhjMGQifQ==",
    "nonce": 111863,
    "balances": {
      "current": "254776455432115679121057",
      "previous": "254778588285858476766351"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x73b0510c893bc02426e75ef70a739c29eff6bae5",
    "nonce": 17,
    "balances": {
      "current": "35559502800664893833",
      "previous": "33428779780887026406"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:39.824Z",
  "updated": "2022-05-04T09:00:39.904Z",
  "id": "627240b77832e20011830d95"
}
```
* *stageAmount*: `35559502800664893833`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000001d91d94c249b7ea30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001d91d94c249b7ea3000000000000000000000000000000000000000000000001ed7cbb6517239989ed479235382cced3efce010edb6a8af594ac44f0d3227229dc7d9eaa0f462abec5a59e2db13061436769116cb3ec946b5659394117edd90ed0f3c52a25a57c62238beb521e7b5b3720807b0283b6baf8d8c000ec970d14a31382fce50baaf77b000000000000000000000000000000000000000000000000000000000000001c1a80a00f643a6b3b9480cb5805ad1ec1eb07842991dfe987d2d8279e8b84e9b9089a172d515894d2ecf1eaab1ffb8e11e7c3348fe43e0929c3509611fe4594b15ea960600a6b0e2adfe7e622cd4c7e26eb67be0e92f85300e5142ee39ac429bb000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b4f7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000035f375963ffeec3bcea10000000000000000000000000000000000000000000035f3932fab2cad8cb48f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000791e19cb5674b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005de95ca857c1be91a100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b595445784d44517a4e6930345a6d55794c5456684f445174596d59354d693168597a517a4d324d335a6a686a4d47516966513d3d000000000000000000000000000000000000000000000000000000000000001100000000000000000000000073b0510c893bc02426e75ef70a739c29eff6bae5000000000000000000000000000000000000000000000001ed7cbb6517239989000000000000000000000000000000000000000000000001cfeae218f2881ae600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xed479235382cced3efce010edb6a8af594ac44f0d3227229dc7d9eaa0f462abe",
      "signature": {
        "s": "0x238beb521e7b5b3720807b0283b6baf8d8c000ec970d14a31382fce50baaf77b",
        "r": "0xc5a59e2db13061436769116cb3ec946b5659394117edd90ed0f3c52a25a57c62",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1a80a00f643a6b3b9480cb5805ad1ec1eb07842991dfe987d2d8279e8b84e9b9",
      "signature": {
        "s": "0x5ea960600a6b0e2adfe7e622cd4c7e26eb67be0e92f85300e5142ee39ac429bb",
        "r": "0x089a172d515894d2ecf1eaab1ffb8e11e7c3348fe43e0929c3509611fe4594b1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2130723019777867427",
    "total": "35559502800664893833"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2130723019777867427",
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
            "amount": "27717803184936784042512"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2130723019777867"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkYTExMDQzNi04ZmUyLTVhODQtYmY5Mi1hYzQzM2M3ZjhjMGQifQ==",
    "nonce": 111863,
    "balances": {
      "current": "254776455432115679121057",
      "previous": "254778588285858476766351"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x73b0510c893bc02426e75ef70a739c29eff6bae5",
    "nonce": 17,
    "balances": {
      "current": "35559502800664893833",
      "previous": "33428779780887026406"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:39.824Z",
  "updated": "2022-05-04T09:00:39.904Z",
  "id": "627240b77832e20011830d95"
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
0x0f200f9b000000000000000000000000000000000000000000000001ed7cbb65172399890000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `35559502800664893833`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`