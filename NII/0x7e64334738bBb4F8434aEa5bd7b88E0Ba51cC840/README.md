# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7e64334738bBb4F8434aEa5bd7b88E0Ba51cC840`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001e79270c60e95c37f0000000000000000000000000000000000000000000000000b8f4dd8f0c7bdcd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b8f4dd8f0c7bdcd0000000000000000000000000000000000000000000000014460f33ac1c8053a9f7d5694f8adbc0694c8efde52245347cd88768b0e2999f4af9ea29bae11ac59e79a452fdce0e7464b29528e15a73338976bd50547077263a321733e8d9b7601766718a9229aed7d93ae8f0a676f191fa3c55e6c86ad0d50973ec580c83f5a4c000000000000000000000000000000000000000000000000000000000000001c80494f2c60257db65c2ac0991c483768876ea1b466afc6f041f3f2a04a87d1d310c96ebdc5d23c79e568f396a7540b784da7f93eb816ae51a6a91beb58d0f02f3c8924bde9b48c56cc52252f7bbb997c1b17aa5455356513d3f4af26c1978ac3000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af0a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095accb36fb87b6fadc220000000000000000000000000000000000000000000095acd6c93ef59bb6835600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002f594f3f3e9670000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61ab14c443859f6360000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e7a46694d544e6a5a4330784e32517a4c54566b59545174596a41334d693035597a526b4f47497a4d545a6d4e44516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000007e64334738bbb4f8434aea5bd7b88e0ba51cc840000000000000000000000000000000000000000000000001e79270c60e95c37f000000000000000000000000000000000000000000000001dc0322ed1dce05b200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9f7d5694f8adbc0694c8efde52245347cd88768b0e2999f4af9ea29bae11ac59",
      "signature": {
        "s": "0x766718a9229aed7d93ae8f0a676f191fa3c55e6c86ad0d50973ec580c83f5a4c",
        "r": "0xe79a452fdce0e7464b29528e15a73338976bd50547077263a321733e8d9b7601",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x80494f2c60257db65c2ac0991c483768876ea1b466afc6f041f3f2a04a87d1d3",
      "signature": {
        "s": "0x3c8924bde9b48c56cc52252f7bbb997c1b17aa5455356513d3f4af26c1978ac3",
        "r": "0x10c96ebdc5d23c79e568f396a7540b784da7f93eb816ae51a6a91beb58d0f02f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "832970050234727885",
    "total": "23373949499737638202"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "832970050234727885",
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
            "amount": "27266211143314468107830"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "832970050234727"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNzFiMTNjZC0xN2QzLTVkYTQtYjA3Mi05YzRkOGIzMTZmNDQifQ==",
    "nonce": 110346,
    "balances": {
      "current": "706820089096053930515490",
      "previous": "706820922899074215478102"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7e64334738bbb4f8434aea5bd7b88e0ba51cc840",
    "nonce": 46,
    "balances": {
      "current": "35133267639021192063",
      "previous": "34300297588786464178"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:48.085Z",
  "updated": "2022-05-04T08:52:48.163Z",
  "id": "62723ee07832e20011830b96"
}
```
* *stageAmount*: `35133267639021192063`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000b8f4dd8f0c7bdcd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b8f4dd8f0c7bdcd0000000000000000000000000000000000000000000000014460f33ac1c8053a9f7d5694f8adbc0694c8efde52245347cd88768b0e2999f4af9ea29bae11ac59e79a452fdce0e7464b29528e15a73338976bd50547077263a321733e8d9b7601766718a9229aed7d93ae8f0a676f191fa3c55e6c86ad0d50973ec580c83f5a4c000000000000000000000000000000000000000000000000000000000000001c80494f2c60257db65c2ac0991c483768876ea1b466afc6f041f3f2a04a87d1d310c96ebdc5d23c79e568f396a7540b784da7f93eb816ae51a6a91beb58d0f02f3c8924bde9b48c56cc52252f7bbb997c1b17aa5455356513d3f4af26c1978ac3000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af0a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095accb36fb87b6fadc220000000000000000000000000000000000000000000095acd6c93ef59bb6835600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002f594f3f3e9670000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61ab14c443859f6360000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e7a46694d544e6a5a4330784e32517a4c54566b59545174596a41334d693035597a526b4f47497a4d545a6d4e44516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000007e64334738bbb4f8434aea5bd7b88e0ba51cc840000000000000000000000000000000000000000000000001e79270c60e95c37f000000000000000000000000000000000000000000000001dc0322ed1dce05b200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9f7d5694f8adbc0694c8efde52245347cd88768b0e2999f4af9ea29bae11ac59",
      "signature": {
        "s": "0x766718a9229aed7d93ae8f0a676f191fa3c55e6c86ad0d50973ec580c83f5a4c",
        "r": "0xe79a452fdce0e7464b29528e15a73338976bd50547077263a321733e8d9b7601",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x80494f2c60257db65c2ac0991c483768876ea1b466afc6f041f3f2a04a87d1d3",
      "signature": {
        "s": "0x3c8924bde9b48c56cc52252f7bbb997c1b17aa5455356513d3f4af26c1978ac3",
        "r": "0x10c96ebdc5d23c79e568f396a7540b784da7f93eb816ae51a6a91beb58d0f02f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "832970050234727885",
    "total": "23373949499737638202"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "832970050234727885",
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
            "amount": "27266211143314468107830"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "832970050234727"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNzFiMTNjZC0xN2QzLTVkYTQtYjA3Mi05YzRkOGIzMTZmNDQifQ==",
    "nonce": 110346,
    "balances": {
      "current": "706820089096053930515490",
      "previous": "706820922899074215478102"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7e64334738bbb4f8434aea5bd7b88e0ba51cc840",
    "nonce": 46,
    "balances": {
      "current": "35133267639021192063",
      "previous": "34300297588786464178"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:48.085Z",
  "updated": "2022-05-04T08:52:48.163Z",
  "id": "62723ee07832e20011830b96"
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
0x0f200f9b000000000000000000000000000000000000000000000001e79270c60e95c37f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `35133267639021192063`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`