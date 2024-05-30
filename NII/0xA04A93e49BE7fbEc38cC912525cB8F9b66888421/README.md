# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA04A93e49BE7fbEc38cC912525cB8F9b66888421`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000005cdef0e51e7f3cda0000000000000000000000000000000000000000000000000233ad4de4b84f7a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000233ad4de4b84f7a0000000000000000000000000000000000000000000000003dc952e69ed024165ca7b1e8108e807d82036517a4ede4eac9ee560f05447b58c0ec4cc7b8d3acd9ac41cee3da0689e3af9d140a23ddd221a86bd2e691f21210f5acf9504f6949675cb640167845bcbf65129ed48034ea3a1f76822c74909734fb2655b1aa25c85a000000000000000000000000000000000000000000000000000000000000001c9fe3625b860b25d0370ceecbfbdb2d7a89993e20751539282005da386b8efd817f6114122991ac48376f0abb032e6eebbaa300b94a36bc11f7f300e06d02eb4232d6b10d5e5b90f9f6e5f76d32f8c288b225fed15fc8e943ee508e54475e966e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afaa000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052dfad1d5c877980dfd40000000000000000000000000000000000000000000052dfaf519a228080066c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000904d2246d71e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d730348533575b9de60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493059574d335a4751355a53316d4d7a59784c54557a597a55744f5463784e79316d4d475932596a49325a4746685932516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a04a93e49be7fbec38cc912525cb8f9b668884210000000000000000000000000000000000000000000000005cdef0e51e7f3cda0000000000000000000000000000000000000000000000005aab439739c6ed6000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5ca7b1e8108e807d82036517a4ede4eac9ee560f05447b58c0ec4cc7b8d3acd9",
      "signature": {
        "s": "0x5cb640167845bcbf65129ed48034ea3a1f76822c74909734fb2655b1aa25c85a",
        "r": "0xac41cee3da0689e3af9d140a23ddd221a86bd2e691f21210f5acf9504f694967",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9fe3625b860b25d0370ceecbfbdb2d7a89993e20751539282005da386b8efd81",
      "signature": {
        "s": "0x32d6b10d5e5b90f9f6e5f76d32f8c288b225fed15fc8e943ee508e54475e966e",
        "r": "0x7f6114122991ac48376f0abb032e6eebbaa300b94a36bc11f7f300e06d02eb42",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "158660961949470586",
    "total": "4452180857092842518"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949470586",
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
            "amount": "27581355937863944609254"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949470"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0YWM3ZGQ5ZS1mMzYxLTUzYzUtOTcxNy1mMGY2YjI2ZGFhY2QifQ==",
    "nonce": 110506,
    "balances": {
      "current": "391360149752027952504788",
      "previous": "391360308571650863924844"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa04a93e49be7fbec38cc912525cb8f9b66888421",
    "nonce": 46,
    "balances": {
      "current": "6692050963168967898",
      "previous": "6533390001219497312"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:37.905Z",
  "updated": "2022-05-04T08:53:37.991Z",
  "id": "62723f113592fd001130b4ee"
}
```
* *stageAmount*: `6692050963168967898`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000233ad4de4b84f7a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000233ad4de4b84f7a0000000000000000000000000000000000000000000000003dc952e69ed024165ca7b1e8108e807d82036517a4ede4eac9ee560f05447b58c0ec4cc7b8d3acd9ac41cee3da0689e3af9d140a23ddd221a86bd2e691f21210f5acf9504f6949675cb640167845bcbf65129ed48034ea3a1f76822c74909734fb2655b1aa25c85a000000000000000000000000000000000000000000000000000000000000001c9fe3625b860b25d0370ceecbfbdb2d7a89993e20751539282005da386b8efd817f6114122991ac48376f0abb032e6eebbaa300b94a36bc11f7f300e06d02eb4232d6b10d5e5b90f9f6e5f76d32f8c288b225fed15fc8e943ee508e54475e966e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afaa000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052dfad1d5c877980dfd40000000000000000000000000000000000000000000052dfaf519a228080066c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000904d2246d71e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d730348533575b9de60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493059574d335a4751355a53316d4d7a59784c54557a597a55744f5463784e79316d4d475932596a49325a4746685932516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a04a93e49be7fbec38cc912525cb8f9b668884210000000000000000000000000000000000000000000000005cdef0e51e7f3cda0000000000000000000000000000000000000000000000005aab439739c6ed6000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5ca7b1e8108e807d82036517a4ede4eac9ee560f05447b58c0ec4cc7b8d3acd9",
      "signature": {
        "s": "0x5cb640167845bcbf65129ed48034ea3a1f76822c74909734fb2655b1aa25c85a",
        "r": "0xac41cee3da0689e3af9d140a23ddd221a86bd2e691f21210f5acf9504f694967",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9fe3625b860b25d0370ceecbfbdb2d7a89993e20751539282005da386b8efd81",
      "signature": {
        "s": "0x32d6b10d5e5b90f9f6e5f76d32f8c288b225fed15fc8e943ee508e54475e966e",
        "r": "0x7f6114122991ac48376f0abb032e6eebbaa300b94a36bc11f7f300e06d02eb42",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "158660961949470586",
    "total": "4452180857092842518"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949470586",
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
            "amount": "27581355937863944609254"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949470"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0YWM3ZGQ5ZS1mMzYxLTUzYzUtOTcxNy1mMGY2YjI2ZGFhY2QifQ==",
    "nonce": 110506,
    "balances": {
      "current": "391360149752027952504788",
      "previous": "391360308571650863924844"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa04a93e49be7fbec38cc912525cb8f9b66888421",
    "nonce": 46,
    "balances": {
      "current": "6692050963168967898",
      "previous": "6533390001219497312"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:37.905Z",
  "updated": "2022-05-04T08:53:37.991Z",
  "id": "62723f113592fd001130b4ee"
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
0x0f200f9b0000000000000000000000000000000000000000000000005cdef0e51e7f3cda0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6692050963168967898`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`