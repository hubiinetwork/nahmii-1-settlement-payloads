# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x00953F52B3C894686343998a99A0C944Df35Bd3e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000008f78a470000000000000000000000000000000000000000000000000000000008f78a47000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000008f78a470000000000000000000000000000000000000000000000000000000008f78a4763e9680e152e99e565b32a5001792b49015c37e1039c9620430cc30d4dff3acd1866f84d43685419a19e8090eaa1b938d11552b087db2cdf8d53dd637b2d43af2b8ea8db8f409848e28f697a85fa485de0efdf37d2a33867522a474d3f4b9104000000000000000000000000000000000000000000000000000000000000001cd257a302a3f25fb9501635f9e9feb94810c9ad2a0015168f0f100e4799eabbbb1fbc1b86f0eedf588f055e77e8d58144c2b42d31792a172d02b8dad5fc0e96746a129b91122b6865adbfc9b29b1d76e6082a58a92dd9174747aa40cc6f096b58000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56860000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000184900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad5a19371e4000000000000000000000000000000000000000000000000002e1ad5aa8d47d300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000024ba8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009638ea765000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a5a6a4f545577595330324f444d7a4c54566b597a63744f44426a596931684f544e695a574a694e6d55784e6d496966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000000953f52b3c894686343998a99a0c944df35bd3e0000000000000000000000000000000000000000000000000000000008f78a47000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x63e9680e152e99e565b32a5001792b49015c37e1039c9620430cc30d4dff3acd",
      "signature": {
        "s": "0x2b8ea8db8f409848e28f697a85fa485de0efdf37d2a33867522a474d3f4b9104",
        "r": "0x1866f84d43685419a19e8090eaa1b938d11552b087db2cdf8d53dd637b2d43af",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd257a302a3f25fb9501635f9e9feb94810c9ad2a0015168f0f100e4799eabbbb",
      "signature": {
        "s": "0x6a129b91122b6865adbfc9b29b1d76e6082a58a92dd9174747aa40cc6f096b58",
        "r": "0x1fbc1b86f0eedf588f055e77e8d58144c2b42d31792a172d02b8dad5fc0e9674",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "150440519",
    "total": "150440519"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "150440519",
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
            "amount": "40324999013"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "150440"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2YzZjOTUwYS02ODMzLTVkYzctODBjYi1hOTNiZWJiNmUxNmIifQ==",
    "nonce": 6217,
    "balances": {
      "current": "12977353769841124",
      "previous": "12977353920432083"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x00953f52b3c894686343998a99a0c944df35bd3e",
    "nonce": 22,
    "balances": {
      "current": "150440519",
      "previous": "0"
    }
  },
  "blockNumber": "10114694",
  "created": "2020-05-22T08:47:27.370Z",
  "updated": "2020-05-22T08:47:27.441Z",
  "id": "5ec7919fb0c6090011d5b0e0"
}
```
* *stageAmount*: `150440519`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000008f78a47000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000008f78a470000000000000000000000000000000000000000000000000000000008f78a4763e9680e152e99e565b32a5001792b49015c37e1039c9620430cc30d4dff3acd1866f84d43685419a19e8090eaa1b938d11552b087db2cdf8d53dd637b2d43af2b8ea8db8f409848e28f697a85fa485de0efdf37d2a33867522a474d3f4b9104000000000000000000000000000000000000000000000000000000000000001cd257a302a3f25fb9501635f9e9feb94810c9ad2a0015168f0f100e4799eabbbb1fbc1b86f0eedf588f055e77e8d58144c2b42d31792a172d02b8dad5fc0e96746a129b91122b6865adbfc9b29b1d76e6082a58a92dd9174747aa40cc6f096b58000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56860000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000184900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad5a19371e4000000000000000000000000000000000000000000000000002e1ad5aa8d47d300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000024ba8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009638ea765000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a5a6a4f545577595330324f444d7a4c54566b597a63744f44426a596931684f544e695a574a694e6d55784e6d496966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000000953f52b3c894686343998a99a0c944df35bd3e0000000000000000000000000000000000000000000000000000000008f78a47000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x63e9680e152e99e565b32a5001792b49015c37e1039c9620430cc30d4dff3acd",
      "signature": {
        "s": "0x2b8ea8db8f409848e28f697a85fa485de0efdf37d2a33867522a474d3f4b9104",
        "r": "0x1866f84d43685419a19e8090eaa1b938d11552b087db2cdf8d53dd637b2d43af",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd257a302a3f25fb9501635f9e9feb94810c9ad2a0015168f0f100e4799eabbbb",
      "signature": {
        "s": "0x6a129b91122b6865adbfc9b29b1d76e6082a58a92dd9174747aa40cc6f096b58",
        "r": "0x1fbc1b86f0eedf588f055e77e8d58144c2b42d31792a172d02b8dad5fc0e9674",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "150440519",
    "total": "150440519"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "150440519",
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
            "amount": "40324999013"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "150440"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2YzZjOTUwYS02ODMzLTVkYzctODBjYi1hOTNiZWJiNmUxNmIifQ==",
    "nonce": 6217,
    "balances": {
      "current": "12977353769841124",
      "previous": "12977353920432083"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x00953f52b3c894686343998a99a0c944df35bd3e",
    "nonce": 22,
    "balances": {
      "current": "150440519",
      "previous": "0"
    }
  },
  "blockNumber": "10114694",
  "created": "2020-05-22T08:47:27.370Z",
  "updated": "2020-05-22T08:47:27.441Z",
  "id": "5ec7919fb0c6090011d5b0e0"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000008f78a47000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `150440519`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`