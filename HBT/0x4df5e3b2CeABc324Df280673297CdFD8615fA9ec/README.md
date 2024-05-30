# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4df5e3b2CeABc324Df280673297CdFD8615fA9ec`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000764048420000000000000000000000000000000000000000000000000000000076404842000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000764048420000000000000000000000000000000000000000000000000000000076404842090ea361cfd6f43c7b23900ac2de1ba5167e14ab6ede5f446f88902e7419a5e37b41e9ff90e4d5198777574128c874f81b801c5e97c5204d5b9aaa0198e336f04493b8ec9839d1018c1a84c71356b0c8e431fbdf924397224fdab3ab896e6254000000000000000000000000000000000000000000000000000000000000001b436b3a02d897ab0c913b634533b8999b69fdddb606862cca4c848fbce6c8be07789569c166cd69fea8edb91b1130e4de48b97745e766ce6b0406c8cf6f08b9221b6fa2009014245daef547e7ecfcc8f53a85bd72487d330e43b2730070107561000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ad300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1614c2a3a5be000000000000000000000000000000000000000000000000002e1615390233b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e45b4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9ac3d41c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595451325a545a694e5330775932566a4c54566a4e474974595759324e69316d5a6d5a6c5a5749794e7a6b355a47556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004df5e3b2ceabc324df280673297cdfd8615fa9ec0000000000000000000000000000000000000000000000000000000076404842000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x090ea361cfd6f43c7b23900ac2de1ba5167e14ab6ede5f446f88902e7419a5e3",
      "signature": {
        "s": "0x4493b8ec9839d1018c1a84c71356b0c8e431fbdf924397224fdab3ab896e6254",
        "r": "0x7b41e9ff90e4d5198777574128c874f81b801c5e97c5204d5b9aaa0198e336f0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x436b3a02d897ab0c913b634533b8999b69fdddb606862cca4c848fbce6c8be07",
      "signature": {
        "s": "0x1b6fa2009014245daef547e7ecfcc8f53a85bd72487d330e43b2730070107561",
        "r": "0x789569c166cd69fea8edb91b1130e4de48b97745e766ce6b0406c8cf6f08b922",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1983924290",
    "total": "1983924290"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1983924290",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "45546198044"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1983924"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YTQ2ZTZiNS0wY2VjLTVjNGItYWY2Ni1mZmZlZWIyNzk5ZGUifQ==",
    "nonce": 6867,
    "balances": {
      "current": "12972127349351870",
      "previous": "12972129335260084"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4df5e3b2ceabc324df280673297cdfd8615fa9ec",
    "nonce": 22,
    "balances": {
      "current": "1983924290",
      "previous": "0"
    }
  },
  "blockNumber": "10114717",
  "created": "2020-05-22T08:52:13.083Z",
  "updated": "2020-05-22T08:52:13.155Z",
  "id": "5ec792bde5756b00111b8830"
}
```
* *stageAmount*: `1983924290`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000076404842000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000764048420000000000000000000000000000000000000000000000000000000076404842090ea361cfd6f43c7b23900ac2de1ba5167e14ab6ede5f446f88902e7419a5e37b41e9ff90e4d5198777574128c874f81b801c5e97c5204d5b9aaa0198e336f04493b8ec9839d1018c1a84c71356b0c8e431fbdf924397224fdab3ab896e6254000000000000000000000000000000000000000000000000000000000000001b436b3a02d897ab0c913b634533b8999b69fdddb606862cca4c848fbce6c8be07789569c166cd69fea8edb91b1130e4de48b97745e766ce6b0406c8cf6f08b9221b6fa2009014245daef547e7ecfcc8f53a85bd72487d330e43b2730070107561000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ad300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1614c2a3a5be000000000000000000000000000000000000000000000000002e1615390233b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001e45b4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9ac3d41c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595451325a545a694e5330775932566a4c54566a4e474974595759324e69316d5a6d5a6c5a5749794e7a6b355a47556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004df5e3b2ceabc324df280673297cdfd8615fa9ec0000000000000000000000000000000000000000000000000000000076404842000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x090ea361cfd6f43c7b23900ac2de1ba5167e14ab6ede5f446f88902e7419a5e3",
      "signature": {
        "s": "0x4493b8ec9839d1018c1a84c71356b0c8e431fbdf924397224fdab3ab896e6254",
        "r": "0x7b41e9ff90e4d5198777574128c874f81b801c5e97c5204d5b9aaa0198e336f0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x436b3a02d897ab0c913b634533b8999b69fdddb606862cca4c848fbce6c8be07",
      "signature": {
        "s": "0x1b6fa2009014245daef547e7ecfcc8f53a85bd72487d330e43b2730070107561",
        "r": "0x789569c166cd69fea8edb91b1130e4de48b97745e766ce6b0406c8cf6f08b922",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1983924290",
    "total": "1983924290"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1983924290",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "45546198044"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1983924"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YTQ2ZTZiNS0wY2VjLTVjNGItYWY2Ni1mZmZlZWIyNzk5ZGUifQ==",
    "nonce": 6867,
    "balances": {
      "current": "12972127349351870",
      "previous": "12972129335260084"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4df5e3b2ceabc324df280673297cdfd8615fa9ec",
    "nonce": 22,
    "balances": {
      "current": "1983924290",
      "previous": "0"
    }
  },
  "blockNumber": "10114717",
  "created": "2020-05-22T08:52:13.083Z",
  "updated": "2020-05-22T08:52:13.155Z",
  "id": "5ec792bde5756b00111b8830"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000076404842000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1983924290`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`