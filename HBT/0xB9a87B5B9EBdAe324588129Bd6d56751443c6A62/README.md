# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB9a87B5B9EBdAe324588129Bd6d56751443c6A62`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000009dabfe18000000000000000000000000000000000000000000000000000000009dabfe18000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009dabfe18000000000000000000000000000000000000000000000000000000009dabfe189d4ff04d712eeb7ca3eeb23f81842fce51bc968d439069292b8c8a7d654c6347366e8cf5b517070eff3fbd3e6dee3c9360cfe26812f2cf642b731dd00a5e448f1add3a6f25719ba7d419ff2b9184f641cb1023bb8c97066c2842ac29f4ff9363000000000000000000000000000000000000000000000000000000000000001b514a461ba3d7497e466e885d899e42ceb3afce42a5960c475f2e70f056bed2464f973d583c7bcafd48334d64877348a5b6224b4c61e2e3f1f1b622faaba43d21466d348fffd61df5a37ea98e25bbc82860ffb6e0a04a36030c257bfd8bc19951000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018b100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a0e22b1823f000000000000000000000000000000000000000000000000002e1a0ec085dd8500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000285d2e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099693bcf7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e47466c595449785953316a4e3256694c545579596a67744f474579595330314d7a67304e4449774d4451304f47516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b9a87b5b9ebdae324588129bd6d56751443c6a62000000000000000000000000000000000000000000000000000000009dabfe18000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9d4ff04d712eeb7ca3eeb23f81842fce51bc968d439069292b8c8a7d654c6347",
      "signature": {
        "s": "0x1add3a6f25719ba7d419ff2b9184f641cb1023bb8c97066c2842ac29f4ff9363",
        "r": "0x366e8cf5b517070eff3fbd3e6dee3c9360cfe26812f2cf642b731dd00a5e448f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x514a461ba3d7497e466e885d899e42ceb3afce42a5960c475f2e70f056bed246",
      "signature": {
        "s": "0x466d348fffd61df5a37ea98e25bbc82860ffb6e0a04a36030c257bfd8bc19951",
        "r": "0x4f973d583c7bcafd48334d64877348a5b6224b4c61e2e3f1f1b622faaba43d21",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2645294616",
    "total": "2645294616"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2645294616",
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
            "amount": "41180970231"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2645294"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NGFlYTIxYS1jN2ViLTUyYjgtOGEyYS01Mzg0NDIwMDQ0OGQifQ==",
    "nonce": 6321,
    "balances": {
      "current": "12976496942613055",
      "previous": "12976499590552965"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb9a87b5b9ebdae324588129bd6d56751443c6a62",
    "nonce": 22,
    "balances": {
      "current": "2645294616",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:12.038Z",
  "updated": "2020-05-22T08:48:12.190Z",
  "id": "5ec791cc005df800101bca78"
}
```
* *stageAmount*: `2645294616`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000009dabfe18000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009dabfe18000000000000000000000000000000000000000000000000000000009dabfe189d4ff04d712eeb7ca3eeb23f81842fce51bc968d439069292b8c8a7d654c6347366e8cf5b517070eff3fbd3e6dee3c9360cfe26812f2cf642b731dd00a5e448f1add3a6f25719ba7d419ff2b9184f641cb1023bb8c97066c2842ac29f4ff9363000000000000000000000000000000000000000000000000000000000000001b514a461ba3d7497e466e885d899e42ceb3afce42a5960c475f2e70f056bed2464f973d583c7bcafd48334d64877348a5b6224b4c61e2e3f1f1b622faaba43d21466d348fffd61df5a37ea98e25bbc82860ffb6e0a04a36030c257bfd8bc19951000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018b100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a0e22b1823f000000000000000000000000000000000000000000000000002e1a0ec085dd8500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000285d2e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099693bcf7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e47466c595449785953316a4e3256694c545579596a67744f474579595330314d7a67304e4449774d4451304f47516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b9a87b5b9ebdae324588129bd6d56751443c6a62000000000000000000000000000000000000000000000000000000009dabfe18000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9d4ff04d712eeb7ca3eeb23f81842fce51bc968d439069292b8c8a7d654c6347",
      "signature": {
        "s": "0x1add3a6f25719ba7d419ff2b9184f641cb1023bb8c97066c2842ac29f4ff9363",
        "r": "0x366e8cf5b517070eff3fbd3e6dee3c9360cfe26812f2cf642b731dd00a5e448f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x514a461ba3d7497e466e885d899e42ceb3afce42a5960c475f2e70f056bed246",
      "signature": {
        "s": "0x466d348fffd61df5a37ea98e25bbc82860ffb6e0a04a36030c257bfd8bc19951",
        "r": "0x4f973d583c7bcafd48334d64877348a5b6224b4c61e2e3f1f1b622faaba43d21",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2645294616",
    "total": "2645294616"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2645294616",
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
            "amount": "41180970231"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2645294"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NGFlYTIxYS1jN2ViLTUyYjgtOGEyYS01Mzg0NDIwMDQ0OGQifQ==",
    "nonce": 6321,
    "balances": {
      "current": "12976496942613055",
      "previous": "12976499590552965"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb9a87b5b9ebdae324588129bd6d56751443c6a62",
    "nonce": 22,
    "balances": {
      "current": "2645294616",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:12.038Z",
  "updated": "2020-05-22T08:48:12.190Z",
  "id": "5ec791cc005df800101bca78"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000009dabfe18000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2645294616`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`