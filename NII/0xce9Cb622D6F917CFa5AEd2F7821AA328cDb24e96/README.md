# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xce9Cb622D6F917CFa5AEd2F7821AA328cDb24e96`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000001d40f11ba0dbec1300000000000000000000000000000000000000000000000000000016df03b04d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000016df03b04d00000000000000000000000000000000000000000000000000000215c661f75d59136e052036c2c151fb0c724dc6e32391add0f8cc159381ee8caaf357b10f6485a04c4c3468093a090ba0e6f1aa361e3daeaf51ec5e4a4f329015679f8532d808a1e18f0a985652912a76e7544817beb036921852f547673401f4d441bb1561000000000000000000000000000000000000000000000000000000000000001be33e7ddc386f56bf68f64a79a81fced0616b1ae6403797c0964411bd135484096eab3f2a22e556edb2a8440b393db38783eec9e3b9b3ad61931ed11ead546999353501ae31b700d9fc199a135f27500cc2f9583e132fe91b0ffde201fdb9dc54000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afd7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000524375e692c6af3ae06300000000000000000000000000000000000000000000524375e692dd941972e900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000005dae2390000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d758280b28067d30590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a5759304e4455784f53316a597a45334c54566c596d4d744f544d794d69307a4f4463344f544e6b4e5459315a44556966513d3d0000000000000000000000000000000000000000000000000000000000000029000000000000000000000000ce9cb622d6f917cfa5aed2f7821aa328cdb24e960000000000000000000000000000000000000000000000001d40f11ba0dbec130000000000000000000000000000000000000000000000001d40f104c1d83bc600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x59136e052036c2c151fb0c724dc6e32391add0f8cc159381ee8caaf357b10f64",
      "signature": {
        "s": "0x08a1e18f0a985652912a76e7544817beb036921852f547673401f4d441bb1561",
        "r": "0x85a04c4c3468093a090ba0e6f1aa361e3daeaf51ec5e4a4f329015679f8532d8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe33e7ddc386f56bf68f64a79a81fced0616b1ae6403797c0964411bd13548409",
      "signature": {
        "s": "0x353501ae31b700d9fc199a135f27500cc2f9583e132fe91b0ffde201fdb9dc54",
        "r": "0x6eab3f2a22e556edb2a8440b393db38783eec9e3b9b3ad61931ed11ead546999",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "98230841421",
    "total": "2292545877853"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "98230841421",
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
            "amount": "27584234729736721215577"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "98230841"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZWY0NDUxOS1jYzE3LTVlYmMtOTMyMi0zODc4OTNkNTY1ZDUifQ==",
    "nonce": 110551,
    "balances": {
      "current": "388478479087378569551971",
      "previous": "388478479087476898624233"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce9cb622d6f917cfa5aed2f7821aa328cdb24e96",
    "nonce": 41,
    "balances": {
      "current": "2107949726574570515",
      "previous": "2107949628343729094"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:51.429Z",
  "updated": "2022-05-04T08:53:51.503Z",
  "id": "62723f1f3592fd001130b4fa"
}
```
* *stageAmount*: `2107949726574570515`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000016df03b04d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000016df03b04d00000000000000000000000000000000000000000000000000000215c661f75d59136e052036c2c151fb0c724dc6e32391add0f8cc159381ee8caaf357b10f6485a04c4c3468093a090ba0e6f1aa361e3daeaf51ec5e4a4f329015679f8532d808a1e18f0a985652912a76e7544817beb036921852f547673401f4d441bb1561000000000000000000000000000000000000000000000000000000000000001be33e7ddc386f56bf68f64a79a81fced0616b1ae6403797c0964411bd135484096eab3f2a22e556edb2a8440b393db38783eec9e3b9b3ad61931ed11ead546999353501ae31b700d9fc199a135f27500cc2f9583e132fe91b0ffde201fdb9dc54000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afd7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000524375e692c6af3ae06300000000000000000000000000000000000000000000524375e692dd941972e900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000005dae2390000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d758280b28067d30590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a5759304e4455784f53316a597a45334c54566c596d4d744f544d794d69307a4f4463344f544e6b4e5459315a44556966513d3d0000000000000000000000000000000000000000000000000000000000000029000000000000000000000000ce9cb622d6f917cfa5aed2f7821aa328cdb24e960000000000000000000000000000000000000000000000001d40f11ba0dbec130000000000000000000000000000000000000000000000001d40f104c1d83bc600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x59136e052036c2c151fb0c724dc6e32391add0f8cc159381ee8caaf357b10f64",
      "signature": {
        "s": "0x08a1e18f0a985652912a76e7544817beb036921852f547673401f4d441bb1561",
        "r": "0x85a04c4c3468093a090ba0e6f1aa361e3daeaf51ec5e4a4f329015679f8532d8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe33e7ddc386f56bf68f64a79a81fced0616b1ae6403797c0964411bd13548409",
      "signature": {
        "s": "0x353501ae31b700d9fc199a135f27500cc2f9583e132fe91b0ffde201fdb9dc54",
        "r": "0x6eab3f2a22e556edb2a8440b393db38783eec9e3b9b3ad61931ed11ead546999",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "98230841421",
    "total": "2292545877853"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "98230841421",
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
            "amount": "27584234729736721215577"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "98230841"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZWY0NDUxOS1jYzE3LTVlYmMtOTMyMi0zODc4OTNkNTY1ZDUifQ==",
    "nonce": 110551,
    "balances": {
      "current": "388478479087378569551971",
      "previous": "388478479087476898624233"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce9cb622d6f917cfa5aed2f7821aa328cdb24e96",
    "nonce": 41,
    "balances": {
      "current": "2107949726574570515",
      "previous": "2107949628343729094"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:51.429Z",
  "updated": "2022-05-04T08:53:51.503Z",
  "id": "62723f1f3592fd001130b4fa"
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
0x0f200f9b0000000000000000000000000000000000000000000000001d40f11ba0dbec130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2107949726574570515`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`