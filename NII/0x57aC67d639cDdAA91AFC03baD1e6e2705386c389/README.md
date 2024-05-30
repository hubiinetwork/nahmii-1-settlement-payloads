# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x57aC67d639cDdAA91AFC03baD1e6e2705386c389`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000016a42fa69237000000000000000000000000000000000000000000000000000000896bc7d7510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000896bc7d75100000000000000000000000000000000000000000000000000000f102ad97755295e37b2845a218351058f6e7a39fb7f7f5b4e0a1ad0ee650614ad5aefaa8baaa27f1caff61ec086f4bfeef70faf765f6bc95bce4a3c716a62085615b71912bb041b4e5d63822af12c62fe69372e84241660371b93c4c29bd2f3c730e44d1f7a000000000000000000000000000000000000000000000000000000000000001b921a9ae9625c02f5cb4cfa50970bd893fcf11dfb844b403eb9c24bdf91f0a660988acdea067ff24b11bff9f0181cf5101cc4360c437f309897e824447d99755179d1693ec8f02862910330bf02a808d5b3adf27741f18ebf2f5ef349a7173e91000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac08000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009aaa4db2338086119a2b000000000000000000000000000000000000000000009aaa4db2340a1507779600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000232e061a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d3fa0fdadc5515ff0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6d56694e4749314d4330334e444d334c54566b4d5455744f545269597931684e445978595745354f57526b5a446b6966513d3d000000000000000000000000000000000000000000000000000000000000002d00000000000000000000000057ac67d639cddaa91afc03bad1e6e2705386c389000000000000000000000000000000000000000000000000000016a42fa692370000000000000000000000000000000000000000000000000000161ac3debae600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x295e37b2845a218351058f6e7a39fb7f7f5b4e0a1ad0ee650614ad5aefaa8baa",
      "signature": {
        "s": "0x041b4e5d63822af12c62fe69372e84241660371b93c4c29bd2f3c730e44d1f7a",
        "r": "0xa27f1caff61ec086f4bfeef70faf765f6bc95bce4a3c716a62085615b71912bb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x921a9ae9625c02f5cb4cfa50970bd893fcf11dfb844b403eb9c24bdf91f0a660",
      "signature": {
        "s": "0x79d1693ec8f02862910330bf02a808d5b3adf27741f18ebf2f5ef349a7173e91",
        "r": "0x988acdea067ff24b11bff9f0181cf5101cc4360c437f309897e824447d997551",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "590218778449",
    "total": "16562112788309"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "590218778449",
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
            "amount": "27242668791314152494591"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "590218778"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZmViNGI1MC03NDM3LTVkMTUtOTRiYy1hNDYxYWE5OWRkZDkifQ==",
    "nonce": 109576,
    "balances": {
      "current": "730385983448369859762731",
      "previous": "730385983448960668759958"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x57ac67d639cddaa91afc03bad1e6e2705386c389",
    "nonce": 45,
    "balances": {
      "current": "24894429893175",
      "previous": "24304211114726"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:48.310Z",
  "updated": "2022-05-04T08:48:48.371Z",
  "id": "62723df07832e20011830a97"
}
```
* *stageAmount*: `24894429893175`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000896bc7d7510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000896bc7d75100000000000000000000000000000000000000000000000000000f102ad97755295e37b2845a218351058f6e7a39fb7f7f5b4e0a1ad0ee650614ad5aefaa8baaa27f1caff61ec086f4bfeef70faf765f6bc95bce4a3c716a62085615b71912bb041b4e5d63822af12c62fe69372e84241660371b93c4c29bd2f3c730e44d1f7a000000000000000000000000000000000000000000000000000000000000001b921a9ae9625c02f5cb4cfa50970bd893fcf11dfb844b403eb9c24bdf91f0a660988acdea067ff24b11bff9f0181cf5101cc4360c437f309897e824447d99755179d1693ec8f02862910330bf02a808d5b3adf27741f18ebf2f5ef349a7173e91000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac08000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009aaa4db2338086119a2b000000000000000000000000000000000000000000009aaa4db2340a1507779600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000232e061a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4d3fa0fdadc5515ff0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6d56694e4749314d4330334e444d334c54566b4d5455744f545269597931684e445978595745354f57526b5a446b6966513d3d000000000000000000000000000000000000000000000000000000000000002d00000000000000000000000057ac67d639cddaa91afc03bad1e6e2705386c389000000000000000000000000000000000000000000000000000016a42fa692370000000000000000000000000000000000000000000000000000161ac3debae600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x295e37b2845a218351058f6e7a39fb7f7f5b4e0a1ad0ee650614ad5aefaa8baa",
      "signature": {
        "s": "0x041b4e5d63822af12c62fe69372e84241660371b93c4c29bd2f3c730e44d1f7a",
        "r": "0xa27f1caff61ec086f4bfeef70faf765f6bc95bce4a3c716a62085615b71912bb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x921a9ae9625c02f5cb4cfa50970bd893fcf11dfb844b403eb9c24bdf91f0a660",
      "signature": {
        "s": "0x79d1693ec8f02862910330bf02a808d5b3adf27741f18ebf2f5ef349a7173e91",
        "r": "0x988acdea067ff24b11bff9f0181cf5101cc4360c437f309897e824447d997551",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "590218778449",
    "total": "16562112788309"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "590218778449",
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
            "amount": "27242668791314152494591"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "590218778"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZmViNGI1MC03NDM3LTVkMTUtOTRiYy1hNDYxYWE5OWRkZDkifQ==",
    "nonce": 109576,
    "balances": {
      "current": "730385983448369859762731",
      "previous": "730385983448960668759958"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x57ac67d639cddaa91afc03bad1e6e2705386c389",
    "nonce": 45,
    "balances": {
      "current": "24894429893175",
      "previous": "24304211114726"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:48.310Z",
  "updated": "2022-05-04T08:48:48.371Z",
  "id": "62723df07832e20011830a97"
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
0x0f200f9b000000000000000000000000000000000000000000000000000016a42fa692370000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `24894429893175`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`