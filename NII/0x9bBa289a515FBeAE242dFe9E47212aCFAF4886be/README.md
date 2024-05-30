# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9bBa289a515FBeAE242dFe9E47212aCFAF4886be`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000002af0666d02b7ffffed0f00000000000000000000000000000000000000000000012822eb878576343cd50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000012822eb878576343cd5000000000000000000000000000000000000000000002075e02063a54345faa94b61e8c42588c519e56d47406c0ac8ea9dd014a518aeb41ba19c86ee310bc66e4f71e37ef1c00eb44607f9b854a4ddac3afee901ec2e36f77fdb27178c04c5b6505dbbe8a0e84b29244da9356ed801fc009018316fdaa747d567a3f3dee0b55c000000000000000000000000000000000000000000000000000000000000001c493c90c1ce03eee12d31bb631d791f120ed07bf02fed9dc02676a04d133181e8b9901daecb7dd57138e359a70aa37d247de7d3ee128b09f9bd0028f0bdee6c2e11c13f955bc7340158247abc5c7b87e4b23b29136334a3f649970d4fd6837a53000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af49000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000072a4886d1f53c242d44b0000000000000000000000000000000000000000000073ccf7283f4dd582e52700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000004bcf98749d0bd4070000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005cf10461644c89474690000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497859574a6a5a475a6a5a5330785a4464694c5455354e544574595449314f5330354d32557959575a6d4d575a6b4e32596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009bba289a515fbeae242dfe9e47212acfaf4886be000000000000000000000000000000000000000000002af0666d02b7ffffed0f0000000000000000000000000000000000000000000029c843817b3289cbb03a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4b61e8c42588c519e56d47406c0ac8ea9dd014a518aeb41ba19c86ee310bc66e",
      "signature": {
        "s": "0x505dbbe8a0e84b29244da9356ed801fc009018316fdaa747d567a3f3dee0b55c",
        "r": "0x4f71e37ef1c00eb44607f9b854a4ddac3afee901ec2e36f77fdb27178c04c5b6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x493c90c1ce03eee12d31bb631d791f120ed07bf02fed9dc02676a04d133181e8",
      "signature": {
        "s": "0x11c13f955bc7340158247abc5c7b87e4b23b29136334a3f649970d4fd6837a53",
        "r": "0xb9901daecb7dd57138e359a70aa37d247de7d3ee128b09f9bd0028f0bdee6c2e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5462752499642127367381",
    "total": "153290146526277864389289"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5462752499642127367381",
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
            "amount": "27431481086843758605417"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5462752499642127367"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxYWJjZGZjZS0xZDdiLTU5NTEtYTI1OS05M2UyYWZmMWZkN2YifQ==",
    "nonce": 110409,
    "balances": {
      "current": "541384875623234142393419",
      "previous": "546853090875375911888167"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9bba289a515fbeae242dfe9e47212acfaf4886be",
    "nonce": 46,
    "balances": {
      "current": "202773991416569018707215",
      "previous": "197311238916926891339834"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:08.320Z",
  "updated": "2022-05-04T08:53:08.434Z",
  "id": "62723ef4bbd75600116d055f"
}
```
* *stageAmount*: `202773991416569018707215`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000012822eb878576343cd50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000012822eb878576343cd5000000000000000000000000000000000000000000002075e02063a54345faa94b61e8c42588c519e56d47406c0ac8ea9dd014a518aeb41ba19c86ee310bc66e4f71e37ef1c00eb44607f9b854a4ddac3afee901ec2e36f77fdb27178c04c5b6505dbbe8a0e84b29244da9356ed801fc009018316fdaa747d567a3f3dee0b55c000000000000000000000000000000000000000000000000000000000000001c493c90c1ce03eee12d31bb631d791f120ed07bf02fed9dc02676a04d133181e8b9901daecb7dd57138e359a70aa37d247de7d3ee128b09f9bd0028f0bdee6c2e11c13f955bc7340158247abc5c7b87e4b23b29136334a3f649970d4fd6837a53000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af49000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000072a4886d1f53c242d44b0000000000000000000000000000000000000000000073ccf7283f4dd582e52700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000004bcf98749d0bd4070000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005cf10461644c89474690000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497859574a6a5a475a6a5a5330785a4464694c5455354e544574595449314f5330354d32557959575a6d4d575a6b4e32596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009bba289a515fbeae242dfe9e47212acfaf4886be000000000000000000000000000000000000000000002af0666d02b7ffffed0f0000000000000000000000000000000000000000000029c843817b3289cbb03a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4b61e8c42588c519e56d47406c0ac8ea9dd014a518aeb41ba19c86ee310bc66e",
      "signature": {
        "s": "0x505dbbe8a0e84b29244da9356ed801fc009018316fdaa747d567a3f3dee0b55c",
        "r": "0x4f71e37ef1c00eb44607f9b854a4ddac3afee901ec2e36f77fdb27178c04c5b6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x493c90c1ce03eee12d31bb631d791f120ed07bf02fed9dc02676a04d133181e8",
      "signature": {
        "s": "0x11c13f955bc7340158247abc5c7b87e4b23b29136334a3f649970d4fd6837a53",
        "r": "0xb9901daecb7dd57138e359a70aa37d247de7d3ee128b09f9bd0028f0bdee6c2e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5462752499642127367381",
    "total": "153290146526277864389289"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5462752499642127367381",
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
            "amount": "27431481086843758605417"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5462752499642127367"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxYWJjZGZjZS0xZDdiLTU5NTEtYTI1OS05M2UyYWZmMWZkN2YifQ==",
    "nonce": 110409,
    "balances": {
      "current": "541384875623234142393419",
      "previous": "546853090875375911888167"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9bba289a515fbeae242dfe9e47212acfaf4886be",
    "nonce": 46,
    "balances": {
      "current": "202773991416569018707215",
      "previous": "197311238916926891339834"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:08.320Z",
  "updated": "2022-05-04T08:53:08.434Z",
  "id": "62723ef4bbd75600116d055f"
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
0x0f200f9b000000000000000000000000000000000000000000002af0666d02b7ffffed0f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `202773991416569018707215`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`