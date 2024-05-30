# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8Ebd10FE696288c6ED1E024064FDF54541Aa63e0`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000025c8e787004a90000000000000000000000000000000000000000000000000000000000004e960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004e960000000000000000000000000000000000000000000000000000baa2622daa373037409a6d5f91b668696829f3af8c24612122c0497c4f999e490211480c6b935df5d5c20ec02febc02556e0cf2bd95702f2b501892bba3d33e697c0d5b0b6bd490ff678cfe5f73cbfd1c49a912717776fccc842b5d5b8abdf87d63dff92d172000000000000000000000000000000000000000000000000000000000000001b31faf370fafd7fc14d7820cef02084c540f1193e479d6d9cfc7a5d5ffab23e9ed3565f25da7fc01c73d0f91ed024e94df293011d72ba0708c7bc7954699473817cbd4b251dffd86dd82b20978552249244bbbd326423432d956a5bd317634d62000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b488000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000395d3ab05624d1d4783e00000000000000000000000000000000000000000000395d3ab05624d1d4c6e800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddb654576dbfde76f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a597a6b314e474d7a4d7930784d544d344c545530595749744f5749344d4330785a6d457a4d445a6d4e3251335932596966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000008ebd10fe696288c6ed1e024064fdf54541aa63e000000000000000000000000000000000000000000000000000025c8e787004a900000000000000000000000000000000000000000000000000025c8e786fb61300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3037409a6d5f91b668696829f3af8c24612122c0497c4f999e490211480c6b93",
      "signature": {
        "s": "0x490ff678cfe5f73cbfd1c49a912717776fccc842b5d5b8abdf87d63dff92d172",
        "r": "0x5df5d5c20ec02febc02556e0cf2bd95702f2b501892bba3d33e697c0d5b0b6bd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x31faf370fafd7fc14d7820cef02084c540f1193e479d6d9cfc7a5d5ffab23e9e",
      "signature": {
        "s": "0x7cbd4b251dffd86dd82b20978552249244bbbd326423432d956a5bd317634d62",
        "r": "0xd3565f25da7fc01c73d0f91ed024e94df293011d72ba0708c7bc795469947381",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "20118",
    "total": "205206594628151"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20118",
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
            "amount": "27701701076779865634549"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "20"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjYzk1NGMzMy0xMTM4LTU0YWItOWI4MC0xZmEzMDZmN2Q3Y2YifQ==",
    "nonce": 111752,
    "balances": {
      "current": "270894665697191005550654",
      "previous": "270894665697191005570792"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8ebd10fe696288c6ed1e024064fdf54541aa63e0",
    "nonce": 29,
    "balances": {
      "current": "664716929139881",
      "previous": "664716929119763"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:57.826Z",
  "updated": "2022-05-04T08:59:57.888Z",
  "id": "6272408d7832e20011830d74"
}
```
* *stageAmount*: `664716929139881`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004e960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004e960000000000000000000000000000000000000000000000000000baa2622daa373037409a6d5f91b668696829f3af8c24612122c0497c4f999e490211480c6b935df5d5c20ec02febc02556e0cf2bd95702f2b501892bba3d33e697c0d5b0b6bd490ff678cfe5f73cbfd1c49a912717776fccc842b5d5b8abdf87d63dff92d172000000000000000000000000000000000000000000000000000000000000001b31faf370fafd7fc14d7820cef02084c540f1193e479d6d9cfc7a5d5ffab23e9ed3565f25da7fc01c73d0f91ed024e94df293011d72ba0708c7bc7954699473817cbd4b251dffd86dd82b20978552249244bbbd326423432d956a5bd317634d62000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b488000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000395d3ab05624d1d4783e00000000000000000000000000000000000000000000395d3ab05624d1d4c6e800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddb654576dbfde76f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a597a6b314e474d7a4d7930784d544d344c545530595749744f5749344d4330785a6d457a4d445a6d4e3251335932596966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000008ebd10fe696288c6ed1e024064fdf54541aa63e000000000000000000000000000000000000000000000000000025c8e787004a900000000000000000000000000000000000000000000000000025c8e786fb61300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3037409a6d5f91b668696829f3af8c24612122c0497c4f999e490211480c6b93",
      "signature": {
        "s": "0x490ff678cfe5f73cbfd1c49a912717776fccc842b5d5b8abdf87d63dff92d172",
        "r": "0x5df5d5c20ec02febc02556e0cf2bd95702f2b501892bba3d33e697c0d5b0b6bd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x31faf370fafd7fc14d7820cef02084c540f1193e479d6d9cfc7a5d5ffab23e9e",
      "signature": {
        "s": "0x7cbd4b251dffd86dd82b20978552249244bbbd326423432d956a5bd317634d62",
        "r": "0xd3565f25da7fc01c73d0f91ed024e94df293011d72ba0708c7bc795469947381",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "20118",
    "total": "205206594628151"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20118",
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
            "amount": "27701701076779865634549"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "20"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjYzk1NGMzMy0xMTM4LTU0YWItOWI4MC0xZmEzMDZmN2Q3Y2YifQ==",
    "nonce": 111752,
    "balances": {
      "current": "270894665697191005550654",
      "previous": "270894665697191005570792"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8ebd10fe696288c6ed1e024064fdf54541aa63e0",
    "nonce": 29,
    "balances": {
      "current": "664716929139881",
      "previous": "664716929119763"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:57.826Z",
  "updated": "2022-05-04T08:59:57.888Z",
  "id": "6272408d7832e20011830d74"
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
0x0f200f9b00000000000000000000000000000000000000000000000000025c8e787004a90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `664716929139881`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`