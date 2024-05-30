# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb873e51b06B2DbEb43737430D878B8F089691D1d`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002d3e6eb394b7d7059d00000000000000000000000000000000000000000000000000000019ced3463e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000019ced3463e0000000000000000000000000000000000000000000000000000025a4dd7e62af6654a0baf5195a00741f8cfa978fd2044db552c1123a0c1bd4ace7c812e799697a9e74e094ae7ca7b5f6a2bbe8f0ffe35ca87aa4c1e6c6e924d5d1ad8d776ea20a7572b6c2cf0d41b8cea793e524b6e4f40edba4243a276114c1358b8a32eda000000000000000000000000000000000000000000000000000000000000001b4716cb148d536ea2ee69a70892fd227e5c2138a82bd2837a17aa1746c906b19507f7cea66348c140430dd91d85da8eb8b53127869b99cd571a1dbf1450b16fcf3afc44453de19d81747445fabf12df32f13c047e6611c23fea1cc226be26b9bf000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3a7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bce791f5882366a9caa000000000000000000000000000000000000000000003bce791f589c0bd93bce00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000069b58e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd166d4b268f2d57610000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f4459334e444a6b4d7930795957526a4c5455304d5749744f474979596930305a5441355a474e6d4f4749354d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000023000000000000000000000000b873e51b06b2dbeb43737430d878b8f089691d1d00000000000000000000000000000000000000000000002d3e6eb394b7d7059d00000000000000000000000000000000000000000000002d3e6eb37ae903bf5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf6654a0baf5195a00741f8cfa978fd2044db552c1123a0c1bd4ace7c812e7996",
      "signature": {
        "s": "0x20a7572b6c2cf0d41b8cea793e524b6e4f40edba4243a276114c1358b8a32eda",
        "r": "0x97a9e74e094ae7ca7b5f6a2bbe8f0ffe35ca87aa4c1e6c6e924d5d1ad8d776ea",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4716cb148d536ea2ee69a70892fd227e5c2138a82bd2837a17aa1746c906b195",
      "signature": {
        "s": "0x3afc44453de19d81747445fabf12df32f13c047e6611c23fea1cc226be26b9bf",
        "r": "0x07f7cea66348c140430dd91d85da8eb8b53127869b99cd571a1dbf1450b16fcf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "110844134974",
    "total": "2586876306986"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "110844134974",
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
            "amount": "27690178885108315805537"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "110844134"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlODY3NDJkMy0yYWRjLTU0MWItOGIyYi00ZTA5ZGNmOGI5MmMifQ==",
    "nonce": 111527,
    "balances": {
      "current": "282428379560412384500906",
      "previous": "282428379560523339480014"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb873e51b06b2dbeb43737430d878b8f089691d1d",
    "nonce": 35,
    "balances": {
      "current": "834602213846040380829",
      "previous": "834602213735196245855"
    }
  },
  "blockNumber": "14709980",
  "created": "2022-05-04T08:58:46.767Z",
  "updated": "2022-05-04T08:58:46.860Z",
  "id": "627240463592fd001130b655"
}
```
* *stageAmount*: `834602213846040380829`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000019ced3463e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000019ced3463e0000000000000000000000000000000000000000000000000000025a4dd7e62af6654a0baf5195a00741f8cfa978fd2044db552c1123a0c1bd4ace7c812e799697a9e74e094ae7ca7b5f6a2bbe8f0ffe35ca87aa4c1e6c6e924d5d1ad8d776ea20a7572b6c2cf0d41b8cea793e524b6e4f40edba4243a276114c1358b8a32eda000000000000000000000000000000000000000000000000000000000000001b4716cb148d536ea2ee69a70892fd227e5c2138a82bd2837a17aa1746c906b19507f7cea66348c140430dd91d85da8eb8b53127869b99cd571a1dbf1450b16fcf3afc44453de19d81747445fabf12df32f13c047e6611c23fea1cc226be26b9bf000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3a7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bce791f5882366a9caa000000000000000000000000000000000000000000003bce791f589c0bd93bce00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000069b58e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd166d4b268f2d57610000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f4459334e444a6b4d7930795957526a4c5455304d5749744f474979596930305a5441355a474e6d4f4749354d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000023000000000000000000000000b873e51b06b2dbeb43737430d878b8f089691d1d00000000000000000000000000000000000000000000002d3e6eb394b7d7059d00000000000000000000000000000000000000000000002d3e6eb37ae903bf5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf6654a0baf5195a00741f8cfa978fd2044db552c1123a0c1bd4ace7c812e7996",
      "signature": {
        "s": "0x20a7572b6c2cf0d41b8cea793e524b6e4f40edba4243a276114c1358b8a32eda",
        "r": "0x97a9e74e094ae7ca7b5f6a2bbe8f0ffe35ca87aa4c1e6c6e924d5d1ad8d776ea",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4716cb148d536ea2ee69a70892fd227e5c2138a82bd2837a17aa1746c906b195",
      "signature": {
        "s": "0x3afc44453de19d81747445fabf12df32f13c047e6611c23fea1cc226be26b9bf",
        "r": "0x07f7cea66348c140430dd91d85da8eb8b53127869b99cd571a1dbf1450b16fcf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "110844134974",
    "total": "2586876306986"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "110844134974",
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
            "amount": "27690178885108315805537"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "110844134"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlODY3NDJkMy0yYWRjLTU0MWItOGIyYi00ZTA5ZGNmOGI5MmMifQ==",
    "nonce": 111527,
    "balances": {
      "current": "282428379560412384500906",
      "previous": "282428379560523339480014"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb873e51b06b2dbeb43737430d878b8f089691d1d",
    "nonce": 35,
    "balances": {
      "current": "834602213846040380829",
      "previous": "834602213735196245855"
    }
  },
  "blockNumber": "14709980",
  "created": "2022-05-04T08:58:46.767Z",
  "updated": "2022-05-04T08:58:46.860Z",
  "id": "627240463592fd001130b655"
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
0x0f200f9b00000000000000000000000000000000000000000000002d3e6eb394b7d7059d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `834602213846040380829`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`