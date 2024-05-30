# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD7C93D864110c2b0517446B74330C1E5a2094CFd`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000005cdef0dad558b78d0000000000000000000000000000000000000000000000000233ad4de4b8402b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000233ad4de4b8402b0000000000000000000000000000000000000000000000003dc952e69ece788ac973d267d584686018170d8df1e329eeee81ce3571ed9e840594f235a1430729935b080a207f1ab2e12b7c9f5242f6791d474416015dcd6e6aed7dee775750cb425430a3985156bdadf209ca5e521717b296feec99ce007754f78255ffa2f352000000000000000000000000000000000000000000000000000000000000001c685d6d29fec963abf7063958e98c05bbe07541b9bf5197c9c297e94f9fae21e9fe05590cc3a62df3ab0049b6ca796446e0052cfc0f43c3f021c2ee5a14ad8b6e2d00f1df95d150037b455a419e64028bcbd638d8824fcf71cb12c851696bde4a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1bf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a83a813b7a52ce443ac000000000000000000000000000000000000000000004a83aa47f54033e35af100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000904d2246d71a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d95380bde27f1323390000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a597a49774e4441304d53316d593259324c545532596d55744f575178596930355a44526c4d574d314e474e6a596a496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d7c93d864110c2b0517446b74330c1e5a2094cfd0000000000000000000000000000000000000000000000005cdef0dad558b78d0000000000000000000000000000000000000000000000005aab438cf0a0776200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc973d267d584686018170d8df1e329eeee81ce3571ed9e840594f235a1430729",
      "signature": {
        "s": "0x425430a3985156bdadf209ca5e521717b296feec99ce007754f78255ffa2f352",
        "r": "0x935b080a207f1ab2e12b7c9f5242f6791d474416015dcd6e6aed7dee775750cb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x685d6d29fec963abf7063958e98c05bbe07541b9bf5197c9c297e94f9fae21e9",
      "signature": {
        "s": "0x2d00f1df95d150037b455a419e64028bcbd638d8824fcf71cb12c851696bde4a",
        "r": "0xfe05590cc3a62df3ab0049b6ca796446e0052cfc0f43c3f021c2ee5a14ad8b6e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "158660961949466667",
    "total": "4452180857092733066"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949466667",
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
            "amount": "27620792896225857971001"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949466"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYzIwNDA0MS1mY2Y2LTU2YmUtOWQxYi05ZDRlMWM1NGNjYjIifQ==",
    "nonce": 111039,
    "balances": {
      "current": "351883754431752677114796",
      "previous": "351883913251375588530929"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd7c93d864110c2b0517446b74330c1e5a2094cfd",
    "nonce": 46,
    "balances": {
      "current": "6692050918992033677",
      "previous": "6533389957042567010"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:16.052Z",
  "updated": "2022-05-04T08:56:16.143Z",
  "id": "62723fb07832e20011830c7a"
}
```
* *stageAmount*: `6692050918992033677`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000233ad4de4b8402b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000233ad4de4b8402b0000000000000000000000000000000000000000000000003dc952e69ece788ac973d267d584686018170d8df1e329eeee81ce3571ed9e840594f235a1430729935b080a207f1ab2e12b7c9f5242f6791d474416015dcd6e6aed7dee775750cb425430a3985156bdadf209ca5e521717b296feec99ce007754f78255ffa2f352000000000000000000000000000000000000000000000000000000000000001c685d6d29fec963abf7063958e98c05bbe07541b9bf5197c9c297e94f9fae21e9fe05590cc3a62df3ab0049b6ca796446e0052cfc0f43c3f021c2ee5a14ad8b6e2d00f1df95d150037b455a419e64028bcbd638d8824fcf71cb12c851696bde4a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1bf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a83a813b7a52ce443ac000000000000000000000000000000000000000000004a83aa47f54033e35af100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000904d2246d71a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d95380bde27f1323390000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a597a49774e4441304d53316d593259324c545532596d55744f575178596930355a44526c4d574d314e474e6a596a496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d7c93d864110c2b0517446b74330c1e5a2094cfd0000000000000000000000000000000000000000000000005cdef0dad558b78d0000000000000000000000000000000000000000000000005aab438cf0a0776200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc973d267d584686018170d8df1e329eeee81ce3571ed9e840594f235a1430729",
      "signature": {
        "s": "0x425430a3985156bdadf209ca5e521717b296feec99ce007754f78255ffa2f352",
        "r": "0x935b080a207f1ab2e12b7c9f5242f6791d474416015dcd6e6aed7dee775750cb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x685d6d29fec963abf7063958e98c05bbe07541b9bf5197c9c297e94f9fae21e9",
      "signature": {
        "s": "0x2d00f1df95d150037b455a419e64028bcbd638d8824fcf71cb12c851696bde4a",
        "r": "0xfe05590cc3a62df3ab0049b6ca796446e0052cfc0f43c3f021c2ee5a14ad8b6e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "158660961949466667",
    "total": "4452180857092733066"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158660961949466667",
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
            "amount": "27620792896225857971001"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "158660961949466"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYzIwNDA0MS1mY2Y2LTU2YmUtOWQxYi05ZDRlMWM1NGNjYjIifQ==",
    "nonce": 111039,
    "balances": {
      "current": "351883754431752677114796",
      "previous": "351883913251375588530929"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd7c93d864110c2b0517446b74330c1e5a2094cfd",
    "nonce": 46,
    "balances": {
      "current": "6692050918992033677",
      "previous": "6533389957042567010"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:16.052Z",
  "updated": "2022-05-04T08:56:16.143Z",
  "id": "62723fb07832e20011830c7a"
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
0x0f200f9b0000000000000000000000000000000000000000000000005cdef0dad558b78d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6692050918992033677`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`