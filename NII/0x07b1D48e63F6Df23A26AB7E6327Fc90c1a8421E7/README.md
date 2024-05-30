# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x07b1D48e63F6Df23A26AB7E6327Fc90c1a8421E7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000f936bc251654e90000000000000000000000000000000000000000000000000005e8988ba38a4f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000005e8988ba38a4f00000000000000000000000000000000000000000000000000a5cce93db6b08f8a887d6ddb18f7449d7c30e511e90c9c5f5cc32e0b30da4d73f95d64a1c17ea5db1f46d25a811347a37283b5b9befd7b0f05e1092e2ae936f60e048d68eedd766d70a07e62139c85d0a176ad636546efe4c21a3b0f85c48df34048b9310ce830000000000000000000000000000000000000000000000000000000000000001c6a45e5e3ac7c4d47a0d799b8785c7bdcc8d7bf2b8c11ed071aa70b7972ab5b31e8d59fa6191fd8a04f35a50171f60248a9cfb36e8635b4c2dc6c8ea884398fc13bd42a194bbc1a43a5b3439eff55a7692ea9f2aebd5c0960df9f99636506956a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1a4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004ac72b059835b5385da2000000000000000000000000000000000000000000004ac72b0b82517a57b7b200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000183397bcfc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9423cba55f2ca6c230000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a64684e47526b4f533077593251784c5455354e6a4d74595456684e7931694e7a42684d7a59784e5751335954516966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000007b1d48e63f6df23a26ab7e6327fc90c1a8421e700000000000000000000000000000000000000000000000000f936bc251654e900000000000000000000000000000000000000000000000000f34e239972ca9a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8a887d6ddb18f7449d7c30e511e90c9c5f5cc32e0b30da4d73f95d64a1c17ea5",
      "signature": {
        "s": "0x6d70a07e62139c85d0a176ad636546efe4c21a3b0f85c48df34048b9310ce830",
        "r": "0xdb1f46d25a811347a37283b5b9befd7b0f05e1092e2ae936f60e048d68eedd76",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a45e5e3ac7c4d47a0d799b8785c7bdcc8d7bf2b8c11ed071aa70b7972ab5b31",
      "signature": {
        "s": "0x3bd42a194bbc1a43a5b3439eff55a7692ea9f2aebd5c0960df9f99636506956a",
        "r": "0xe8d59fa6191fd8a04f35a50171f60248a9cfb36e8635b4c2dc6c8ea884398fc1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1663116758977103",
    "total": "46668673292087439"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1663116758977103",
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
            "amount": "27619548772926612991011"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1663116758977"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjZjdhNGRkOS0wY2QxLTU5NjMtYTVhNy1iNzBhMzYxNWQ3YTQifQ==",
    "nonce": 111012,
    "balances": {
      "current": "353129121854296902098338",
      "previous": "353129123519076777834418"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x07b1d48e63f6df23a26ab7e6327fc90c1a8421e7",
    "nonce": 46,
    "balances": {
      "current": "70147450904925417",
      "previous": "68484334145948314"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:08.860Z",
  "updated": "2022-05-04T08:56:08.926Z",
  "id": "62723fa87832e20011830c72"
}
```
* *stageAmount*: `70147450904925417`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000005e8988ba38a4f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000005e8988ba38a4f00000000000000000000000000000000000000000000000000a5cce93db6b08f8a887d6ddb18f7449d7c30e511e90c9c5f5cc32e0b30da4d73f95d64a1c17ea5db1f46d25a811347a37283b5b9befd7b0f05e1092e2ae936f60e048d68eedd766d70a07e62139c85d0a176ad636546efe4c21a3b0f85c48df34048b9310ce830000000000000000000000000000000000000000000000000000000000000001c6a45e5e3ac7c4d47a0d799b8785c7bdcc8d7bf2b8c11ed071aa70b7972ab5b31e8d59fa6191fd8a04f35a50171f60248a9cfb36e8635b4c2dc6c8ea884398fc13bd42a194bbc1a43a5b3439eff55a7692ea9f2aebd5c0960df9f99636506956a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1a4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004ac72b059835b5385da2000000000000000000000000000000000000000000004ac72b0b82517a57b7b200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000183397bcfc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9423cba55f2ca6c230000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a64684e47526b4f533077593251784c5455354e6a4d74595456684e7931694e7a42684d7a59784e5751335954516966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000007b1d48e63f6df23a26ab7e6327fc90c1a8421e700000000000000000000000000000000000000000000000000f936bc251654e900000000000000000000000000000000000000000000000000f34e239972ca9a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8a887d6ddb18f7449d7c30e511e90c9c5f5cc32e0b30da4d73f95d64a1c17ea5",
      "signature": {
        "s": "0x6d70a07e62139c85d0a176ad636546efe4c21a3b0f85c48df34048b9310ce830",
        "r": "0xdb1f46d25a811347a37283b5b9befd7b0f05e1092e2ae936f60e048d68eedd76",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a45e5e3ac7c4d47a0d799b8785c7bdcc8d7bf2b8c11ed071aa70b7972ab5b31",
      "signature": {
        "s": "0x3bd42a194bbc1a43a5b3439eff55a7692ea9f2aebd5c0960df9f99636506956a",
        "r": "0xe8d59fa6191fd8a04f35a50171f60248a9cfb36e8635b4c2dc6c8ea884398fc1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1663116758977103",
    "total": "46668673292087439"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1663116758977103",
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
            "amount": "27619548772926612991011"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1663116758977"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjZjdhNGRkOS0wY2QxLTU5NjMtYTVhNy1iNzBhMzYxNWQ3YTQifQ==",
    "nonce": 111012,
    "balances": {
      "current": "353129121854296902098338",
      "previous": "353129123519076777834418"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x07b1d48e63f6df23a26ab7e6327fc90c1a8421e7",
    "nonce": 46,
    "balances": {
      "current": "70147450904925417",
      "previous": "68484334145948314"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:08.860Z",
  "updated": "2022-05-04T08:56:08.926Z",
  "id": "62723fa87832e20011830c72"
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
0x0f200f9b00000000000000000000000000000000000000000000000000f936bc251654e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `70147450904925417`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`