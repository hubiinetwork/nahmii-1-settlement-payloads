# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9C384e855c749e53D5B95C1E89Cd42425Bc911ac`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000ac55600000000000000000000000000000000000000000000000000000000000ac556000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000ac55600000000000000000000000000000000000000000000000000000000000ac556a4e76eadb353c8cba9f43a5e4d5e3d91160e08b5313f5ff67e9bae4d2d024645806d7f23c5365b4047f490ad68c3c30c60ce629848ab52f3e3122f4e6ca1d9e10d9eb0d09e6e1a5c6e9327cb6d17d3f06231ebd0b5aaf01c923318587b06670e000000000000000000000000000000000000000000000000000000000000001cd85d025b524318240d7446de9b1eca4bb7cb3f71db02f662ae0215ee1b28dd0c1aa7d0a40dbb480204e9b1489670402f3da09c3870030357e8234f2327bdee2f36f474f8adbb2b32bac4a17a8d249117e432bac45d2435f50393f85864a37e0d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000004000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2df2d92b4000000000000000000000000000000000000000000000000002386f2df385acb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002c10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000347be00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a6d526c4d6d49344d5330314f5467344c54566b5a474974596d45795a5330774e6a51305a5467795a5451304d47496966513d3d000000000000000000000000000000000000000000000000000000000000001f0000000000000000000000009c384e855c749e53d5b95c1e89cd42425bc911ac00000000000000000000000000000000000000000000000000000000000ac556000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa4e76eadb353c8cba9f43a5e4d5e3d91160e08b5313f5ff67e9bae4d2d024645",
      "signature": {
        "s": "0x0d9eb0d09e6e1a5c6e9327cb6d17d3f06231ebd0b5aaf01c923318587b06670e",
        "r": "0x806d7f23c5365b4047f490ad68c3c30c60ce629848ab52f3e3122f4e6ca1d9e1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd85d025b524318240d7446de9b1eca4bb7cb3f71db02f662ae0215ee1b28dd0c",
      "signature": {
        "s": "0x36f474f8adbb2b32bac4a17a8d249117e432bac45d2435f50393f85864a37e0d",
        "r": "0x1aa7d0a40dbb480204e9b1489670402f3da09c3870030357e8234f2327bdee2f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "705878",
    "total": "705878"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "705878",
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
            "amount": "214974"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "705"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZmRlMmI4MS01OTg4LTVkZGItYmEyZS0wNjQ0ZTgyZTQ0MGIifQ==",
    "nonce": 64,
    "balances": {
      "current": "10000001869386420",
      "previous": "10000001870093003"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c384e855c749e53d5b95c1e89cd42425bc911ac",
    "nonce": 31,
    "balances": {
      "current": "705878",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:26.569Z",
  "updated": "2020-05-22T07:59:26.638Z",
  "id": "5ec7865eb0c6090011d5a8e9"
}
```
* *stageAmount*: `705878`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000ac556000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000ac55600000000000000000000000000000000000000000000000000000000000ac556a4e76eadb353c8cba9f43a5e4d5e3d91160e08b5313f5ff67e9bae4d2d024645806d7f23c5365b4047f490ad68c3c30c60ce629848ab52f3e3122f4e6ca1d9e10d9eb0d09e6e1a5c6e9327cb6d17d3f06231ebd0b5aaf01c923318587b06670e000000000000000000000000000000000000000000000000000000000000001cd85d025b524318240d7446de9b1eca4bb7cb3f71db02f662ae0215ee1b28dd0c1aa7d0a40dbb480204e9b1489670402f3da09c3870030357e8234f2327bdee2f36f474f8adbb2b32bac4a17a8d249117e432bac45d2435f50393f85864a37e0d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000004000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2df2d92b4000000000000000000000000000000000000000000000000002386f2df385acb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002c10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000347be00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a6d526c4d6d49344d5330314f5467344c54566b5a474974596d45795a5330774e6a51305a5467795a5451304d47496966513d3d000000000000000000000000000000000000000000000000000000000000001f0000000000000000000000009c384e855c749e53d5b95c1e89cd42425bc911ac00000000000000000000000000000000000000000000000000000000000ac556000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa4e76eadb353c8cba9f43a5e4d5e3d91160e08b5313f5ff67e9bae4d2d024645",
      "signature": {
        "s": "0x0d9eb0d09e6e1a5c6e9327cb6d17d3f06231ebd0b5aaf01c923318587b06670e",
        "r": "0x806d7f23c5365b4047f490ad68c3c30c60ce629848ab52f3e3122f4e6ca1d9e1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd85d025b524318240d7446de9b1eca4bb7cb3f71db02f662ae0215ee1b28dd0c",
      "signature": {
        "s": "0x36f474f8adbb2b32bac4a17a8d249117e432bac45d2435f50393f85864a37e0d",
        "r": "0x1aa7d0a40dbb480204e9b1489670402f3da09c3870030357e8234f2327bdee2f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "705878",
    "total": "705878"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "705878",
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
            "amount": "214974"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "705"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZmRlMmI4MS01OTg4LTVkZGItYmEyZS0wNjQ0ZTgyZTQ0MGIifQ==",
    "nonce": 64,
    "balances": {
      "current": "10000001869386420",
      "previous": "10000001870093003"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c384e855c749e53d5b95c1e89cd42425bc911ac",
    "nonce": 31,
    "balances": {
      "current": "705878",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:26.569Z",
  "updated": "2020-05-22T07:59:26.638Z",
  "id": "5ec7865eb0c6090011d5a8e9"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000ac5560000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `705878`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``