# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x47709F8497DFb6a77255488769Bdb709A8E1DC1c`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000016d030cd93ffbce0000000000000000000000000000000000000000000000000008a76dd72705710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000008a76dd727057100000000000000000000000000000000000000000000000000f2d717f53f75f729da59d67865ae08b19bdd1c4a1994bb5806faae04d1e5f5657d38a1a6284c2cd90193205d28c312a535c3378c7aa42b398716eda661e864b3658629701e89647084a0c00a127b38ef9b7e03c2fa01acf584c52752e35369f623bc3bcc119f43000000000000000000000000000000000000000000000000000000000000001c006ba26f1288d13daca117c7c63b724a4532f6831bd3281d976f3df77d8a8df4d53ecedb740899aff941ce61c675c0d8faa626b49e0827e7c44c1b1e676d773c3bc9f3fbeb6db1ab5c423b96667eb877b6c052bf191f60330504a178130eb76a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af21000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095ac787bae7620fedbd70000000000000000000000000000000000000000000095ac7884581b1e81d2b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000237265bf1690000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61ac674c0460e41db0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e44646b597a63335953316b5a6d4d304c5455794e6a63744f54686b4e5330785a54526b4e5446694f446b334d6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000047709f8497dfb6a77255488769bdb709a8e1dc1c000000000000000000000000000000000000000000000000016d030cd93ffbce00000000000000000000000000000000000000000000000001645b9f0218f65d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x29da59d67865ae08b19bdd1c4a1994bb5806faae04d1e5f5657d38a1a6284c2c",
      "signature": {
        "s": "0x7084a0c00a127b38ef9b7e03c2fa01acf584c52752e35369f623bc3bcc119f43",
        "r": "0xd90193205d28c312a535c3378c7aa42b398716eda661e864b3658629701e8964",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x006ba26f1288d13daca117c7c63b724a4532f6831bd3281d976f3df77d8a8df4",
      "signature": {
        "s": "0x3bc9f3fbeb6db1ab5c423b96667eb877b6c052bf191f60330504a178130eb76a",
        "r": "0xd53ecedb740899aff941ce61c675c0d8faa626b49e0827e7c44c1b1e676d773c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2435890016617841",
    "total": "68353442262775287"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2435890016617841",
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
            "amount": "27266217098802250007003"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2435890016617"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NDdkYzc3YS1kZmM0LTUyNjctOThkNS0xZTRkNTFiODk3MjMifQ==",
    "nonce": 110369,
    "balances": {
      "current": "706814127652784249428951",
      "previous": "706814130091110156063409"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x47709f8497dfb6a77255488769bdb709a8e1dc1c",
    "nonce": 46,
    "balances": {
      "current": "102741720218729422",
      "previous": "100305830202111581"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:55.813Z",
  "updated": "2022-05-04T08:52:55.892Z",
  "id": "62723ee73592fd001130b4c4"
}
```
* *stageAmount*: `102741720218729422`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000008a76dd72705710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000008a76dd727057100000000000000000000000000000000000000000000000000f2d717f53f75f729da59d67865ae08b19bdd1c4a1994bb5806faae04d1e5f5657d38a1a6284c2cd90193205d28c312a535c3378c7aa42b398716eda661e864b3658629701e89647084a0c00a127b38ef9b7e03c2fa01acf584c52752e35369f623bc3bcc119f43000000000000000000000000000000000000000000000000000000000000001c006ba26f1288d13daca117c7c63b724a4532f6831bd3281d976f3df77d8a8df4d53ecedb740899aff941ce61c675c0d8faa626b49e0827e7c44c1b1e676d773c3bc9f3fbeb6db1ab5c423b96667eb877b6c052bf191f60330504a178130eb76a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af21000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095ac787bae7620fedbd70000000000000000000000000000000000000000000095ac7884581b1e81d2b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000237265bf1690000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61ac674c0460e41db0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e44646b597a63335953316b5a6d4d304c5455794e6a63744f54686b4e5330785a54526b4e5446694f446b334d6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000047709f8497dfb6a77255488769bdb709a8e1dc1c000000000000000000000000000000000000000000000000016d030cd93ffbce00000000000000000000000000000000000000000000000001645b9f0218f65d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x29da59d67865ae08b19bdd1c4a1994bb5806faae04d1e5f5657d38a1a6284c2c",
      "signature": {
        "s": "0x7084a0c00a127b38ef9b7e03c2fa01acf584c52752e35369f623bc3bcc119f43",
        "r": "0xd90193205d28c312a535c3378c7aa42b398716eda661e864b3658629701e8964",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x006ba26f1288d13daca117c7c63b724a4532f6831bd3281d976f3df77d8a8df4",
      "signature": {
        "s": "0x3bc9f3fbeb6db1ab5c423b96667eb877b6c052bf191f60330504a178130eb76a",
        "r": "0xd53ecedb740899aff941ce61c675c0d8faa626b49e0827e7c44c1b1e676d773c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2435890016617841",
    "total": "68353442262775287"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2435890016617841",
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
            "amount": "27266217098802250007003"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2435890016617"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NDdkYzc3YS1kZmM0LTUyNjctOThkNS0xZTRkNTFiODk3MjMifQ==",
    "nonce": 110369,
    "balances": {
      "current": "706814127652784249428951",
      "previous": "706814130091110156063409"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x47709f8497dfb6a77255488769bdb709a8e1dc1c",
    "nonce": 46,
    "balances": {
      "current": "102741720218729422",
      "previous": "100305830202111581"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:55.813Z",
  "updated": "2022-05-04T08:52:55.892Z",
  "id": "62723ee73592fd001130b4c4"
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
0x0f200f9b000000000000000000000000000000000000000000000000016d030cd93ffbce0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `102741720218729422`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`