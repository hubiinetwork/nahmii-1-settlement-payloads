# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0xA92aF217A22c94ae332AAFF58B24a6755bb19683`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000005681de47c0ec0000000000000000000000000000000000000000000000000000003ffde8492a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000003ffde8492a000000000000000000000000000000000000000000000000000005d56fd9a7ff86e0a707003dc9fb2a3eadbb39d24a78ddd57aaab11e0e25628808dd007c67207bb7dd8c15ee7d9a3f5862ad921da1330a42dc1c5098abc27006673061a2df075c41e640a5789b8eecb72bcf58005edf3959ccd42636deddec829100cd1d3253000000000000000000000000000000000000000000000000000000000000001c552b94fbc660ca916f163e7e5d4cc566288f3afe02046d0859563a8add88b85614ac3181569b5f0c226172749dbef3cbf17d70a275794bbba361a3be1d59163f1c416b77d19a2cbb2be906f691026f321f9a49f2ea3beeedffdfc73beeec4d98000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ed00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b789000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021af08421266bc2b837a0000000000000000000000000000000000000000000021af084212a6ca75915200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000001061c4ae0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e3c4b396aa4b86e8490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a6d51774e47566d597931684f4451794c5455314d6a55744f544d775979316b4f4451794e7a42684d4441324f44676966513d3d0000000000000000000000000000000000000000000000000000000000000022000000000000000000000000a92af217a22c94ae332aaff58b24a6755bb1968300000000000000000000000000000000000000000000000000005681de47c0ec00000000000000000000000000000000000000000000000000005641e05f77c200000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001b48eb57e0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x86e0a707003dc9fb2a3eadbb39d24a78ddd57aaab11e0e25628808dd007c6720",
      "signature": {
        "s": "0x5c41e640a5789b8eecb72bcf58005edf3959ccd42636deddec829100cd1d3253",
        "r": "0x7bb7dd8c15ee7d9a3f5862ad921da1330a42dc1c5098abc27006673061a2df07",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x552b94fbc660ca916f163e7e5d4cc566288f3afe02046d0859563a8add88b856",
      "signature": {
        "s": "0x1c416b77d19a2cbb2be906f691026f321f9a49f2ea3beeedffdfc73beeec4d98",
        "r": "0x14ac3181569b5f0c226172749dbef3cbf17d70a275794bbba361a3be1d59163f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "274842798378",
    "total": "6414262708223"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "274842798378",
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
            "amount": "27813417157190715107401"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "274842798"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxZmQwNGVmYy1hODQyLTU1MjUtOTMwYy1kODQyNzBhMDA2ODgifQ==",
    "nonce": 112521,
    "balances": {
      "current": "159066869205930682844026",
      "previous": "159066869206205800485202"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "30000000000000"
          }
        }
      ]
    },
    "wallet": "0xa92af217a22c94ae332aaff58b24a6755bb19683",
    "nonce": 34,
    "balances": {
      "current": "95115780014316",
      "previous": "94840937215938"
    }
  },
  "blockNumber": "14709997",
  "created": "2022-05-04T09:04:17.703Z",
  "updated": "2022-05-04T09:04:17.795Z",
  "id": "62724191bbd75600116d0805"
}
```
* *stageAmount*: `95115780014316`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006800000000000000000000000000000000000000000000000000000003ffde8492a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000003ffde8492a000000000000000000000000000000000000000000000000000005d56fd9a7ff86e0a707003dc9fb2a3eadbb39d24a78ddd57aaab11e0e25628808dd007c67207bb7dd8c15ee7d9a3f5862ad921da1330a42dc1c5098abc27006673061a2df075c41e640a5789b8eecb72bcf58005edf3959ccd42636deddec829100cd1d3253000000000000000000000000000000000000000000000000000000000000001c552b94fbc660ca916f163e7e5d4cc566288f3afe02046d0859563a8add88b85614ac3181569b5f0c226172749dbef3cbf17d70a275794bbba361a3be1d59163f1c416b77d19a2cbb2be906f691026f321f9a49f2ea3beeedffdfc73beeec4d98000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ed00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b789000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021af08421266bc2b837a0000000000000000000000000000000000000000000021af084212a6ca75915200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000001061c4ae0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e3c4b396aa4b86e8490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a6d51774e47566d597931684f4451794c5455314d6a55744f544d775979316b4f4451794e7a42684d4441324f44676966513d3d0000000000000000000000000000000000000000000000000000000000000022000000000000000000000000a92af217a22c94ae332aaff58b24a6755bb1968300000000000000000000000000000000000000000000000000005681de47c0ec00000000000000000000000000000000000000000000000000005641e05f77c200000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001b48eb57e0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x86e0a707003dc9fb2a3eadbb39d24a78ddd57aaab11e0e25628808dd007c6720",
      "signature": {
        "s": "0x5c41e640a5789b8eecb72bcf58005edf3959ccd42636deddec829100cd1d3253",
        "r": "0x7bb7dd8c15ee7d9a3f5862ad921da1330a42dc1c5098abc27006673061a2df07",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x552b94fbc660ca916f163e7e5d4cc566288f3afe02046d0859563a8add88b856",
      "signature": {
        "s": "0x1c416b77d19a2cbb2be906f691026f321f9a49f2ea3beeedffdfc73beeec4d98",
        "r": "0x14ac3181569b5f0c226172749dbef3cbf17d70a275794bbba361a3be1d59163f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "274842798378",
    "total": "6414262708223"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "274842798378",
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
            "amount": "27813417157190715107401"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "274842798"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxZmQwNGVmYy1hODQyLTU1MjUtOTMwYy1kODQyNzBhMDA2ODgifQ==",
    "nonce": 112521,
    "balances": {
      "current": "159066869205930682844026",
      "previous": "159066869206205800485202"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "30000000000000"
          }
        }
      ]
    },
    "wallet": "0xa92af217a22c94ae332aaff58b24a6755bb19683",
    "nonce": 34,
    "balances": {
      "current": "95115780014316",
      "previous": "94840937215938"
    }
  },
  "blockNumber": "14709997",
  "created": "2022-05-04T09:04:17.703Z",
  "updated": "2022-05-04T09:04:17.795Z",
  "id": "62724191bbd75600116d0805"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000005681de47c0ec0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `95115780014316`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`