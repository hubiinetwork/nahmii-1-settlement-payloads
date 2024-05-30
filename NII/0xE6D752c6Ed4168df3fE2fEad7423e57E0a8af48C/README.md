# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE6D752c6Ed4168df3fE2fEad7423e57E0a8af48C`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000025ea3ea93e36e44b0000000000000000000000000000000000000000000000000a543a5bf139fc7f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000a543a5bf139fc7f00000000000000000000000000000000000000000000000025ea3ea93e36e44ba89972493d2d0c611afdd0d18c47c31e357ad34017e4bbe738328a266203635abfc584f42f797085e82ee63cdc496e735599e8642754d74ca69ee3773abe43757e477776b35014da0712654a57cf6637ada1f2664da44d56a96ca2ab25855cce000000000000000000000000000000000000000000000000000000000000001b2ce28039d77993407e719e7f839654b682172aeeb85f39a1191e1a95ed2f215cba78ebc0a2988f6894d6eef26133038aeda79ca9954a3a3d670a8e3401c7665d5aa77ed716b1b886cb129e39674fd797ed8966e2cdf3333352a966573d557640000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd38410000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001210e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000024c75b1863ef44ca0eeb0000000000000000000000000000000000000000000024c7656f433755beba0000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002a4ec1fbaae960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003591afb9297b5a4335d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e4459344f5755324e6930784d446b784c5456694d544d74596a51324f4330774d324d315a4459785a54526a5a54596966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000e6d752c6ed4168df3fe2fead7423e57e0a8af48c00000000000000000000000000000000000000000000000025ea3ea93e36e44b0000000000000000000000000000000000000000000000001b96044d4cfce7cc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa89972493d2d0c611afdd0d18c47c31e357ad34017e4bbe738328a266203635a",
      "signature": {
        "s": "0x7e477776b35014da0712654a57cf6637ada1f2664da44d56a96ca2ab25855cce",
        "r": "0xbfc584f42f797085e82ee63cdc496e735599e8642754d74ca69ee3773abe4375",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2ce28039d77993407e719e7f839654b682172aeeb85f39a1191e1a95ed2f215c",
      "signature": {
        "s": "0x5aa77ed716b1b886cb129e39674fd797ed8966e2cdf3333352a966573d557640",
        "r": "0xba78ebc0a2988f6894d6eef26133038aeda79ca9954a3a3d670a8e3401c7665d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "744284004986518655",
    "total": "2732065020567807051"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "744284004986518655",
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
            "amount": "15810803980013511390045"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "744284004986518"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNDY4OWU2Ni0xMDkxLTViMTMtYjQ2OC0wM2M1ZDYxZTRjZTYifQ==",
    "nonce": 73998,
    "balances": {
      "current": "173682659560311623388907",
      "previous": "173683404588600614894080"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe6d752c6ed4168df3fe2fead7423e57e0a8af48c",
    "nonce": 3,
    "balances": {
      "current": "2732065020567807051",
      "previous": "1987781015581288396"
    }
  },
  "blockNumber": "12400705",
  "created": "2021-05-09T14:36:29.115Z",
  "updated": "2021-05-09T14:36:29.185Z",
  "id": "6097f36d0f95a80011b4b43a"
}
```
* *stageAmount*: `2732065020567807051`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000a543a5bf139fc7f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000a543a5bf139fc7f00000000000000000000000000000000000000000000000025ea3ea93e36e44ba89972493d2d0c611afdd0d18c47c31e357ad34017e4bbe738328a266203635abfc584f42f797085e82ee63cdc496e735599e8642754d74ca69ee3773abe43757e477776b35014da0712654a57cf6637ada1f2664da44d56a96ca2ab25855cce000000000000000000000000000000000000000000000000000000000000001b2ce28039d77993407e719e7f839654b682172aeeb85f39a1191e1a95ed2f215cba78ebc0a2988f6894d6eef26133038aeda79ca9954a3a3d670a8e3401c7665d5aa77ed716b1b886cb129e39674fd797ed8966e2cdf3333352a966573d557640000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd38410000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001210e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000024c75b1863ef44ca0eeb0000000000000000000000000000000000000000000024c7656f433755beba0000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002a4ec1fbaae960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003591afb9297b5a4335d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e4459344f5755324e6930784d446b784c5456694d544d74596a51324f4330774d324d315a4459785a54526a5a54596966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000e6d752c6ed4168df3fe2fead7423e57e0a8af48c00000000000000000000000000000000000000000000000025ea3ea93e36e44b0000000000000000000000000000000000000000000000001b96044d4cfce7cc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa89972493d2d0c611afdd0d18c47c31e357ad34017e4bbe738328a266203635a",
      "signature": {
        "s": "0x7e477776b35014da0712654a57cf6637ada1f2664da44d56a96ca2ab25855cce",
        "r": "0xbfc584f42f797085e82ee63cdc496e735599e8642754d74ca69ee3773abe4375",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2ce28039d77993407e719e7f839654b682172aeeb85f39a1191e1a95ed2f215c",
      "signature": {
        "s": "0x5aa77ed716b1b886cb129e39674fd797ed8966e2cdf3333352a966573d557640",
        "r": "0xba78ebc0a2988f6894d6eef26133038aeda79ca9954a3a3d670a8e3401c7665d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "744284004986518655",
    "total": "2732065020567807051"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "744284004986518655",
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
            "amount": "15810803980013511390045"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "744284004986518"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNDY4OWU2Ni0xMDkxLTViMTMtYjQ2OC0wM2M1ZDYxZTRjZTYifQ==",
    "nonce": 73998,
    "balances": {
      "current": "173682659560311623388907",
      "previous": "173683404588600614894080"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe6d752c6ed4168df3fe2fead7423e57e0a8af48c",
    "nonce": 3,
    "balances": {
      "current": "2732065020567807051",
      "previous": "1987781015581288396"
    }
  },
  "blockNumber": "12400705",
  "created": "2021-05-09T14:36:29.115Z",
  "updated": "2021-05-09T14:36:29.185Z",
  "id": "6097f36d0f95a80011b4b43a"
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
0x0f200f9b00000000000000000000000000000000000000000000000025ea3ea93e36e44b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2732065020567807051`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`