# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1b1C368395f3Db0A794ABE201Fd43A0effe25e19`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000177ca00000000000000000000000000000000000000000000000000000000000177ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000177ca00000000000000000000000000000000000000000000000000000000000177ca34de72f09c3e45fd750ef95fd225566317f4e48ae15af65aef665f152aeda7bb598d97ec9b447de16fc530a8214679eabe7b9c9b46a9ae2a0dceab939deb7d9f75e6f84694f54b262d3b4c48756ea865196ad5b905df039c4a36b71dab4efaaa000000000000000000000000000000000000000000000000000000000000001ba666680b490cdadbae156f4aff14f7333289f939afdccb2f17875c362759612160c1e1a04e099b8277ed78c277f615d929501824e7a83799183b0de2d848ece1590092c3b922e3bccdd2ff94cfb19a0c87664511d5877596e18a3174b2f0e57d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000020700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb4e4859000000000000000000000000000000000000000000000000002386f2cb4fc08300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000085c5700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d575a684e7a55315979316c5a6a63304c54557a4f4755744f57466a4f4331684e6d566d593249334f4755334d6a496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000001b1c368395f3db0a794abe201fd43a0effe25e1900000000000000000000000000000000000000000000000000000000000177ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x34de72f09c3e45fd750ef95fd225566317f4e48ae15af65aef665f152aeda7bb",
      "signature": {
        "s": "0x75e6f84694f54b262d3b4c48756ea865196ad5b905df039c4a36b71dab4efaaa",
        "r": "0x598d97ec9b447de16fc530a8214679eabe7b9c9b46a9ae2a0dceab939deb7d9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa666680b490cdadbae156f4aff14f7333289f939afdccb2f17875c3627596121",
      "signature": {
        "s": "0x590092c3b922e3bccdd2ff94cfb19a0c87664511d5877596e18a3174b2f0e57d",
        "r": "0x60c1e1a04e099b8277ed78c277f615d929501824e7a83799183b0de2d848ece1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "96202",
    "total": "96202"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "96202",
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
            "amount": "547927"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "96"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMWZhNzU1Yy1lZjc0LTUzOGUtOWFjOC1hNmVmY2I3OGU3MjIifQ==",
    "nonce": 519,
    "balances": {
      "current": "10000001535985753",
      "previous": "10000001536082051"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1b1c368395f3db0a794abe201fd43a0effe25e19",
    "nonce": 20,
    "balances": {
      "current": "96202",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:36.691Z",
  "updated": "2020-05-22T08:02:36.789Z",
  "id": "5ec7871cb0c6090011d5a97c"
}
```
* *stageAmount*: `96202`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000177ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000177ca00000000000000000000000000000000000000000000000000000000000177ca34de72f09c3e45fd750ef95fd225566317f4e48ae15af65aef665f152aeda7bb598d97ec9b447de16fc530a8214679eabe7b9c9b46a9ae2a0dceab939deb7d9f75e6f84694f54b262d3b4c48756ea865196ad5b905df039c4a36b71dab4efaaa000000000000000000000000000000000000000000000000000000000000001ba666680b490cdadbae156f4aff14f7333289f939afdccb2f17875c362759612160c1e1a04e099b8277ed78c277f615d929501824e7a83799183b0de2d848ece1590092c3b922e3bccdd2ff94cfb19a0c87664511d5877596e18a3174b2f0e57d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000020700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb4e4859000000000000000000000000000000000000000000000000002386f2cb4fc08300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000085c5700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d575a684e7a55315979316c5a6a63304c54557a4f4755744f57466a4f4331684e6d566d593249334f4755334d6a496966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000001b1c368395f3db0a794abe201fd43a0effe25e1900000000000000000000000000000000000000000000000000000000000177ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x34de72f09c3e45fd750ef95fd225566317f4e48ae15af65aef665f152aeda7bb",
      "signature": {
        "s": "0x75e6f84694f54b262d3b4c48756ea865196ad5b905df039c4a36b71dab4efaaa",
        "r": "0x598d97ec9b447de16fc530a8214679eabe7b9c9b46a9ae2a0dceab939deb7d9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa666680b490cdadbae156f4aff14f7333289f939afdccb2f17875c3627596121",
      "signature": {
        "s": "0x590092c3b922e3bccdd2ff94cfb19a0c87664511d5877596e18a3174b2f0e57d",
        "r": "0x60c1e1a04e099b8277ed78c277f615d929501824e7a83799183b0de2d848ece1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "96202",
    "total": "96202"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "96202",
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
            "amount": "547927"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "96"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMWZhNzU1Yy1lZjc0LTUzOGUtOWFjOC1hNmVmY2I3OGU3MjIifQ==",
    "nonce": 519,
    "balances": {
      "current": "10000001535985753",
      "previous": "10000001536082051"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1b1c368395f3db0a794abe201fd43a0effe25e19",
    "nonce": 20,
    "balances": {
      "current": "96202",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:36.691Z",
  "updated": "2020-05-22T08:02:36.789Z",
  "id": "5ec7871cb0c6090011d5a97c"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000177ca0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `96202`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``