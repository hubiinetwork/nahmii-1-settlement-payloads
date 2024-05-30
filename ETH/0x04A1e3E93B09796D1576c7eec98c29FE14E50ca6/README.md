# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x04A1e3E93B09796D1576c7eec98c29FE14E50ca6`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000100d7c3a18f79ac79e6b5c50ac99368b8e0dda86219a7450e6aa4dfb93f0a6050ea58cc8b73310901dcb7709d43981036908bd8630f01188b77e284b1730acba36a003d82bcb3b4f87baef520c2ca37ba9cbf1679923c17c2c6c40da75afebb5f52000000000000000000000000000000000000000000000000000000000000001b0472caab4a4599023d00b2b3a48a1f25ebad390d6cc5c37167da6b1d1eee3cfb43693e69d8010e892a2d6dadff392c6514478ab6511109bb00afe6ce2a37b5f33d1cb6799eb3e750d6915ecd274d214bb4908703d578e3ffc1650f70d4946ba5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005e500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c66fbbf4000000000000000000000000000000000000000000000000002386f2c66fbcf500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000999f700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e54686b4d4463785a6930354d444d304c54566d5a6a63744f544a684d7930325a475a6b4f574e6b4f5745314e446b6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000004a1e3e93b09796d1576c7eec98c29fe14e50ca60000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd7c3a18f79ac79e6b5c50ac99368b8e0dda86219a7450e6aa4dfb93f0a6050ea",
      "signature": {
        "s": "0x003d82bcb3b4f87baef520c2ca37ba9cbf1679923c17c2c6c40da75afebb5f52",
        "r": "0x58cc8b73310901dcb7709d43981036908bd8630f01188b77e284b1730acba36a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0472caab4a4599023d00b2b3a48a1f25ebad390d6cc5c37167da6b1d1eee3cfb",
      "signature": {
        "s": "0x3d1cb6799eb3e750d6915ecd274d214bb4908703d578e3ffc1650f70d4946ba5",
        "r": "0x43693e69d8010e892a2d6dadff392c6514478ab6511109bb00afe6ce2a37b5f3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "256",
    "total": "256"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "256",
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
            "amount": "629239"
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
    "data": "eyJyZWYiOiIyNThkMDcxZi05MDM0LTVmZjctOTJhMy02ZGZkOWNkOWE1NDkifQ==",
    "nonce": 1509,
    "balances": {
      "current": "10000001454291956",
      "previous": "10000001454292213"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x04a1e3e93b09796d1576c7eec98c29fe14e50ca6",
    "nonce": 20,
    "balances": {
      "current": "256",
      "previous": "0"
    }
  },
  "blockNumber": "10114531",
  "created": "2020-05-22T08:10:05.898Z",
  "updated": "2020-05-22T08:10:05.993Z",
  "id": "5ec788ddb0c6090011d5aac7"
}
```
* *stageAmount*: `256`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000100d7c3a18f79ac79e6b5c50ac99368b8e0dda86219a7450e6aa4dfb93f0a6050ea58cc8b73310901dcb7709d43981036908bd8630f01188b77e284b1730acba36a003d82bcb3b4f87baef520c2ca37ba9cbf1679923c17c2c6c40da75afebb5f52000000000000000000000000000000000000000000000000000000000000001b0472caab4a4599023d00b2b3a48a1f25ebad390d6cc5c37167da6b1d1eee3cfb43693e69d8010e892a2d6dadff392c6514478ab6511109bb00afe6ce2a37b5f33d1cb6799eb3e750d6915ecd274d214bb4908703d578e3ffc1650f70d4946ba5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005e500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c66fbbf4000000000000000000000000000000000000000000000000002386f2c66fbcf500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000999f700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e54686b4d4463785a6930354d444d304c54566d5a6a63744f544a684d7930325a475a6b4f574e6b4f5745314e446b6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000004a1e3e93b09796d1576c7eec98c29fe14e50ca60000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd7c3a18f79ac79e6b5c50ac99368b8e0dda86219a7450e6aa4dfb93f0a6050ea",
      "signature": {
        "s": "0x003d82bcb3b4f87baef520c2ca37ba9cbf1679923c17c2c6c40da75afebb5f52",
        "r": "0x58cc8b73310901dcb7709d43981036908bd8630f01188b77e284b1730acba36a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0472caab4a4599023d00b2b3a48a1f25ebad390d6cc5c37167da6b1d1eee3cfb",
      "signature": {
        "s": "0x3d1cb6799eb3e750d6915ecd274d214bb4908703d578e3ffc1650f70d4946ba5",
        "r": "0x43693e69d8010e892a2d6dadff392c6514478ab6511109bb00afe6ce2a37b5f3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "256",
    "total": "256"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "256",
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
            "amount": "629239"
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
    "data": "eyJyZWYiOiIyNThkMDcxZi05MDM0LTVmZjctOTJhMy02ZGZkOWNkOWE1NDkifQ==",
    "nonce": 1509,
    "balances": {
      "current": "10000001454291956",
      "previous": "10000001454292213"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x04a1e3e93b09796d1576c7eec98c29fe14e50ca6",
    "nonce": 20,
    "balances": {
      "current": "256",
      "previous": "0"
    }
  },
  "blockNumber": "10114531",
  "created": "2020-05-22T08:10:05.898Z",
  "updated": "2020-05-22T08:10:05.993Z",
  "id": "5ec788ddb0c6090011d5aac7"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `256`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``