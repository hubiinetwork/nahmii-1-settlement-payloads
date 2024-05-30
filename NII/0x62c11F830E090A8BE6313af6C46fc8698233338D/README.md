# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x62c11F830E090A8BE6313af6C46fc8698233338D`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000186e49c4028b3000000000000000000000000000000000000000000000000000000000000d25a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000d25a0000000000000000000000000000000000000000000000000000000000132d25507e231509f797ba37ffbe5a8266f98fb5ceb70273ca7c51653b067f66559f083fe8f210d7323c11e34b423d5a4ef2baa1d5b443c760eb5e483b8bf3abf3e7ec3bcf5bc5ca9bd662fb20a872d123a1d7d58d73888accaa94cb674d95fe0f4c3c000000000000000000000000000000000000000000000000000000000000001c86cd6352b299861d339ba75b76aba94873d6756e3b7c02603ba9ff8115aec3b483fef721e2ecceab8b64dedcbb41dd1c59004f745653a30315d6de577b8d03f6579cd4cf8cf1ce6c4dc3728a8fce81b806eb40b3320f964d2cca9304dd7ac2ce000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b36f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c862f2572620be52161000000000000000000000000000000000000000000003c862f2572620be5f3f000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce771a296dcf741de0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a5467324d475a69596930794d47526d4c5455334d6a6b74595451795953316b596a4d774f574d794e44686a5932556966513d3d000000000000000000000000000000000000000000000000000000000000001d00000000000000000000000062c11f830e090a8be6313af6c46fc8698233338d000000000000000000000000000000000000000000000000000186e49c4028b3000000000000000000000000000000000000000000000000000186e49c3f565900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x507e231509f797ba37ffbe5a8266f98fb5ceb70273ca7c51653b067f66559f08",
      "signature": {
        "s": "0x3bcf5bc5ca9bd662fb20a872d123a1d7d58d73888accaa94cb674d95fe0f4c3c",
        "r": "0x3fe8f210d7323c11e34b423d5a4ef2baa1d5b443c760eb5e483b8bf3abf3e7ec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x86cd6352b299861d339ba75b76aba94873d6756e3b7c02603ba9ff8115aec3b4",
      "signature": {
        "s": "0x579cd4cf8cf1ce6c4dc3728a8fce81b806eb40b3320f964d2cca9304dd7ac2ce",
        "r": "0x83fef721e2ecceab8b64dedcbb41dd1c59004f745653a30315d6de577b8d03f6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "53850",
    "total": "1256741"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "53850",
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
            "amount": "27686793400228293067230"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "53"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZTg2MGZiYi0yMGRmLTU3MjktYTQyYS1kYjMwOWMyNDhjY2UifQ==",
    "nonce": 111471,
    "balances": {
      "current": "285817249925315145572705",
      "previous": "285817249925315145626608"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x62c11f830e090a8be6313af6c46fc8698233338d",
    "nonce": 29,
    "balances": {
      "current": "429791408826547",
      "previous": "429791408772697"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:29.192Z",
  "updated": "2022-05-04T08:58:29.259Z",
  "id": "627240357832e20011830d0f"
}
```
* *stageAmount*: `429791408826547`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000d25a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000d25a0000000000000000000000000000000000000000000000000000000000132d25507e231509f797ba37ffbe5a8266f98fb5ceb70273ca7c51653b067f66559f083fe8f210d7323c11e34b423d5a4ef2baa1d5b443c760eb5e483b8bf3abf3e7ec3bcf5bc5ca9bd662fb20a872d123a1d7d58d73888accaa94cb674d95fe0f4c3c000000000000000000000000000000000000000000000000000000000000001c86cd6352b299861d339ba75b76aba94873d6756e3b7c02603ba9ff8115aec3b483fef721e2ecceab8b64dedcbb41dd1c59004f745653a30315d6de577b8d03f6579cd4cf8cf1ce6c4dc3728a8fce81b806eb40b3320f964d2cca9304dd7ac2ce000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b36f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c862f2572620be52161000000000000000000000000000000000000000000003c862f2572620be5f3f000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce771a296dcf741de0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a5467324d475a69596930794d47526d4c5455334d6a6b74595451795953316b596a4d774f574d794e44686a5932556966513d3d000000000000000000000000000000000000000000000000000000000000001d00000000000000000000000062c11f830e090a8be6313af6c46fc8698233338d000000000000000000000000000000000000000000000000000186e49c4028b3000000000000000000000000000000000000000000000000000186e49c3f565900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x507e231509f797ba37ffbe5a8266f98fb5ceb70273ca7c51653b067f66559f08",
      "signature": {
        "s": "0x3bcf5bc5ca9bd662fb20a872d123a1d7d58d73888accaa94cb674d95fe0f4c3c",
        "r": "0x3fe8f210d7323c11e34b423d5a4ef2baa1d5b443c760eb5e483b8bf3abf3e7ec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x86cd6352b299861d339ba75b76aba94873d6756e3b7c02603ba9ff8115aec3b4",
      "signature": {
        "s": "0x579cd4cf8cf1ce6c4dc3728a8fce81b806eb40b3320f964d2cca9304dd7ac2ce",
        "r": "0x83fef721e2ecceab8b64dedcbb41dd1c59004f745653a30315d6de577b8d03f6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "53850",
    "total": "1256741"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "53850",
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
            "amount": "27686793400228293067230"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "53"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZTg2MGZiYi0yMGRmLTU3MjktYTQyYS1kYjMwOWMyNDhjY2UifQ==",
    "nonce": 111471,
    "balances": {
      "current": "285817249925315145572705",
      "previous": "285817249925315145626608"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x62c11f830e090a8be6313af6c46fc8698233338d",
    "nonce": 29,
    "balances": {
      "current": "429791408826547",
      "previous": "429791408772697"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:29.192Z",
  "updated": "2022-05-04T08:58:29.259Z",
  "id": "627240357832e20011830d0f"
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
0x0f200f9b000000000000000000000000000000000000000000000000000186e49c4028b30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `429791408826547`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`