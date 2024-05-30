# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x464dc0ed896a2bcAa56C5F0418084BDa12b64b23`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000047660000000000000000000000000000000000000000000000000000000000004766000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047660000000000000000000000000000000000000000000000000000000000004766ec208fb5e7273bf9d218a2d2df3d3ea0af01079b8bcfa3bc55f4fec42f1681dee326f82a64bb97cd53539dbdf2177949e43bf2efdf393bb3007703731575adc77b0d7aadb48d4d7c58852b0b4c3a792cbeed4e76fc72faaf0088ea236c28170e000000000000000000000000000000000000000000000000000000000000001b8ddeecb41c5c8e76cb25b391d9f994c6403c3c052c93a0f05dcd63466ac7158a85ac18e76028df45106c9c1d911e719b19cfcbd8dbdf9d0a90e0daf601ab8cd04f3fd1cbb5b26fafde6c89b600b5625bd11dfb8aa9aa06f89c5cc328d01a7d0b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55cb000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002d200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf1619d000000000000000000000000000000000000000000000000002386f2caf1a91500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000873d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493059546732596d45304e69316a4d6d4e6c4c5455794d5463744f474d795a53307a4d5464684e5749354e6a56684d32516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000464dc0ed896a2bcaa56c5f0418084bda12b64b230000000000000000000000000000000000000000000000000000000000004766000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xec208fb5e7273bf9d218a2d2df3d3ea0af01079b8bcfa3bc55f4fec42f1681de",
      "signature": {
        "s": "0x7b0d7aadb48d4d7c58852b0b4c3a792cbeed4e76fc72faaf0088ea236c28170e",
        "r": "0xe326f82a64bb97cd53539dbdf2177949e43bf2efdf393bb3007703731575adc7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8ddeecb41c5c8e76cb25b391d9f994c6403c3c052c93a0f05dcd63466ac7158a",
      "signature": {
        "s": "0x4f3fd1cbb5b26fafde6c89b600b5625bd11dfb8aa9aa06f89c5cc328d01a7d0b",
        "r": "0x85ac18e76028df45106c9c1d911e719b19cfcbd8dbdf9d0a90e0daf601ab8cd0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18278",
    "total": "18278"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18278",
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
            "amount": "553936"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YTg2YmE0Ni1jMmNlLTUyMTctOGMyZS0zMTdhNWI5NjVhM2QifQ==",
    "nonce": 722,
    "balances": {
      "current": "10000001529897373",
      "previous": "10000001529915669"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x464dc0ed896a2bcaa56c5f0418084bda12b64b23",
    "nonce": 20,
    "balances": {
      "current": "18278",
      "previous": "0"
    }
  },
  "blockNumber": "10114507",
  "created": "2020-05-22T08:04:19.540Z",
  "updated": "2020-05-22T08:04:19.623Z",
  "id": "5ec78783005df800101bc307"
}
```
* *stageAmount*: `18278`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004766000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047660000000000000000000000000000000000000000000000000000000000004766ec208fb5e7273bf9d218a2d2df3d3ea0af01079b8bcfa3bc55f4fec42f1681dee326f82a64bb97cd53539dbdf2177949e43bf2efdf393bb3007703731575adc77b0d7aadb48d4d7c58852b0b4c3a792cbeed4e76fc72faaf0088ea236c28170e000000000000000000000000000000000000000000000000000000000000001b8ddeecb41c5c8e76cb25b391d9f994c6403c3c052c93a0f05dcd63466ac7158a85ac18e76028df45106c9c1d911e719b19cfcbd8dbdf9d0a90e0daf601ab8cd04f3fd1cbb5b26fafde6c89b600b5625bd11dfb8aa9aa06f89c5cc328d01a7d0b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55cb000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002d200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf1619d000000000000000000000000000000000000000000000000002386f2caf1a91500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000873d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493059546732596d45304e69316a4d6d4e6c4c5455794d5463744f474d795a53307a4d5464684e5749354e6a56684d32516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000464dc0ed896a2bcaa56c5f0418084bda12b64b230000000000000000000000000000000000000000000000000000000000004766000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xec208fb5e7273bf9d218a2d2df3d3ea0af01079b8bcfa3bc55f4fec42f1681de",
      "signature": {
        "s": "0x7b0d7aadb48d4d7c58852b0b4c3a792cbeed4e76fc72faaf0088ea236c28170e",
        "r": "0xe326f82a64bb97cd53539dbdf2177949e43bf2efdf393bb3007703731575adc7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8ddeecb41c5c8e76cb25b391d9f994c6403c3c052c93a0f05dcd63466ac7158a",
      "signature": {
        "s": "0x4f3fd1cbb5b26fafde6c89b600b5625bd11dfb8aa9aa06f89c5cc328d01a7d0b",
        "r": "0x85ac18e76028df45106c9c1d911e719b19cfcbd8dbdf9d0a90e0daf601ab8cd0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18278",
    "total": "18278"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18278",
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
            "amount": "553936"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YTg2YmE0Ni1jMmNlLTUyMTctOGMyZS0zMTdhNWI5NjVhM2QifQ==",
    "nonce": 722,
    "balances": {
      "current": "10000001529897373",
      "previous": "10000001529915669"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x464dc0ed896a2bcaa56c5f0418084bda12b64b23",
    "nonce": 20,
    "balances": {
      "current": "18278",
      "previous": "0"
    }
  },
  "blockNumber": "10114507",
  "created": "2020-05-22T08:04:19.540Z",
  "updated": "2020-05-22T08:04:19.623Z",
  "id": "5ec78783005df800101bc307"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047660000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18278`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``