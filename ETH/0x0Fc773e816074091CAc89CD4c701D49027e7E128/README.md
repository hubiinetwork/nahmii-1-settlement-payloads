# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0Fc773e816074091CAc89CD4c701D49027e7E128`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000013b130000000000000000000000000000000000000000000000000000000000013b1300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000013b130000000000000000000000000000000000000000000000000000000000013b1356b19cdc70f3c779efc03993165b5fc782416d1dfe67a33b8499b5ab5f8f71b9ee7ebe4a0bd4feb485813d1230749c81a78c8db31f2d5e9f25a3fb9240c206750a67157162d59429ce48a7efe49a86ccb9c25cbfa19cdf3ba9f2b2f709207ac6000000000000000000000000000000000000000000000000000000000000001baa0c486d3a4169cb62f0059b4335e8416dfd2ebde70e65fb7b052a105c5a75c4b4cb3c17af55858f2a93d72baf979031ff9be88470362ce3a1579ac2471a91f809931ec8a120c2329551ef73ecc5ecc6d6919eb6fa373f2021151034235b43f1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000060300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c65b3822000000000000000000000000000000000000000000000000002386f2c65c738500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099f2c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d544e6a596d4d355a53316a5957526c4c5456694e5751744f57466d4d7930795a4464694e7a4269597a6c684e47596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000fc773e816074091cac89cd4c701d49027e7e1280000000000000000000000000000000000000000000000000000000000013b13000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x56b19cdc70f3c779efc03993165b5fc782416d1dfe67a33b8499b5ab5f8f71b9",
      "signature": {
        "s": "0x0a67157162d59429ce48a7efe49a86ccb9c25cbfa19cdf3ba9f2b2f709207ac6",
        "r": "0xee7ebe4a0bd4feb485813d1230749c81a78c8db31f2d5e9f25a3fb9240c20675",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaa0c486d3a4169cb62f0059b4335e8416dfd2ebde70e65fb7b052a105c5a75c4",
      "signature": {
        "s": "0x09931ec8a120c2329551ef73ecc5ecc6d6919eb6fa373f2021151034235b43f1",
        "r": "0xb4cb3c17af55858f2a93d72baf979031ff9be88470362ce3a1579ac2471a91f8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "80659",
    "total": "80659"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "80659",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "630572"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "80"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMTNjYmM5ZS1jYWRlLTViNWQtOWFmMy0yZDdiNzBiYzlhNGYifQ==",
    "nonce": 1539,
    "balances": {
      "current": "10000001452947490",
      "previous": "10000001453028229"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fc773e816074091cac89cd4c701d49027e7e128",
    "nonce": 20,
    "balances": {
      "current": "80659",
      "previous": "0"
    }
  },
  "blockNumber": "10114532",
  "created": "2020-05-22T08:10:20.989Z",
  "updated": "2020-05-22T08:10:21.072Z",
  "id": "5ec788ec005df800101bc42f"
}
```
* *stageAmount*: `80659`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000013b1300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000013b130000000000000000000000000000000000000000000000000000000000013b1356b19cdc70f3c779efc03993165b5fc782416d1dfe67a33b8499b5ab5f8f71b9ee7ebe4a0bd4feb485813d1230749c81a78c8db31f2d5e9f25a3fb9240c206750a67157162d59429ce48a7efe49a86ccb9c25cbfa19cdf3ba9f2b2f709207ac6000000000000000000000000000000000000000000000000000000000000001baa0c486d3a4169cb62f0059b4335e8416dfd2ebde70e65fb7b052a105c5a75c4b4cb3c17af55858f2a93d72baf979031ff9be88470362ce3a1579ac2471a91f809931ec8a120c2329551ef73ecc5ecc6d6919eb6fa373f2021151034235b43f1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000060300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c65b3822000000000000000000000000000000000000000000000000002386f2c65c738500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099f2c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d544e6a596d4d355a53316a5957526c4c5456694e5751744f57466d4d7930795a4464694e7a4269597a6c684e47596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000fc773e816074091cac89cd4c701d49027e7e1280000000000000000000000000000000000000000000000000000000000013b13000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x56b19cdc70f3c779efc03993165b5fc782416d1dfe67a33b8499b5ab5f8f71b9",
      "signature": {
        "s": "0x0a67157162d59429ce48a7efe49a86ccb9c25cbfa19cdf3ba9f2b2f709207ac6",
        "r": "0xee7ebe4a0bd4feb485813d1230749c81a78c8db31f2d5e9f25a3fb9240c20675",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaa0c486d3a4169cb62f0059b4335e8416dfd2ebde70e65fb7b052a105c5a75c4",
      "signature": {
        "s": "0x09931ec8a120c2329551ef73ecc5ecc6d6919eb6fa373f2021151034235b43f1",
        "r": "0xb4cb3c17af55858f2a93d72baf979031ff9be88470362ce3a1579ac2471a91f8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "80659",
    "total": "80659"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "80659",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "630572"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "80"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMTNjYmM5ZS1jYWRlLTViNWQtOWFmMy0yZDdiNzBiYzlhNGYifQ==",
    "nonce": 1539,
    "balances": {
      "current": "10000001452947490",
      "previous": "10000001453028229"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fc773e816074091cac89cd4c701d49027e7e128",
    "nonce": 20,
    "balances": {
      "current": "80659",
      "previous": "0"
    }
  },
  "blockNumber": "10114532",
  "created": "2020-05-22T08:10:20.989Z",
  "updated": "2020-05-22T08:10:21.072Z",
  "id": "5ec788ec005df800101bc42f"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000000000000013b130000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `80659`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``