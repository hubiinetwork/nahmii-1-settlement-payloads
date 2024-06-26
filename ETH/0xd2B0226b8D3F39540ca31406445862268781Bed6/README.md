# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd2B0226b8D3F39540ca31406445862268781Bed6`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000004b2cf800000000000000000000000000000000000000000000000000000000004b2cf8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004b2cf800000000000000000000000000000000000000000000000000000000004b2cf8b273683b77db9fe26b23ed8dfc48732f18f72b86fbf11cd4c2d4a0801be8901ac026600a283c1b118e967103c7457d7ae16b97ba9bbe6fbbcafc352b91cd034b4a2d23129abc70c64c285d61dd023755e83efcc6f4c55659e1f4b505eb1ae674000000000000000000000000000000000000000000000000000000000000001c088dbfa094f399451c3b2e77268122fd923ef5e843cd177ccfa5979f8c79dd3ccafc44304f415590a73f26e604787a55cb13794c75d7686a0f12e24b5e05379f0d37a0390bd440a8dbe393522d87364e23e3a9e3136f4f7c2c99149c4e4928c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000081300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c328fab9000000000000000000000000000000000000000000000000002386f2c3743aef00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000133e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a6fac00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a67314f47526a4e433030597a51324c5455314d44417459575a6a4d6931695a4759794d4459784e32493059574d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d2b0226b8d3f39540ca31406445862268781bed600000000000000000000000000000000000000000000000000000000004b2cf8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb273683b77db9fe26b23ed8dfc48732f18f72b86fbf11cd4c2d4a0801be8901a",
      "signature": {
        "s": "0x4a2d23129abc70c64c285d61dd023755e83efcc6f4c55659e1f4b505eb1ae674",
        "r": "0xc026600a283c1b118e967103c7457d7ae16b97ba9bbe6fbbcafc352b91cd034b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x088dbfa094f399451c3b2e77268122fd923ef5e843cd177ccfa5979f8c79dd3c",
      "signature": {
        "s": "0x0d37a0390bd440a8dbe393522d87364e23e3a9e3136f4f7c2c99149c4e4928c9",
        "r": "0xcafc44304f415590a73f26e604787a55cb13794c75d7686a0f12e24b5e05379f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4926712",
    "total": "4926712"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4926712",
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
            "amount": "683948"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4926"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2Mzg1OGRjNC00YzQ2LTU1MDAtYWZjMi1iZGYyMDYxN2I0YWMifQ==",
    "nonce": 2067,
    "balances": {
      "current": "10000001399323321",
      "previous": "10000001404254959"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd2b0226b8d3f39540ca31406445862268781bed6",
    "nonce": 20,
    "balances": {
      "current": "4926712",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:14:09.874Z",
  "updated": "2020-05-22T08:14:09.962Z",
  "id": "5ec789d1e5756b00111b8213"
}
```
* *stageAmount*: `4926712`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000004b2cf8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004b2cf800000000000000000000000000000000000000000000000000000000004b2cf8b273683b77db9fe26b23ed8dfc48732f18f72b86fbf11cd4c2d4a0801be8901ac026600a283c1b118e967103c7457d7ae16b97ba9bbe6fbbcafc352b91cd034b4a2d23129abc70c64c285d61dd023755e83efcc6f4c55659e1f4b505eb1ae674000000000000000000000000000000000000000000000000000000000000001c088dbfa094f399451c3b2e77268122fd923ef5e843cd177ccfa5979f8c79dd3ccafc44304f415590a73f26e604787a55cb13794c75d7686a0f12e24b5e05379f0d37a0390bd440a8dbe393522d87364e23e3a9e3136f4f7c2c99149c4e4928c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000081300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c328fab9000000000000000000000000000000000000000000000000002386f2c3743aef00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000133e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a6fac00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a67314f47526a4e433030597a51324c5455314d44417459575a6a4d6931695a4759794d4459784e32493059574d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d2b0226b8d3f39540ca31406445862268781bed600000000000000000000000000000000000000000000000000000000004b2cf8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb273683b77db9fe26b23ed8dfc48732f18f72b86fbf11cd4c2d4a0801be8901a",
      "signature": {
        "s": "0x4a2d23129abc70c64c285d61dd023755e83efcc6f4c55659e1f4b505eb1ae674",
        "r": "0xc026600a283c1b118e967103c7457d7ae16b97ba9bbe6fbbcafc352b91cd034b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x088dbfa094f399451c3b2e77268122fd923ef5e843cd177ccfa5979f8c79dd3c",
      "signature": {
        "s": "0x0d37a0390bd440a8dbe393522d87364e23e3a9e3136f4f7c2c99149c4e4928c9",
        "r": "0xcafc44304f415590a73f26e604787a55cb13794c75d7686a0f12e24b5e05379f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4926712",
    "total": "4926712"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4926712",
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
            "amount": "683948"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4926"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2Mzg1OGRjNC00YzQ2LTU1MDAtYWZjMi1iZGYyMDYxN2I0YWMifQ==",
    "nonce": 2067,
    "balances": {
      "current": "10000001399323321",
      "previous": "10000001404254959"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd2b0226b8d3f39540ca31406445862268781bed6",
    "nonce": 20,
    "balances": {
      "current": "4926712",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:14:09.874Z",
  "updated": "2020-05-22T08:14:09.962Z",
  "id": "5ec789d1e5756b00111b8213"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000004b2cf80000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4926712`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``
