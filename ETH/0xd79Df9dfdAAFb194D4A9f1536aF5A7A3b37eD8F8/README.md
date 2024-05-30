# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd79Df9dfdAAFb194D4A9f1536aF5A7A3b37eD8F8`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000072440000000000000000000000000000000000000000000000000000000000007244000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000072440000000000000000000000000000000000000000000000000000000000007244ccb1cdf38a868415fab601b95c8f2ae9d7251db552b80c6afa52af43f82fe251d9ffa41be588879479cdc6936c82df189c7391f79fdfb1e7082f4878c0e160d35182d21ff9af1eae174df0fc1728a3e1024884e778aef88dc373873106034cea000000000000000000000000000000000000000000000000000000000000001cea3dbdf32e60fe39171ee5b2ceb923ef6460ca57dc5512b08b7a9fb6acf821646ca847f43281eb025d99e97d3060fab86042898723914950fe242893ab2c2170217fe93492d60f8002936c5406be4cc193be2afa7e4f270d71c10e0642cfb97c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000004200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2df28a0ce000000000000000000000000000000000000000000000000002386f2df29132f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003490100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e444133596d59794f43316b596d5a6b4c5455774d4445745954646959693169595751335954686b4d32526a4e32596966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000d79df9dfdaafb194d4a9f1536af5a7a3b37ed8f80000000000000000000000000000000000000000000000000000000000007244000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xccb1cdf38a868415fab601b95c8f2ae9d7251db552b80c6afa52af43f82fe251",
      "signature": {
        "s": "0x5182d21ff9af1eae174df0fc1728a3e1024884e778aef88dc373873106034cea",
        "r": "0xd9ffa41be588879479cdc6936c82df189c7391f79fdfb1e7082f4878c0e160d3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xea3dbdf32e60fe39171ee5b2ceb923ef6460ca57dc5512b08b7a9fb6acf82164",
      "signature": {
        "s": "0x217fe93492d60f8002936c5406be4cc193be2afa7e4f270d71c10e0642cfb97c",
        "r": "0x6ca847f43281eb025d99e97d3060fab86042898723914950fe242893ab2c2170",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "29252",
    "total": "29252"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "29252",
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
            "amount": "215297"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "29"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNDA3YmYyOC1kYmZkLTUwMDEtYTdiYi1iYWQ3YThkM2RjN2YifQ==",
    "nonce": 66,
    "balances": {
      "current": "10000001869062350",
      "previous": "10000001869091631"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd79df9dfdaafb194d4a9f1536af5a7a3b37ed8f8",
    "nonce": 12,
    "balances": {
      "current": "29252",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:26.939Z",
  "updated": "2020-05-22T07:59:27.013Z",
  "id": "5ec7865e005df800101bc224"
}
```
* *stageAmount*: `29252`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000007244000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000072440000000000000000000000000000000000000000000000000000000000007244ccb1cdf38a868415fab601b95c8f2ae9d7251db552b80c6afa52af43f82fe251d9ffa41be588879479cdc6936c82df189c7391f79fdfb1e7082f4878c0e160d35182d21ff9af1eae174df0fc1728a3e1024884e778aef88dc373873106034cea000000000000000000000000000000000000000000000000000000000000001cea3dbdf32e60fe39171ee5b2ceb923ef6460ca57dc5512b08b7a9fb6acf821646ca847f43281eb025d99e97d3060fab86042898723914950fe242893ab2c2170217fe93492d60f8002936c5406be4cc193be2afa7e4f270d71c10e0642cfb97c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000004200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2df28a0ce000000000000000000000000000000000000000000000000002386f2df29132f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003490100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e444133596d59794f43316b596d5a6b4c5455774d4445745954646959693169595751335954686b4d32526a4e32596966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000d79df9dfdaafb194d4a9f1536af5a7a3b37ed8f80000000000000000000000000000000000000000000000000000000000007244000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xccb1cdf38a868415fab601b95c8f2ae9d7251db552b80c6afa52af43f82fe251",
      "signature": {
        "s": "0x5182d21ff9af1eae174df0fc1728a3e1024884e778aef88dc373873106034cea",
        "r": "0xd9ffa41be588879479cdc6936c82df189c7391f79fdfb1e7082f4878c0e160d3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xea3dbdf32e60fe39171ee5b2ceb923ef6460ca57dc5512b08b7a9fb6acf82164",
      "signature": {
        "s": "0x217fe93492d60f8002936c5406be4cc193be2afa7e4f270d71c10e0642cfb97c",
        "r": "0x6ca847f43281eb025d99e97d3060fab86042898723914950fe242893ab2c2170",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "29252",
    "total": "29252"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "29252",
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
            "amount": "215297"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "29"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNDA3YmYyOC1kYmZkLTUwMDEtYTdiYi1iYWQ3YThkM2RjN2YifQ==",
    "nonce": 66,
    "balances": {
      "current": "10000001869062350",
      "previous": "10000001869091631"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd79df9dfdaafb194d4a9f1536af5a7a3b37ed8f8",
    "nonce": 12,
    "balances": {
      "current": "29252",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:26.939Z",
  "updated": "2020-05-22T07:59:27.013Z",
  "id": "5ec7865e005df800101bc224"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000072440000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `29252`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``