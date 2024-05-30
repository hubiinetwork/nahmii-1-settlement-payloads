# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf1C8b6Fd02C9B12C7130C371d98c095C243dc971`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000073e280432c60000000000000000000000000000000000000000000000000000002bf5bf3d440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002bf5bf3d44000000000000000000000000000000000000000000000000000004d18f1563d1736db28690d744909243afdd1761a27358ee7ec8f1efa7b298bbeec4d30ddfda27956c5df0314c332c6b7c25d9f855cb2fe0e2b4d6bb0eea38ad2d973a4732933f2c7bc35cc3b895ea04531173a311cfbda3cab11b916361ffd524d4b28091c0000000000000000000000000000000000000000000000000000000000000001ba0f990b741f8f87501dd6206ba9167473601ec5c0657afdfb078206942f4efaee059a14ec981dbfc2d039ba3453cfc530622842ee03beae9eafd4a145939c1976a52ee7139b40d95c061b695a66fd07fe1aeb2179865235db858854bc41b8257000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074bc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac85000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a35205969667ad83393000000000000000000000000000000000000000000009a35205969927bd8666700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000b40f5900000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4f1f1b608ebb02ff20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596a686a4d4759784d6930775a47566c4c5455795a6a4d74595464684f43316b5a6d4d354e475a68596a41774d546b6966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000f1c8b6fd02c9b12c7130c371d98c095c243dc9710000000000000000000000000000000000000000000000000000073e280432c6000000000000000000000000000000000000000000000000000007123244f58200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x736db28690d744909243afdd1761a27358ee7ec8f1efa7b298bbeec4d30ddfda",
      "signature": {
        "s": "0x3f2c7bc35cc3b895ea04531173a311cfbda3cab11b916361ffd524d4b28091c0",
        "r": "0x27956c5df0314c332c6b7c25d9f855cb2fe0e2b4d6bb0eea38ad2d973a473293",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa0f990b741f8f87501dd6206ba9167473601ec5c0657afdfb078206942f4efae",
      "signature": {
        "s": "0x6a52ee7139b40d95c061b695a66fd07fe1aeb2179865235db858854bc41b8257",
        "r": "0xe059a14ec981dbfc2d039ba3453cfc530622842ee03beae9eafd4a145939c197",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "188806544708",
    "total": "5298095219665"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "188806544708",
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
            "amount": "27244828168577256271858"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "188806544"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YjhjMGYxMi0wZGVlLTUyZjMtYTdhOC1kZmM5NGZhYjAwMTkifQ==",
    "nonce": 109701,
    "balances": {
      "current": "728224446808002978657171",
      "previous": "728224446808191974008423"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf1c8b6fd02c9b12c7130c371d98c095c243dc971",
    "nonce": 45,
    "balances": {
      "current": "7963540730566",
      "previous": "7774734185858"
    }
  },
  "blockNumber": "14709948",
  "created": "2022-05-04T08:49:28.818Z",
  "updated": "2022-05-04T08:49:28.939Z",
  "id": "62723e183592fd001130b3e6"
}
```
* *stageAmount*: `7963540730566`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000002bf5bf3d440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002bf5bf3d44000000000000000000000000000000000000000000000000000004d18f1563d1736db28690d744909243afdd1761a27358ee7ec8f1efa7b298bbeec4d30ddfda27956c5df0314c332c6b7c25d9f855cb2fe0e2b4d6bb0eea38ad2d973a4732933f2c7bc35cc3b895ea04531173a311cfbda3cab11b916361ffd524d4b28091c0000000000000000000000000000000000000000000000000000000000000001ba0f990b741f8f87501dd6206ba9167473601ec5c0657afdfb078206942f4efaee059a14ec981dbfc2d039ba3453cfc530622842ee03beae9eafd4a145939c1976a52ee7139b40d95c061b695a66fd07fe1aeb2179865235db858854bc41b8257000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074bc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac85000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a35205969667ad83393000000000000000000000000000000000000000000009a35205969927bd8666700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000b40f5900000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4f1f1b608ebb02ff20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596a686a4d4759784d6930775a47566c4c5455795a6a4d74595464684f43316b5a6d4d354e475a68596a41774d546b6966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000f1c8b6fd02c9b12c7130c371d98c095c243dc9710000000000000000000000000000000000000000000000000000073e280432c6000000000000000000000000000000000000000000000000000007123244f58200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x736db28690d744909243afdd1761a27358ee7ec8f1efa7b298bbeec4d30ddfda",
      "signature": {
        "s": "0x3f2c7bc35cc3b895ea04531173a311cfbda3cab11b916361ffd524d4b28091c0",
        "r": "0x27956c5df0314c332c6b7c25d9f855cb2fe0e2b4d6bb0eea38ad2d973a473293",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa0f990b741f8f87501dd6206ba9167473601ec5c0657afdfb078206942f4efae",
      "signature": {
        "s": "0x6a52ee7139b40d95c061b695a66fd07fe1aeb2179865235db858854bc41b8257",
        "r": "0xe059a14ec981dbfc2d039ba3453cfc530622842ee03beae9eafd4a145939c197",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "188806544708",
    "total": "5298095219665"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "188806544708",
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
            "amount": "27244828168577256271858"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "188806544"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YjhjMGYxMi0wZGVlLTUyZjMtYTdhOC1kZmM5NGZhYjAwMTkifQ==",
    "nonce": 109701,
    "balances": {
      "current": "728224446808002978657171",
      "previous": "728224446808191974008423"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf1c8b6fd02c9b12c7130c371d98c095c243dc971",
    "nonce": 45,
    "balances": {
      "current": "7963540730566",
      "previous": "7774734185858"
    }
  },
  "blockNumber": "14709948",
  "created": "2022-05-04T08:49:28.818Z",
  "updated": "2022-05-04T08:49:28.939Z",
  "id": "62723e183592fd001130b3e6"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000073e280432c60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7963540730566`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`