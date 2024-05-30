# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6Fc1fe7eC4EFbaD5FF35873037cE4A7f9d17b78d`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000228e571d781acb500000000000000000000000000000000000000000000000000026e10266967eb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000026e10266967eb000000000000000000000000000000000000000000000000021ab59abe9a9054e4c12a38c11aa1d5b824b6dc902a188b52c9771dca13cabbc267d913ed80dcff2b308b417888b5ee54c05d90c76975ac08ac0c66c01cd832bc1bd992bbf3de3c71b54ab82fafe2914971076d1ec047e8234d1e36afd2e7e7e55e9e82f5f55e5c000000000000000000000000000000000000000000000000000000000000001ba60019d5990ee36d2f3a0c10de36ec284e47ef5a3d54a0ee513fd0dafcf7ccad80c2e97b9db2801299a6e9ccb532d0d890def86d4157105cfa4605c797371aad7615e39a8b9c08d9fc60827ca6f960493b93ad59dd2ef94f90126a5a7dc19463000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3eb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039f661b9e43ea09b02e80000000000000000000000000000000000000000000039f661bc52ee068b2dbe00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000009f3f86c2eb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd8f295defa44c3ccf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6a67354f54526a4d6931684f444e6a4c54566b4e6d55744f475179596930784f4467315a6a5a694e44466b4e6a456966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000006fc1fe7ec4efbad5ff35873037ce4a7f9d17b78d0000000000000000000000000000000000000000000000000228e571d781acb500000000000000000000000000000000000000000000000002267761b11844ca00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe4c12a38c11aa1d5b824b6dc902a188b52c9771dca13cabbc267d913ed80dcff",
      "signature": {
        "s": "0x71b54ab82fafe2914971076d1ec047e8234d1e36afd2e7e7e55e9e82f5f55e5c",
        "r": "0x2b308b417888b5ee54c05d90c76975ac08ac0c66c01cd832bc1bd992bbf3de3c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa60019d5990ee36d2f3a0c10de36ec284e47ef5a3d54a0ee513fd0dafcf7ccad",
      "signature": {
        "s": "0x7615e39a8b9c08d9fc60827ca6f960493b93ad59dd2ef94f90126a5a7dc19463",
        "r": "0x80c2e97b9db2801299a6e9ccb532d0d890def86d4157105cfa4605c797371aad",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "683965596395499",
    "total": "151633213697724500"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "683965596395499",
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
            "amount": "27698878734343340833999"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "683965596395"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5Zjg5OTRjMi1hODNjLTVkNmUtOGQyYi0xODg1ZjZiNDFkNjEifQ==",
    "nonce": 111595,
    "balances": {
      "current": "273719830476152330978024",
      "previous": "273719831160801892969918"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6fc1fe7ec4efbad5ff35873037ce4a7f9d17b78d",
    "nonce": 29,
    "balances": {
      "current": "155626464253947061",
      "previous": "154942498657551562"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:09.684Z",
  "updated": "2022-05-04T08:59:09.776Z",
  "id": "6272405d3592fd001130b669"
}
```
* *stageAmount*: `155626464253947061`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000026e10266967eb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000026e10266967eb000000000000000000000000000000000000000000000000021ab59abe9a9054e4c12a38c11aa1d5b824b6dc902a188b52c9771dca13cabbc267d913ed80dcff2b308b417888b5ee54c05d90c76975ac08ac0c66c01cd832bc1bd992bbf3de3c71b54ab82fafe2914971076d1ec047e8234d1e36afd2e7e7e55e9e82f5f55e5c000000000000000000000000000000000000000000000000000000000000001ba60019d5990ee36d2f3a0c10de36ec284e47ef5a3d54a0ee513fd0dafcf7ccad80c2e97b9db2801299a6e9ccb532d0d890def86d4157105cfa4605c797371aad7615e39a8b9c08d9fc60827ca6f960493b93ad59dd2ef94f90126a5a7dc19463000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3eb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039f661b9e43ea09b02e80000000000000000000000000000000000000000000039f661bc52ee068b2dbe00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000009f3f86c2eb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd8f295defa44c3ccf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6a67354f54526a4d6931684f444e6a4c54566b4e6d55744f475179596930784f4467315a6a5a694e44466b4e6a456966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000006fc1fe7ec4efbad5ff35873037ce4a7f9d17b78d0000000000000000000000000000000000000000000000000228e571d781acb500000000000000000000000000000000000000000000000002267761b11844ca00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe4c12a38c11aa1d5b824b6dc902a188b52c9771dca13cabbc267d913ed80dcff",
      "signature": {
        "s": "0x71b54ab82fafe2914971076d1ec047e8234d1e36afd2e7e7e55e9e82f5f55e5c",
        "r": "0x2b308b417888b5ee54c05d90c76975ac08ac0c66c01cd832bc1bd992bbf3de3c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa60019d5990ee36d2f3a0c10de36ec284e47ef5a3d54a0ee513fd0dafcf7ccad",
      "signature": {
        "s": "0x7615e39a8b9c08d9fc60827ca6f960493b93ad59dd2ef94f90126a5a7dc19463",
        "r": "0x80c2e97b9db2801299a6e9ccb532d0d890def86d4157105cfa4605c797371aad",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "683965596395499",
    "total": "151633213697724500"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "683965596395499",
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
            "amount": "27698878734343340833999"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "683965596395"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5Zjg5OTRjMi1hODNjLTVkNmUtOGQyYi0xODg1ZjZiNDFkNjEifQ==",
    "nonce": 111595,
    "balances": {
      "current": "273719830476152330978024",
      "previous": "273719831160801892969918"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6fc1fe7ec4efbad5ff35873037ce4a7f9d17b78d",
    "nonce": 29,
    "balances": {
      "current": "155626464253947061",
      "previous": "154942498657551562"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:09.684Z",
  "updated": "2022-05-04T08:59:09.776Z",
  "id": "6272405d3592fd001130b669"
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
0x0f200f9b0000000000000000000000000000000000000000000000000228e571d781acb50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `155626464253947061`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`