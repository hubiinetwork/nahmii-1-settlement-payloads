# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6427Fc587266813B6993ae4c8DE672640cB3B43F`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000170000000000000000000000000000000000000000000000000000000000000017000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000001700000000000000000000000000000000000000000000000000000000000000177f0d93044d53d5feca3a0d95d32650b89794c9bd96ae911ca1f4fe0f7b7438379a3f448a35ff6fb2def57ab999cc67db80f3f4a29035957c5d28061ed5d7d5373398c7fcd86ab895f85c7764d7139a46d2f9b12c1a140af067032be7016f8c64000000000000000000000000000000000000000000000000000000000000001b8d72d90e5af062bfb263eb4c460257390009388e658c10b1a16f796e9a626f01b20a1d5dc076e4c85f963dc7f168d9f236a675ec22f8c95194d0157494a49f477d6ab64a0bc44da499728bf32e30c67d34afcccd0ce2c7763f0a64f1b8da678b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e3b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b05d1d2ed51000000000000000000000000000000000000000000000000002e0b05d1d2ed6900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ec301ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f444a694d444d305a4330314f5755784c5455354e574974596a51344d43316d4d5459334f574d775a6a4e695a6d556966513d3d00000000000000000000000000000000000000000000000000000000000000040000000000000000000000006427fc587266813b6993ae4c8de672640cb3b43f0000000000000000000000000000000000000000000000000000000000000017000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7f0d93044d53d5feca3a0d95d32650b89794c9bd96ae911ca1f4fe0f7b743837",
      "signature": {
        "s": "0x3398c7fcd86ab895f85c7764d7139a46d2f9b12c1a140af067032be7016f8c64",
        "r": "0x9a3f448a35ff6fb2def57ab999cc67db80f3f4a29035957c5d28061ed5d7d537",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8d72d90e5af062bfb263eb4c460257390009388e658c10b1a16f796e9a626f01",
      "signature": {
        "s": "0x7d6ab64a0bc44da499728bf32e30c67d34afcccd0ce2c7763f0a64f1b8da678b",
        "r": "0xb20a1d5dc076e4c85f963dc7f168d9f236a675ec22f8c95194d0157494a49f47",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "23",
    "total": "23"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23",
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
            "amount": "57692848639"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzODJiMDM0ZC01OWUxLTU5NWItYjQ4MC1mMTY3OWMwZjNiZmUifQ==",
    "nonce": 7739,
    "balances": {
      "current": "12959968551693649",
      "previous": "12959968551693673"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6427fc587266813b6993ae4c8de672640cb3b43f",
    "nonce": 4,
    "balances": {
      "current": "23",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:11.477Z",
  "updated": "2020-05-22T08:59:11.553Z",
  "id": "5ec7945fe5756b00111b8941"
}
```
* *stageAmount*: `23`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000017000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000001700000000000000000000000000000000000000000000000000000000000000177f0d93044d53d5feca3a0d95d32650b89794c9bd96ae911ca1f4fe0f7b7438379a3f448a35ff6fb2def57ab999cc67db80f3f4a29035957c5d28061ed5d7d5373398c7fcd86ab895f85c7764d7139a46d2f9b12c1a140af067032be7016f8c64000000000000000000000000000000000000000000000000000000000000001b8d72d90e5af062bfb263eb4c460257390009388e658c10b1a16f796e9a626f01b20a1d5dc076e4c85f963dc7f168d9f236a675ec22f8c95194d0157494a49f477d6ab64a0bc44da499728bf32e30c67d34afcccd0ce2c7763f0a64f1b8da678b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e3b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b05d1d2ed51000000000000000000000000000000000000000000000000002e0b05d1d2ed6900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ec301ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f444a694d444d305a4330314f5755784c5455354e574974596a51344d43316d4d5459334f574d775a6a4e695a6d556966513d3d00000000000000000000000000000000000000000000000000000000000000040000000000000000000000006427fc587266813b6993ae4c8de672640cb3b43f0000000000000000000000000000000000000000000000000000000000000017000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7f0d93044d53d5feca3a0d95d32650b89794c9bd96ae911ca1f4fe0f7b743837",
      "signature": {
        "s": "0x3398c7fcd86ab895f85c7764d7139a46d2f9b12c1a140af067032be7016f8c64",
        "r": "0x9a3f448a35ff6fb2def57ab999cc67db80f3f4a29035957c5d28061ed5d7d537",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8d72d90e5af062bfb263eb4c460257390009388e658c10b1a16f796e9a626f01",
      "signature": {
        "s": "0x7d6ab64a0bc44da499728bf32e30c67d34afcccd0ce2c7763f0a64f1b8da678b",
        "r": "0xb20a1d5dc076e4c85f963dc7f168d9f236a675ec22f8c95194d0157494a49f47",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "23",
    "total": "23"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23",
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
            "amount": "57692848639"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzODJiMDM0ZC01OWUxLTU5NWItYjQ4MC1mMTY3OWMwZjNiZmUifQ==",
    "nonce": 7739,
    "balances": {
      "current": "12959968551693649",
      "previous": "12959968551693673"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6427fc587266813b6993ae4c8de672640cb3b43f",
    "nonce": 4,
    "balances": {
      "current": "23",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:11.477Z",
  "updated": "2020-05-22T08:59:11.553Z",
  "id": "5ec7945fe5756b00111b8941"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000017000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `23`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`