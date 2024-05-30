# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7d35A7400EE4587481a776900F37020D723dD3f0`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000024ca00000000000000000000000000000000000000000000000000000000000024ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000024ca00000000000000000000000000000000000000000000000000000000000024ca0f8b99466759cc17d97f0cbdc41d6f2aaee028009dc5013daec35261350225bb3ae6c9033b68a2ae18090fa5711f503ec941278482f1cad3a0f00f81b1018fb6458b90be7dc617ff494caf4bdbc27cc1729c1865489d6f7d91d8c07325067477000000000000000000000000000000000000000000000000000000000000001cc1d053aebb09548705f42f9397e73f5494a62db1c7a3e185b27d6660983b682605db35cba09cb6e11a68e57a6ea33d3d7dc9bb0969bec60724750b094ff903eb5389f1dece190e3fa7879942188e768f51a896f1ced206045b24c5bab3626743000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000032e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae35a23000000000000000000000000000000000000000000000000002386f2cae37ef600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008773a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a6a45344f54526b4d43316b4d47526b4c54566b4e6a41744f474531596930784e474a6c4f4745794d324e6d5a574d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007d35a7400ee4587481a776900f37020d723dd3f000000000000000000000000000000000000000000000000000000000000024ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f8b99466759cc17d97f0cbdc41d6f2aaee028009dc5013daec35261350225bb",
      "signature": {
        "s": "0x458b90be7dc617ff494caf4bdbc27cc1729c1865489d6f7d91d8c07325067477",
        "r": "0x3ae6c9033b68a2ae18090fa5711f503ec941278482f1cad3a0f00f81b1018fb6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc1d053aebb09548705f42f9397e73f5494a62db1c7a3e185b27d6660983b6826",
      "signature": {
        "s": "0x5389f1dece190e3fa7879942188e768f51a896f1ced206045b24c5bab3626743",
        "r": "0x05db35cba09cb6e11a68e57a6ea33d3d7dc9bb0969bec60724750b094ff903eb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9418",
    "total": "9418"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9418",
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
            "amount": "554810"
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
    "data": "eyJyZWYiOiI0ZjE4OTRkMC1kMGRkLTVkNjAtOGE1Yi0xNGJlOGEyM2NmZWMifQ==",
    "nonce": 814,
    "balances": {
      "current": "10000001528977955",
      "previous": "10000001528987382"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7d35a7400ee4587481a776900f37020d723dd3f0",
    "nonce": 20,
    "balances": {
      "current": "9418",
      "previous": "0"
    }
  },
  "blockNumber": "10114511",
  "created": "2020-05-22T08:04:52.329Z",
  "updated": "2020-05-22T08:04:52.398Z",
  "id": "5ec787a4e5756b00111b8079"
}
```
* *stageAmount*: `9418`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000024ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000024ca00000000000000000000000000000000000000000000000000000000000024ca0f8b99466759cc17d97f0cbdc41d6f2aaee028009dc5013daec35261350225bb3ae6c9033b68a2ae18090fa5711f503ec941278482f1cad3a0f00f81b1018fb6458b90be7dc617ff494caf4bdbc27cc1729c1865489d6f7d91d8c07325067477000000000000000000000000000000000000000000000000000000000000001cc1d053aebb09548705f42f9397e73f5494a62db1c7a3e185b27d6660983b682605db35cba09cb6e11a68e57a6ea33d3d7dc9bb0969bec60724750b094ff903eb5389f1dece190e3fa7879942188e768f51a896f1ced206045b24c5bab3626743000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000032e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae35a23000000000000000000000000000000000000000000000000002386f2cae37ef600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008773a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a6a45344f54526b4d43316b4d47526b4c54566b4e6a41744f474531596930784e474a6c4f4745794d324e6d5a574d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007d35a7400ee4587481a776900f37020d723dd3f000000000000000000000000000000000000000000000000000000000000024ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f8b99466759cc17d97f0cbdc41d6f2aaee028009dc5013daec35261350225bb",
      "signature": {
        "s": "0x458b90be7dc617ff494caf4bdbc27cc1729c1865489d6f7d91d8c07325067477",
        "r": "0x3ae6c9033b68a2ae18090fa5711f503ec941278482f1cad3a0f00f81b1018fb6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc1d053aebb09548705f42f9397e73f5494a62db1c7a3e185b27d6660983b6826",
      "signature": {
        "s": "0x5389f1dece190e3fa7879942188e768f51a896f1ced206045b24c5bab3626743",
        "r": "0x05db35cba09cb6e11a68e57a6ea33d3d7dc9bb0969bec60724750b094ff903eb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9418",
    "total": "9418"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9418",
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
            "amount": "554810"
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
    "data": "eyJyZWYiOiI0ZjE4OTRkMC1kMGRkLTVkNjAtOGE1Yi0xNGJlOGEyM2NmZWMifQ==",
    "nonce": 814,
    "balances": {
      "current": "10000001528977955",
      "previous": "10000001528987382"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7d35a7400ee4587481a776900f37020d723dd3f0",
    "nonce": 20,
    "balances": {
      "current": "9418",
      "previous": "0"
    }
  },
  "blockNumber": "10114511",
  "created": "2020-05-22T08:04:52.329Z",
  "updated": "2020-05-22T08:04:52.398Z",
  "id": "5ec787a4e5756b00111b8079"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000024ca0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9418`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``