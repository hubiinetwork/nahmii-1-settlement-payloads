# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD83Fd5b1575068E46f403be32954464007061bCE`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000911c5846ae9d6ebff100000000000000000000000000000000000000000000000370bec9b55fcd995d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000370bec9b55fcd995d0000000000000000000000000000000000000000000000608a91885820445449baaeff237739c8048f585b25f38a68ad7e477afe0f8b34d5af74069314c4c78f28d72a4b2f98b048bc4dac747a46c3baf797b524622b72c695f82767afc27b9248cbabcba2bfeaeddabefee7361a1f7431a6ba1184c896367396a5ecfaa92b02000000000000000000000000000000000000000000000000000000000000001c9b85259db8fd29fa68c8790cf2068c9ea0cf290bc7e2252ea469ed448c1649522b9629fc22467c67a9b8582971b52d90c4509590e3a5bb2897054d892445f05261529db0b6cf075d7b2668ad1f3c5edcd356fb00066b262d2802dad8cb7e27d7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b684000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030a5f56c3c4736c9b5dd0000000000000000000000000000000000000000000030a9670c7e822547631700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000e178858eb013dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dff0f6cea1a1971e6f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e574e694d324e6c4d4330335a6a41354c54557a59546b744f44466b5969307a4d6d4e6d5a474a6c5a6d59325957456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d83fd5b1575068e46f403be32954464007061bce0000000000000000000000000000000000000000000000911c5846ae9d6ebff100000000000000000000000000000000000000000000008dab997cf93da1269400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbaaeff237739c8048f585b25f38a68ad7e477afe0f8b34d5af74069314c4c78f",
      "signature": {
        "s": "0x48cbabcba2bfeaeddabefee7361a1f7431a6ba1184c896367396a5ecfaa92b02",
        "r": "0x28d72a4b2f98b048bc4dac747a46c3baf797b524622b72c695f82767afc27b92",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9b85259db8fd29fa68c8790cf2068c9ea0cf290bc7e2252ea469ed448c164952",
      "signature": {
        "s": "0x61529db0b6cf075d7b2668ad1f3c5edcd356fb00066b262d2802dad8cb7e27d7",
        "r": "0x2b9629fc22467c67a9b8582971b52d90c4509590e3a5bb2897054d892445f052",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "63464384779785181533",
    "total": "1780872342837053903945"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "63464384779785181533",
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
            "amount": "27742819635392425696879"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "63464384779785181"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NWNiM2NlMC03ZjA5LTUzYTktODFkYi0zMmNmZGJlZmY2YWEifQ==",
    "nonce": 112260,
    "balances": {
      "current": "229734988526018382902749",
      "previous": "229798516375182947869463"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd83fd5b1575068e46f403be32954464007061bce",
    "nonce": 46,
    "balances": {
      "current": "2676820350834677039089",
      "previous": "2613355966054891857556"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:50.146Z",
  "updated": "2022-05-04T09:02:50.224Z",
  "id": "6272413abbd75600116d07b3"
}
```
* *stageAmount*: `2676820350834677039089`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000370bec9b55fcd995d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000370bec9b55fcd995d0000000000000000000000000000000000000000000000608a91885820445449baaeff237739c8048f585b25f38a68ad7e477afe0f8b34d5af74069314c4c78f28d72a4b2f98b048bc4dac747a46c3baf797b524622b72c695f82767afc27b9248cbabcba2bfeaeddabefee7361a1f7431a6ba1184c896367396a5ecfaa92b02000000000000000000000000000000000000000000000000000000000000001c9b85259db8fd29fa68c8790cf2068c9ea0cf290bc7e2252ea469ed448c1649522b9629fc22467c67a9b8582971b52d90c4509590e3a5bb2897054d892445f05261529db0b6cf075d7b2668ad1f3c5edcd356fb00066b262d2802dad8cb7e27d7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b684000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030a5f56c3c4736c9b5dd0000000000000000000000000000000000000000000030a9670c7e822547631700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000e178858eb013dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dff0f6cea1a1971e6f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e574e694d324e6c4d4330335a6a41354c54557a59546b744f44466b5969307a4d6d4e6d5a474a6c5a6d59325957456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d83fd5b1575068e46f403be32954464007061bce0000000000000000000000000000000000000000000000911c5846ae9d6ebff100000000000000000000000000000000000000000000008dab997cf93da1269400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbaaeff237739c8048f585b25f38a68ad7e477afe0f8b34d5af74069314c4c78f",
      "signature": {
        "s": "0x48cbabcba2bfeaeddabefee7361a1f7431a6ba1184c896367396a5ecfaa92b02",
        "r": "0x28d72a4b2f98b048bc4dac747a46c3baf797b524622b72c695f82767afc27b92",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9b85259db8fd29fa68c8790cf2068c9ea0cf290bc7e2252ea469ed448c164952",
      "signature": {
        "s": "0x61529db0b6cf075d7b2668ad1f3c5edcd356fb00066b262d2802dad8cb7e27d7",
        "r": "0x2b9629fc22467c67a9b8582971b52d90c4509590e3a5bb2897054d892445f052",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "63464384779785181533",
    "total": "1780872342837053903945"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "63464384779785181533",
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
            "amount": "27742819635392425696879"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "63464384779785181"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NWNiM2NlMC03ZjA5LTUzYTktODFkYi0zMmNmZGJlZmY2YWEifQ==",
    "nonce": 112260,
    "balances": {
      "current": "229734988526018382902749",
      "previous": "229798516375182947869463"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd83fd5b1575068e46f403be32954464007061bce",
    "nonce": 46,
    "balances": {
      "current": "2676820350834677039089",
      "previous": "2613355966054891857556"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:50.146Z",
  "updated": "2022-05-04T09:02:50.224Z",
  "id": "6272413abbd75600116d07b3"
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
0x0f200f9b0000000000000000000000000000000000000000000000911c5846ae9d6ebff10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2676820350834677039089`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`