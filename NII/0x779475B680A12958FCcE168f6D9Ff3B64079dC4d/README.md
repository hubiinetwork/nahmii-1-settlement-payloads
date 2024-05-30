# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x779475B680A12958FCcE168f6D9Ff3B64079dC4d`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000033f751c172e4b1c6f000000000000000000000000000000000000000000000000000000014e5aea260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000014e5aea260000000000000000000000000000000000000000000000000000001e7b369899fddbb5157cdc010599dfad964d0b7a11a87ffff7a819cf9711c2d3de37c3b35a4a382aa1b96e0696886806933773a5fcc4cc9992d4600681cea8b843612277893b3d616e524872d7f34ef2a9374d255a8117c52cc5cb6d656bd78c09e14c73b5000000000000000000000000000000000000000000000000000000000000001c73303faa05b6a5f9a22cf6217955282279a6b6aced6a8b207210593d5a3e9ad08db1b4200df34aad27a9daf81dc82a83a86ad3a7f4a76302717beae2b5ae7eac2a49c354ca4e8b357ec14f0be5c49b47a3c248176fc22c4fdc5221d3fd331313000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b050000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f0348d9e80b501a9253000000000000000000000000000000000000000000004f0348d9e80c9ecb14c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000055984c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d82cfb0b9528da91170000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a45345a544a6c4d43316b4e6d5a684c5455344d7a45745954466a5a4330794d575a6a5a54526a596d4a6a5a44636966513d3d000000000000000000000000000000000000000000000000000000000000002a000000000000000000000000779475b680a12958fcce168f6d9ff3b64079dc4d0000000000000000000000000000000000000000000000033f751c172e4b1c6f0000000000000000000000000000000000000000000000033f751c15dff0324900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfddbb5157cdc010599dfad964d0b7a11a87ffff7a819cf9711c2d3de37c3b35a",
      "signature": {
        "s": "0x3b3d616e524872d7f34ef2a9374d255a8117c52cc5cb6d656bd78c09e14c73b5",
        "r": "0x4a382aa1b96e0696886806933773a5fcc4cc9992d4600681cea8b84361227789",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x73303faa05b6a5f9a22cf6217955282279a6b6aced6a8b207210593d5a3e9ad0",
      "signature": {
        "s": "0x2a49c354ca4e8b357ec14f0be5c49b47a3c248176fc22c4fdc5221d3fd331313",
        "r": "0x8db1b4200df34aad27a9daf81dc82a83a86ad3a7f4a76302717beae2b5ae7eac",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5609548326",
    "total": "130916194457"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5609548326",
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
            "amount": "27599570331361575866647"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5609548"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMzE4ZTJlMC1kNmZhLTU4MzEtYTFjZC0yMWZjZTRjYmJjZDcifQ==",
    "nonce": 110672,
    "balances": {
      "current": "373127541860899063763539",
      "previous": "373127541860904678921413"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x779475b680a12958fcce168f6d9ff3b64079dc4d",
    "nonce": 42,
    "balances": {
      "current": "59912824103679761519",
      "previous": "59912824098070213193"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:26.940Z",
  "updated": "2022-05-04T08:54:27.018Z",
  "id": "62723f423592fd001130b524"
}
```
* *stageAmount*: `59912824103679761519`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000014e5aea260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000014e5aea260000000000000000000000000000000000000000000000000000001e7b369899fddbb5157cdc010599dfad964d0b7a11a87ffff7a819cf9711c2d3de37c3b35a4a382aa1b96e0696886806933773a5fcc4cc9992d4600681cea8b843612277893b3d616e524872d7f34ef2a9374d255a8117c52cc5cb6d656bd78c09e14c73b5000000000000000000000000000000000000000000000000000000000000001c73303faa05b6a5f9a22cf6217955282279a6b6aced6a8b207210593d5a3e9ad08db1b4200df34aad27a9daf81dc82a83a86ad3a7f4a76302717beae2b5ae7eac2a49c354ca4e8b357ec14f0be5c49b47a3c248176fc22c4fdc5221d3fd331313000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b050000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f0348d9e80b501a9253000000000000000000000000000000000000000000004f0348d9e80c9ecb14c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000055984c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d82cfb0b9528da91170000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a45345a544a6c4d43316b4e6d5a684c5455344d7a45745954466a5a4330794d575a6a5a54526a596d4a6a5a44636966513d3d000000000000000000000000000000000000000000000000000000000000002a000000000000000000000000779475b680a12958fcce168f6d9ff3b64079dc4d0000000000000000000000000000000000000000000000033f751c172e4b1c6f0000000000000000000000000000000000000000000000033f751c15dff0324900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfddbb5157cdc010599dfad964d0b7a11a87ffff7a819cf9711c2d3de37c3b35a",
      "signature": {
        "s": "0x3b3d616e524872d7f34ef2a9374d255a8117c52cc5cb6d656bd78c09e14c73b5",
        "r": "0x4a382aa1b96e0696886806933773a5fcc4cc9992d4600681cea8b84361227789",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x73303faa05b6a5f9a22cf6217955282279a6b6aced6a8b207210593d5a3e9ad0",
      "signature": {
        "s": "0x2a49c354ca4e8b357ec14f0be5c49b47a3c248176fc22c4fdc5221d3fd331313",
        "r": "0x8db1b4200df34aad27a9daf81dc82a83a86ad3a7f4a76302717beae2b5ae7eac",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5609548326",
    "total": "130916194457"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5609548326",
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
            "amount": "27599570331361575866647"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5609548"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMzE4ZTJlMC1kNmZhLTU4MzEtYTFjZC0yMWZjZTRjYmJjZDcifQ==",
    "nonce": 110672,
    "balances": {
      "current": "373127541860899063763539",
      "previous": "373127541860904678921413"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x779475b680a12958fcce168f6d9ff3b64079dc4d",
    "nonce": 42,
    "balances": {
      "current": "59912824103679761519",
      "previous": "59912824098070213193"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:26.940Z",
  "updated": "2022-05-04T08:54:27.018Z",
  "id": "62723f423592fd001130b524"
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
0x0f200f9b0000000000000000000000000000000000000000000000033f751c172e4b1c6f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `59912824103679761519`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`