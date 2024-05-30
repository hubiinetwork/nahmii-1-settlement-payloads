# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0253cDc202B5e1BcBeA03e4D571366a5C1f203f5`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000005f18a4389885762180000000000000000000000000000000000000000000000028b47184f130b02dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000028b47184f130b02dd000000000000000000000000000000000000000000000005f18a438988576218b67eb989866601fe13c26f92a6192c30adf6b404422b804ac4c5d999d60445c11f8bafe24586d71355cf2ae4bac698829c0e153fa235eb056ad6520c06ee2c850190715c62ef4a57773cbef3d45a812094c900149d9180cd44d934c855ae2690000000000000000000000000000000000000000000000000000000000000001ccfc703c3d3b5d630aa0c05059f59f7abbb2e8e6bc34171aad827fc1579e5b275b102c832298e4340ef426d44eb238690ef66ff4474abeeea7155da58063aa95e3f5a367666dc77b3117d45e3472e9227d5ad78231e390dbe584463441306a507000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000dd3f2900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000019244000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000e6d19a84c774806e1ef300000000000000000000000000000000000000000000e6d4267299e6789cba2200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000a6ba22e52398520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005450a516a163df7713c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e7a5a6a4e7a4e6c4d7930794f446c6a4c5455354d325974595463334d6930795a57466b4f54426b4f4755324d444d6966513d3d00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000253cdc202b5e1bcbea03e4d571366a5c1f203f5000000000000000000000000000000000000000000000005f18a43898857621800000000000000000000000000000000000000000000000366432b3a754c5f3b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb67eb989866601fe13c26f92a6192c30adf6b404422b804ac4c5d999d60445c1",
      "signature": {
        "s": "0x0190715c62ef4a57773cbef3d45a812094c900149d9180cd44d934c855ae2690",
        "r": "0x1f8bafe24586d71355cf2ae4bac698829c0e153fa235eb056ad6520c06ee2c85",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcfc703c3d3b5d630aa0c05059f59f7abbb2e8e6bc34171aad827fc1579e5b275",
      "signature": {
        "s": "0x3f5a367666dc77b3117d45e3472e9227d5ad78231e390dbe584463441306a507",
        "r": "0xb102c832298e4340ef426d44eb238690ef66ff4474abeeea7155da58063aa95e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "46929505169938514653",
    "total": "109638518336451469848"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "46929505169938514653",
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
            "amount": "24885401247491439423804"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "46929505169938514"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NzZjNzNlMy0yODljLTU5M2YtYTc3Mi0yZWFkOTBkOGU2MDMifQ==",
    "nonce": 102980,
    "balances": {
      "current": "1090010794814905646980851",
      "previous": "1090057771249580755434018"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0253cdc202b5e1bcbea03e4d571366a5c1f203f5",
    "nonce": 2,
    "balances": {
      "current": "109638518336451469848",
      "previous": "62709013166512955195"
    }
  },
  "blockNumber": "14499625",
  "created": "2022-04-01T09:52:40.293Z",
  "updated": "2022-04-01T09:52:40.346Z",
  "id": "6246cb68bbd75600116cfae9"
}
```
* *stageAmount*: `109638518336451469848`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000028b47184f130b02dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000028b47184f130b02dd000000000000000000000000000000000000000000000005f18a438988576218b67eb989866601fe13c26f92a6192c30adf6b404422b804ac4c5d999d60445c11f8bafe24586d71355cf2ae4bac698829c0e153fa235eb056ad6520c06ee2c850190715c62ef4a57773cbef3d45a812094c900149d9180cd44d934c855ae2690000000000000000000000000000000000000000000000000000000000000001ccfc703c3d3b5d630aa0c05059f59f7abbb2e8e6bc34171aad827fc1579e5b275b102c832298e4340ef426d44eb238690ef66ff4474abeeea7155da58063aa95e3f5a367666dc77b3117d45e3472e9227d5ad78231e390dbe584463441306a507000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000dd3f2900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000019244000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000e6d19a84c774806e1ef300000000000000000000000000000000000000000000e6d4267299e6789cba2200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000a6ba22e52398520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005450a516a163df7713c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e7a5a6a4e7a4e6c4d7930794f446c6a4c5455354d325974595463334d6930795a57466b4f54426b4f4755324d444d6966513d3d00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000253cdc202b5e1bcbea03e4d571366a5c1f203f5000000000000000000000000000000000000000000000005f18a43898857621800000000000000000000000000000000000000000000000366432b3a754c5f3b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb67eb989866601fe13c26f92a6192c30adf6b404422b804ac4c5d999d60445c1",
      "signature": {
        "s": "0x0190715c62ef4a57773cbef3d45a812094c900149d9180cd44d934c855ae2690",
        "r": "0x1f8bafe24586d71355cf2ae4bac698829c0e153fa235eb056ad6520c06ee2c85",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcfc703c3d3b5d630aa0c05059f59f7abbb2e8e6bc34171aad827fc1579e5b275",
      "signature": {
        "s": "0x3f5a367666dc77b3117d45e3472e9227d5ad78231e390dbe584463441306a507",
        "r": "0xb102c832298e4340ef426d44eb238690ef66ff4474abeeea7155da58063aa95e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "46929505169938514653",
    "total": "109638518336451469848"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "46929505169938514653",
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
            "amount": "24885401247491439423804"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "46929505169938514"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NzZjNzNlMy0yODljLTU5M2YtYTc3Mi0yZWFkOTBkOGU2MDMifQ==",
    "nonce": 102980,
    "balances": {
      "current": "1090010794814905646980851",
      "previous": "1090057771249580755434018"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0253cdc202b5e1bcbea03e4d571366a5c1f203f5",
    "nonce": 2,
    "balances": {
      "current": "109638518336451469848",
      "previous": "62709013166512955195"
    }
  },
  "blockNumber": "14499625",
  "created": "2022-04-01T09:52:40.293Z",
  "updated": "2022-04-01T09:52:40.346Z",
  "id": "6246cb68bbd75600116cfae9"
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
0x0f200f9b000000000000000000000000000000000000000000000005f18a4389885762180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `109638518336451469848`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`