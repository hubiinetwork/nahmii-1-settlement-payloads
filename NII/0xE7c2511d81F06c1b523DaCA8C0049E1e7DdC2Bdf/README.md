# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE7c2511d81F06c1b523DaCA8C0049E1e7DdC2Bdf`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000b5636e531fbd680de80000000000000000000000000000000000000000000000044cee7c22b7b938860000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000044cee7c22b7b93886000000000000000000000000000000000000000000000078ad35ea6e277f96f6f5b1babef4bdebed47d13f73245d7401179b14c803cb9bcabdea62c7e3b4b8463cec6c467c1fdf6c77266efbec77b061e026c69f2e81c88a8a5037e42761f23f0804baa4da2605322d1fd1884c388b5e14c5ffa8502aed1c0e315c65ba5aaf0e000000000000000000000000000000000000000000000000000000000000001cc808cb74cc69b28a03390f1a07c2c19ab2094e6ce65409018243ada014018742f234219b2455306fdd49ab73ac32c9967ba9644e5fbc7888ddd363e95677d7a6646a524232ccacc54f7ea0c58f16e360a9319a28de8ff416fe4495b9fdf8405f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6f9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002fb84151ca651078f330000000000000000000000000000000000000000000002fbc8f5a1d2eba8e428d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000119d6a6f25c16d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e02dc1620dc7fd7f0e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d545a6d4d544d33596930774e7a49354c54553259574d744f5445334d53316b5932566a5a5749784d6a4e695957596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e7c2511d81f06c1b523daca8c0049e1e7ddc2bdf0000000000000000000000000000000000000000000000b5636e531fbd680de80000000000000000000000000000000000000000000000b1167fd6fd05aed56200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf5b1babef4bdebed47d13f73245d7401179b14c803cb9bcabdea62c7e3b4b846",
      "signature": {
        "s": "0x0804baa4da2605322d1fd1884c388b5e14c5ffa8502aed1c0e315c65ba5aaf0e",
        "r": "0x3cec6c467c1fdf6c77266efbec77b061e026c69f2e81c88a8a5037e42761f23f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc808cb74cc69b28a03390f1a07c2c19ab2094e6ce65409018243ada014018742",
      "signature": {
        "s": "0x646a524232ccacc54f7ea0c58f16e360a9319a28de8ff416fe4495b9fdf8405f",
        "r": "0xf234219b2455306fdd49ab73ac32c9967ba9644e5fbc7888ddd363e95677d7a6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "79330480974730967174",
    "total": "2226090428546303366902"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "79330480974730967174",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27747200111072706920206"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "79330480974730967"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MTZmMTM3Yi0wNzI5LTU2YWMtOTE3MS1kY2VjZWIxMjNiYWYifQ==",
    "nonce": 112377,
    "balances": {
      "current": "225350132370056878289712",
      "previous": "225429542181512583987853"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe7c2511d81f06c1b523daca8c0049e1e7ddc2bdf",
    "nonce": 46,
    "balances": {
      "current": "3346025432794408685032",
      "previous": "3266694951819677717858"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:29.226Z",
  "updated": "2022-05-04T09:03:29.300Z",
  "id": "627241613592fd001130b779"
}
```
* *stageAmount*: `3346025432794408685032`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000044cee7c22b7b938860000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000044cee7c22b7b93886000000000000000000000000000000000000000000000078ad35ea6e277f96f6f5b1babef4bdebed47d13f73245d7401179b14c803cb9bcabdea62c7e3b4b8463cec6c467c1fdf6c77266efbec77b061e026c69f2e81c88a8a5037e42761f23f0804baa4da2605322d1fd1884c388b5e14c5ffa8502aed1c0e315c65ba5aaf0e000000000000000000000000000000000000000000000000000000000000001cc808cb74cc69b28a03390f1a07c2c19ab2094e6ce65409018243ada014018742f234219b2455306fdd49ab73ac32c9967ba9644e5fbc7888ddd363e95677d7a6646a524232ccacc54f7ea0c58f16e360a9319a28de8ff416fe4495b9fdf8405f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6f9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002fb84151ca651078f330000000000000000000000000000000000000000000002fbc8f5a1d2eba8e428d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000119d6a6f25c16d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e02dc1620dc7fd7f0e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d545a6d4d544d33596930774e7a49354c54553259574d744f5445334d53316b5932566a5a5749784d6a4e695957596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e7c2511d81f06c1b523daca8c0049e1e7ddc2bdf0000000000000000000000000000000000000000000000b5636e531fbd680de80000000000000000000000000000000000000000000000b1167fd6fd05aed56200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf5b1babef4bdebed47d13f73245d7401179b14c803cb9bcabdea62c7e3b4b846",
      "signature": {
        "s": "0x0804baa4da2605322d1fd1884c388b5e14c5ffa8502aed1c0e315c65ba5aaf0e",
        "r": "0x3cec6c467c1fdf6c77266efbec77b061e026c69f2e81c88a8a5037e42761f23f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc808cb74cc69b28a03390f1a07c2c19ab2094e6ce65409018243ada014018742",
      "signature": {
        "s": "0x646a524232ccacc54f7ea0c58f16e360a9319a28de8ff416fe4495b9fdf8405f",
        "r": "0xf234219b2455306fdd49ab73ac32c9967ba9644e5fbc7888ddd363e95677d7a6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "79330480974730967174",
    "total": "2226090428546303366902"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "79330480974730967174",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27747200111072706920206"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "79330480974730967"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MTZmMTM3Yi0wNzI5LTU2YWMtOTE3MS1kY2VjZWIxMjNiYWYifQ==",
    "nonce": 112377,
    "balances": {
      "current": "225350132370056878289712",
      "previous": "225429542181512583987853"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe7c2511d81f06c1b523daca8c0049e1e7ddc2bdf",
    "nonce": 46,
    "balances": {
      "current": "3346025432794408685032",
      "previous": "3266694951819677717858"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:29.226Z",
  "updated": "2022-05-04T09:03:29.300Z",
  "id": "627241613592fd001130b779"
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
0x0f200f9b0000000000000000000000000000000000000000000000b5636e531fbd680de80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3346025432794408685032`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`