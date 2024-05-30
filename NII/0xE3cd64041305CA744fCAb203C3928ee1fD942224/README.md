# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE3cd64041305CA744fCAb203C3928ee1fD942224`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000131bfb8e6e16e6300000000000000000000000000000000000000000000000000073fbbeaabc6f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000073fbbeaabc6f500000000000000000000000000000000000000000000000000cb69b3a59b0acca95e724ac831b7d055718653c873cdb6a6c7952bb2373306edc1f3fc98d89e43839d908b052b37463fd4be952049cde2933b36ec06831476e70e2bdf12b949807d268455a31c1d94a2a03c9652c3d229a71acd9844c3b4150bdf6779a17899f2000000000000000000000000000000000000000000000000000000000000001b21e9f18c86a05563e63f9602a1aaf09077ee21c9df71660dfddc902064de7a35f9a0bb5ce6513587acd70e8c38c8ff4ebf9d35dfe1f4e62629cde1ca8831643a09bf4a2921e084934d6600a7ef578c620f1486091d1e8d6a4ab6350b4981ef7c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1ce000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a80b7ab8d2926a5e101000000000000000000000000000000000000000000004a80b7b2cec022b4a4d400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000001db1162fcde0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d954412a5cddb4d4850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6a6c6a4e4446695a69316b4e5441354c5455304e6a49744f4441324e7930334d544e694e4751354e6a4533596a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e3cd64041305ca744fcab203c3928ee1fd9422240000000000000000000000000000000000000000000000000131bfb8e6e16e63000000000000000000000000000000000000000000000000012a7ffcfc35a76e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa95e724ac831b7d055718653c873cdb6a6c7952bb2373306edc1f3fc98d89e43",
      "signature": {
        "s": "0x7d268455a31c1d94a2a03c9652c3d229a71acd9844c3b4150bdf6779a17899f2",
        "r": "0x839d908b052b37463fd4be952049cde2933b36ec06831476e70e2bdf12b94980",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x21e9f18c86a05563e63f9602a1aaf09077ee21c9df71660dfddc902064de7a35",
      "signature": {
        "s": "0x09bf4a2921e084934d6600a7ef578c620f1486091d1e8d6a4ab6350b4981ef7c",
        "r": "0xf9a0bb5ce6513587acd70e8c38c8ff4ebf9d35dfe1f4e62629cde1ca8831643a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2040401165534965",
    "total": "57255640570727116"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2040401165534965",
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
            "amount": "27620847058694215881861"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2040401165534"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMjljNDFiZi1kNTA5LTU0NjItODA2Ny03MTNiNGQ5NjE3YjcifQ==",
    "nonce": 111054,
    "balances": {
      "current": "351829537800926408335617",
      "previous": "351829539843367975036116"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe3cd64041305ca744fcab203c3928ee1fd942224",
    "nonce": 46,
    "balances": {
      "current": "86060668765171299",
      "previous": "84020267599636334"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:20.157Z",
  "updated": "2022-05-04T08:56:20.272Z",
  "id": "62723fb4bbd75600116d0639"
}
```
* *stageAmount*: `86060668765171299`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000073fbbeaabc6f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000073fbbeaabc6f500000000000000000000000000000000000000000000000000cb69b3a59b0acca95e724ac831b7d055718653c873cdb6a6c7952bb2373306edc1f3fc98d89e43839d908b052b37463fd4be952049cde2933b36ec06831476e70e2bdf12b949807d268455a31c1d94a2a03c9652c3d229a71acd9844c3b4150bdf6779a17899f2000000000000000000000000000000000000000000000000000000000000001b21e9f18c86a05563e63f9602a1aaf09077ee21c9df71660dfddc902064de7a35f9a0bb5ce6513587acd70e8c38c8ff4ebf9d35dfe1f4e62629cde1ca8831643a09bf4a2921e084934d6600a7ef578c620f1486091d1e8d6a4ab6350b4981ef7c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1ce000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a80b7ab8d2926a5e101000000000000000000000000000000000000000000004a80b7b2cec022b4a4d400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000001db1162fcde0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d954412a5cddb4d4850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6a6c6a4e4446695a69316b4e5441354c5455304e6a49744f4441324e7930334d544e694e4751354e6a4533596a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e3cd64041305ca744fcab203c3928ee1fd9422240000000000000000000000000000000000000000000000000131bfb8e6e16e63000000000000000000000000000000000000000000000000012a7ffcfc35a76e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa95e724ac831b7d055718653c873cdb6a6c7952bb2373306edc1f3fc98d89e43",
      "signature": {
        "s": "0x7d268455a31c1d94a2a03c9652c3d229a71acd9844c3b4150bdf6779a17899f2",
        "r": "0x839d908b052b37463fd4be952049cde2933b36ec06831476e70e2bdf12b94980",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x21e9f18c86a05563e63f9602a1aaf09077ee21c9df71660dfddc902064de7a35",
      "signature": {
        "s": "0x09bf4a2921e084934d6600a7ef578c620f1486091d1e8d6a4ab6350b4981ef7c",
        "r": "0xf9a0bb5ce6513587acd70e8c38c8ff4ebf9d35dfe1f4e62629cde1ca8831643a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2040401165534965",
    "total": "57255640570727116"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2040401165534965",
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
            "amount": "27620847058694215881861"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2040401165534"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMjljNDFiZi1kNTA5LTU0NjItODA2Ny03MTNiNGQ5NjE3YjcifQ==",
    "nonce": 111054,
    "balances": {
      "current": "351829537800926408335617",
      "previous": "351829539843367975036116"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe3cd64041305ca744fcab203c3928ee1fd942224",
    "nonce": 46,
    "balances": {
      "current": "86060668765171299",
      "previous": "84020267599636334"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:20.157Z",
  "updated": "2022-05-04T08:56:20.272Z",
  "id": "62723fb4bbd75600116d0639"
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
0x0f200f9b0000000000000000000000000000000000000000000000000131bfb8e6e16e630000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `86060668765171299`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`