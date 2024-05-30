# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x739066Ed2D1718FD100CEC4d9F347382Ec6440DC`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000018a294feb000000000000000000000000000000000000000000000000000000018a294feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018a294feb000000000000000000000000000000000000000000000000000000018a294febafd2a7726c4519fd3baf0c5509da382cb1411c6bb08ea7f83d18a448d5e7f427a6473a159a413fcd08d3e9442d8c92f565ab5a34775eb97091244d79d590ec8a02b5cdc266f7c40db4007524b2712b3b6e5432cd8422144e92eba2f21a2f21a1000000000000000000000000000000000000000000000000000000000000001c1576d4cc594ee7e7fd8f179af44a2325efc1a4ac216e15579617c771eefb9dafb947296619f9b4eebcf61a34d20f5280bb1f7c628623086528e26b90f929f7de57b285078128223211b34afdac52b3030dc701469ee3078cf52500a2a93dff01000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c9d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1336c3382ff4000000000000000000000000000000000000000000000000002e13384dc667a100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064e7c2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b567b0ba5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f5463784f5449304d7930304d5749314c5455304d444974595751304d7930334d574a6a5957526b4d5467355a44636966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000739066ed2d1718fd100cec4d9f347382ec6440dc000000000000000000000000000000000000000000000000000000018a294feb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xafd2a7726c4519fd3baf0c5509da382cb1411c6bb08ea7f83d18a448d5e7f427",
      "signature": {
        "s": "0x02b5cdc266f7c40db4007524b2712b3b6e5432cd8422144e92eba2f21a2f21a1",
        "r": "0xa6473a159a413fcd08d3e9442d8c92f565ab5a34775eb97091244d79d590ec8a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1576d4cc594ee7e7fd8f179af44a2325efc1a4ac216e15579617c771eefb9daf",
      "signature": {
        "s": "0x57b285078128223211b34afdac52b3030dc701469ee3078cf52500a2a93dff01",
        "r": "0xb947296619f9b4eebcf61a34d20f5280bb1f7c628623086528e26b90f929f7de",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6612930539",
    "total": "6612930539"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6612930539",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "48695544741"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6612930"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhOTcxOTI0My00MWI1LTU0MDItYWQ0My03MWJjYWRkMTg5ZDcifQ==",
    "nonce": 7325,
    "balances": {
      "current": "12968974853091316",
      "previous": "12968981472634785"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x739066ed2d1718fd100cec4d9f347382ec6440dc",
    "nonce": 22,
    "balances": {
      "current": "6612930539",
      "previous": "0"
    }
  },
  "blockNumber": "10114736",
  "created": "2020-05-22T08:55:55.629Z",
  "updated": "2020-05-22T08:55:55.695Z",
  "id": "5ec7939b005df800101bcbda"
}
```
* *stageAmount*: `6612930539`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000018a294feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018a294feb000000000000000000000000000000000000000000000000000000018a294febafd2a7726c4519fd3baf0c5509da382cb1411c6bb08ea7f83d18a448d5e7f427a6473a159a413fcd08d3e9442d8c92f565ab5a34775eb97091244d79d590ec8a02b5cdc266f7c40db4007524b2712b3b6e5432cd8422144e92eba2f21a2f21a1000000000000000000000000000000000000000000000000000000000000001c1576d4cc594ee7e7fd8f179af44a2325efc1a4ac216e15579617c771eefb9dafb947296619f9b4eebcf61a34d20f5280bb1f7c628623086528e26b90f929f7de57b285078128223211b34afdac52b3030dc701469ee3078cf52500a2a93dff01000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c9d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1336c3382ff4000000000000000000000000000000000000000000000000002e13384dc667a100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064e7c2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b567b0ba5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f5463784f5449304d7930304d5749314c5455304d444974595751304d7930334d574a6a5957526b4d5467355a44636966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000739066ed2d1718fd100cec4d9f347382ec6440dc000000000000000000000000000000000000000000000000000000018a294feb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xafd2a7726c4519fd3baf0c5509da382cb1411c6bb08ea7f83d18a448d5e7f427",
      "signature": {
        "s": "0x02b5cdc266f7c40db4007524b2712b3b6e5432cd8422144e92eba2f21a2f21a1",
        "r": "0xa6473a159a413fcd08d3e9442d8c92f565ab5a34775eb97091244d79d590ec8a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1576d4cc594ee7e7fd8f179af44a2325efc1a4ac216e15579617c771eefb9daf",
      "signature": {
        "s": "0x57b285078128223211b34afdac52b3030dc701469ee3078cf52500a2a93dff01",
        "r": "0xb947296619f9b4eebcf61a34d20f5280bb1f7c628623086528e26b90f929f7de",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6612930539",
    "total": "6612930539"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6612930539",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "48695544741"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6612930"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhOTcxOTI0My00MWI1LTU0MDItYWQ0My03MWJjYWRkMTg5ZDcifQ==",
    "nonce": 7325,
    "balances": {
      "current": "12968974853091316",
      "previous": "12968981472634785"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x739066ed2d1718fd100cec4d9f347382ec6440dc",
    "nonce": 22,
    "balances": {
      "current": "6612930539",
      "previous": "0"
    }
  },
  "blockNumber": "10114736",
  "created": "2020-05-22T08:55:55.629Z",
  "updated": "2020-05-22T08:55:55.695Z",
  "id": "5ec7939b005df800101bcbda"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000018a294feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6612930539`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`