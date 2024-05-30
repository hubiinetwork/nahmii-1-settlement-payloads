# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe78bb84c4bf268bc9AaBb8699bb32a3B08C0Fb3b`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000009370000000000000000000000000000000000000000000000000000000000000937000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000009370000000000000000000000000000000000000000000000000000000000000937137c20f8955515365ec4bc15f5b001c5c3ce6b3ec725cec9c808fa099711eff17d98cfdb8620e0998d94def1abc7ec54506d8cb9a1dbc9b250f1cacabeb2531f68d2c7f24d9e1a7a47a6472337eea6d0351432b1e7e8f0a3507532c448690965000000000000000000000000000000000000000000000000000000000000001bbb9071f42006e2160bf2373fd2bfd3e78de1f6c2c03ae36f7bdb3ec2f66b12b97137bc3c8929239fde3f8c3d0bfed3e81dbd8302f273a2c891d9924fb907aa005917a4f535a1cda3b015f2baa4237844358394c681cd29914a6afaa8e9b7eb27000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000033a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae2078c000000000000000000000000000000000000000000000000002386f2cae210c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008778c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6d4a694d444e6a4f4330315a574d314c5455304e324d74596a557a4d53307a596a41785a6a6b7759544178597a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000008000000000000000000000000e78bb84c4bf268bc9aabb8699bb32a3b08c0fb3b0000000000000000000000000000000000000000000000000000000000000937000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x137c20f8955515365ec4bc15f5b001c5c3ce6b3ec725cec9c808fa099711eff1",
      "signature": {
        "s": "0x68d2c7f24d9e1a7a47a6472337eea6d0351432b1e7e8f0a3507532c448690965",
        "r": "0x7d98cfdb8620e0998d94def1abc7ec54506d8cb9a1dbc9b250f1cacabeb2531f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbb9071f42006e2160bf2373fd2bfd3e78de1f6c2c03ae36f7bdb3ec2f66b12b9",
      "signature": {
        "s": "0x5917a4f535a1cda3b015f2baa4237844358394c681cd29914a6afaa8e9b7eb27",
        "r": "0x7137bc3c8929239fde3f8c3d0bfed3e81dbd8302f273a2c891d9924fb907aa00",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2359",
    "total": "2359"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2359",
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
            "amount": "554892"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NmJiMDNjOC01ZWM1LTU0N2MtYjUzMS0zYjAxZjkwYTAxYzMifQ==",
    "nonce": 826,
    "balances": {
      "current": "10000001528891276",
      "previous": "10000001528893637"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe78bb84c4bf268bc9aabb8699bb32a3b08c0fb3b",
    "nonce": 8,
    "balances": {
      "current": "2359",
      "previous": "0"
    }
  },
  "blockNumber": "10114511",
  "created": "2020-05-22T08:04:55.602Z",
  "updated": "2020-05-22T08:04:55.746Z",
  "id": "5ec787a7005df800101bc32a"
}
```
* *stageAmount*: `2359`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000937000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000009370000000000000000000000000000000000000000000000000000000000000937137c20f8955515365ec4bc15f5b001c5c3ce6b3ec725cec9c808fa099711eff17d98cfdb8620e0998d94def1abc7ec54506d8cb9a1dbc9b250f1cacabeb2531f68d2c7f24d9e1a7a47a6472337eea6d0351432b1e7e8f0a3507532c448690965000000000000000000000000000000000000000000000000000000000000001bbb9071f42006e2160bf2373fd2bfd3e78de1f6c2c03ae36f7bdb3ec2f66b12b97137bc3c8929239fde3f8c3d0bfed3e81dbd8302f273a2c891d9924fb907aa005917a4f535a1cda3b015f2baa4237844358394c681cd29914a6afaa8e9b7eb27000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000033a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae2078c000000000000000000000000000000000000000000000000002386f2cae210c500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008778c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6d4a694d444e6a4f4330315a574d314c5455304e324d74596a557a4d53307a596a41785a6a6b7759544178597a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000008000000000000000000000000e78bb84c4bf268bc9aabb8699bb32a3b08c0fb3b0000000000000000000000000000000000000000000000000000000000000937000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x137c20f8955515365ec4bc15f5b001c5c3ce6b3ec725cec9c808fa099711eff1",
      "signature": {
        "s": "0x68d2c7f24d9e1a7a47a6472337eea6d0351432b1e7e8f0a3507532c448690965",
        "r": "0x7d98cfdb8620e0998d94def1abc7ec54506d8cb9a1dbc9b250f1cacabeb2531f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbb9071f42006e2160bf2373fd2bfd3e78de1f6c2c03ae36f7bdb3ec2f66b12b9",
      "signature": {
        "s": "0x5917a4f535a1cda3b015f2baa4237844358394c681cd29914a6afaa8e9b7eb27",
        "r": "0x7137bc3c8929239fde3f8c3d0bfed3e81dbd8302f273a2c891d9924fb907aa00",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2359",
    "total": "2359"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2359",
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
            "amount": "554892"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NmJiMDNjOC01ZWM1LTU0N2MtYjUzMS0zYjAxZjkwYTAxYzMifQ==",
    "nonce": 826,
    "balances": {
      "current": "10000001528891276",
      "previous": "10000001528893637"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe78bb84c4bf268bc9aabb8699bb32a3b08c0fb3b",
    "nonce": 8,
    "balances": {
      "current": "2359",
      "previous": "0"
    }
  },
  "blockNumber": "10114511",
  "created": "2020-05-22T08:04:55.602Z",
  "updated": "2020-05-22T08:04:55.746Z",
  "id": "5ec787a7005df800101bc32a"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000009370000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2359`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``