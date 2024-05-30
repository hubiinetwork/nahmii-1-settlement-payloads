# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7D9305303E1bD60747B5429afb5262e389463feE`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000003c200000000000000000000000000000000000000000000000000000000000003c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000003c200000000000000000000000000000000000000000000000000000000000003c2df1ee9ad4cc6b8479c299d3af0ee818fb4c36b9ddf70a3a70360f01219a7f63ed8195eed50106eeeee624df18c634c834af1e990af9e70e9ec4614a3858617536a456ccf5adbfb45fb41bfbdcd9d4383299e47a1b15509c61ef525f33ac413a1000000000000000000000000000000000000000000000000000000000000001b1dcebbdf22fe4f6c1151d0ee88ead5eee7eb159c291dc403a2eb4ccc3a112d59897c3aac9501b0bc50d75cda226540ce970b7b3b616721aac5d8b083704c4897216e88f87fe8eeaf6820c355c42948f9128abff33af6d2db26030e1fbfe353dc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003d400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ca92d52a000000000000000000000000000000000000000000000000002386f2ca92d8ed00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000088b9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a597a4e6d4e7a5a694f53307859544e684c54566d4d7a4974596a457a5a69316c4f4445314d5455795a6d59785a44596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007d9305303e1bd60747b5429afb5262e389463fee00000000000000000000000000000000000000000000000000000000000003c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdf1ee9ad4cc6b8479c299d3af0ee818fb4c36b9ddf70a3a70360f01219a7f63e",
      "signature": {
        "s": "0x6a456ccf5adbfb45fb41bfbdcd9d4383299e47a1b15509c61ef525f33ac413a1",
        "r": "0xd8195eed50106eeeee624df18c634c834af1e990af9e70e9ec4614a385861753",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1dcebbdf22fe4f6c1151d0ee88ead5eee7eb159c291dc403a2eb4ccc3a112d59",
      "signature": {
        "s": "0x216e88f87fe8eeaf6820c355c42948f9128abff33af6d2db26030e1fbfe353dc",
        "r": "0x897c3aac9501b0bc50d75cda226540ce970b7b3b616721aac5d8b083704c4897",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "962",
    "total": "962"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "962",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "560016"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYzNmNzZiOS0xYTNhLTVmMzItYjEzZi1lODE1MTUyZmYxZDYifQ==",
    "nonce": 980,
    "balances": {
      "current": "10000001523701034",
      "previous": "10000001523701997"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7d9305303e1bd60747b5429afb5262e389463fee",
    "nonce": 20,
    "balances": {
      "current": "962",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:59.372Z",
  "updated": "2020-05-22T08:05:59.446Z",
  "id": "5ec787e7b0c6090011d5aa15"
}
```
* *stageAmount*: `962`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000003c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000003c200000000000000000000000000000000000000000000000000000000000003c2df1ee9ad4cc6b8479c299d3af0ee818fb4c36b9ddf70a3a70360f01219a7f63ed8195eed50106eeeee624df18c634c834af1e990af9e70e9ec4614a3858617536a456ccf5adbfb45fb41bfbdcd9d4383299e47a1b15509c61ef525f33ac413a1000000000000000000000000000000000000000000000000000000000000001b1dcebbdf22fe4f6c1151d0ee88ead5eee7eb159c291dc403a2eb4ccc3a112d59897c3aac9501b0bc50d75cda226540ce970b7b3b616721aac5d8b083704c4897216e88f87fe8eeaf6820c355c42948f9128abff33af6d2db26030e1fbfe353dc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003d400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ca92d52a000000000000000000000000000000000000000000000000002386f2ca92d8ed00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000088b9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a597a4e6d4e7a5a694f53307859544e684c54566d4d7a4974596a457a5a69316c4f4445314d5455795a6d59785a44596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007d9305303e1bd60747b5429afb5262e389463fee00000000000000000000000000000000000000000000000000000000000003c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdf1ee9ad4cc6b8479c299d3af0ee818fb4c36b9ddf70a3a70360f01219a7f63e",
      "signature": {
        "s": "0x6a456ccf5adbfb45fb41bfbdcd9d4383299e47a1b15509c61ef525f33ac413a1",
        "r": "0xd8195eed50106eeeee624df18c634c834af1e990af9e70e9ec4614a385861753",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1dcebbdf22fe4f6c1151d0ee88ead5eee7eb159c291dc403a2eb4ccc3a112d59",
      "signature": {
        "s": "0x216e88f87fe8eeaf6820c355c42948f9128abff33af6d2db26030e1fbfe353dc",
        "r": "0x897c3aac9501b0bc50d75cda226540ce970b7b3b616721aac5d8b083704c4897",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "962",
    "total": "962"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "962",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "560016"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYzNmNzZiOS0xYTNhLTVmMzItYjEzZi1lODE1MTUyZmYxZDYifQ==",
    "nonce": 980,
    "balances": {
      "current": "10000001523701034",
      "previous": "10000001523701997"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7d9305303e1bd60747b5429afb5262e389463fee",
    "nonce": 20,
    "balances": {
      "current": "962",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:59.372Z",
  "updated": "2020-05-22T08:05:59.446Z",
  "id": "5ec787e7b0c6090011d5aa15"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000003c20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `962`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``