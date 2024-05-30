# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5c8DF693DF16F1db3c6FE165b8aC0ABd26Ae6617`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000070ce23b5c9f3d5e788000000000000000000000000000000000000000000000000000000186e3c8ce70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000186e3c8ce700000000000000000000000000000000000000000000003417eb02a9bff2a8ae83c8b0bf79a62947316353a1565d814b4b604965f8882cfe3e9a5a48db03aa3912f8fbf786161668896a34fb618e6919c454de21e51d8b1e486247d30d1361845fe7fa326135d5518d62f6f5d31fcc9dc1c3787e9ebdff032b2f9b6b8d811751000000000000000000000000000000000000000000000000000000000000001c94a0c856b80bf042a6c677b2732cb893303bb42e06bed76d99802dac0358459f573968587be638946e86676c4a475527a92e214352feac569fc41a19fe830344178182b84bbbef6162fca5ae836fce65a60b7722e96393bff2aa4586d1ad137b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001acd9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000983c68c2c08eb2a3efbc00000000000000000000000000000000000000000000983c68c2c0a72721924800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000064115a50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c57305cf443690c8490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d44457a4e5749324e7930784f546b784c5455304f475574596a5a6d4d69316c4f475979597a6b774d6a63324e474d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005c8df693df16f1db3c6fe165b8ac0abd26ae6617000000000000000000000000000000000000000000000070ce23b5c9f3d5e788000000000000000000000000000000000000000000000070ce23b5b185995aa100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x83c8b0bf79a62947316353a1565d814b4b604965f8882cfe3e9a5a48db03aa39",
      "signature": {
        "s": "0x5fe7fa326135d5518d62f6f5d31fcc9dc1c3787e9ebdff032b2f9b6b8d811751",
        "r": "0x12f8fbf786161668896a34fb618e6919c454de21e51d8b1e486247d30d136184",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x94a0c856b80bf042a6c677b2732cb893303bb42e06bed76d99802dac0358459f",
      "signature": {
        "s": "0x178182b84bbbef6162fca5ae836fce65a60b7722e96393bff2aa4586d1ad137b",
        "r": "0x573968587be638946e86676c4a475527a92e214352feac569fc41a19fe830344",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "104928677095",
    "total": "960954166043389110446"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "104928677095",
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
            "amount": "27254129255450133186633"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "104928677"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2MDEzNWI2Ny0xOTkxLTU0OGUtYjZmMi1lOGYyYzkwMjc2NGMifQ==",
    "nonce": 109785,
    "balances": {
      "current": "718914058848253186928572",
      "previous": "718914058848358220534344"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c8df693df16f1db3c6fe165b8ac0abd26ae6617",
    "nonce": 46,
    "balances": {
      "current": "2080889252130451744648",
      "previous": "2080889252025523067553"
    }
  },
  "blockNumber": "14709950",
  "created": "2022-05-04T08:49:53.694Z",
  "updated": "2022-05-04T08:49:53.792Z",
  "id": "62723e313592fd001130b401"
}
```
* *stageAmount*: `2080889252130451744648`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000186e3c8ce70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000186e3c8ce700000000000000000000000000000000000000000000003417eb02a9bff2a8ae83c8b0bf79a62947316353a1565d814b4b604965f8882cfe3e9a5a48db03aa3912f8fbf786161668896a34fb618e6919c454de21e51d8b1e486247d30d1361845fe7fa326135d5518d62f6f5d31fcc9dc1c3787e9ebdff032b2f9b6b8d811751000000000000000000000000000000000000000000000000000000000000001c94a0c856b80bf042a6c677b2732cb893303bb42e06bed76d99802dac0358459f573968587be638946e86676c4a475527a92e214352feac569fc41a19fe830344178182b84bbbef6162fca5ae836fce65a60b7722e96393bff2aa4586d1ad137b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074be0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001acd9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000983c68c2c08eb2a3efbc00000000000000000000000000000000000000000000983c68c2c0a72721924800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000064115a50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c57305cf443690c8490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d44457a4e5749324e7930784f546b784c5455304f475574596a5a6d4d69316c4f475979597a6b774d6a63324e474d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005c8df693df16f1db3c6fe165b8ac0abd26ae6617000000000000000000000000000000000000000000000070ce23b5c9f3d5e788000000000000000000000000000000000000000000000070ce23b5b185995aa100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x83c8b0bf79a62947316353a1565d814b4b604965f8882cfe3e9a5a48db03aa39",
      "signature": {
        "s": "0x5fe7fa326135d5518d62f6f5d31fcc9dc1c3787e9ebdff032b2f9b6b8d811751",
        "r": "0x12f8fbf786161668896a34fb618e6919c454de21e51d8b1e486247d30d136184",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x94a0c856b80bf042a6c677b2732cb893303bb42e06bed76d99802dac0358459f",
      "signature": {
        "s": "0x178182b84bbbef6162fca5ae836fce65a60b7722e96393bff2aa4586d1ad137b",
        "r": "0x573968587be638946e86676c4a475527a92e214352feac569fc41a19fe830344",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "104928677095",
    "total": "960954166043389110446"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "104928677095",
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
            "amount": "27254129255450133186633"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "104928677"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2MDEzNWI2Ny0xOTkxLTU0OGUtYjZmMi1lOGYyYzkwMjc2NGMifQ==",
    "nonce": 109785,
    "balances": {
      "current": "718914058848253186928572",
      "previous": "718914058848358220534344"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c8df693df16f1db3c6fe165b8ac0abd26ae6617",
    "nonce": 46,
    "balances": {
      "current": "2080889252130451744648",
      "previous": "2080889252025523067553"
    }
  },
  "blockNumber": "14709950",
  "created": "2022-05-04T08:49:53.694Z",
  "updated": "2022-05-04T08:49:53.792Z",
  "id": "62723e313592fd001130b401"
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
0x0f200f9b000000000000000000000000000000000000000000000070ce23b5c9f3d5e7880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2080889252130451744648`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`