# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA057A235531c4Bf078fA10CbFECDd8d4c0f1A648`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000022c000000000000000000000000000000000000000000000000000000000000022c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000022c000000000000000000000000000000000000000000000000000000000000022c5ad6d9c4d7a4535aa2a8147ad6639652262bfc6e3624fd81059d99fc4844b69cf2fd671ee99c09cf1430d07796e38263565be34a7649cdcf9dca0655e35e3ce475fbecaadb3cf7d45816818795a793d568ca6b75d82170eaf926508101f1d73e000000000000000000000000000000000000000000000000000000000000001c38735275a739788a8c68f83af9907d4c52f80ff7e77b68d8339fe28fca5b20b4d92c05ceb5a88a85dcc10ed93edd6a848363d23019749f3e5a796f180a55dc8575161b34252c3da57ff21953dfbd29c18879436bdfedef26fd19f8efc8024bd7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008fb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc560345000000000000000000000000000000000000000000000000002386f2bc56057200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e4700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a574d31596d466a597930324d4751774c5455354d5451744f5449774d4330344e7a63794d4455794e6d4d305a47596966513d3d0000000000000000000000000000000000000000000000000000000000000008000000000000000000000000a057a235531c4bf078fa10cbfecdd8d4c0f1a648000000000000000000000000000000000000000000000000000000000000022c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5ad6d9c4d7a4535aa2a8147ad6639652262bfc6e3624fd81059d99fc4844b69c",
      "signature": {
        "s": "0x75fbecaadb3cf7d45816818795a793d568ca6b75d82170eaf926508101f1d73e",
        "r": "0xf2fd671ee99c09cf1430d07796e38263565be34a7649cdcf9dca0655e35e3ce4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x38735275a739788a8c68f83af9907d4c52f80ff7e77b68d8339fe28fca5b20b4",
      "signature": {
        "s": "0x75161b34252c3da57ff21953dfbd29c18879436bdfedef26fd19f8efc8024bd7",
        "r": "0xd92c05ceb5a88a85dcc10ed93edd6a848363d23019749f3e5a796f180a55dc85",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "556",
    "total": "556"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "556",
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
            "amount": "798279"
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
    "data": "eyJyZWYiOiJlZWM1YmFjYy02MGQwLTU5MTQtOTIwMC04NzcyMDUyNmM0ZGYifQ==",
    "nonce": 2299,
    "balances": {
      "current": "10000001284834117",
      "previous": "10000001284834674"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa057a235531c4bf078fa10cbfecdd8d4c0f1a648",
    "nonce": 8,
    "balances": {
      "current": "556",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:36.458Z",
  "updated": "2020-05-22T08:15:36.531Z",
  "id": "5ec78a28b0c6090011d5abcb"
}
```
* *stageAmount*: `556`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000022c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000022c000000000000000000000000000000000000000000000000000000000000022c5ad6d9c4d7a4535aa2a8147ad6639652262bfc6e3624fd81059d99fc4844b69cf2fd671ee99c09cf1430d07796e38263565be34a7649cdcf9dca0655e35e3ce475fbecaadb3cf7d45816818795a793d568ca6b75d82170eaf926508101f1d73e000000000000000000000000000000000000000000000000000000000000001c38735275a739788a8c68f83af9907d4c52f80ff7e77b68d8339fe28fca5b20b4d92c05ceb5a88a85dcc10ed93edd6a848363d23019749f3e5a796f180a55dc8575161b34252c3da57ff21953dfbd29c18879436bdfedef26fd19f8efc8024bd7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008fb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc560345000000000000000000000000000000000000000000000000002386f2bc56057200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e4700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a574d31596d466a597930324d4751774c5455354d5451744f5449774d4330344e7a63794d4455794e6d4d305a47596966513d3d0000000000000000000000000000000000000000000000000000000000000008000000000000000000000000a057a235531c4bf078fa10cbfecdd8d4c0f1a648000000000000000000000000000000000000000000000000000000000000022c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5ad6d9c4d7a4535aa2a8147ad6639652262bfc6e3624fd81059d99fc4844b69c",
      "signature": {
        "s": "0x75fbecaadb3cf7d45816818795a793d568ca6b75d82170eaf926508101f1d73e",
        "r": "0xf2fd671ee99c09cf1430d07796e38263565be34a7649cdcf9dca0655e35e3ce4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x38735275a739788a8c68f83af9907d4c52f80ff7e77b68d8339fe28fca5b20b4",
      "signature": {
        "s": "0x75161b34252c3da57ff21953dfbd29c18879436bdfedef26fd19f8efc8024bd7",
        "r": "0xd92c05ceb5a88a85dcc10ed93edd6a848363d23019749f3e5a796f180a55dc85",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "556",
    "total": "556"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "556",
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
            "amount": "798279"
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
    "data": "eyJyZWYiOiJlZWM1YmFjYy02MGQwLTU5MTQtOTIwMC04NzcyMDUyNmM0ZGYifQ==",
    "nonce": 2299,
    "balances": {
      "current": "10000001284834117",
      "previous": "10000001284834674"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa057a235531c4bf078fa10cbfecdd8d4c0f1a648",
    "nonce": 8,
    "balances": {
      "current": "556",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:36.458Z",
  "updated": "2020-05-22T08:15:36.531Z",
  "id": "5ec78a28b0c6090011d5abcb"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000022c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `556`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``