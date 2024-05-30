# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x20A1E9779253d82d08E5ccD4E407E1Fd09BaF239`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000003000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000003b2a5eb63e381d900dc916efe700a56b9568e58f187b94f9f72408cb287dc388a77677923cdbdb5f34ccd76dd0cb36995f237e50e70242c0f4ad42fc406a939bc4c0e64a015eba91a70b7ecd5d3c21a6843358f6d238dcd0ab2b8eab95d071581000000000000000000000000000000000000000000000000000000000000001b550c5c08e7487d358ac24b0a7d19f0f781944b3189837bb665796a01a29261c4ec42d934be2d2b613da6f2c874bf3ad84bfe42700362b3aab1e0b961bff4b01d1443a834abf5b7de66d3bc43fbf12bafdfe00abffa5e8524c4bef9884ce0813c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000037600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cada7a4b000000000000000000000000000000000000000000000000002386f2cada7a4f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008796100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d5455774e6a417a596930304d6d49354c54566a4f4455744f5749325953316d4f5449354e5751334e3251325954496966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000020a1e9779253d82d08e5ccd4e407e1fd09baf2390000000000000000000000000000000000000000000000000000000000000003000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb2a5eb63e381d900dc916efe700a56b9568e58f187b94f9f72408cb287dc388a",
      "signature": {
        "s": "0x4c0e64a015eba91a70b7ecd5d3c21a6843358f6d238dcd0ab2b8eab95d071581",
        "r": "0x77677923cdbdb5f34ccd76dd0cb36995f237e50e70242c0f4ad42fc406a939bc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x550c5c08e7487d358ac24b0a7d19f0f781944b3189837bb665796a01a29261c4",
      "signature": {
        "s": "0x1443a834abf5b7de66d3bc43fbf12bafdfe00abffa5e8524c4bef9884ce0813c",
        "r": "0xec42d934be2d2b613da6f2c874bf3ad84bfe42700362b3aab1e0b961bff4b01d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3",
    "total": "3"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3",
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
            "amount": "555361"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjMTUwNjAzYi00MmI5LTVjODUtOWI2YS1mOTI5NWQ3N2Q2YTIifQ==",
    "nonce": 886,
    "balances": {
      "current": "10000001528396363",
      "previous": "10000001528396367"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x20a1e9779253d82d08e5ccd4e407e1fd09baf239",
    "nonce": 20,
    "balances": {
      "current": "3",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:15.492Z",
  "updated": "2020-05-22T08:05:15.570Z",
  "id": "5ec787bb005df800101bc33e"
}
```
* *stageAmount*: `3`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000003000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000003b2a5eb63e381d900dc916efe700a56b9568e58f187b94f9f72408cb287dc388a77677923cdbdb5f34ccd76dd0cb36995f237e50e70242c0f4ad42fc406a939bc4c0e64a015eba91a70b7ecd5d3c21a6843358f6d238dcd0ab2b8eab95d071581000000000000000000000000000000000000000000000000000000000000001b550c5c08e7487d358ac24b0a7d19f0f781944b3189837bb665796a01a29261c4ec42d934be2d2b613da6f2c874bf3ad84bfe42700362b3aab1e0b961bff4b01d1443a834abf5b7de66d3bc43fbf12bafdfe00abffa5e8524c4bef9884ce0813c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000037600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cada7a4b000000000000000000000000000000000000000000000000002386f2cada7a4f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008796100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d5455774e6a417a596930304d6d49354c54566a4f4455744f5749325953316d4f5449354e5751334e3251325954496966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000020a1e9779253d82d08e5ccd4e407e1fd09baf2390000000000000000000000000000000000000000000000000000000000000003000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb2a5eb63e381d900dc916efe700a56b9568e58f187b94f9f72408cb287dc388a",
      "signature": {
        "s": "0x4c0e64a015eba91a70b7ecd5d3c21a6843358f6d238dcd0ab2b8eab95d071581",
        "r": "0x77677923cdbdb5f34ccd76dd0cb36995f237e50e70242c0f4ad42fc406a939bc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x550c5c08e7487d358ac24b0a7d19f0f781944b3189837bb665796a01a29261c4",
      "signature": {
        "s": "0x1443a834abf5b7de66d3bc43fbf12bafdfe00abffa5e8524c4bef9884ce0813c",
        "r": "0xec42d934be2d2b613da6f2c874bf3ad84bfe42700362b3aab1e0b961bff4b01d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3",
    "total": "3"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3",
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
            "amount": "555361"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjMTUwNjAzYi00MmI5LTVjODUtOWI2YS1mOTI5NWQ3N2Q2YTIifQ==",
    "nonce": 886,
    "balances": {
      "current": "10000001528396363",
      "previous": "10000001528396367"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x20a1e9779253d82d08e5ccd4e407e1fd09baf239",
    "nonce": 20,
    "balances": {
      "current": "3",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:15.492Z",
  "updated": "2020-05-22T08:05:15.570Z",
  "id": "5ec787bb005df800101bc33e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000030000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``