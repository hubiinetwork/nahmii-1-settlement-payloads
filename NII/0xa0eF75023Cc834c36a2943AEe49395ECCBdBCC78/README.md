# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa0eF75023Cc834c36a2943AEe49395ECCBdBCC78`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000016dbcb38c8e6d205a00000000000000000000000000000000000000000000000000000000c67fdd170000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000c67fdd1700000000000000000000000000000000000000000000000000000012189ec8d27c557ae3b63529f85da2e7a2f69f7d63acce069315bfc12bf67e7dbd5ab421ac998b80f7ef1c540ffcf5462e8e60c0343b56ff447f08028f380a4ffe6af83ab13a16b2bfe8432da45ef62bfd7dbc7fe35d33188de107fa68cc9a9765c6088170000000000000000000000000000000000000000000000000000000000000001bd1e011266f2492f8be5588a59a14fc285a06aa356f480c159863868c3cde0a202b54c88d4ecd9ebd9ffc5876ce43c6a8e999c3b27428b7a508d0d7a0d4242f02502b392fe78166679019ca4e8230ba341f6c7ba2846382748aafed46b29c2f03000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae87000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009621b48205ff89fbebf2000000000000000000000000000000000000000000009621b482060050ae99e500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000032d0dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5fccb0d994364b3f70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e3255314f5449354f5331694d6a59304c5455774d6d45744f4449314d4330784d5441304f5755304d574a6c4f44636966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000a0ef75023cc834c36a2943aee49395eccbdbcc780000000000000000000000000000000000000000000000016dbcb38c8e6d205a0000000000000000000000000000000000000000000000016dbcb38bc7ed434300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c557ae3b63529f85da2e7a2f69f7d63acce069315bfc12bf67e7dbd5ab421ac",
      "signature": {
        "s": "0x3a16b2bfe8432da45ef62bfd7dbc7fe35d33188de107fa68cc9a9765c6088170",
        "r": "0x998b80f7ef1c540ffcf5462e8e60c0343b56ff447f08028f380a4ffe6af83ab1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd1e011266f2492f8be5588a59a14fc285a06aa356f480c159863868c3cde0a20",
      "signature": {
        "s": "0x502b392fe78166679019ca4e8230ba341f6c7ba2846382748aafed46b29c2f03",
        "r": "0x2b54c88d4ecd9ebd9ffc5876ce43c6a8e999c3b27428b7a508d0d7a0d4242f02",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3330268439",
    "total": "77722470610"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3330268439",
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
            "amount": "27264056664938749670391"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3330268"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzN2U1OTI5OS1iMjY0LTUwMmEtODI1MC0xMTA0OWU0MWJlODcifQ==",
    "nonce": 110215,
    "balances": {
      "current": "708976721950148086459378",
      "previous": "708976721950151420058085"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa0ef75023cc834c36a2943aee49395eccbdbcc78",
    "nonce": 36,
    "balances": {
      "current": "26354136535731609690",
      "previous": "26354136532401341251"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:08.625Z",
  "updated": "2022-05-04T08:52:08.939Z",
  "id": "62723eb8bbd75600116d051a"
}
```
* *stageAmount*: `26354136535731609690`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000c67fdd170000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000c67fdd1700000000000000000000000000000000000000000000000000000012189ec8d27c557ae3b63529f85da2e7a2f69f7d63acce069315bfc12bf67e7dbd5ab421ac998b80f7ef1c540ffcf5462e8e60c0343b56ff447f08028f380a4ffe6af83ab13a16b2bfe8432da45ef62bfd7dbc7fe35d33188de107fa68cc9a9765c6088170000000000000000000000000000000000000000000000000000000000000001bd1e011266f2492f8be5588a59a14fc285a06aa356f480c159863868c3cde0a202b54c88d4ecd9ebd9ffc5876ce43c6a8e999c3b27428b7a508d0d7a0d4242f02502b392fe78166679019ca4e8230ba341f6c7ba2846382748aafed46b29c2f03000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae87000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009621b48205ff89fbebf2000000000000000000000000000000000000000000009621b482060050ae99e500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000032d0dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5fccb0d994364b3f70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e3255314f5449354f5331694d6a59304c5455774d6d45744f4449314d4330784d5441304f5755304d574a6c4f44636966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000a0ef75023cc834c36a2943aee49395eccbdbcc780000000000000000000000000000000000000000000000016dbcb38c8e6d205a0000000000000000000000000000000000000000000000016dbcb38bc7ed434300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c557ae3b63529f85da2e7a2f69f7d63acce069315bfc12bf67e7dbd5ab421ac",
      "signature": {
        "s": "0x3a16b2bfe8432da45ef62bfd7dbc7fe35d33188de107fa68cc9a9765c6088170",
        "r": "0x998b80f7ef1c540ffcf5462e8e60c0343b56ff447f08028f380a4ffe6af83ab1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd1e011266f2492f8be5588a59a14fc285a06aa356f480c159863868c3cde0a20",
      "signature": {
        "s": "0x502b392fe78166679019ca4e8230ba341f6c7ba2846382748aafed46b29c2f03",
        "r": "0x2b54c88d4ecd9ebd9ffc5876ce43c6a8e999c3b27428b7a508d0d7a0d4242f02",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3330268439",
    "total": "77722470610"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3330268439",
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
            "amount": "27264056664938749670391"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3330268"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzN2U1OTI5OS1iMjY0LTUwMmEtODI1MC0xMTA0OWU0MWJlODcifQ==",
    "nonce": 110215,
    "balances": {
      "current": "708976721950148086459378",
      "previous": "708976721950151420058085"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa0ef75023cc834c36a2943aee49395eccbdbcc78",
    "nonce": 36,
    "balances": {
      "current": "26354136535731609690",
      "previous": "26354136532401341251"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:08.625Z",
  "updated": "2022-05-04T08:52:08.939Z",
  "id": "62723eb8bbd75600116d051a"
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
0x0f200f9b0000000000000000000000000000000000000000000000016dbcb38c8e6d205a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `26354136535731609690`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`