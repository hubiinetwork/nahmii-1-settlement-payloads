# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3EB2BC45b8CE8D00731D68EB9BDdb55931f90133`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000015cd466511b4610c000000000000000000000000000000000000000000000000031ac8d6b889e7ca0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000031ac8d6b889e7ca00000000000000000000000000000000000000000000000015cd466511b4610ce6efa898971becafcbc156f1581807134d981e600c85dec2c8e83d287c1b9626e9d84df095e6c561e47cfd29d66f134f6b59375f9dbe6736494def6b210527d413ca164b8608384acdaa8715c5b7e1aaac60b6a224ff54d6065b4860b97e5c87000000000000000000000000000000000000000000000000000000000000001ceab82f124454ba1f6ea5bbbabe35e90d9c56d46c55c0feb141d2dbcb8ef16fa56e3d0c7d3c3e3fe863bd2a837e11742f77c8630b7fbe5a223aae273902172dbf0d547d7e664dfbf0a53736ca7ff4ee5511cbb212d8fd3abf85ad8e8da5da1532000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b667000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030f89b7fa2dcefb1d9ad0000000000000000000000000000000000000000000030f89e9b372aa7e7ecf500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000cb76ffac2b7e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfdbd3c0350bcb920d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f57466d5a546b7a5a69316a596a51784c54566d4f4749745957597a5a69316d596a686d4e444e6859324a6a4d44596966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000003eb2bc45b8ce8d00731d68eb9bddb55931f9013300000000000000000000000000000000000000000000000015cd466511b4610c00000000000000000000000000000000000000000000000012b27d8e592a794200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe6efa898971becafcbc156f1581807134d981e600c85dec2c8e83d287c1b9626",
      "signature": {
        "s": "0x13ca164b8608384acdaa8715c5b7e1aaac60b6a224ff54d6065b4860b97e5c87",
        "r": "0xe9d84df095e6c561e47cfd29d66f134f6b59375f9dbe6736494def6b210527d4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xeab82f124454ba1f6ea5bbbabe35e90d9c56d46c55c0feb141d2dbcb8ef16fa5",
      "signature": {
        "s": "0x0d547d7e664dfbf0a53736ca7ff4ee5511cbb212d8fd3abf85ad8e8da5da1532",
        "r": "0x6e3d0c7d3c3e3fe863bd2a837e11742f77c8630b7fbe5a223aae273902172dbf",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "223711956052862922",
    "total": "1570989244924846348"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "223711956052862922",
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
            "amount": "27741296558433911935501"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "223711956052862"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4OWFmZTkzZi1jYjQxLTVmOGItYWYzZi1mYjhmNDNhY2JjMDYifQ==",
    "nonce": 112231,
    "balances": {
      "current": "231259588561490658056621",
      "previous": "231259812497158666972405"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3eb2bc45b8ce8d00731d68eb9bddb55931f90133",
    "nonce": 8,
    "balances": {
      "current": "1570989244924846348",
      "previous": "1347277288871983426"
    }
  },
  "blockNumber": "14709989",
  "created": "2022-05-04T09:02:41.129Z",
  "updated": "2022-05-04T09:02:41.255Z",
  "id": "627241313592fd001130b741"
}
```
* *stageAmount*: `1570989244924846348`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000031ac8d6b889e7ca0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000031ac8d6b889e7ca00000000000000000000000000000000000000000000000015cd466511b4610ce6efa898971becafcbc156f1581807134d981e600c85dec2c8e83d287c1b9626e9d84df095e6c561e47cfd29d66f134f6b59375f9dbe6736494def6b210527d413ca164b8608384acdaa8715c5b7e1aaac60b6a224ff54d6065b4860b97e5c87000000000000000000000000000000000000000000000000000000000000001ceab82f124454ba1f6ea5bbbabe35e90d9c56d46c55c0feb141d2dbcb8ef16fa56e3d0c7d3c3e3fe863bd2a837e11742f77c8630b7fbe5a223aae273902172dbf0d547d7e664dfbf0a53736ca7ff4ee5511cbb212d8fd3abf85ad8e8da5da1532000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b667000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030f89b7fa2dcefb1d9ad0000000000000000000000000000000000000000000030f89e9b372aa7e7ecf500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000cb76ffac2b7e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfdbd3c0350bcb920d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f57466d5a546b7a5a69316a596a51784c54566d4f4749745957597a5a69316d596a686d4e444e6859324a6a4d44596966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000003eb2bc45b8ce8d00731d68eb9bddb55931f9013300000000000000000000000000000000000000000000000015cd466511b4610c00000000000000000000000000000000000000000000000012b27d8e592a794200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe6efa898971becafcbc156f1581807134d981e600c85dec2c8e83d287c1b9626",
      "signature": {
        "s": "0x13ca164b8608384acdaa8715c5b7e1aaac60b6a224ff54d6065b4860b97e5c87",
        "r": "0xe9d84df095e6c561e47cfd29d66f134f6b59375f9dbe6736494def6b210527d4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xeab82f124454ba1f6ea5bbbabe35e90d9c56d46c55c0feb141d2dbcb8ef16fa5",
      "signature": {
        "s": "0x0d547d7e664dfbf0a53736ca7ff4ee5511cbb212d8fd3abf85ad8e8da5da1532",
        "r": "0x6e3d0c7d3c3e3fe863bd2a837e11742f77c8630b7fbe5a223aae273902172dbf",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "223711956052862922",
    "total": "1570989244924846348"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "223711956052862922",
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
            "amount": "27741296558433911935501"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "223711956052862"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4OWFmZTkzZi1jYjQxLTVmOGItYWYzZi1mYjhmNDNhY2JjMDYifQ==",
    "nonce": 112231,
    "balances": {
      "current": "231259588561490658056621",
      "previous": "231259812497158666972405"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3eb2bc45b8ce8d00731d68eb9bddb55931f90133",
    "nonce": 8,
    "balances": {
      "current": "1570989244924846348",
      "previous": "1347277288871983426"
    }
  },
  "blockNumber": "14709989",
  "created": "2022-05-04T09:02:41.129Z",
  "updated": "2022-05-04T09:02:41.255Z",
  "id": "627241313592fd001130b741"
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
0x0f200f9b00000000000000000000000000000000000000000000000015cd466511b4610c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1570989244924846348`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`