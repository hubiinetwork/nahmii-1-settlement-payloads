# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9ba0a2EdCCBeB7d114C29d37fe15C18A058A0a7B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000006cd5422f9d9e9f1dd1000000000000000000000000000000000000000000000002948f174807d22c290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000002948f174807d22c2900000000000000000000000000000000000000000000004867ed2642175ad97c8591543bbb667fdd19d7dcb940fbdf64c7a744db9b9937a98dc374d9e7bf6c18ca2a2ae1e17e515028b547acc3afc58f915d85c11991fbbad82407728b6f73335f25125497e3b46997fc521c6b1a721f6aab28068d82c698b7b556ac396c4f21000000000000000000000000000000000000000000000000000000000000001c01ba056d5a332de3d4d3a954dc7e8d7f7042e2c139eee3e808e0c24f243d144b194d7a58c4253627e4ab7f6eb25daea62584c31dd1a25edb773c91f4de22e2aa2f28c16103610ac95aad03ed50a1e7a8ed1a9d4d66ba966beb1c64c44c909693000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b708000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002f6de0b5a83832270978000000000000000000000000000000000000000000002f7075edd9e464fd427900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000a91a642b040cd80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e040c6e8dd7d88f56b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a64694d6d59795969316c4e5463324c5455344e446b744f44646d4f433031597a526d4e6d5a6a4d6a6b325a54556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009ba0a2edccbeb7d114c29d37fe15c18a058a0a7b00000000000000000000000000000000000000000000006cd5422f9d9e9f1dd100000000000000000000000000000000000000000000006a40b3185596ccf1a800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8591543bbb667fdd19d7dcb940fbdf64c7a744db9b9937a98dc374d9e7bf6c18",
      "signature": {
        "s": "0x5f25125497e3b46997fc521c6b1a721f6aab28068d82c698b7b556ac396c4f21",
        "r": "0xca2a2ae1e17e515028b547acc3afc58f915d85c11991fbbad82407728b6f7333",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x01ba056d5a332de3d4d3a954dc7e8d7f7042e2c139eee3e808e0c24f243d144b",
      "signature": {
        "s": "0x2f28c16103610ac95aad03ed50a1e7a8ed1a9d4d66ba966beb1c64c44c909693",
        "r": "0x194d7a58c4253627e4ab7f6eb25daea62584c31dd1a25edb773c91f4de22e2aa",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "47598288584838360105",
    "total": "1335654257127776246140"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "47598288584838360105",
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
            "amount": "27748570760960973272427"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "47598288584838360"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YzdiMmYyYi1lNTc2LTU4NDktODdmOC01YzRmNmZjMjk2ZTUifQ==",
    "nonce": 112392,
    "balances": {
      "current": "223978111831902259710328",
      "previous": "224025757718775682908793"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9ba0a2edccbeb7d114c29d37fe15c18a058a0a7b",
    "nonce": 46,
    "balances": {
      "current": "2007615257193190727121",
      "previous": "1960016968608352367016"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:33.642Z",
  "updated": "2022-05-04T09:03:33.728Z",
  "id": "627241657832e20011830e3f"
}
```
* *stageAmount*: `2007615257193190727121`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000002948f174807d22c290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000002948f174807d22c2900000000000000000000000000000000000000000000004867ed2642175ad97c8591543bbb667fdd19d7dcb940fbdf64c7a744db9b9937a98dc374d9e7bf6c18ca2a2ae1e17e515028b547acc3afc58f915d85c11991fbbad82407728b6f73335f25125497e3b46997fc521c6b1a721f6aab28068d82c698b7b556ac396c4f21000000000000000000000000000000000000000000000000000000000000001c01ba056d5a332de3d4d3a954dc7e8d7f7042e2c139eee3e808e0c24f243d144b194d7a58c4253627e4ab7f6eb25daea62584c31dd1a25edb773c91f4de22e2aa2f28c16103610ac95aad03ed50a1e7a8ed1a9d4d66ba966beb1c64c44c909693000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b708000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002f6de0b5a83832270978000000000000000000000000000000000000000000002f7075edd9e464fd427900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000a91a642b040cd80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e040c6e8dd7d88f56b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a64694d6d59795969316c4e5463324c5455344e446b744f44646d4f433031597a526d4e6d5a6a4d6a6b325a54556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009ba0a2edccbeb7d114c29d37fe15c18a058a0a7b00000000000000000000000000000000000000000000006cd5422f9d9e9f1dd100000000000000000000000000000000000000000000006a40b3185596ccf1a800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8591543bbb667fdd19d7dcb940fbdf64c7a744db9b9937a98dc374d9e7bf6c18",
      "signature": {
        "s": "0x5f25125497e3b46997fc521c6b1a721f6aab28068d82c698b7b556ac396c4f21",
        "r": "0xca2a2ae1e17e515028b547acc3afc58f915d85c11991fbbad82407728b6f7333",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x01ba056d5a332de3d4d3a954dc7e8d7f7042e2c139eee3e808e0c24f243d144b",
      "signature": {
        "s": "0x2f28c16103610ac95aad03ed50a1e7a8ed1a9d4d66ba966beb1c64c44c909693",
        "r": "0x194d7a58c4253627e4ab7f6eb25daea62584c31dd1a25edb773c91f4de22e2aa",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "47598288584838360105",
    "total": "1335654257127776246140"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "47598288584838360105",
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
            "amount": "27748570760960973272427"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "47598288584838360"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YzdiMmYyYi1lNTc2LTU4NDktODdmOC01YzRmNmZjMjk2ZTUifQ==",
    "nonce": 112392,
    "balances": {
      "current": "223978111831902259710328",
      "previous": "224025757718775682908793"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9ba0a2edccbeb7d114c29d37fe15c18a058a0a7b",
    "nonce": 46,
    "balances": {
      "current": "2007615257193190727121",
      "previous": "1960016968608352367016"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:33.642Z",
  "updated": "2022-05-04T09:03:33.728Z",
  "id": "627241657832e20011830e3f"
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
0x0f200f9b00000000000000000000000000000000000000000000006cd5422f9d9e9f1dd10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2007615257193190727121`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`