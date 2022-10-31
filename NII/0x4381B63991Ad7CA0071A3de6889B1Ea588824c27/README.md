# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x4381B63991Ad7CA0071A3de6889B1Ea588824c27`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000804e1ea08248c0d300000000000000000000000000000000000000000000000000000017622217d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000017622217d600000000000000000000000000000000000000000000005e7052c5e512177071b37fad61e755efca42dd35f37039c39d7ae5121de6b9b836ff5589d8a3a4a17e5495e2825ed084e9c676366a4a39532aa7be8a0233e17975e8e2082c894af2037e0cde95cc31121f106d63bf1d1de4de5849bd9aea533810c454b42e9a0e39c2000000000000000000000000000000000000000000000000000000000000001cd4c7c79ab63c4ad35c1d5381971605f27ae1fff2008b9c762c3d4edc5e1346ff1561cff34c5da308a66dd03586b31192f3f2937a97a9de1702963f89b93f3690369e108156cb53eae57d576a6816d652773d84525759478888412bb370033eea000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b168000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004aefbfc2fe0d5b5e8f90000000000000000000000000000000000000000000004aefbfc2fe24c37d1a9f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000005fc73390000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d937dbde09c6e478800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e3245354e7a55344e4330304e6a5a6d4c5456694d475974595445334f433032596a5979596d4a684f4463354d6a556966513d3d000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000004381b63991ad7ca0071a3de6889b1ea588824c27000000000000000000000000000000000000000000000000804e1ea08248c0d3000000000000000000000000000000000000000000000000804e1e892026a8fd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xb37fad61e755efca42dd35f37039c39d7ae5121de6b9b836ff5589d8a3a4a17e",
      "signature": {
        "s": "0x7e0cde95cc31121f106d63bf1d1de4de5849bd9aea533810c454b42e9a0e39c2",
        "r": "0x5495e2825ed084e9c676366a4a39532aa7be8a0233e17975e8e2082c894af203",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd4c7c79ab63c4ad35c1d5381971605f27ae1fff2008b9c762c3d4edc5e1346ff",
      "signature": {
        "s": "0x369e108156cb53eae57d576a6816d652773d84525759478888412bb370033eea",
        "r": "0x1561cff34c5da308a66dd03586b31192f3f2937a97a9de1702963f89b93f3690",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "100430649302",
    "total": "1742087691996677763185"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "100430649302",
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
            "amount": "27618800933168757373056"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "100430649"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmN2E5NzU4NC00NjZmLTViMGYtYTE3OC02YjYyYmJhODc5MjUifQ==",
    "nonce": 110952,
    "balances": {
      "current": "353877709451910375706512",
      "previous": "353877709452010906786463"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4381b63991ad7ca0071a3de6889b1ea588824c27",
    "nonce": 47,
    "balances": {
      "current": "9245360759767613651",
      "previous": "9245360659336964349"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:50.086Z",
  "updated": "2022-05-04T08:55:50.165Z",
  "id": "62723f96bbd75600116d0617"
}
```
* *stageAmount*: `9245360759767613651`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000017622217d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000017622217d600000000000000000000000000000000000000000000005e7052c5e512177071b37fad61e755efca42dd35f37039c39d7ae5121de6b9b836ff5589d8a3a4a17e5495e2825ed084e9c676366a4a39532aa7be8a0233e17975e8e2082c894af2037e0cde95cc31121f106d63bf1d1de4de5849bd9aea533810c454b42e9a0e39c2000000000000000000000000000000000000000000000000000000000000001cd4c7c79ab63c4ad35c1d5381971605f27ae1fff2008b9c762c3d4edc5e1346ff1561cff34c5da308a66dd03586b31192f3f2937a97a9de1702963f89b93f3690369e108156cb53eae57d576a6816d652773d84525759478888412bb370033eea000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b168000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004aefbfc2fe0d5b5e8f90000000000000000000000000000000000000000000004aefbfc2fe24c37d1a9f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000005fc73390000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d937dbde09c6e478800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e3245354e7a55344e4330304e6a5a6d4c5456694d475974595445334f433032596a5979596d4a684f4463354d6a556966513d3d000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000004381b63991ad7ca0071a3de6889b1ea588824c27000000000000000000000000000000000000000000000000804e1ea08248c0d3000000000000000000000000000000000000000000000000804e1e892026a8fd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xb37fad61e755efca42dd35f37039c39d7ae5121de6b9b836ff5589d8a3a4a17e",
      "signature": {
        "s": "0x7e0cde95cc31121f106d63bf1d1de4de5849bd9aea533810c454b42e9a0e39c2",
        "r": "0x5495e2825ed084e9c676366a4a39532aa7be8a0233e17975e8e2082c894af203",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd4c7c79ab63c4ad35c1d5381971605f27ae1fff2008b9c762c3d4edc5e1346ff",
      "signature": {
        "s": "0x369e108156cb53eae57d576a6816d652773d84525759478888412bb370033eea",
        "r": "0x1561cff34c5da308a66dd03586b31192f3f2937a97a9de1702963f89b93f3690",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "100430649302",
    "total": "1742087691996677763185"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "100430649302",
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
            "amount": "27618800933168757373056"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "100430649"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmN2E5NzU4NC00NjZmLTViMGYtYTE3OC02YjYyYmJhODc5MjUifQ==",
    "nonce": 110952,
    "balances": {
      "current": "353877709451910375706512",
      "previous": "353877709452010906786463"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4381b63991ad7ca0071a3de6889b1ea588824c27",
    "nonce": 47,
    "balances": {
      "current": "9245360759767613651",
      "previous": "9245360659336964349"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:50.086Z",
  "updated": "2022-05-04T08:55:50.165Z",
  "id": "62723f96bbd75600116d0617"
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
0x0f200f9b000000000000000000000000000000000000000000000000804e1ea08248c0d30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `9245360759767613651`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`