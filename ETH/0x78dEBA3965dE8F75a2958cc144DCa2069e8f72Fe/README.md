# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x78dEBA3965dE8F75a2958cc144DCa2069e8f72Fe`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000002ef940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000002ef942f354d35e9d92b6b56a1e5504b8e596816619557baa745130a6c3ad420ed528e5e11536d362fdb49a1197bebc4a63a3a857be2bf332c97ae131f336bc30ff4fd6f65db494f866acd17d19cac686162e593cece678d921ecc8431ecd8ea405f6c000000000000000000000000000000000000000000000000000000000000001b87f9dba1b40cb023b21d41e6e29af46137898e2f7e1880edb905931d910fd6aa759f6ea2ea84db200adbd60e39cf71319a90401608bbfd1658f2b6ffe1f12e26525bd805febf7adacf1ccfb159e70d29ec3123dfad8bf977a64fc174e4b28213000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001de00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb8e2665000000000000000000000000000000000000000000000000002386f2cb9116b900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000084c1200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493059544a6c596d4e6b4e69307a5a544d774c5455334e546b744f474578596930794d6a6b334e57526c4e544e6c4f57556966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000078deba3965de8f75a2958cc144dca2069e8f72fe000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2f354d35e9d92b6b56a1e5504b8e596816619557baa745130a6c3ad420ed528e",
      "signature": {
        "s": "0x6f65db494f866acd17d19cac686162e593cece678d921ecc8431ecd8ea405f6c",
        "r": "0x5e11536d362fdb49a1197bebc4a63a3a857be2bf332c97ae131f336bc30ff4fd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x87f9dba1b40cb023b21d41e6e29af46137898e2f7e1880edb905931d910fd6aa",
      "signature": {
        "s": "0x525bd805febf7adacf1ccfb159e70d29ec3123dfad8bf977a64fc174e4b28213",
        "r": "0x759f6ea2ea84db200adbd60e39cf71319a90401608bbfd1658f2b6ffe1f12e26",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "192404",
    "total": "192404"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "192404",
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
            "amount": "543762"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "192"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YTJlYmNkNi0zZTMwLTU3NTktOGExYi0yMjk3NWRlNTNlOWUifQ==",
    "nonce": 478,
    "balances": {
      "current": "10000001540171365",
      "previous": "10000001540363961"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x78deba3965de8f75a2958cc144dca2069e8f72fe",
    "nonce": 20,
    "balances": {
      "current": "192404",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:18.714Z",
  "updated": "2020-05-22T08:02:18.784Z",
  "id": "5ec7870a005df800101bc2b1"
}
```
* *stageAmount*: `192404`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002ef940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000002ef942f354d35e9d92b6b56a1e5504b8e596816619557baa745130a6c3ad420ed528e5e11536d362fdb49a1197bebc4a63a3a857be2bf332c97ae131f336bc30ff4fd6f65db494f866acd17d19cac686162e593cece678d921ecc8431ecd8ea405f6c000000000000000000000000000000000000000000000000000000000000001b87f9dba1b40cb023b21d41e6e29af46137898e2f7e1880edb905931d910fd6aa759f6ea2ea84db200adbd60e39cf71319a90401608bbfd1658f2b6ffe1f12e26525bd805febf7adacf1ccfb159e70d29ec3123dfad8bf977a64fc174e4b28213000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001de00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb8e2665000000000000000000000000000000000000000000000000002386f2cb9116b900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000084c1200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493059544a6c596d4e6b4e69307a5a544d774c5455334e546b744f474578596930794d6a6b334e57526c4e544e6c4f57556966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000078deba3965de8f75a2958cc144dca2069e8f72fe000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2f354d35e9d92b6b56a1e5504b8e596816619557baa745130a6c3ad420ed528e",
      "signature": {
        "s": "0x6f65db494f866acd17d19cac686162e593cece678d921ecc8431ecd8ea405f6c",
        "r": "0x5e11536d362fdb49a1197bebc4a63a3a857be2bf332c97ae131f336bc30ff4fd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x87f9dba1b40cb023b21d41e6e29af46137898e2f7e1880edb905931d910fd6aa",
      "signature": {
        "s": "0x525bd805febf7adacf1ccfb159e70d29ec3123dfad8bf977a64fc174e4b28213",
        "r": "0x759f6ea2ea84db200adbd60e39cf71319a90401608bbfd1658f2b6ffe1f12e26",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "192404",
    "total": "192404"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "192404",
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
            "amount": "543762"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "192"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YTJlYmNkNi0zZTMwLTU3NTktOGExYi0yMjk3NWRlNTNlOWUifQ==",
    "nonce": 478,
    "balances": {
      "current": "10000001540171365",
      "previous": "10000001540363961"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x78deba3965de8f75a2958cc144dca2069e8f72fe",
    "nonce": 20,
    "balances": {
      "current": "192404",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:18.714Z",
  "updated": "2020-05-22T08:02:18.784Z",
  "id": "5ec7870a005df800101bc2b1"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000002ef940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `192404`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``