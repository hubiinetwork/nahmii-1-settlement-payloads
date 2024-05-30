# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x07F069c74d2F2B803f7baebA083Ef80A87C993E7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001248b1075e362fdd800000000000000000000000000000000000000000000000006ef951bc3ab0a110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000006ef951bc3ab0a11000000000000000000000000000000000000000000000000c2a091f00dde3b88212d1ae54101d8614ddcf9f5321d4075fc827f9dbe0a5360c98e79412c384df920a04a42426647adba6d13c19e2141fa817bce0fa40fd98b9cc86d36f3acfcd523005d54168f6a71caa141bb77fc0a1f015c82fdc034aaf333819f8056d50408000000000000000000000000000000000000000000000000000000000000001ccb73f5b3c628b9ade3e2d3eb4a06581258edfad59891248dc54d80c4d10f2ce5dbb11f2fe25477950ab4776e4453d98bb3ef893f00d0a02069fbc155daae531520c080d0d03948e9dc781000295b8a33e6e01681be799dfe7345392fccbe27d3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af09000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095acd6c93ef59bb683560000000000000000000000000000000000000000000095acddba9a9df1c0b30b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000001c68c925f25a40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61aae56af44660ccf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a47466c596d51354e7930305a6d4d794c5456684e7a63744f474a6b5a5330334d57526b5a6a646959574979597a556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000007f069c74d2f2b803f7baeba083ef80a87c993e7000000000000000000000000000000000000000000000001248b1075e362fdd80000000000000000000000000000000000000000000000011d9b7b5a1fb7f3c700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x212d1ae54101d8614ddcf9f5321d4075fc827f9dbe0a5360c98e79412c384df9",
      "signature": {
        "s": "0x23005d54168f6a71caa141bb77fc0a1f015c82fdc034aaf333819f8056d50408",
        "r": "0x20a04a42426647adba6d13c19e2141fa817bce0fa40fd98b9cc86d36f3acfcd5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcb73f5b3c628b9ade3e2d3eb4a06581258edfad59891248dc54d80c4d10f2ce5",
      "signature": {
        "s": "0x20c080d0d03948e9dc781000295b8a33e6e01681be799dfe7345392fccbe27d3",
        "r": "0xdbb11f2fe25477950ab4776e4453d98bb3ef893f00d0a02069fbc155daae5315",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "499782030140836369",
    "total": "14024369699842571144"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "499782030140836369",
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
            "amount": "27266210310344417873103"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "499782030140836"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZGFlYmQ5Ny00ZmMyLTVhNzctOGJkZS03MWRkZjdiYWIyYzUifQ==",
    "nonce": 110345,
    "balances": {
      "current": "706820922899074215478102",
      "previous": "706821423180886386455307"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x07f069c74d2f2b803f7baeba083ef80a87c993e7",
    "nonce": 46,
    "balances": {
      "current": "21079960579349872088",
      "previous": "20580178549209035719"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:47.780Z",
  "updated": "2022-05-04T08:52:47.869Z",
  "id": "62723edfbbd75600116d0547"
}
```
* *stageAmount*: `21079960579349872088`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000006ef951bc3ab0a110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000006ef951bc3ab0a11000000000000000000000000000000000000000000000000c2a091f00dde3b88212d1ae54101d8614ddcf9f5321d4075fc827f9dbe0a5360c98e79412c384df920a04a42426647adba6d13c19e2141fa817bce0fa40fd98b9cc86d36f3acfcd523005d54168f6a71caa141bb77fc0a1f015c82fdc034aaf333819f8056d50408000000000000000000000000000000000000000000000000000000000000001ccb73f5b3c628b9ade3e2d3eb4a06581258edfad59891248dc54d80c4d10f2ce5dbb11f2fe25477950ab4776e4453d98bb3ef893f00d0a02069fbc155daae531520c080d0d03948e9dc781000295b8a33e6e01681be799dfe7345392fccbe27d3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af09000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095acd6c93ef59bb683560000000000000000000000000000000000000000000095acddba9a9df1c0b30b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000001c68c925f25a40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61aae56af44660ccf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a47466c596d51354e7930305a6d4d794c5456684e7a63744f474a6b5a5330334d57526b5a6a646959574979597a556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000007f069c74d2f2b803f7baeba083ef80a87c993e7000000000000000000000000000000000000000000000001248b1075e362fdd80000000000000000000000000000000000000000000000011d9b7b5a1fb7f3c700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x212d1ae54101d8614ddcf9f5321d4075fc827f9dbe0a5360c98e79412c384df9",
      "signature": {
        "s": "0x23005d54168f6a71caa141bb77fc0a1f015c82fdc034aaf333819f8056d50408",
        "r": "0x20a04a42426647adba6d13c19e2141fa817bce0fa40fd98b9cc86d36f3acfcd5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcb73f5b3c628b9ade3e2d3eb4a06581258edfad59891248dc54d80c4d10f2ce5",
      "signature": {
        "s": "0x20c080d0d03948e9dc781000295b8a33e6e01681be799dfe7345392fccbe27d3",
        "r": "0xdbb11f2fe25477950ab4776e4453d98bb3ef893f00d0a02069fbc155daae5315",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "499782030140836369",
    "total": "14024369699842571144"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "499782030140836369",
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
            "amount": "27266210310344417873103"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "499782030140836"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZGFlYmQ5Ny00ZmMyLTVhNzctOGJkZS03MWRkZjdiYWIyYzUifQ==",
    "nonce": 110345,
    "balances": {
      "current": "706820922899074215478102",
      "previous": "706821423180886386455307"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x07f069c74d2f2b803f7baeba083ef80a87c993e7",
    "nonce": 46,
    "balances": {
      "current": "21079960579349872088",
      "previous": "20580178549209035719"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:47.780Z",
  "updated": "2022-05-04T08:52:47.869Z",
  "id": "62723edfbbd75600116d0547"
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
0x0f200f9b000000000000000000000000000000000000000000000001248b1075e362fdd80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `21079960579349872088`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`