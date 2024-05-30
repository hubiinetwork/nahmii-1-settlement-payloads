# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf345252e297158df1615d6ce5c160F666FdB92C5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000003a866452425453c36c00000000000000000000000000000000000000000000000163372fe95bcbcea40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000163372fe95bcbcea4000000000000000000000000000000000000000000000026efb1c4619fd9bd3da704d69c2a651837d944425ba58bf2b3efa43c2707f4d6ed09bb5f3275ad130f65d2f9fc4b2e6c71f5901635aa53ac2cef2b9387a5da24af268c135b4d5f1639327786abb3b8f1ae959194bf99ed7e4ea46adb914a728fc08dd704682e86053f000000000000000000000000000000000000000000000000000000000000001b29a14bbf400474667ed55591e0ffdfce29d3ba573fab8546e9a2f6e2831d56b0374baf7146b967ccaecb158d24f54686da1ba2e2abbc19541d84cbfdd5b153971a51eaacb256e618ab788eb72f0521926f5018c4d879a96f4285aa13cedf4371000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b280000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000480f8ff4419b05b23c35000000000000000000000000000000000000000000004810f38660ecce62579900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000005aef686ce44cc00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9f422674e2cc3a64c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e6d59324e7a52694f53307a5a444a6a4c5455314e474574596a646d4d6930334e54597a4d4759344e6a466d4e7a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f345252e297158df1615d6ce5c160f666fdb92c500000000000000000000000000000000000000000000003a866452425453c36c000000000000000000000000000000000000000000000039232d2258f887f4c800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa704d69c2a651837d944425ba58bf2b3efa43c2707f4d6ed09bb5f3275ad130f",
      "signature": {
        "s": "0x327786abb3b8f1ae959194bf99ed7e4ea46adb914a728fc08dd704682e86053f",
        "r": "0x65d2f9fc4b2e6c71f5901635aa53ac2cef2b9387a5da24af268c135b4d5f1639",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x29a14bbf400474667ed55591e0ffdfce29d3ba573fab8546e9a2f6e2831d56b0",
      "signature": {
        "s": "0x1a51eaacb256e618ab788eb72f0521926f5018c4d879a96f4285aa13cedf4371",
        "r": "0x374baf7146b967ccaecb158d24f54686da1ba2e2abbc19541d84cbfdd5b15397",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "25595979686497472164",
    "total": "718248076770478243133"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "25595979686497472164",
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
            "amount": "27632367615023117477452"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "25595979686497472"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmNmY2NzRiOS0zZDJjLTU1NGEtYjdmMi03NTYzMGY4NjFmNzMifQ==",
    "nonce": 111232,
    "balances": {
      "current": "340297460915695911058485",
      "previous": "340323082491362095028121"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf345252e297158df1615d6ce5c160f666fdb92c5",
    "nonce": 46,
    "balances": {
      "current": "1079595111818743497580",
      "previous": "1053999132132246025416"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:14.587Z",
  "updated": "2022-05-04T08:57:14.667Z",
  "id": "62723feabbd75600116d066a"
}
```
* *stageAmount*: `1079595111818743497580`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000163372fe95bcbcea40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000163372fe95bcbcea4000000000000000000000000000000000000000000000026efb1c4619fd9bd3da704d69c2a651837d944425ba58bf2b3efa43c2707f4d6ed09bb5f3275ad130f65d2f9fc4b2e6c71f5901635aa53ac2cef2b9387a5da24af268c135b4d5f1639327786abb3b8f1ae959194bf99ed7e4ea46adb914a728fc08dd704682e86053f000000000000000000000000000000000000000000000000000000000000001b29a14bbf400474667ed55591e0ffdfce29d3ba573fab8546e9a2f6e2831d56b0374baf7146b967ccaecb158d24f54686da1ba2e2abbc19541d84cbfdd5b153971a51eaacb256e618ab788eb72f0521926f5018c4d879a96f4285aa13cedf4371000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b280000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000480f8ff4419b05b23c35000000000000000000000000000000000000000000004810f38660ecce62579900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000005aef686ce44cc00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9f422674e2cc3a64c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e6d59324e7a52694f53307a5a444a6a4c5455314e474574596a646d4d6930334e54597a4d4759344e6a466d4e7a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f345252e297158df1615d6ce5c160f666fdb92c500000000000000000000000000000000000000000000003a866452425453c36c000000000000000000000000000000000000000000000039232d2258f887f4c800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa704d69c2a651837d944425ba58bf2b3efa43c2707f4d6ed09bb5f3275ad130f",
      "signature": {
        "s": "0x327786abb3b8f1ae959194bf99ed7e4ea46adb914a728fc08dd704682e86053f",
        "r": "0x65d2f9fc4b2e6c71f5901635aa53ac2cef2b9387a5da24af268c135b4d5f1639",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x29a14bbf400474667ed55591e0ffdfce29d3ba573fab8546e9a2f6e2831d56b0",
      "signature": {
        "s": "0x1a51eaacb256e618ab788eb72f0521926f5018c4d879a96f4285aa13cedf4371",
        "r": "0x374baf7146b967ccaecb158d24f54686da1ba2e2abbc19541d84cbfdd5b15397",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "25595979686497472164",
    "total": "718248076770478243133"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "25595979686497472164",
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
            "amount": "27632367615023117477452"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "25595979686497472"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmNmY2NzRiOS0zZDJjLTU1NGEtYjdmMi03NTYzMGY4NjFmNzMifQ==",
    "nonce": 111232,
    "balances": {
      "current": "340297460915695911058485",
      "previous": "340323082491362095028121"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf345252e297158df1615d6ce5c160f666fdb92c5",
    "nonce": 46,
    "balances": {
      "current": "1079595111818743497580",
      "previous": "1053999132132246025416"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:14.587Z",
  "updated": "2022-05-04T08:57:14.667Z",
  "id": "62723feabbd75600116d066a"
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
0x0f200f9b00000000000000000000000000000000000000000000003a866452425453c36c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1079595111818743497580`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`