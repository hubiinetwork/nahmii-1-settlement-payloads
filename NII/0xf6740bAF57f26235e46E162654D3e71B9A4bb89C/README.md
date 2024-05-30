# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf6740bAF57f26235e46E162654D3e71B9A4bb89C`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000306302bc1d9200000000000000000000000000000000000000000000000000000125ae987fc80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000125ae987fc80000000000000000000000000000000000000000000000000000203100bc1a48f8f71b86536411656be891631752355497f3ff2866d1d0b1867944c28c4cda729e98076dd688fa5cd1d3db883d15faddb29eb6e94b2c969b9421dc7b6e5df4b127f08a55174efbfa676da3b6882293a4d006ec55166b39d23c76bcf9a5f58ac9000000000000000000000000000000000000000000000000000000000000001b39de64fcd4acd7765b74073cdee515e278f569af323ba1b4e3b542baca9563575474348e283ebd1d061613c123588d49b60a0baf5c61c656b439ab9724edd67427b2676c44f2d8247e51c9a091e3e7baf3fa5d61a3573c98e5d04fe723d3a56b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac54000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a8df4018ea153d01641000000000000000000000000000000000000000000009a8df4018fc74d9754a000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000004b2ebe970000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4db3a2ca9b999f22c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e5463314e5749304d5330334e4751304c5455784e47497459574d785a4330324d6d45354e444578596a49314d6a676966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000f6740baf57f26235e46e162654d3e71b9a4bb89c0000000000000000000000000000000000000000000000000000306302bc1d9200000000000000000000000000000000000000000000000000002f3d54239dca00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8f71b86536411656be891631752355497f3ff2866d1d0b1867944c28c4cda72",
      "signature": {
        "s": "0x27f08a55174efbfa676da3b6882293a4d006ec55166b39d23c76bcf9a5f58ac9",
        "r": "0x9e98076dd688fa5cd1d3db883d15faddb29eb6e94b2c969b9421dc7b6e5df4b1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x39de64fcd4acd7765b74073cdee515e278f569af323ba1b4e3b542baca956357",
      "signature": {
        "s": "0x27b2676c44f2d8247e51c9a091e3e7baf3fa5d61a3573c98e5d04fe723d3a56b",
        "r": "0x5474348e283ebd1d061613c123588d49b60a0baf5c61c656b439ab9724edd674",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1261354647496",
    "total": "35394837813832"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1261354647496",
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
            "amount": "27243191240545728590380"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1261354647"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNTc1NWI0MS03NGQ0LTUxNGItYWMxZC02MmE5NDExYjI1MjgifQ==",
    "nonce": 109652,
    "balances": {
      "current": "729863011767562187839041",
      "previous": "729863011768824803841184"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf6740baf57f26235e46e162654d3e71b9a4bb89c",
    "nonce": 45,
    "balances": {
      "current": "53201805778322",
      "previous": "51940451130826"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:49:12.638Z",
  "updated": "2022-05-04T08:49:12.701Z",
  "id": "62723e08bbd75600116d0458"
}
```
* *stageAmount*: `53201805778322`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000125ae987fc80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000125ae987fc80000000000000000000000000000000000000000000000000000203100bc1a48f8f71b86536411656be891631752355497f3ff2866d1d0b1867944c28c4cda729e98076dd688fa5cd1d3db883d15faddb29eb6e94b2c969b9421dc7b6e5df4b127f08a55174efbfa676da3b6882293a4d006ec55166b39d23c76bcf9a5f58ac9000000000000000000000000000000000000000000000000000000000000001b39de64fcd4acd7765b74073cdee515e278f569af323ba1b4e3b542baca9563575474348e283ebd1d061613c123588d49b60a0baf5c61c656b439ab9724edd67427b2676c44f2d8247e51c9a091e3e7baf3fa5d61a3573c98e5d04fe723d3a56b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac54000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a8df4018ea153d01641000000000000000000000000000000000000000000009a8df4018fc74d9754a000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000004b2ebe970000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4db3a2ca9b999f22c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e5463314e5749304d5330334e4751304c5455784e47497459574d785a4330324d6d45354e444578596a49314d6a676966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000f6740baf57f26235e46e162654d3e71b9a4bb89c0000000000000000000000000000000000000000000000000000306302bc1d9200000000000000000000000000000000000000000000000000002f3d54239dca00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8f71b86536411656be891631752355497f3ff2866d1d0b1867944c28c4cda72",
      "signature": {
        "s": "0x27f08a55174efbfa676da3b6882293a4d006ec55166b39d23c76bcf9a5f58ac9",
        "r": "0x9e98076dd688fa5cd1d3db883d15faddb29eb6e94b2c969b9421dc7b6e5df4b1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x39de64fcd4acd7765b74073cdee515e278f569af323ba1b4e3b542baca956357",
      "signature": {
        "s": "0x27b2676c44f2d8247e51c9a091e3e7baf3fa5d61a3573c98e5d04fe723d3a56b",
        "r": "0x5474348e283ebd1d061613c123588d49b60a0baf5c61c656b439ab9724edd674",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1261354647496",
    "total": "35394837813832"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1261354647496",
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
            "amount": "27243191240545728590380"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1261354647"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNTc1NWI0MS03NGQ0LTUxNGItYWMxZC02MmE5NDExYjI1MjgifQ==",
    "nonce": 109652,
    "balances": {
      "current": "729863011767562187839041",
      "previous": "729863011768824803841184"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf6740baf57f26235e46e162654d3e71b9a4bb89c",
    "nonce": 45,
    "balances": {
      "current": "53201805778322",
      "previous": "51940451130826"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:49:12.638Z",
  "updated": "2022-05-04T08:49:12.701Z",
  "id": "62723e08bbd75600116d0458"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000306302bc1d920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `53201805778322`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`