# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbeAc85d604db81715e690d919C1abe953f8554bD`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000b700000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000b700000000000000000000000000000000000000000000000000000000000000b7d2a82ec4570ba8e62cb9a240740c7ab28dfbdc9a7f9570ab5f3c135879a8ec994b2d12fb594e80033e6d1cffa2a9acb2ab38a08060a90822e8e9b589a6a3f8007073c1bafa39ff5b5299ee27808195db309d3959f0cfb2e232c09bc2b866b84b000000000000000000000000000000000000000000000000000000000000001b373d94ac02fb124d4a3689af29c9b0b7ebc48f8687d8216aba16511df388d428cb18034de8fd679e9f8133b27f0e607bccc2440b3bd3b3012188515cb4e70e4c24c9e4903776a291b47c6a8f93a2a3fc8f71b83936f96ed081eb1bbf818455c8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000071e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c42f8493000000000000000000000000000000000000000000000000002386f2c42f854b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2ced00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f475a69596d59304d793079597a457a4c5455774d6d49744f574d794e53307a5a54566d4e325a6b597a5a6d4d54556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000beac85d604db81715e690d919c1abe953f8554bd00000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd2a82ec4570ba8e62cb9a240740c7ab28dfbdc9a7f9570ab5f3c135879a8ec99",
      "signature": {
        "s": "0x7073c1bafa39ff5b5299ee27808195db309d3959f0cfb2e232c09bc2b866b84b",
        "r": "0x4b2d12fb594e80033e6d1cffa2a9acb2ab38a08060a90822e8e9b589a6a3f800",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x373d94ac02fb124d4a3689af29c9b0b7ebc48f8687d8216aba16511df388d428",
      "signature": {
        "s": "0x24c9e4903776a291b47c6a8f93a2a3fc8f71b83936f96ed081eb1bbf818455c8",
        "r": "0xcb18034de8fd679e9f8133b27f0e607bccc2440b3bd3b3012188515cb4e70e4c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "183",
    "total": "183"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "183",
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
            "amount": "666861"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhOGZiYmY0My0yYzEzLTUwMmItOWMyNS0zZTVmN2ZkYzZmMTUifQ==",
    "nonce": 1822,
    "balances": {
      "current": "10000001416529043",
      "previous": "10000001416529227"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbeac85d604db81715e690d919c1abe953f8554bd",
    "nonce": 20,
    "balances": {
      "current": "183",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:21.037Z",
  "updated": "2020-05-22T08:12:21.100Z",
  "id": "5ec78965005df800101bc486"
}
```
* *stageAmount*: `183`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000b700000000000000000000000000000000000000000000000000000000000000b7d2a82ec4570ba8e62cb9a240740c7ab28dfbdc9a7f9570ab5f3c135879a8ec994b2d12fb594e80033e6d1cffa2a9acb2ab38a08060a90822e8e9b589a6a3f8007073c1bafa39ff5b5299ee27808195db309d3959f0cfb2e232c09bc2b866b84b000000000000000000000000000000000000000000000000000000000000001b373d94ac02fb124d4a3689af29c9b0b7ebc48f8687d8216aba16511df388d428cb18034de8fd679e9f8133b27f0e607bccc2440b3bd3b3012188515cb4e70e4c24c9e4903776a291b47c6a8f93a2a3fc8f71b83936f96ed081eb1bbf818455c8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000071e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c42f8493000000000000000000000000000000000000000000000000002386f2c42f854b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2ced00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f475a69596d59304d793079597a457a4c5455774d6d49744f574d794e53307a5a54566d4e325a6b597a5a6d4d54556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000beac85d604db81715e690d919c1abe953f8554bd00000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd2a82ec4570ba8e62cb9a240740c7ab28dfbdc9a7f9570ab5f3c135879a8ec99",
      "signature": {
        "s": "0x7073c1bafa39ff5b5299ee27808195db309d3959f0cfb2e232c09bc2b866b84b",
        "r": "0x4b2d12fb594e80033e6d1cffa2a9acb2ab38a08060a90822e8e9b589a6a3f800",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x373d94ac02fb124d4a3689af29c9b0b7ebc48f8687d8216aba16511df388d428",
      "signature": {
        "s": "0x24c9e4903776a291b47c6a8f93a2a3fc8f71b83936f96ed081eb1bbf818455c8",
        "r": "0xcb18034de8fd679e9f8133b27f0e607bccc2440b3bd3b3012188515cb4e70e4c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "183",
    "total": "183"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "183",
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
            "amount": "666861"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhOGZiYmY0My0yYzEzLTUwMmItOWMyNS0zZTVmN2ZkYzZmMTUifQ==",
    "nonce": 1822,
    "balances": {
      "current": "10000001416529043",
      "previous": "10000001416529227"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbeac85d604db81715e690d919c1abe953f8554bd",
    "nonce": 20,
    "balances": {
      "current": "183",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:21.037Z",
  "updated": "2020-05-22T08:12:21.100Z",
  "id": "5ec78965005df800101bc486"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000b70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `183`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``