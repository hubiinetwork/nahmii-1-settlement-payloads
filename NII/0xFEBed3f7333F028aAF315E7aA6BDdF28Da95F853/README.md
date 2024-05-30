# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFEBed3f7333F028aAF315E7aA6BDdF28Da95F853`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000d18de249ec37000000000000000000000000000000000000000000000000000004f7e21c036b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000004f7e21c036b00000000000000000000000000000000000000000000000000008b6a47c55784531eeecdad61a9a2e7e05ba23a5e105618c8a8f419cf515bb0a43bea625433cdd4d9a37a7c815b09746f533b4779274e777ac9b64fbfe72b94e3d5f06b0c067e42f81ee4263672e4d9b0bbe5188c38ccf26c66dc51a91a4baba2cfe3c7a0d8ad000000000000000000000000000000000000000000000000000000000000001bb4f06020c5d30351c07489faa9b6d1f2f8eb742b46a6987d753b2d95a26656dc27d96f0ed3ab7bd1bdb3634901525da673411628ecd41a364a8df86380a1e22b74c223d9994bdccace42faee9c4605ff0708248a13152db7177fd8076a1eb9fb000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074bc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac8f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a34c4708900bbf70327000000000000000000000000000000000000000000009a34c4708df9e3ad2a6900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001459a23d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4f2093768ed285b310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a595467794f5745324d6931685a54526d4c5456694d4759744f5751354f43316d4e4441784e5446684e7a6b324e44596966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000febed3f7333f028aaf315e7aa6bddf28da95f8530000000000000000000000000000000000000000000000000000d18de249ec370000000000000000000000000000000000000000000000000000cc96002de8cc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x531eeecdad61a9a2e7e05ba23a5e105618c8a8f419cf515bb0a43bea625433cd",
      "signature": {
        "s": "0x42f81ee4263672e4d9b0bbe5188c38ccf26c66dc51a91a4baba2cfe3c7a0d8ad",
        "r": "0xd4d9a37a7c815b09746f533b4779274e777ac9b64fbfe72b94e3d5f06b0c067e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb4f06020c5d30351c07489faa9b6d1f2f8eb742b46a6987d753b2d95a26656dc",
      "signature": {
        "s": "0x74c223d9994bdccace42faee9c4605ff0708248a13152db7177fd8076a1eb9fb",
        "r": "0x27d96f0ed3ab7bd1bdb3634901525da673411628ecd41a364a8df86380a1e22b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5462696919915",
    "total": "153288586909572"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5462696919915",
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
            "amount": "27244834784751062113073"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5462696919"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYTgyOWE2Mi1hZTRmLTViMGYtOWQ5OC1mNDAxNTFhNzk2NDYifQ==",
    "nonce": 109711,
    "balances": {
      "current": "728217824018023331595047",
      "previous": "728217824023491491211881"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfebed3f7333f028aaf315e7aa6bddf28da95f853",
    "nonce": 45,
    "balances": {
      "current": "230407317089335",
      "previous": "224944620169420"
    }
  },
  "blockNumber": "14709948",
  "created": "2022-05-04T08:49:31.894Z",
  "updated": "2022-05-04T08:49:31.980Z",
  "id": "62723e1b7832e20011830acb"
}
```
* *stageAmount*: `230407317089335`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000004f7e21c036b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000004f7e21c036b00000000000000000000000000000000000000000000000000008b6a47c55784531eeecdad61a9a2e7e05ba23a5e105618c8a8f419cf515bb0a43bea625433cdd4d9a37a7c815b09746f533b4779274e777ac9b64fbfe72b94e3d5f06b0c067e42f81ee4263672e4d9b0bbe5188c38ccf26c66dc51a91a4baba2cfe3c7a0d8ad000000000000000000000000000000000000000000000000000000000000001bb4f06020c5d30351c07489faa9b6d1f2f8eb742b46a6987d753b2d95a26656dc27d96f0ed3ab7bd1bdb3634901525da673411628ecd41a364a8df86380a1e22b74c223d9994bdccace42faee9c4605ff0708248a13152db7177fd8076a1eb9fb000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074bc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac8f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a34c4708900bbf70327000000000000000000000000000000000000000000009a34c4708df9e3ad2a6900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001459a23d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4f2093768ed285b310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a595467794f5745324d6931685a54526d4c5456694d4759744f5751354f43316d4e4441784e5446684e7a6b324e44596966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000febed3f7333f028aaf315e7aa6bddf28da95f8530000000000000000000000000000000000000000000000000000d18de249ec370000000000000000000000000000000000000000000000000000cc96002de8cc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x531eeecdad61a9a2e7e05ba23a5e105618c8a8f419cf515bb0a43bea625433cd",
      "signature": {
        "s": "0x42f81ee4263672e4d9b0bbe5188c38ccf26c66dc51a91a4baba2cfe3c7a0d8ad",
        "r": "0xd4d9a37a7c815b09746f533b4779274e777ac9b64fbfe72b94e3d5f06b0c067e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb4f06020c5d30351c07489faa9b6d1f2f8eb742b46a6987d753b2d95a26656dc",
      "signature": {
        "s": "0x74c223d9994bdccace42faee9c4605ff0708248a13152db7177fd8076a1eb9fb",
        "r": "0x27d96f0ed3ab7bd1bdb3634901525da673411628ecd41a364a8df86380a1e22b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5462696919915",
    "total": "153288586909572"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5462696919915",
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
            "amount": "27244834784751062113073"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5462696919"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYTgyOWE2Mi1hZTRmLTViMGYtOWQ5OC1mNDAxNTFhNzk2NDYifQ==",
    "nonce": 109711,
    "balances": {
      "current": "728217824018023331595047",
      "previous": "728217824023491491211881"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfebed3f7333f028aaf315e7aa6bddf28da95f853",
    "nonce": 45,
    "balances": {
      "current": "230407317089335",
      "previous": "224944620169420"
    }
  },
  "blockNumber": "14709948",
  "created": "2022-05-04T08:49:31.894Z",
  "updated": "2022-05-04T08:49:31.980Z",
  "id": "62723e1b7832e20011830acb"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000d18de249ec370000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `230407317089335`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`