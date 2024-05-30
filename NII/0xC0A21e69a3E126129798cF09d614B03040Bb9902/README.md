# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC0A21e69a3E126129798cF09d614B03040Bb9902`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000571101ca9360aebcc0000000000000000000000000000000000000000000000002107279066cb853e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000002107279066cb853e0000000000000000000000000000000000000000000000039ecbdb834e12bf9c64c4be51c92f9943be1af112396acce291a2383d445f06a73ac0c7b7d7b0cd48ed922abfa61b094e229bbc95b79d499853541f869161c7b697118589ca0d74016a4d179317f623ded09a8c3449d670a2265a420bf15d78594f17a39ba12a1475000000000000000000000000000000000000000000000000000000000000001c0877eef506260f457155602db27d2e398c51a4eb866d5d2c4ad6bfe85875bb4ea1d4f692f4e1b39fcf7eeba5b895b6410e54340f5099c94f4a5dad85503cfec72e6f32d6b218656d7d508ccf409dd6580a1e5e29c23804b69ca7022c22393233000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b245000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000493ab3119603cd3af92900000000000000000000000000000000000000000000493ad4213219362d18e700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000008748502269a800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9a7a1bc20cdaf0dce0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f546b7a4e6d49305a5331695a544a6b4c5455324d474574596d4e6a4e5330344f44673259544e6c5a4445784f54556966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c0a21e69a3e126129798cf09d614b03040bb990200000000000000000000000000000000000000000000000571101ca9360aebcc0000000000000000000000000000000000000000000000055008f518cf3f668e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x64c4be51c92f9943be1af112396acce291a2383d445f06a73ac0c7b7d7b0cd48",
      "signature": {
        "s": "0x6a4d179317f623ded09a8c3449d670a2265a420bf15d78594f17a39ba12a1475",
        "r": "0xed922abfa61b094e229bbc95b79d499853541f869161c7b697118589ca0d7401",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0877eef506260f457155602db27d2e398c51a4eb866d5d2c4ad6bfe85875bb4e",
      "signature": {
        "s": "0x2e6f32d6b218656d7d508ccf409dd6580a1e5e29c23804b69ca7022c22393233",
        "r": "0xa1d4f692f4e1b39fcf7eeba5b895b6410e54340f5099c94f4a5dad85503cfec7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2379914429241984318",
    "total": "66782712856390582172"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2379914429241984318",
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
            "amount": "27626855020867858927054"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2379914429241984"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzOTkzNmI0ZS1iZTJkLTU2MGEtYmNjNS04ODg2YTNlZDExOTUifQ==",
    "nonce": 111173,
    "balances": {
      "current": "345815567665109720037673",
      "previous": "345817949959453391263975"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc0a21e69a3e126129798cf09d614b03040bb9902",
    "nonce": 46,
    "balances": {
      "current": "100380763607542721484",
      "previous": "98000849178300737166"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:56:56.173Z",
  "updated": "2022-05-04T08:56:56.260Z",
  "id": "62723fd87832e20011830cac"
}
```
* *stageAmount*: `100380763607542721484`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000002107279066cb853e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000002107279066cb853e0000000000000000000000000000000000000000000000039ecbdb834e12bf9c64c4be51c92f9943be1af112396acce291a2383d445f06a73ac0c7b7d7b0cd48ed922abfa61b094e229bbc95b79d499853541f869161c7b697118589ca0d74016a4d179317f623ded09a8c3449d670a2265a420bf15d78594f17a39ba12a1475000000000000000000000000000000000000000000000000000000000000001c0877eef506260f457155602db27d2e398c51a4eb866d5d2c4ad6bfe85875bb4ea1d4f692f4e1b39fcf7eeba5b895b6410e54340f5099c94f4a5dad85503cfec72e6f32d6b218656d7d508ccf409dd6580a1e5e29c23804b69ca7022c22393233000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b245000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000493ab3119603cd3af92900000000000000000000000000000000000000000000493ad4213219362d18e700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000008748502269a800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9a7a1bc20cdaf0dce0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f546b7a4e6d49305a5331695a544a6b4c5455324d474574596d4e6a4e5330344f44673259544e6c5a4445784f54556966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c0a21e69a3e126129798cf09d614b03040bb990200000000000000000000000000000000000000000000000571101ca9360aebcc0000000000000000000000000000000000000000000000055008f518cf3f668e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x64c4be51c92f9943be1af112396acce291a2383d445f06a73ac0c7b7d7b0cd48",
      "signature": {
        "s": "0x6a4d179317f623ded09a8c3449d670a2265a420bf15d78594f17a39ba12a1475",
        "r": "0xed922abfa61b094e229bbc95b79d499853541f869161c7b697118589ca0d7401",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0877eef506260f457155602db27d2e398c51a4eb866d5d2c4ad6bfe85875bb4e",
      "signature": {
        "s": "0x2e6f32d6b218656d7d508ccf409dd6580a1e5e29c23804b69ca7022c22393233",
        "r": "0xa1d4f692f4e1b39fcf7eeba5b895b6410e54340f5099c94f4a5dad85503cfec7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2379914429241984318",
    "total": "66782712856390582172"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2379914429241984318",
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
            "amount": "27626855020867858927054"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2379914429241984"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzOTkzNmI0ZS1iZTJkLTU2MGEtYmNjNS04ODg2YTNlZDExOTUifQ==",
    "nonce": 111173,
    "balances": {
      "current": "345815567665109720037673",
      "previous": "345817949959453391263975"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc0a21e69a3e126129798cf09d614b03040bb9902",
    "nonce": 46,
    "balances": {
      "current": "100380763607542721484",
      "previous": "98000849178300737166"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:56:56.173Z",
  "updated": "2022-05-04T08:56:56.260Z",
  "id": "62723fd87832e20011830cac"
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
0x0f200f9b00000000000000000000000000000000000000000000000571101ca9360aebcc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `100380763607542721484`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`