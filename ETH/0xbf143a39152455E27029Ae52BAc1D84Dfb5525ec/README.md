# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbf143a39152455E27029Ae52BAc1D84Dfb5525ec`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000010e9d3000000000000000000000000000000000000000000000000000000000010e9d30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000010e9d3000000000000000000000000000000000000000000000000000000000010e9d35c1bc498cea9afe07a78de636fe838e32540aa762901fbce7907782e3b450fbd7d9178ed8137680a35bba93cea204aa91ae8d3cf18395560b8c6e7a526f529426b90557fac5a85cd504c023303b87ae02eaf5a3fad403381980760d52cd24009000000000000000000000000000000000000000000000000000000000000001bb947373d8f4f1315234a6636f2690da6acfc2a79cb6c4431934127dfabed49dd5534c3b512a9fab24d630b4141d8165221ac8f384dd19c87c64bf7de981366a60a4b71ee3562f8f0224c4dde0ec6636f2b24f14a14726584f3a9f5692c395e2a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001a900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cc5c2f89000000000000000000000000000000000000000000000000002386f2cc6d1db000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000045400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008176c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979595441334e7a45314e7930355a5749794c54566d596a4174595746685a6930314d6d51774d324a6b4d7a68695932496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000bf143a39152455e27029ae52bac1d84dfb5525ec000000000000000000000000000000000000000000000000000000000010e9d3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5c1bc498cea9afe07a78de636fe838e32540aa762901fbce7907782e3b450fbd",
      "signature": {
        "s": "0x6b90557fac5a85cd504c023303b87ae02eaf5a3fad403381980760d52cd24009",
        "r": "0x7d9178ed8137680a35bba93cea204aa91ae8d3cf18395560b8c6e7a526f52942",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb947373d8f4f1315234a6636f2690da6acfc2a79cb6c4431934127dfabed49dd",
      "signature": {
        "s": "0x0a4b71ee3562f8f0224c4dde0ec6636f2b24f14a14726584f3a9f5692c395e2a",
        "r": "0x5534c3b512a9fab24d630b4141d8165221ac8f384dd19c87c64bf7de981366a6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1108435",
    "total": "1108435"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1108435",
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
            "amount": "530284"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1108"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYTA3NzE1Ny05ZWIyLTVmYjAtYWFhZi01MmQwM2JkMzhiY2IifQ==",
    "nonce": 425,
    "balances": {
      "current": "10000001553674121",
      "previous": "10000001554783664"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbf143a39152455e27029ae52bac1d84dfb5525ec",
    "nonce": 20,
    "balances": {
      "current": "1108435",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:01:57.336Z",
  "updated": "2020-05-22T08:01:57.404Z",
  "id": "5ec786f5b0c6090011d5a959"
}
```
* *stageAmount*: `1108435`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000010e9d30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000010e9d3000000000000000000000000000000000000000000000000000000000010e9d35c1bc498cea9afe07a78de636fe838e32540aa762901fbce7907782e3b450fbd7d9178ed8137680a35bba93cea204aa91ae8d3cf18395560b8c6e7a526f529426b90557fac5a85cd504c023303b87ae02eaf5a3fad403381980760d52cd24009000000000000000000000000000000000000000000000000000000000000001bb947373d8f4f1315234a6636f2690da6acfc2a79cb6c4431934127dfabed49dd5534c3b512a9fab24d630b4141d8165221ac8f384dd19c87c64bf7de981366a60a4b71ee3562f8f0224c4dde0ec6636f2b24f14a14726584f3a9f5692c395e2a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001a900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cc5c2f89000000000000000000000000000000000000000000000000002386f2cc6d1db000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000045400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008176c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979595441334e7a45314e7930355a5749794c54566d596a4174595746685a6930314d6d51774d324a6b4d7a68695932496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000bf143a39152455e27029ae52bac1d84dfb5525ec000000000000000000000000000000000000000000000000000000000010e9d3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5c1bc498cea9afe07a78de636fe838e32540aa762901fbce7907782e3b450fbd",
      "signature": {
        "s": "0x6b90557fac5a85cd504c023303b87ae02eaf5a3fad403381980760d52cd24009",
        "r": "0x7d9178ed8137680a35bba93cea204aa91ae8d3cf18395560b8c6e7a526f52942",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb947373d8f4f1315234a6636f2690da6acfc2a79cb6c4431934127dfabed49dd",
      "signature": {
        "s": "0x0a4b71ee3562f8f0224c4dde0ec6636f2b24f14a14726584f3a9f5692c395e2a",
        "r": "0x5534c3b512a9fab24d630b4141d8165221ac8f384dd19c87c64bf7de981366a6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1108435",
    "total": "1108435"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1108435",
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
            "amount": "530284"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1108"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYTA3NzE1Ny05ZWIyLTVmYjAtYWFhZi01MmQwM2JkMzhiY2IifQ==",
    "nonce": 425,
    "balances": {
      "current": "10000001553674121",
      "previous": "10000001554783664"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbf143a39152455e27029ae52bac1d84dfb5525ec",
    "nonce": 20,
    "balances": {
      "current": "1108435",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:01:57.336Z",
  "updated": "2020-05-22T08:01:57.404Z",
  "id": "5ec786f5b0c6090011d5a959"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000010e9d30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1108435`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``