# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x910c4BA923B2243dc13e00A066eEfb8ffd905EB0`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000001283f000000000000000000000000000000000000000000000000000000000001283f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001283f000000000000000000000000000000000000000000000000000000000001283f12b050a21c78d33100f701e63ccc43b87ecdc4871e9327db78813891656b17d34bfc34f29f656982839e72a5d28189140083cd1c91298af0f8880a35ce9c49e666051398fe2aa99f237a17bd6205f5bd500e00fb659a953ed1981a15eeb952a3000000000000000000000000000000000000000000000000000000000000001cd6af74025feaf6981e2630bf2b58596f0730c90d26aa1b6a302894e8854e9e1f8f81d6197874458982a73607e659787dafa7235304a1c75bd487b234e7cf7b554fef2b7f53edce830bbd23cfd20f62240b587a3bed19c23e60a855fdca665e2a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5665000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014ed00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e217d4c95b7b7000000000000000000000000000000000000000000000000002e217d4c96e04100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000004b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007afda9ce3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6d49304e446b774e6930304d324e6c4c5455304e5445744f5463324f53316d4e446c6d4e445534597a55775954516966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000910c4ba923b2243dc13e00a066eefb8ffd905eb0000000000000000000000000000000000000000000000000000000000001283f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x12b050a21c78d33100f701e63ccc43b87ecdc4871e9327db78813891656b17d3",
      "signature": {
        "s": "0x66051398fe2aa99f237a17bd6205f5bd500e00fb659a953ed1981a15eeb952a3",
        "r": "0x4bfc34f29f656982839e72a5d28189140083cd1c91298af0f8880a35ce9c49e6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd6af74025feaf6981e2630bf2b58596f0730c90d26aa1b6a302894e8854e9e1f",
      "signature": {
        "s": "0x4fef2b7f53edce830bbd23cfd20f62240b587a3bed19c23e60a855fdca665e2a",
        "r": "0x8f81d6197874458982a73607e659787dafa7235304a1c75bd487b234e7cf7b55",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "75839",
    "total": "75839"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "75839",
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
            "amount": "33015110883"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "75"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZmI0NDkwNi00M2NlLTU0NTEtOTc2OS1mNDlmNDU4YzUwYTQifQ==",
    "nonce": 5357,
    "balances": {
      "current": "12984670968199095",
      "previous": "12984670968275009"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x910c4ba923b2243dc13e00a066eefb8ffd905eb0",
    "nonce": 6,
    "balances": {
      "current": "75839",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:32.926Z",
  "updated": "2020-05-22T08:40:32.996Z",
  "id": "5ec79000b0c6090011d5afb4"
}
```
* *stageAmount*: `75839`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000001283f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001283f000000000000000000000000000000000000000000000000000000000001283f12b050a21c78d33100f701e63ccc43b87ecdc4871e9327db78813891656b17d34bfc34f29f656982839e72a5d28189140083cd1c91298af0f8880a35ce9c49e666051398fe2aa99f237a17bd6205f5bd500e00fb659a953ed1981a15eeb952a3000000000000000000000000000000000000000000000000000000000000001cd6af74025feaf6981e2630bf2b58596f0730c90d26aa1b6a302894e8854e9e1f8f81d6197874458982a73607e659787dafa7235304a1c75bd487b234e7cf7b554fef2b7f53edce830bbd23cfd20f62240b587a3bed19c23e60a855fdca665e2a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5665000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014ed00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e217d4c95b7b7000000000000000000000000000000000000000000000000002e217d4c96e04100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000004b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007afda9ce3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6d49304e446b774e6930304d324e6c4c5455304e5445744f5463324f53316d4e446c6d4e445534597a55775954516966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000910c4ba923b2243dc13e00a066eefb8ffd905eb0000000000000000000000000000000000000000000000000000000000001283f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x12b050a21c78d33100f701e63ccc43b87ecdc4871e9327db78813891656b17d3",
      "signature": {
        "s": "0x66051398fe2aa99f237a17bd6205f5bd500e00fb659a953ed1981a15eeb952a3",
        "r": "0x4bfc34f29f656982839e72a5d28189140083cd1c91298af0f8880a35ce9c49e6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd6af74025feaf6981e2630bf2b58596f0730c90d26aa1b6a302894e8854e9e1f",
      "signature": {
        "s": "0x4fef2b7f53edce830bbd23cfd20f62240b587a3bed19c23e60a855fdca665e2a",
        "r": "0x8f81d6197874458982a73607e659787dafa7235304a1c75bd487b234e7cf7b55",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "75839",
    "total": "75839"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "75839",
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
            "amount": "33015110883"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "75"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjZmI0NDkwNi00M2NlLTU0NTEtOTc2OS1mNDlmNDU4YzUwYTQifQ==",
    "nonce": 5357,
    "balances": {
      "current": "12984670968199095",
      "previous": "12984670968275009"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x910c4ba923b2243dc13e00a066eefb8ffd905eb0",
    "nonce": 6,
    "balances": {
      "current": "75839",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:32.926Z",
  "updated": "2020-05-22T08:40:32.996Z",
  "id": "5ec79000b0c6090011d5afb4"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000001283f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `75839`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`