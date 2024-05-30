# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdf6C50e9b5af51120104A627159b5a00995eaf3C`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000007280000000000000000000000000000000000000000000000000000000000000728000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000007280000000000000000000000000000000000000000000000000000000000000728f2657a30c6a47bfb28c543cf1e24882078082e7766813793d0afdcdf6ba3666df3507d1e9673758ad5a8b2f5efb0390ec0ff2561e8b08e936a4552af069bd70666b65331339760c8d3332f694446009d50b5270528e6d093ba4fee58d52bc9e9000000000000000000000000000000000000000000000000000000000000001bb3259755471c33ba20cca3396c85b7e1a6675bc7fd314d5266bdb77a5c9a016741ef69171c081ca8e6d607c45c77af06d88c877f38cf49fd220e58940471ae1f1f0e94bf97a6b178ed6fc7407e9c7ccf49e4e08ceed4e4c58500c4d8a20e9340000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55cc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002d800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf010a0000000000000000000000000000000000000000000000000002386f2caf017c900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008742300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a54597a4d574a6c5a43316c4d7a4d334c5455314f57557459574a6a59693035596a646b4f4751795a6d4d334e6a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000df6c50e9b5af51120104a627159b5a00995eaf3c0000000000000000000000000000000000000000000000000000000000000728000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf2657a30c6a47bfb28c543cf1e24882078082e7766813793d0afdcdf6ba3666d",
      "signature": {
        "s": "0x66b65331339760c8d3332f694446009d50b5270528e6d093ba4fee58d52bc9e9",
        "r": "0xf3507d1e9673758ad5a8b2f5efb0390ec0ff2561e8b08e936a4552af069bd706",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb3259755471c33ba20cca3396c85b7e1a6675bc7fd314d5266bdb77a5c9a0167",
      "signature": {
        "s": "0x1f0e94bf97a6b178ed6fc7407e9c7ccf49e4e08ceed4e4c58500c4d8a20e9340",
        "r": "0x41ef69171c081ca8e6d607c45c77af06d88c877f38cf49fd220e58940471ae1f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1832",
    "total": "1832"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1832",
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
            "amount": "554019"
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
    "data": "eyJyZWYiOiJiZTYzMWJlZC1lMzM3LTU1OWUtYWJjYi05YjdkOGQyZmM3NjIifQ==",
    "nonce": 728,
    "balances": {
      "current": "10000001529811104",
      "previous": "10000001529812937"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdf6c50e9b5af51120104a627159b5a00995eaf3c",
    "nonce": 20,
    "balances": {
      "current": "1832",
      "previous": "0"
    }
  },
  "blockNumber": "10114508",
  "created": "2020-05-22T08:04:22.780Z",
  "updated": "2020-05-22T08:04:22.848Z",
  "id": "5ec78786e5756b00111b805f"
}
```
* *stageAmount*: `1832`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000728000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000007280000000000000000000000000000000000000000000000000000000000000728f2657a30c6a47bfb28c543cf1e24882078082e7766813793d0afdcdf6ba3666df3507d1e9673758ad5a8b2f5efb0390ec0ff2561e8b08e936a4552af069bd70666b65331339760c8d3332f694446009d50b5270528e6d093ba4fee58d52bc9e9000000000000000000000000000000000000000000000000000000000000001bb3259755471c33ba20cca3396c85b7e1a6675bc7fd314d5266bdb77a5c9a016741ef69171c081ca8e6d607c45c77af06d88c877f38cf49fd220e58940471ae1f1f0e94bf97a6b178ed6fc7407e9c7ccf49e4e08ceed4e4c58500c4d8a20e9340000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55cc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002d800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf010a0000000000000000000000000000000000000000000000000002386f2caf017c900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008742300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a54597a4d574a6c5a43316c4d7a4d334c5455314f57557459574a6a59693035596a646b4f4751795a6d4d334e6a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000df6c50e9b5af51120104a627159b5a00995eaf3c0000000000000000000000000000000000000000000000000000000000000728000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf2657a30c6a47bfb28c543cf1e24882078082e7766813793d0afdcdf6ba3666d",
      "signature": {
        "s": "0x66b65331339760c8d3332f694446009d50b5270528e6d093ba4fee58d52bc9e9",
        "r": "0xf3507d1e9673758ad5a8b2f5efb0390ec0ff2561e8b08e936a4552af069bd706",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb3259755471c33ba20cca3396c85b7e1a6675bc7fd314d5266bdb77a5c9a0167",
      "signature": {
        "s": "0x1f0e94bf97a6b178ed6fc7407e9c7ccf49e4e08ceed4e4c58500c4d8a20e9340",
        "r": "0x41ef69171c081ca8e6d607c45c77af06d88c877f38cf49fd220e58940471ae1f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1832",
    "total": "1832"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1832",
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
            "amount": "554019"
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
    "data": "eyJyZWYiOiJiZTYzMWJlZC1lMzM3LTU1OWUtYWJjYi05YjdkOGQyZmM3NjIifQ==",
    "nonce": 728,
    "balances": {
      "current": "10000001529811104",
      "previous": "10000001529812937"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdf6c50e9b5af51120104a627159b5a00995eaf3c",
    "nonce": 20,
    "balances": {
      "current": "1832",
      "previous": "0"
    }
  },
  "blockNumber": "10114508",
  "created": "2020-05-22T08:04:22.780Z",
  "updated": "2020-05-22T08:04:22.848Z",
  "id": "5ec78786e5756b00111b805f"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000007280000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1832`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``