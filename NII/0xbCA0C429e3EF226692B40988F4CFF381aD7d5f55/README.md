# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbCA0C429e3EF226692B40988F4CFF381aD7d5f55`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000008515b8fafd4caed60000000000000000000000000000000000000000000000000d5005e47bcfc8150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000d5005e47bcfc8150000000000000000000000000000000000000000000000008515b8fafd4caed6c731756ee593cf72502411667c9b7375ec54b87bc1c74e417835de5dfb3047098d46ab9b164359d60019f9862365152b36fa8a58fa0321df82e5c9d9d214e7ef568baea37c9633dee88de07efbaa972862f96bae253631c34909c5aebe90fba9000000000000000000000000000000000000000000000000000000000000001b6689027f4c9aea884818b33d1bc842fa0bc8dbf08711042d789e1c96ed57485c52559b790e61844c77c09fe333251b2e45980200190679596b894afe76a97fbe1ae1b575ff7a71f0c57d4cf4ca759e7b8ce172127d7dc3b9d5a1aa057ed9a5f4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5ce000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000032e8dd98eafab8b5be120000000000000000000000000000000000000000000032e8eaec595366d2469b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000036874324cc0740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df5ce976bc8f8ef4d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497959545a6c4d4441785a69316b4d7a67774c54566c4d446374596d466c4f4330784e6a5578595445314d6d55334e44596966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000bca0c429e3ef226692b40988f4cff381ad7d5f550000000000000000000000000000000000000000000000008515b8fafd4caed600000000000000000000000000000000000000000000000077c5b316817ce6c100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc731756ee593cf72502411667c9b7375ec54b87bc1c74e417835de5dfb304709",
      "signature": {
        "s": "0x568baea37c9633dee88de07efbaa972862f96bae253631c34909c5aebe90fba9",
        "r": "0x8d46ab9b164359d60019f9862365152b36fa8a58fa0321df82e5c9d9d214e7ef",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6689027f4c9aea884818b33d1bc842fa0bc8dbf08711042d789e1c96ed57485c",
      "signature": {
        "s": "0x1ae1b575ff7a71f0c57d4cf4ca759e7b8ce172127d7dc3b9d5a1aa057ed9a5f4",
        "r": "0x52559b790e61844c77c09fe333251b2e45980200190679596b894afe76a97fbe",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "959273199517812757",
    "total": "9589774369686335190"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "959273199517812757",
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
            "amount": "27732151355658753471702"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "959273199517812"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyYTZlMDAxZi1kMzgwLTVlMDctYmFlOC0xNjUxYTE1MmU3NDYifQ==",
    "nonce": 112078,
    "balances": {
      "current": "240413936539424280395282",
      "previous": "240414896771896997725851"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbca0c429e3ef226692b40988f4cff381ad7d5f55",
    "nonce": 11,
    "balances": {
      "current": "9589774369686335190",
      "previous": "8630501170168522433"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:01:53.995Z",
  "updated": "2022-05-04T09:01:54.057Z",
  "id": "62724101bbd75600116d0777"
}
```
* *stageAmount*: `9589774369686335190`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000d5005e47bcfc8150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000d5005e47bcfc8150000000000000000000000000000000000000000000000008515b8fafd4caed6c731756ee593cf72502411667c9b7375ec54b87bc1c74e417835de5dfb3047098d46ab9b164359d60019f9862365152b36fa8a58fa0321df82e5c9d9d214e7ef568baea37c9633dee88de07efbaa972862f96bae253631c34909c5aebe90fba9000000000000000000000000000000000000000000000000000000000000001b6689027f4c9aea884818b33d1bc842fa0bc8dbf08711042d789e1c96ed57485c52559b790e61844c77c09fe333251b2e45980200190679596b894afe76a97fbe1ae1b575ff7a71f0c57d4cf4ca759e7b8ce172127d7dc3b9d5a1aa057ed9a5f4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5ce000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000032e8dd98eafab8b5be120000000000000000000000000000000000000000000032e8eaec595366d2469b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000036874324cc0740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df5ce976bc8f8ef4d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497959545a6c4d4441785a69316b4d7a67774c54566c4d446374596d466c4f4330784e6a5578595445314d6d55334e44596966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000bca0c429e3ef226692b40988f4cff381ad7d5f550000000000000000000000000000000000000000000000008515b8fafd4caed600000000000000000000000000000000000000000000000077c5b316817ce6c100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc731756ee593cf72502411667c9b7375ec54b87bc1c74e417835de5dfb304709",
      "signature": {
        "s": "0x568baea37c9633dee88de07efbaa972862f96bae253631c34909c5aebe90fba9",
        "r": "0x8d46ab9b164359d60019f9862365152b36fa8a58fa0321df82e5c9d9d214e7ef",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6689027f4c9aea884818b33d1bc842fa0bc8dbf08711042d789e1c96ed57485c",
      "signature": {
        "s": "0x1ae1b575ff7a71f0c57d4cf4ca759e7b8ce172127d7dc3b9d5a1aa057ed9a5f4",
        "r": "0x52559b790e61844c77c09fe333251b2e45980200190679596b894afe76a97fbe",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "959273199517812757",
    "total": "9589774369686335190"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "959273199517812757",
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
            "amount": "27732151355658753471702"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "959273199517812"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyYTZlMDAxZi1kMzgwLTVlMDctYmFlOC0xNjUxYTE1MmU3NDYifQ==",
    "nonce": 112078,
    "balances": {
      "current": "240413936539424280395282",
      "previous": "240414896771896997725851"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbca0c429e3ef226692b40988f4cff381ad7d5f55",
    "nonce": 11,
    "balances": {
      "current": "9589774369686335190",
      "previous": "8630501170168522433"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:01:53.995Z",
  "updated": "2022-05-04T09:01:54.057Z",
  "id": "62724101bbd75600116d0777"
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
0x0f200f9b0000000000000000000000000000000000000000000000008515b8fafd4caed60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9589774369686335190`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`