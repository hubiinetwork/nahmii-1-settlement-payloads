# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7614265a0b4C62Bd84db6Ad9a4451d33c4bda8dc`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000ff00000000000000000000000000000000000000000000000000000000000000ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000ff00000000000000000000000000000000000000000000000000000000000000ff32c4662828997b2f13e9ffa40f613965c064dd900f2a4f21c002dbba3e6fec3270de15a9b1987ccbb1aad3e1b10bc5dfb52e803464e6fbb627f2e8b7de8d3ed74e5be4bf2d0f4e1ec06af8ee6304887684b47ba246986df26c3c05db4eef4686000000000000000000000000000000000000000000000000000000000000001b6a44d5b74f8c6f7ec54ff1d6a83d20cd196eb5fe80c0ee1fa110a9b9a1940914bf8c68699cf1e7e8c1ec26db9d942decf09a4b06ecbccf33149a97e8865996a27226e74d8ae84211fb0236c336fe14377248d7e31a05f2c9e2aaaad3b4e31c73000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015c200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d4ccb7ccf0b000000000000000000000000000000000000000000000000002e1d4ccb7cd00b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c2240916000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f47466c4e5759334e4330334e54466b4c54566c5a5463744f445934597931684e57517a596a4e6d4e574a6d4d44596966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000007614265a0b4c62bd84db6ad9a4451d33c4bda8dc00000000000000000000000000000000000000000000000000000000000000ff000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x32c4662828997b2f13e9ffa40f613965c064dd900f2a4f21c002dbba3e6fec32",
      "signature": {
        "s": "0x4e5be4bf2d0f4e1ec06af8ee6304887684b47ba246986df26c3c05db4eef4686",
        "r": "0x70de15a9b1987ccbb1aad3e1b10bc5dfb52e803464e6fbb627f2e8b7de8d3ed7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6a44d5b74f8c6f7ec54ff1d6a83d20cd196eb5fe80c0ee1fa110a9b9a1940914",
      "signature": {
        "s": "0x7226e74d8ae84211fb0236c336fe14377248d7e31a05f2c9e2aaaad3b4e31c73",
        "r": "0xbf8c68699cf1e7e8c1ec26db9d942decf09a4b06ecbccf33149a97e8865996a2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "255",
    "total": "255"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "255",
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
            "amount": "37616879894"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OGFlNWY3NC03NTFkLTVlZTctODY4Yy1hNWQzYjNmNWJmMDYifQ==",
    "nonce": 5570,
    "balances": {
      "current": "12980064597364491",
      "previous": "12980064597364747"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7614265a0b4c62bd84db6ad9a4451d33c4bda8dc",
    "nonce": 21,
    "balances": {
      "current": "255",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:42:10.028Z",
  "updated": "2020-05-22T08:42:10.094Z",
  "id": "5ec79062e5756b00111b8691"
}
```
* *stageAmount*: `255`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000ff00000000000000000000000000000000000000000000000000000000000000ff32c4662828997b2f13e9ffa40f613965c064dd900f2a4f21c002dbba3e6fec3270de15a9b1987ccbb1aad3e1b10bc5dfb52e803464e6fbb627f2e8b7de8d3ed74e5be4bf2d0f4e1ec06af8ee6304887684b47ba246986df26c3c05db4eef4686000000000000000000000000000000000000000000000000000000000000001b6a44d5b74f8c6f7ec54ff1d6a83d20cd196eb5fe80c0ee1fa110a9b9a1940914bf8c68699cf1e7e8c1ec26db9d942decf09a4b06ecbccf33149a97e8865996a27226e74d8ae84211fb0236c336fe14377248d7e31a05f2c9e2aaaad3b4e31c73000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015c200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d4ccb7ccf0b000000000000000000000000000000000000000000000000002e1d4ccb7cd00b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c2240916000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f47466c4e5759334e4330334e54466b4c54566c5a5463744f445934597931684e57517a596a4e6d4e574a6d4d44596966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000007614265a0b4c62bd84db6ad9a4451d33c4bda8dc00000000000000000000000000000000000000000000000000000000000000ff000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x32c4662828997b2f13e9ffa40f613965c064dd900f2a4f21c002dbba3e6fec32",
      "signature": {
        "s": "0x4e5be4bf2d0f4e1ec06af8ee6304887684b47ba246986df26c3c05db4eef4686",
        "r": "0x70de15a9b1987ccbb1aad3e1b10bc5dfb52e803464e6fbb627f2e8b7de8d3ed7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6a44d5b74f8c6f7ec54ff1d6a83d20cd196eb5fe80c0ee1fa110a9b9a1940914",
      "signature": {
        "s": "0x7226e74d8ae84211fb0236c336fe14377248d7e31a05f2c9e2aaaad3b4e31c73",
        "r": "0xbf8c68699cf1e7e8c1ec26db9d942decf09a4b06ecbccf33149a97e8865996a2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "255",
    "total": "255"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "255",
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
            "amount": "37616879894"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OGFlNWY3NC03NTFkLTVlZTctODY4Yy1hNWQzYjNmNWJmMDYifQ==",
    "nonce": 5570,
    "balances": {
      "current": "12980064597364491",
      "previous": "12980064597364747"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7614265a0b4c62bd84db6ad9a4451d33c4bda8dc",
    "nonce": 21,
    "balances": {
      "current": "255",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:42:10.028Z",
  "updated": "2020-05-22T08:42:10.094Z",
  "id": "5ec79062e5756b00111b8691"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `255`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`