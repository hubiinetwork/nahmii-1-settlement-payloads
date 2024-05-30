# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1Bd9e072cA1BA5AcCFb30478e0E0485386F77419`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000ae220389d938ce9f3000000000000000000000000000000000000000000000000420e4f20cd95fd720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000420e4f20cd95fd720000000000000000000000000000000000000000000000073d97b7069c099429a897ed9d679f0749b07d2e3c11fccac584ecb69385dfbd578b33b5845c2926b60616acd7f668ef1d088e13b0db04b9b9e69dda377a7dcf17cc91e3c32787e217339a1e2404774e062f0d96f2a668f699a1d726eaaf9ee39a055d65afddf51d56000000000000000000000000000000000000000000000000000000000000001cbdc5210ef69209db24018f7dcff79eb156e23eb11d573e479a08d4b56fbc1c2af46193c421b33b872010204b63369c67217afe567bf659f4b1a725a8d05a06367f84854456d9f456e8931ea0f209c44e3cfa64c5340603bc832f4e80eb4df2dc000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b683000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030a9670c7e82254763170000000000000000000000000000000000000000000030a9a92bb6acf72a954400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000010e90a044d34bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dff015561c12e70a920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d545577596a4a6a4f5330324d6d49324c54566c5a6d5974595759785a4331684e7a51334e6a41325a575a6b597a516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001bd9e072ca1ba5accfb30478e0e0485386f7741900000000000000000000000000000000000000000000000ae220389d938ce9f300000000000000000000000000000000000000000000000aa011e97cc5f6ec8100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa897ed9d679f0749b07d2e3c11fccac584ecb69385dfbd578b33b5845c2926b6",
      "signature": {
        "s": "0x339a1e2404774e062f0d96f2a668f699a1d726eaaf9ee39a055d65afddf51d56",
        "r": "0x0616acd7f668ef1d088e13b0db04b9b9e69dda377a7dcf17cc91e3c32787e217",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbdc5210ef69209db24018f7dcff79eb156e23eb11d573e479a08d4b56fbc1c2a",
      "signature": {
        "s": "0x7f84854456d9f456e8931ea0f209c44e3cfa64c5340603bc832f4e80eb4df2dc",
        "r": "0xf46193c421b33b872010204b63369c67217afe567bf659f4b1a725a8d05a0636",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4759828858483899762",
    "total": "133565425712779334697"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4759828858483899762",
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
            "amount": "27742756171007645911698"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4759828858483899"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MTUwYjJjOS02MmI2LTVlZmYtYWYxZC1hNzQ3NjA2ZWZkYzQifQ==",
    "nonce": 112259,
    "balances": {
      "current": "229798516375182947869463",
      "previous": "229803280963870290253124"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1bd9e072ca1ba5accfb30478e0e0485386f77419",
    "nonce": 46,
    "balances": {
      "current": "200761526438358477299",
      "previous": "196001697579874577537"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:49.886Z",
  "updated": "2022-05-04T09:02:49.983Z",
  "id": "627241393592fd001130b74d"
}
```
* *stageAmount*: `200761526438358477299`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000420e4f20cd95fd720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000420e4f20cd95fd720000000000000000000000000000000000000000000000073d97b7069c099429a897ed9d679f0749b07d2e3c11fccac584ecb69385dfbd578b33b5845c2926b60616acd7f668ef1d088e13b0db04b9b9e69dda377a7dcf17cc91e3c32787e217339a1e2404774e062f0d96f2a668f699a1d726eaaf9ee39a055d65afddf51d56000000000000000000000000000000000000000000000000000000000000001cbdc5210ef69209db24018f7dcff79eb156e23eb11d573e479a08d4b56fbc1c2af46193c421b33b872010204b63369c67217afe567bf659f4b1a725a8d05a06367f84854456d9f456e8931ea0f209c44e3cfa64c5340603bc832f4e80eb4df2dc000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b683000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030a9670c7e82254763170000000000000000000000000000000000000000000030a9a92bb6acf72a954400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000010e90a044d34bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dff015561c12e70a920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d545577596a4a6a4f5330324d6d49324c54566c5a6d5974595759785a4331684e7a51334e6a41325a575a6b597a516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001bd9e072ca1ba5accfb30478e0e0485386f7741900000000000000000000000000000000000000000000000ae220389d938ce9f300000000000000000000000000000000000000000000000aa011e97cc5f6ec8100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa897ed9d679f0749b07d2e3c11fccac584ecb69385dfbd578b33b5845c2926b6",
      "signature": {
        "s": "0x339a1e2404774e062f0d96f2a668f699a1d726eaaf9ee39a055d65afddf51d56",
        "r": "0x0616acd7f668ef1d088e13b0db04b9b9e69dda377a7dcf17cc91e3c32787e217",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbdc5210ef69209db24018f7dcff79eb156e23eb11d573e479a08d4b56fbc1c2a",
      "signature": {
        "s": "0x7f84854456d9f456e8931ea0f209c44e3cfa64c5340603bc832f4e80eb4df2dc",
        "r": "0xf46193c421b33b872010204b63369c67217afe567bf659f4b1a725a8d05a0636",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4759828858483899762",
    "total": "133565425712779334697"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4759828858483899762",
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
            "amount": "27742756171007645911698"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4759828858483899"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MTUwYjJjOS02MmI2LTVlZmYtYWYxZC1hNzQ3NjA2ZWZkYzQifQ==",
    "nonce": 112259,
    "balances": {
      "current": "229798516375182947869463",
      "previous": "229803280963870290253124"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1bd9e072ca1ba5accfb30478e0e0485386f77419",
    "nonce": 46,
    "balances": {
      "current": "200761526438358477299",
      "previous": "196001697579874577537"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:49.886Z",
  "updated": "2022-05-04T09:02:49.983Z",
  "id": "627241393592fd001130b74d"
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
0x0f200f9b00000000000000000000000000000000000000000000000ae220389d938ce9f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `200761526438358477299`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`