# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2b616914adA8484Ab9D70398dBE86B029b1a9a39`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000066330000000000000000000000000000000000000000000000000000000000006633000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000066330000000000000000000000000000000000000000000000000000000000006633cd7831b818d9d58963b46e173d5da4062a628897bc5800078ef00cbdd8633cd84c2b8aa005d6c189d3adf950cf08428c829bf82083901e38c544a1e1958fa795684f234940ac487b9bd413074f0e97cc04a8af9e73d2b2d49080a4b71d2f27d9000000000000000000000000000000000000000000000000000000000000001ba07465a062aca58b8214d92d827c5f248352c3ebbfe98471e77acbee9cdf1a5dc8fc0efb27a73f73ae91ca35f9d59f05899cef0cf1f227b53b45b777819fd59f02d8320515695d9f9d733311cf3edfc6388bd6f2ec7621104c5936c8a0cdf282000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001be00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cc0d70e2000000000000000000000000000000000000000000000000002386f2cc0dd72f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000082b9100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775954526b4e6a51775a69316d4d6d4e6a4c54566a4e7a5974595459774e43316c5a6d4d774d7a4e6b597a67334d6d496966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000002b616914ada8484ab9d70398dbe86b029b1a9a390000000000000000000000000000000000000000000000000000000000006633000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcd7831b818d9d58963b46e173d5da4062a628897bc5800078ef00cbdd8633cd8",
      "signature": {
        "s": "0x684f234940ac487b9bd413074f0e97cc04a8af9e73d2b2d49080a4b71d2f27d9",
        "r": "0x4c2b8aa005d6c189d3adf950cf08428c829bf82083901e38c544a1e1958fa795",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa07465a062aca58b8214d92d827c5f248352c3ebbfe98471e77acbee9cdf1a5d",
      "signature": {
        "s": "0x02d8320515695d9f9d733311cf3edfc6388bd6f2ec7621104c5936c8a0cdf282",
        "r": "0xc8fc0efb27a73f73ae91ca35f9d59f05899cef0cf1f227b53b45b777819fd59f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "26163",
    "total": "26163"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26163",
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
            "amount": "535441"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "26"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYTRkNjQwZi1mMmNjLTVjNzYtYTYwNC1lZmMwMzNkYzg3MmIifQ==",
    "nonce": 446,
    "balances": {
      "current": "10000001548513506",
      "previous": "10000001548539695"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2b616914ada8484ab9d70398dbe86b029b1a9a39",
    "nonce": 9,
    "balances": {
      "current": "26163",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:06.473Z",
  "updated": "2020-05-22T08:02:06.553Z",
  "id": "5ec786feb0c6090011d5a960"
}
```
* *stageAmount*: `26163`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000006633000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000066330000000000000000000000000000000000000000000000000000000000006633cd7831b818d9d58963b46e173d5da4062a628897bc5800078ef00cbdd8633cd84c2b8aa005d6c189d3adf950cf08428c829bf82083901e38c544a1e1958fa795684f234940ac487b9bd413074f0e97cc04a8af9e73d2b2d49080a4b71d2f27d9000000000000000000000000000000000000000000000000000000000000001ba07465a062aca58b8214d92d827c5f248352c3ebbfe98471e77acbee9cdf1a5dc8fc0efb27a73f73ae91ca35f9d59f05899cef0cf1f227b53b45b777819fd59f02d8320515695d9f9d733311cf3edfc6388bd6f2ec7621104c5936c8a0cdf282000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001be00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cc0d70e2000000000000000000000000000000000000000000000000002386f2cc0dd72f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000082b9100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775954526b4e6a51775a69316d4d6d4e6a4c54566a4e7a5974595459774e43316c5a6d4d774d7a4e6b597a67334d6d496966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000002b616914ada8484ab9d70398dbe86b029b1a9a390000000000000000000000000000000000000000000000000000000000006633000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcd7831b818d9d58963b46e173d5da4062a628897bc5800078ef00cbdd8633cd8",
      "signature": {
        "s": "0x684f234940ac487b9bd413074f0e97cc04a8af9e73d2b2d49080a4b71d2f27d9",
        "r": "0x4c2b8aa005d6c189d3adf950cf08428c829bf82083901e38c544a1e1958fa795",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa07465a062aca58b8214d92d827c5f248352c3ebbfe98471e77acbee9cdf1a5d",
      "signature": {
        "s": "0x02d8320515695d9f9d733311cf3edfc6388bd6f2ec7621104c5936c8a0cdf282",
        "r": "0xc8fc0efb27a73f73ae91ca35f9d59f05899cef0cf1f227b53b45b777819fd59f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "26163",
    "total": "26163"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26163",
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
            "amount": "535441"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "26"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYTRkNjQwZi1mMmNjLTVjNzYtYTYwNC1lZmMwMzNkYzg3MmIifQ==",
    "nonce": 446,
    "balances": {
      "current": "10000001548513506",
      "previous": "10000001548539695"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2b616914ada8484ab9d70398dbe86b029b1a9a39",
    "nonce": 9,
    "balances": {
      "current": "26163",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:06.473Z",
  "updated": "2020-05-22T08:02:06.553Z",
  "id": "5ec786feb0c6090011d5a960"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000066330000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `26163`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``