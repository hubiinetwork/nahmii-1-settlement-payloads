# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x08b296a897b1c8A033066A34Dfde80c66A825D7B`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000670f8196c87c85f4005b3a8e41a9963bbb029bde50ed9cf673f37d89fc82b539c1cebe6a655274b4d60ce3ab087dbd31441b6eb2f500f9a380070fe9da3cb1a452eb0d20417fe0e225d5ccef49271d5a25dcc23708e90c38cb7ed589e58431310000000000000000000000000000000000000000000000000000000000000001b85e98373756668f429eda4349a571f3ccada81093918135947f9b8e5820f3829a1a8bea93103da20b70619461678831e88248c72ea264533d27bc3dc2f68aea95565f077aa662a591dc5533dc3c651ea8b2406a11103ac1a309ead58d3cd074d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000084200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bd96e22f000000000000000000000000000000000000000000000000002386f2bd96e23600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000bdc4e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5749795a475a6d4d53316d4d3251334c5455784d544574595464694f5331685a44686c4e7a49794f544e6c4e6d556966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000008b296a897b1c8a033066a34dfde80c66a825d7b0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x70f8196c87c85f4005b3a8e41a9963bbb029bde50ed9cf673f37d89fc82b539c",
      "signature": {
        "s": "0x2eb0d20417fe0e225d5ccef49271d5a25dcc23708e90c38cb7ed589e58431310",
        "r": "0x1cebe6a655274b4d60ce3ab087dbd31441b6eb2f500f9a380070fe9da3cb1a45",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x85e98373756668f429eda4349a571f3ccada81093918135947f9b8e5820f3829",
      "signature": {
        "s": "0x5565f077aa662a591dc5533dc3c651ea8b2406a11103ac1a309ead58d3cd074d",
        "r": "0xa1a8bea93103da20b70619461678831e88248c72ea264533d27bc3dc2f68aea9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6",
    "total": "6"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6",
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
            "amount": "777294"
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
    "data": "eyJyZWYiOiI3ZWIyZGZmMS1mM2Q3LTUxMTEtYTdiOS1hZDhlNzIyOTNlNmUifQ==",
    "nonce": 2114,
    "balances": {
      "current": "10000001305862703",
      "previous": "10000001305862710"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x08b296a897b1c8a033066a34dfde80c66a825d7b",
    "nonce": 4,
    "balances": {
      "current": "6",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:30.286Z",
  "updated": "2020-05-22T08:14:30.360Z",
  "id": "5ec789e6e5756b00111b8223"
}
```
* *stageAmount*: `6`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000670f8196c87c85f4005b3a8e41a9963bbb029bde50ed9cf673f37d89fc82b539c1cebe6a655274b4d60ce3ab087dbd31441b6eb2f500f9a380070fe9da3cb1a452eb0d20417fe0e225d5ccef49271d5a25dcc23708e90c38cb7ed589e58431310000000000000000000000000000000000000000000000000000000000000001b85e98373756668f429eda4349a571f3ccada81093918135947f9b8e5820f3829a1a8bea93103da20b70619461678831e88248c72ea264533d27bc3dc2f68aea95565f077aa662a591dc5533dc3c651ea8b2406a11103ac1a309ead58d3cd074d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000084200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bd96e22f000000000000000000000000000000000000000000000000002386f2bd96e23600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000bdc4e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5749795a475a6d4d53316d4d3251334c5455784d544574595464694f5331685a44686c4e7a49794f544e6c4e6d556966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000008b296a897b1c8a033066a34dfde80c66a825d7b0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x70f8196c87c85f4005b3a8e41a9963bbb029bde50ed9cf673f37d89fc82b539c",
      "signature": {
        "s": "0x2eb0d20417fe0e225d5ccef49271d5a25dcc23708e90c38cb7ed589e58431310",
        "r": "0x1cebe6a655274b4d60ce3ab087dbd31441b6eb2f500f9a380070fe9da3cb1a45",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x85e98373756668f429eda4349a571f3ccada81093918135947f9b8e5820f3829",
      "signature": {
        "s": "0x5565f077aa662a591dc5533dc3c651ea8b2406a11103ac1a309ead58d3cd074d",
        "r": "0xa1a8bea93103da20b70619461678831e88248c72ea264533d27bc3dc2f68aea9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6",
    "total": "6"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6",
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
            "amount": "777294"
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
    "data": "eyJyZWYiOiI3ZWIyZGZmMS1mM2Q3LTUxMTEtYTdiOS1hZDhlNzIyOTNlNmUifQ==",
    "nonce": 2114,
    "balances": {
      "current": "10000001305862703",
      "previous": "10000001305862710"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x08b296a897b1c8a033066a34dfde80c66a825d7b",
    "nonce": 4,
    "balances": {
      "current": "6",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:30.286Z",
  "updated": "2020-05-22T08:14:30.360Z",
  "id": "5ec789e6e5756b00111b8223"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``