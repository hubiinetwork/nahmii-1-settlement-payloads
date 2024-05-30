# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6A3A19236c4F413C986271459f907f0C0e40DdaB`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000b2dec1c1c0d4d427000000000000000000000000000000000000000000000000b2dec1c1c0d4d4270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000b2dec1c1c0d4d427000000000000000000000000000000000000000000000000b2dec1c1c0d4d42772def1f1db117d609dc689023a799f9d59e2a9861c227ecb79afb72d66ae7244aedb29456db3ba0e26991422fc23021ce4c2e7cde7c997cee9a5d27fe5e159642637a7a01cecfffb6cc156ed3ad34abb2a46bf3235b1a5d4d0e3f6c295639696000000000000000000000000000000000000000000000000000000000000001b8a42da01aea8de0469018dd03da4cc366350b1faccd0f2e500833dbd485641c4fe6825c8ad6b7e598f7bdc5e9a73dd55e839a53d08825a0a71ded3392b1836f61d76e2625e9f0819a34dcff614f17e326f00f3b8045ecde00154aad592e1d364000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bac19300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011574000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002333f3a7f4c5140e8d1d000000000000000000000000000000000000000000002334a6b480f5df93b88400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000002dca6f0ab057400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003235a3a22bd1bd3b91a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e5463324d325a6d4e4331695a4464694c54557a4d446b744f44426a4d4330774f575933597a4531597a4d32596d496966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000006a3a19236c4f413c986271459f907f0c0e40ddab000000000000000000000000000000000000000000000000b2dec1c1c0d4d427000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x72def1f1db117d609dc689023a799f9d59e2a9861c227ecb79afb72d66ae7244",
      "signature": {
        "s": "0x2637a7a01cecfffb6cc156ed3ad34abb2a46bf3235b1a5d4d0e3f6c295639696",
        "r": "0xaedb29456db3ba0e26991422fc23021ce4c2e7cde7c997cee9a5d27fe5e15964",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8a42da01aea8de0469018dd03da4cc366350b1faccd0f2e500833dbd485641c4",
      "signature": {
        "s": "0x1d76e2625e9f0819a34dcff614f17e326f00f3b8045ecde00154aad592e1d364",
        "r": "0xfe6825c8ad6b7e598f7bdc5e9a73dd55e839a53d08825a0a71ded3392b1836f6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12888952221488960551",
    "total": "12888952221488960551"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12888952221488960551",
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
            "amount": "14819237038396443703578"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12888952221488960"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNTc2M2ZmNC1iZDdiLTUzMDktODBjMC0wOWY3YzE1YzM2YmIifQ==",
    "nonce": 71028,
    "balances": {
      "current": "166241168118996379012381",
      "previous": "166254069960170089461892"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6a3a19236c4f413c986271459f907f0c0e40ddab",
    "nonce": 1,
    "balances": {
      "current": "12888952221488960551",
      "previous": "0"
    }
  },
  "blockNumber": "12239251",
  "created": "2021-04-14T16:22:29.365Z",
  "updated": "2021-04-14T16:22:29.456Z",
  "id": "607716c550c3ba0010570e34"
}
```
* *stageAmount*: `12888952221488960551`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000b2dec1c1c0d4d4270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000b2dec1c1c0d4d427000000000000000000000000000000000000000000000000b2dec1c1c0d4d42772def1f1db117d609dc689023a799f9d59e2a9861c227ecb79afb72d66ae7244aedb29456db3ba0e26991422fc23021ce4c2e7cde7c997cee9a5d27fe5e159642637a7a01cecfffb6cc156ed3ad34abb2a46bf3235b1a5d4d0e3f6c295639696000000000000000000000000000000000000000000000000000000000000001b8a42da01aea8de0469018dd03da4cc366350b1faccd0f2e500833dbd485641c4fe6825c8ad6b7e598f7bdc5e9a73dd55e839a53d08825a0a71ded3392b1836f61d76e2625e9f0819a34dcff614f17e326f00f3b8045ecde00154aad592e1d364000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bac19300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011574000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002333f3a7f4c5140e8d1d000000000000000000000000000000000000000000002334a6b480f5df93b88400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000002dca6f0ab057400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003235a3a22bd1bd3b91a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e5463324d325a6d4e4331695a4464694c54557a4d446b744f44426a4d4330774f575933597a4531597a4d32596d496966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000006a3a19236c4f413c986271459f907f0c0e40ddab000000000000000000000000000000000000000000000000b2dec1c1c0d4d427000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x72def1f1db117d609dc689023a799f9d59e2a9861c227ecb79afb72d66ae7244",
      "signature": {
        "s": "0x2637a7a01cecfffb6cc156ed3ad34abb2a46bf3235b1a5d4d0e3f6c295639696",
        "r": "0xaedb29456db3ba0e26991422fc23021ce4c2e7cde7c997cee9a5d27fe5e15964",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8a42da01aea8de0469018dd03da4cc366350b1faccd0f2e500833dbd485641c4",
      "signature": {
        "s": "0x1d76e2625e9f0819a34dcff614f17e326f00f3b8045ecde00154aad592e1d364",
        "r": "0xfe6825c8ad6b7e598f7bdc5e9a73dd55e839a53d08825a0a71ded3392b1836f6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12888952221488960551",
    "total": "12888952221488960551"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12888952221488960551",
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
            "amount": "14819237038396443703578"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12888952221488960"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNTc2M2ZmNC1iZDdiLTUzMDktODBjMC0wOWY3YzE1YzM2YmIifQ==",
    "nonce": 71028,
    "balances": {
      "current": "166241168118996379012381",
      "previous": "166254069960170089461892"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6a3a19236c4f413c986271459f907f0c0e40ddab",
    "nonce": 1,
    "balances": {
      "current": "12888952221488960551",
      "previous": "0"
    }
  },
  "blockNumber": "12239251",
  "created": "2021-04-14T16:22:29.365Z",
  "updated": "2021-04-14T16:22:29.456Z",
  "id": "607716c550c3ba0010570e34"
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
0x0f200f9b000000000000000000000000000000000000000000000000b2dec1c1c0d4d4270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `12888952221488960551`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`