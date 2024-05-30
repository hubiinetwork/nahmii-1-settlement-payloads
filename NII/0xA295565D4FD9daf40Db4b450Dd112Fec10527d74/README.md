# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA295565D4FD9daf40Db4b450Dd112Fec10527d74`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000034d1f594bf66565160000000000000000000000000000000000000000000000000000000171defc380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000171defc3800000000000000000000000000000000000000000000000000000021b8135fe79910f7976aeadde15d2d51ed9521de3aaf5dd901115d5c914f3466d431c390de363898c593030a9e6d89136960282de64fa165964ef79d6a21d612ba980d94cb6a80af6dd56b00a9409c5eeb658f756048d1788111bb2f481c6bc807e30f20b3000000000000000000000000000000000000000000000000000000000000001be5302e6363edbb2e87bbe74598bc79ac8a9abb5c095abd3ca3694ce0944a3f7fb2987e0875b7fd5abe2e8d95c272df684f3d93136bba46cbc6ac702cb97458495c2d19ee2eb03e9a37b651d03bf665c105a14bff7e7ebb165abad39a71e1725f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1d2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a7d9c60fb0ddd5cfee2000000000000000000000000000000000000000000004a7d9c60fb0f4f9aaaf800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000005eafde0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9550c8e81357ff6c00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5749785a474d324d5330315a5467784c5455305a6a4d744f446869596930324e4467355a445135596d49325957496966513d3d0000000000000000000000000000000000000000000000000000000000000029000000000000000000000000a295565d4fd9daf40db4b450dd112fec10527d740000000000000000000000000000000000000000000000034d1f594bf66565160000000000000000000000000000000000000000000000034d1f594a848668de00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9910f7976aeadde15d2d51ed9521de3aaf5dd901115d5c914f3466d431c390de",
      "signature": {
        "s": "0x6a80af6dd56b00a9409c5eeb658f756048d1788111bb2f481c6bc807e30f20b3",
        "r": "0x363898c593030a9e6d89136960282de64fa165964ef79d6a21d612ba980d94cb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe5302e6363edbb2e87bbe74598bc79ac8a9abb5c095abd3ca3694ce0944a3f7f",
      "signature": {
        "s": "0x5c2d19ee2eb03e9a37b651d03bf665c105a14bff7e7ebb165abad39a71e1725f",
        "r": "0xb2987e0875b7fd5abe2e8d95c272df684f3d93136bba46cbc6ac702cb9745849",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6205406264",
    "total": "144822198247"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6205406264",
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
            "amount": "27620904308221742675648"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6205406"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZWIxZGM2MS01ZTgxLTU0ZjMtODhiYi02NDg5ZDQ5YmI2YWIifQ==",
    "nonce": 111058,
    "balances": {
      "current": "351772231023872087752418",
      "previous": "351772231023878299364088"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa295565d4fd9daf40db4b450dd112fec10527d74",
    "nonce": 41,
    "balances": {
      "current": "60897490869118395670",
      "previous": "60897490862912989406"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:21.586Z",
  "updated": "2022-05-04T08:56:21.679Z",
  "id": "62723fb5bbd75600116d063a"
}
```
* *stageAmount*: `60897490869118395670`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000171defc380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000171defc3800000000000000000000000000000000000000000000000000000021b8135fe79910f7976aeadde15d2d51ed9521de3aaf5dd901115d5c914f3466d431c390de363898c593030a9e6d89136960282de64fa165964ef79d6a21d612ba980d94cb6a80af6dd56b00a9409c5eeb658f756048d1788111bb2f481c6bc807e30f20b3000000000000000000000000000000000000000000000000000000000000001be5302e6363edbb2e87bbe74598bc79ac8a9abb5c095abd3ca3694ce0944a3f7fb2987e0875b7fd5abe2e8d95c272df684f3d93136bba46cbc6ac702cb97458495c2d19ee2eb03e9a37b651d03bf665c105a14bff7e7ebb165abad39a71e1725f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1d2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a7d9c60fb0ddd5cfee2000000000000000000000000000000000000000000004a7d9c60fb0f4f9aaaf800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000005eafde0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9550c8e81357ff6c00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5749785a474d324d5330315a5467784c5455305a6a4d744f446869596930324e4467355a445135596d49325957496966513d3d0000000000000000000000000000000000000000000000000000000000000029000000000000000000000000a295565d4fd9daf40db4b450dd112fec10527d740000000000000000000000000000000000000000000000034d1f594bf66565160000000000000000000000000000000000000000000000034d1f594a848668de00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9910f7976aeadde15d2d51ed9521de3aaf5dd901115d5c914f3466d431c390de",
      "signature": {
        "s": "0x6a80af6dd56b00a9409c5eeb658f756048d1788111bb2f481c6bc807e30f20b3",
        "r": "0x363898c593030a9e6d89136960282de64fa165964ef79d6a21d612ba980d94cb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe5302e6363edbb2e87bbe74598bc79ac8a9abb5c095abd3ca3694ce0944a3f7f",
      "signature": {
        "s": "0x5c2d19ee2eb03e9a37b651d03bf665c105a14bff7e7ebb165abad39a71e1725f",
        "r": "0xb2987e0875b7fd5abe2e8d95c272df684f3d93136bba46cbc6ac702cb9745849",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6205406264",
    "total": "144822198247"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6205406264",
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
            "amount": "27620904308221742675648"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6205406"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZWIxZGM2MS01ZTgxLTU0ZjMtODhiYi02NDg5ZDQ5YmI2YWIifQ==",
    "nonce": 111058,
    "balances": {
      "current": "351772231023872087752418",
      "previous": "351772231023878299364088"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa295565d4fd9daf40db4b450dd112fec10527d74",
    "nonce": 41,
    "balances": {
      "current": "60897490869118395670",
      "previous": "60897490862912989406"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:21.586Z",
  "updated": "2022-05-04T08:56:21.679Z",
  "id": "62723fb5bbd75600116d063a"
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
0x0f200f9b0000000000000000000000000000000000000000000000034d1f594bf66565160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `60897490869118395670`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`