# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbE266dFC8b6F886E6AF5c994ac6EE9f60F97cBaf`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000c4076ab225b27519000000000000000000000000000000000000000000000000000000002038f87f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002038f87f00000000000000000000000000000000000000000000000000000002f0018189a41a2707442cb962b70182da2316394229df3ca191d8cf83f431409bca3da80413a51b61918dc374fc07342c61cd0e91e0d3df6844b2ea62a23b4c4ca57df2cb52f5b2a6a3e324bfd37ba87583043a85782990a2d1f04c3513df0347d426e165000000000000000000000000000000000000000000000000000000000000001bc44930f3c995fadf74f7f54305c2c5c9cf188e501543379327d6a6ffbed6e7d0125be7da3afe5e90b05477fe197e0b14ca198574960bc72990985dc9acc6cade37f06f8819f0644dc33bf87aa2454e3494c8f34a9adfd0151d49f14bf6ef8798000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b487000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000395d3ab05624d1d4c6e800000000000000000000000000000000000000000000395d3ab05624f215ff2300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000083fbc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddb654576dbfde76e10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d596a4e694d6a6c6b5a6931694e446b334c54566b5a544974596d55785a5330315a544d7a4d6a526a5a6a4a685a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000be266dfc8b6f886e6af5c994ac6ee9f60f97cbaf000000000000000000000000000000000000000000000000c4076ab225b27519000000000000000000000000000000000000000000000000c4076ab205797c9a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa41a2707442cb962b70182da2316394229df3ca191d8cf83f431409bca3da804",
      "signature": {
        "s": "0x52f5b2a6a3e324bfd37ba87583043a85782990a2d1f04c3513df0347d426e165",
        "r": "0x13a51b61918dc374fc07342c61cd0e91e0d3df6844b2ea62a23b4c4ca57df2cb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc44930f3c995fadf74f7f54305c2c5c9cf188e501543379327d6a6ffbed6e7d0",
      "signature": {
        "s": "0x37f06f8819f0644dc33bf87aa2454e3494c8f34a9adfd0151d49f14bf6ef8798",
        "r": "0x125be7da3afe5e90b05477fe197e0b14ca198574960bc72990985dc9acc6cade",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "540604543",
    "total": "12616565129"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "540604543",
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
            "amount": "27701701076779865634529"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "540604"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmYjNiMjlkZi1iNDk3LTVkZTItYmUxZS01ZTMzMjRjZjJhZjMifQ==",
    "nonce": 111751,
    "balances": {
      "current": "270894665697191005570792",
      "previous": "270894665697191546715939"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbe266dfc8b6f886e6af5c994ac6ee9f60f97cbaf",
    "nonce": 30,
    "balances": {
      "current": "14125376069640025369",
      "previous": "14125376069099420826"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:57.387Z",
  "updated": "2022-05-04T08:59:57.644Z",
  "id": "6272408d3592fd001130b69a"
}
```
* *stageAmount*: `14125376069640025369`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000002038f87f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002038f87f00000000000000000000000000000000000000000000000000000002f0018189a41a2707442cb962b70182da2316394229df3ca191d8cf83f431409bca3da80413a51b61918dc374fc07342c61cd0e91e0d3df6844b2ea62a23b4c4ca57df2cb52f5b2a6a3e324bfd37ba87583043a85782990a2d1f04c3513df0347d426e165000000000000000000000000000000000000000000000000000000000000001bc44930f3c995fadf74f7f54305c2c5c9cf188e501543379327d6a6ffbed6e7d0125be7da3afe5e90b05477fe197e0b14ca198574960bc72990985dc9acc6cade37f06f8819f0644dc33bf87aa2454e3494c8f34a9adfd0151d49f14bf6ef8798000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b487000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000395d3ab05624d1d4c6e800000000000000000000000000000000000000000000395d3ab05624f215ff2300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000083fbc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddb654576dbfde76e10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d596a4e694d6a6c6b5a6931694e446b334c54566b5a544974596d55785a5330315a544d7a4d6a526a5a6a4a685a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000be266dfc8b6f886e6af5c994ac6ee9f60f97cbaf000000000000000000000000000000000000000000000000c4076ab225b27519000000000000000000000000000000000000000000000000c4076ab205797c9a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa41a2707442cb962b70182da2316394229df3ca191d8cf83f431409bca3da804",
      "signature": {
        "s": "0x52f5b2a6a3e324bfd37ba87583043a85782990a2d1f04c3513df0347d426e165",
        "r": "0x13a51b61918dc374fc07342c61cd0e91e0d3df6844b2ea62a23b4c4ca57df2cb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc44930f3c995fadf74f7f54305c2c5c9cf188e501543379327d6a6ffbed6e7d0",
      "signature": {
        "s": "0x37f06f8819f0644dc33bf87aa2454e3494c8f34a9adfd0151d49f14bf6ef8798",
        "r": "0x125be7da3afe5e90b05477fe197e0b14ca198574960bc72990985dc9acc6cade",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "540604543",
    "total": "12616565129"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "540604543",
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
            "amount": "27701701076779865634529"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "540604"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmYjNiMjlkZi1iNDk3LTVkZTItYmUxZS01ZTMzMjRjZjJhZjMifQ==",
    "nonce": 111751,
    "balances": {
      "current": "270894665697191005570792",
      "previous": "270894665697191546715939"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbe266dfc8b6f886e6af5c994ac6ee9f60f97cbaf",
    "nonce": 30,
    "balances": {
      "current": "14125376069640025369",
      "previous": "14125376069099420826"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:57.387Z",
  "updated": "2022-05-04T08:59:57.644Z",
  "id": "6272408d3592fd001130b69a"
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
0x0f200f9b000000000000000000000000000000000000000000000000c4076ab225b275190000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14125376069640025369`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`