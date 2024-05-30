# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x43c40b598C485d11e05B4306B522e2B539264D22`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000aad76149644da200000000000000000000000000000000000000000000000000000000002a48c40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002a48c40000000000000000000000000000000000000000000000000000000003dad37902571e18ab3a637cae938b194223d86287aedf715a481e5160b226529ad1858e5202db822527d1a7659c46d8738cdd0b2efb38db2ed82633c892eb240b6c873e6bccf77811126c600b6be21aff0e39d3fa510c47eca872a2f75a3678c5ac11c0000000000000000000000000000000000000000000000000000000000000001b2d3ca42ab6a507f934151a26ce9eb9707c801b8da432c79f37bc4aaf15780f19a7b865bdca78f155f187df8aeaebb40099628c39d7788cb84fa221f714ca571079488df9be68880ccb2e53a74b94d5190b8a2d2c38126796e5714c2419962967000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b410000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039d6b5305e8d7ccd40d80000000000000000000000000000000000000000000039d6b5305e8d7cf7946f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000ad30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd97431428d98743940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b595445344d6a526a4d5330304e44466d4c5455334f44417459546779595330304d7a5530596d5a69596a64694e324d6966513d3d000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000043c40b598c485d11e05b4306b522e2b539264d2200000000000000000000000000000000000000000000000000aad76149644da200000000000000000000000000000000000000000000000000aad761493a04de00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x02571e18ab3a637cae938b194223d86287aedf715a481e5160b226529ad1858e",
      "signature": {
        "s": "0x6bccf77811126c600b6be21aff0e39d3fa510c47eca872a2f75a3678c5ac11c0",
        "r": "0x5202db822527d1a7659c46d8738cdd0b2efb38db2ed82633c892eb240b6c873e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2d3ca42ab6a507f934151a26ce9eb9707c801b8da432c79f37bc4aaf15780f19",
      "signature": {
        "s": "0x79488df9be68880ccb2e53a74b94d5190b8a2d2c38126796e5714c2419962967",
        "r": "0xa7b865bdca78f155f187df8aeaebb40099628c39d7788cb84fa221f714ca5710",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2771140",
    "total": "64672633"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2771140",
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
            "amount": "27699462432326884475796"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2771"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkYTE4MjRjMS00NDFmLTU3ODAtYTgyYS00MzU0YmZiYjdiN2MifQ==",
    "nonce": 111632,
    "balances": {
      "current": "273135548794625145520344",
      "previous": "273135548794625148294255"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x43c40b598c485d11e05b4306b522e2b539264d22",
    "nonce": 30,
    "balances": {
      "current": "48087558883921314",
      "previous": "48087558881150174"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:21.232Z",
  "updated": "2022-05-04T08:59:21.308Z",
  "id": "627240697832e20011830d4a"
}
```
* *stageAmount*: `48087558883921314`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000002a48c40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002a48c40000000000000000000000000000000000000000000000000000000003dad37902571e18ab3a637cae938b194223d86287aedf715a481e5160b226529ad1858e5202db822527d1a7659c46d8738cdd0b2efb38db2ed82633c892eb240b6c873e6bccf77811126c600b6be21aff0e39d3fa510c47eca872a2f75a3678c5ac11c0000000000000000000000000000000000000000000000000000000000000001b2d3ca42ab6a507f934151a26ce9eb9707c801b8da432c79f37bc4aaf15780f19a7b865bdca78f155f187df8aeaebb40099628c39d7788cb84fa221f714ca571079488df9be68880ccb2e53a74b94d5190b8a2d2c38126796e5714c2419962967000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b410000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039d6b5305e8d7ccd40d80000000000000000000000000000000000000000000039d6b5305e8d7cf7946f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000ad30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd97431428d98743940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b595445344d6a526a4d5330304e44466d4c5455334f44417459546779595330304d7a5530596d5a69596a64694e324d6966513d3d000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000043c40b598c485d11e05b4306b522e2b539264d2200000000000000000000000000000000000000000000000000aad76149644da200000000000000000000000000000000000000000000000000aad761493a04de00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x02571e18ab3a637cae938b194223d86287aedf715a481e5160b226529ad1858e",
      "signature": {
        "s": "0x6bccf77811126c600b6be21aff0e39d3fa510c47eca872a2f75a3678c5ac11c0",
        "r": "0x5202db822527d1a7659c46d8738cdd0b2efb38db2ed82633c892eb240b6c873e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2d3ca42ab6a507f934151a26ce9eb9707c801b8da432c79f37bc4aaf15780f19",
      "signature": {
        "s": "0x79488df9be68880ccb2e53a74b94d5190b8a2d2c38126796e5714c2419962967",
        "r": "0xa7b865bdca78f155f187df8aeaebb40099628c39d7788cb84fa221f714ca5710",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2771140",
    "total": "64672633"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2771140",
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
            "amount": "27699462432326884475796"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2771"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkYTE4MjRjMS00NDFmLTU3ODAtYTgyYS00MzU0YmZiYjdiN2MifQ==",
    "nonce": 111632,
    "balances": {
      "current": "273135548794625145520344",
      "previous": "273135548794625148294255"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x43c40b598c485d11e05b4306b522e2b539264d22",
    "nonce": 30,
    "balances": {
      "current": "48087558883921314",
      "previous": "48087558881150174"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:21.232Z",
  "updated": "2022-05-04T08:59:21.308Z",
  "id": "627240697832e20011830d4a"
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
0x0f200f9b00000000000000000000000000000000000000000000000000aad76149644da20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `48087558883921314`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`