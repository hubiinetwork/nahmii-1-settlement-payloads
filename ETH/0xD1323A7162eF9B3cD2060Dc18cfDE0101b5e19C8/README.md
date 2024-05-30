# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD1323A7162eF9B3cD2060Dc18cfDE0101b5e19C8`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000026a600000000000000000000000000000000000000000000000000000000000026a6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000026a600000000000000000000000000000000000000000000000000000000000026a6bdc4ca34e744b700ffd810cfad18578a3ade4749ebd3d810bf578e5712f6eecbbc7bbe8db937bb6c70cede7c2b6f014f8f84484b2a8aacfe70226193f2bb7b914dc6e9573463034f2986877a3b97aa9b2f2378ce0caa3d07f0ee25632c9950dc000000000000000000000000000000000000000000000000000000000000001c0dcc7cfe37015f8d27c35f8cd6d91bb59da8f482079a3889f69b1319f61061fde5de4e28a726a02f158a49ce280a79828acc2ca26ca63d06730b91db17210b791a7ea24428a7ce31722080bc29dd1897b1db15cbed07e3e8698409f3f992f3cf000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000071500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c4316e06000000000000000000000000000000000000000000000000002386f2c43194b500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2c7300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d6a4e684d7a686c4e4330784f446b344c54566d4d6d59744f4459785953316c4e474e6c596a466d596a67795a54516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d1323a7162ef9b3cd2060dc18cfde0101b5e19c800000000000000000000000000000000000000000000000000000000000026a6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbdc4ca34e744b700ffd810cfad18578a3ade4749ebd3d810bf578e5712f6eecb",
      "signature": {
        "s": "0x4dc6e9573463034f2986877a3b97aa9b2f2378ce0caa3d07f0ee25632c9950dc",
        "r": "0xbc7bbe8db937bb6c70cede7c2b6f014f8f84484b2a8aacfe70226193f2bb7b91",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0dcc7cfe37015f8d27c35f8cd6d91bb59da8f482079a3889f69b1319f61061fd",
      "signature": {
        "s": "0x1a7ea24428a7ce31722080bc29dd1897b1db15cbed07e3e8698409f3f992f3cf",
        "r": "0xe5de4e28a726a02f158a49ce280a79828acc2ca26ca63d06730b91db17210b79",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9894",
    "total": "9894"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9894",
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
            "amount": "666739"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1MjNhMzhlNC0xODk4LTVmMmYtODYxYS1lNGNlYjFmYjgyZTQifQ==",
    "nonce": 1813,
    "balances": {
      "current": "10000001416654342",
      "previous": "10000001416664245"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd1323a7162ef9b3cd2060dc18cfde0101b5e19c8",
    "nonce": 20,
    "balances": {
      "current": "9894",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:17.354Z",
  "updated": "2020-05-22T08:12:17.445Z",
  "id": "5ec78961005df800101bc482"
}
```
* *stageAmount*: `9894`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000026a6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000026a600000000000000000000000000000000000000000000000000000000000026a6bdc4ca34e744b700ffd810cfad18578a3ade4749ebd3d810bf578e5712f6eecbbc7bbe8db937bb6c70cede7c2b6f014f8f84484b2a8aacfe70226193f2bb7b914dc6e9573463034f2986877a3b97aa9b2f2378ce0caa3d07f0ee25632c9950dc000000000000000000000000000000000000000000000000000000000000001c0dcc7cfe37015f8d27c35f8cd6d91bb59da8f482079a3889f69b1319f61061fde5de4e28a726a02f158a49ce280a79828acc2ca26ca63d06730b91db17210b791a7ea24428a7ce31722080bc29dd1897b1db15cbed07e3e8698409f3f992f3cf000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000071500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c4316e06000000000000000000000000000000000000000000000000002386f2c43194b500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2c7300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d6a4e684d7a686c4e4330784f446b344c54566d4d6d59744f4459785953316c4e474e6c596a466d596a67795a54516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d1323a7162ef9b3cd2060dc18cfde0101b5e19c800000000000000000000000000000000000000000000000000000000000026a6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbdc4ca34e744b700ffd810cfad18578a3ade4749ebd3d810bf578e5712f6eecb",
      "signature": {
        "s": "0x4dc6e9573463034f2986877a3b97aa9b2f2378ce0caa3d07f0ee25632c9950dc",
        "r": "0xbc7bbe8db937bb6c70cede7c2b6f014f8f84484b2a8aacfe70226193f2bb7b91",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0dcc7cfe37015f8d27c35f8cd6d91bb59da8f482079a3889f69b1319f61061fd",
      "signature": {
        "s": "0x1a7ea24428a7ce31722080bc29dd1897b1db15cbed07e3e8698409f3f992f3cf",
        "r": "0xe5de4e28a726a02f158a49ce280a79828acc2ca26ca63d06730b91db17210b79",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9894",
    "total": "9894"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9894",
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
            "amount": "666739"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1MjNhMzhlNC0xODk4LTVmMmYtODYxYS1lNGNlYjFmYjgyZTQifQ==",
    "nonce": 1813,
    "balances": {
      "current": "10000001416654342",
      "previous": "10000001416664245"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd1323a7162ef9b3cd2060dc18cfde0101b5e19c8",
    "nonce": 20,
    "balances": {
      "current": "9894",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:17.354Z",
  "updated": "2020-05-22T08:12:17.445Z",
  "id": "5ec78961005df800101bc482"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000026a60000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9894`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``