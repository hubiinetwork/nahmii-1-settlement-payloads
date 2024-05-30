# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x03390C47a9bFF644C17b7E0608339E3c419180a0`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000764102cb00000000000000000000000000000000000000000000000000000000764102cb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000764102cb00000000000000000000000000000000000000000000000000000000764102cb470100c5c70e3c3885a0f8e71636e9c2356f1b0e1d996fbd3eea0c3ea8884ff4fc549fda3d64f0b27df3dd2e377775f62b28305b624a845d710a407eff6f83a628a41e6cffbee840baa817ff3db77ce0a957a99e3e65f12a960bde821b163aee000000000000000000000000000000000000000000000000000000000000001b2c7aa6a74a1a240d75747e1e835a788c9904cb480812fd3bf2a4d11016c0b59829dec86a93b005f99fd724fa0d942f6548428f3050f8f675555a44f77eee9c675df33c5471d9febf9d6a560c624d0fdf6da198b6c57add68085dd4624c0ee76b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000189e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a97ebf09084000000000000000000000000000000000000000000000000002e1a98624fd93300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e45e4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000097356cee1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d5459774e4749794f533168595467774c54566c4d7a6774595751794d69316a4e4449315a474d784f5452694e6a636966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000003390c47a9bff644c17b7e0608339e3c419180a000000000000000000000000000000000000000000000000000000000764102cb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x470100c5c70e3c3885a0f8e71636e9c2356f1b0e1d996fbd3eea0c3ea8884ff4",
      "signature": {
        "s": "0x28a41e6cffbee840baa817ff3db77ce0a957a99e3e65f12a960bde821b163aee",
        "r": "0xfc549fda3d64f0b27df3dd2e377775f62b28305b624a845d710a407eff6f83a6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2c7aa6a74a1a240d75747e1e835a788c9904cb480812fd3bf2a4d11016c0b598",
      "signature": {
        "s": "0x5df33c5471d9febf9d6a560c624d0fdf6da198b6c57add68085dd4624c0ee76b",
        "r": "0x29dec86a93b005f99fd724fa0d942f6548428f3050f8f675555a44f77eee9c67",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1983972043",
    "total": "1983972043"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1983972043",
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
            "amount": "40589774561"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1983972"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1MTYwNGIyOS1hYTgwLTVlMzgtYWQyMi1jNDI1ZGMxOTRiNjcifQ==",
    "nonce": 6302,
    "balances": {
      "current": "12977088729485444",
      "previous": "12977090715441459"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x03390c47a9bff644c17b7e0608339e3c419180a0",
    "nonce": 22,
    "balances": {
      "current": "1983972043",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:01.512Z",
  "updated": "2020-05-22T08:48:01.586Z",
  "id": "5ec791c1005df800101bca70"
}
```
* *stageAmount*: `1983972043`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000764102cb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000764102cb00000000000000000000000000000000000000000000000000000000764102cb470100c5c70e3c3885a0f8e71636e9c2356f1b0e1d996fbd3eea0c3ea8884ff4fc549fda3d64f0b27df3dd2e377775f62b28305b624a845d710a407eff6f83a628a41e6cffbee840baa817ff3db77ce0a957a99e3e65f12a960bde821b163aee000000000000000000000000000000000000000000000000000000000000001b2c7aa6a74a1a240d75747e1e835a788c9904cb480812fd3bf2a4d11016c0b59829dec86a93b005f99fd724fa0d942f6548428f3050f8f675555a44f77eee9c675df33c5471d9febf9d6a560c624d0fdf6da198b6c57add68085dd4624c0ee76b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000189e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a97ebf09084000000000000000000000000000000000000000000000000002e1a98624fd93300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e45e4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000097356cee1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d5459774e4749794f533168595467774c54566c4d7a6774595751794d69316a4e4449315a474d784f5452694e6a636966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000003390c47a9bff644c17b7e0608339e3c419180a000000000000000000000000000000000000000000000000000000000764102cb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x470100c5c70e3c3885a0f8e71636e9c2356f1b0e1d996fbd3eea0c3ea8884ff4",
      "signature": {
        "s": "0x28a41e6cffbee840baa817ff3db77ce0a957a99e3e65f12a960bde821b163aee",
        "r": "0xfc549fda3d64f0b27df3dd2e377775f62b28305b624a845d710a407eff6f83a6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2c7aa6a74a1a240d75747e1e835a788c9904cb480812fd3bf2a4d11016c0b598",
      "signature": {
        "s": "0x5df33c5471d9febf9d6a560c624d0fdf6da198b6c57add68085dd4624c0ee76b",
        "r": "0x29dec86a93b005f99fd724fa0d942f6548428f3050f8f675555a44f77eee9c67",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1983972043",
    "total": "1983972043"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1983972043",
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
            "amount": "40589774561"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1983972"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1MTYwNGIyOS1hYTgwLTVlMzgtYWQyMi1jNDI1ZGMxOTRiNjcifQ==",
    "nonce": 6302,
    "balances": {
      "current": "12977088729485444",
      "previous": "12977090715441459"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x03390c47a9bff644c17b7e0608339e3c419180a0",
    "nonce": 22,
    "balances": {
      "current": "1983972043",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:01.512Z",
  "updated": "2020-05-22T08:48:01.586Z",
  "id": "5ec791c1005df800101bca70"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000764102cb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1983972043`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`