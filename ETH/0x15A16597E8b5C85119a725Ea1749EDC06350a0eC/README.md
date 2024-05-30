# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x15A16597E8b5C85119a725Ea1749EDC06350a0eC`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000014b960000000000000000000000000000000000000000000000000000000000014b9600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000014b960000000000000000000000000000000000000000000000000000000000014b9602c0dafec542cdc852915afe30e4474bb15f754cb83c1ae5e77080a7ba8f8e6e62c04a60d4efcd8256bc40324d37db61d1e06c3bf8f4a4c3127838cccfb9f42d24ae06cff3d9e4aef8f0fe770f9dd34587056c89cfc5b854932f9c236537d109000000000000000000000000000000000000000000000000000000000000001cad030a984c131d57d167efd333f2f4dc225b90d57c2c438115e29349bd30c54562d12cf1555bbe8db7cae3bd6c1955c463cae58fc8119b96df06d3a18c225b350006bac2b7e268f8cf8a66479b866853bc5bbde5214e53c5098a9bacdf56f0bc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000026200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb115ce0000000000000000000000000000000000000000000000000002386f2cb12a8ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086bc100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e546b334e3249324d5330795a4751354c5455344f446b745954526d4f4330304e445979597a41304e6a5a6c4e6a496966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000015a16597e8b5c85119a725ea1749edc06350a0ec0000000000000000000000000000000000000000000000000000000000014b96000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x02c0dafec542cdc852915afe30e4474bb15f754cb83c1ae5e77080a7ba8f8e6e",
      "signature": {
        "s": "0x24ae06cff3d9e4aef8f0fe770f9dd34587056c89cfc5b854932f9c236537d109",
        "r": "0x62c04a60d4efcd8256bc40324d37db61d1e06c3bf8f4a4c3127838cccfb9f42d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xad030a984c131d57d167efd333f2f4dc225b90d57c2c438115e29349bd30c545",
      "signature": {
        "s": "0x0006bac2b7e268f8cf8a66479b866853bc5bbde5214e53c5098a9bacdf56f0bc",
        "r": "0x62d12cf1555bbe8db7cae3bd6c1955c463cae58fc8119b96df06d3a18c225b35",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "84886",
    "total": "84886"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "84886",
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
            "amount": "551873"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "84"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNTk3N2I2MS0yZGQ5LTU4ODktYTRmOC00NDYyYzA0NjZlNjIifQ==",
    "nonce": 610,
    "balances": {
      "current": "10000001531993312",
      "previous": "10000001532078282"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x15a16597e8b5c85119a725ea1749edc06350a0ec",
    "nonce": 20,
    "balances": {
      "current": "84886",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:18.321Z",
  "updated": "2020-05-22T08:03:18.396Z",
  "id": "5ec78746005df800101bc2dd"
}
```
* *stageAmount*: `84886`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000014b9600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000014b960000000000000000000000000000000000000000000000000000000000014b9602c0dafec542cdc852915afe30e4474bb15f754cb83c1ae5e77080a7ba8f8e6e62c04a60d4efcd8256bc40324d37db61d1e06c3bf8f4a4c3127838cccfb9f42d24ae06cff3d9e4aef8f0fe770f9dd34587056c89cfc5b854932f9c236537d109000000000000000000000000000000000000000000000000000000000000001cad030a984c131d57d167efd333f2f4dc225b90d57c2c438115e29349bd30c54562d12cf1555bbe8db7cae3bd6c1955c463cae58fc8119b96df06d3a18c225b350006bac2b7e268f8cf8a66479b866853bc5bbde5214e53c5098a9bacdf56f0bc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000026200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb115ce0000000000000000000000000000000000000000000000000002386f2cb12a8ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086bc100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e546b334e3249324d5330795a4751354c5455344f446b745954526d4f4330304e445979597a41304e6a5a6c4e6a496966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000015a16597e8b5c85119a725ea1749edc06350a0ec0000000000000000000000000000000000000000000000000000000000014b96000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x02c0dafec542cdc852915afe30e4474bb15f754cb83c1ae5e77080a7ba8f8e6e",
      "signature": {
        "s": "0x24ae06cff3d9e4aef8f0fe770f9dd34587056c89cfc5b854932f9c236537d109",
        "r": "0x62c04a60d4efcd8256bc40324d37db61d1e06c3bf8f4a4c3127838cccfb9f42d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xad030a984c131d57d167efd333f2f4dc225b90d57c2c438115e29349bd30c545",
      "signature": {
        "s": "0x0006bac2b7e268f8cf8a66479b866853bc5bbde5214e53c5098a9bacdf56f0bc",
        "r": "0x62d12cf1555bbe8db7cae3bd6c1955c463cae58fc8119b96df06d3a18c225b35",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "84886",
    "total": "84886"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "84886",
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
            "amount": "551873"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "84"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNTk3N2I2MS0yZGQ5LTU4ODktYTRmOC00NDYyYzA0NjZlNjIifQ==",
    "nonce": 610,
    "balances": {
      "current": "10000001531993312",
      "previous": "10000001532078282"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x15a16597e8b5c85119a725ea1749edc06350a0ec",
    "nonce": 20,
    "balances": {
      "current": "84886",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:18.321Z",
  "updated": "2020-05-22T08:03:18.396Z",
  "id": "5ec78746005df800101bc2dd"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000014b960000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `84886`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``