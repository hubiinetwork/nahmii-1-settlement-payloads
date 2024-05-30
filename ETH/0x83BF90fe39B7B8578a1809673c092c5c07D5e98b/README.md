# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x83BF90fe39B7B8578a1809673c092c5c07D5e98b`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000066b100000000000000000000000000000000000000000000000000000000000066b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000066b100000000000000000000000000000000000000000000000000000000000066b1ec63054c4d6ac6961f7da25031a21f2d458e3c1a023d2667e1aefb596a8673a4b30b99710ab692d2713cbe920104ab65a6aa70c50e3ef96245e31e7bff36d17416f67c1656748b77b438a99b134fedf0799f1b1ac3587a0b4a773e6c54bb15b5000000000000000000000000000000000000000000000000000000000000001cdfe13b136273337ed7e119abc1e69f666b92b0810da7c96d7d9828fa5a23a532d081bd00ff16b0479de1397bc48894063f00c3f3a65925889c42f3dbb8a8da4f1d9b27f8de772e061db2358af1ecdc5649e0dfe140342b84cc848501775f8f2a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000009800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d200e935000000000000000000000000000000000000000000000000002386f2d201500000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006a62500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e445a685a6a646b4d4330314d4441314c5456684f575974596d526c4d69316b4e4745324f444d354e4755774e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000001800000000000000000000000083bf90fe39b7b8578a1809673c092c5c07d5e98b00000000000000000000000000000000000000000000000000000000000066b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xec63054c4d6ac6961f7da25031a21f2d458e3c1a023d2667e1aefb596a8673a4",
      "signature": {
        "s": "0x16f67c1656748b77b438a99b134fedf0799f1b1ac3587a0b4a773e6c54bb15b5",
        "r": "0xb30b99710ab692d2713cbe920104ab65a6aa70c50e3ef96245e31e7bff36d174",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdfe13b136273337ed7e119abc1e69f666b92b0810da7c96d7d9828fa5a23a532",
      "signature": {
        "s": "0x1d9b27f8de772e061db2358af1ecdc5649e0dfe140342b84cc848501775f8f2a",
        "r": "0xd081bd00ff16b0479de1397bc48894063f00c3f3a65925889c42f3dbb8a8da4f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "26289",
    "total": "26289"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26289",
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
            "amount": "435749"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "26"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNDZhZjdkMC01MDA1LTVhOWYtYmRlMi1kNGE2ODM5NGUwNzkifQ==",
    "nonce": 152,
    "balances": {
      "current": "10000001648355637",
      "previous": "10000001648381952"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x83bf90fe39b7b8578a1809673c092c5c07d5e98b",
    "nonce": 24,
    "balances": {
      "current": "26289",
      "previous": "0"
    }
  },
  "blockNumber": "10114491",
  "created": "2020-05-22T08:00:00.422Z",
  "updated": "2020-05-22T08:00:01.536Z",
  "id": "5ec78680b0c6090011d5a909"
}
```
* *stageAmount*: `26289`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000066b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000066b100000000000000000000000000000000000000000000000000000000000066b1ec63054c4d6ac6961f7da25031a21f2d458e3c1a023d2667e1aefb596a8673a4b30b99710ab692d2713cbe920104ab65a6aa70c50e3ef96245e31e7bff36d17416f67c1656748b77b438a99b134fedf0799f1b1ac3587a0b4a773e6c54bb15b5000000000000000000000000000000000000000000000000000000000000001cdfe13b136273337ed7e119abc1e69f666b92b0810da7c96d7d9828fa5a23a532d081bd00ff16b0479de1397bc48894063f00c3f3a65925889c42f3dbb8a8da4f1d9b27f8de772e061db2358af1ecdc5649e0dfe140342b84cc848501775f8f2a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000009800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d200e935000000000000000000000000000000000000000000000000002386f2d201500000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006a62500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e445a685a6a646b4d4330314d4441314c5456684f575974596d526c4d69316b4e4745324f444d354e4755774e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000001800000000000000000000000083bf90fe39b7b8578a1809673c092c5c07d5e98b00000000000000000000000000000000000000000000000000000000000066b1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xec63054c4d6ac6961f7da25031a21f2d458e3c1a023d2667e1aefb596a8673a4",
      "signature": {
        "s": "0x16f67c1656748b77b438a99b134fedf0799f1b1ac3587a0b4a773e6c54bb15b5",
        "r": "0xb30b99710ab692d2713cbe920104ab65a6aa70c50e3ef96245e31e7bff36d174",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdfe13b136273337ed7e119abc1e69f666b92b0810da7c96d7d9828fa5a23a532",
      "signature": {
        "s": "0x1d9b27f8de772e061db2358af1ecdc5649e0dfe140342b84cc848501775f8f2a",
        "r": "0xd081bd00ff16b0479de1397bc48894063f00c3f3a65925889c42f3dbb8a8da4f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "26289",
    "total": "26289"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26289",
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
            "amount": "435749"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "26"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNDZhZjdkMC01MDA1LTVhOWYtYmRlMi1kNGE2ODM5NGUwNzkifQ==",
    "nonce": 152,
    "balances": {
      "current": "10000001648355637",
      "previous": "10000001648381952"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x83bf90fe39b7b8578a1809673c092c5c07d5e98b",
    "nonce": 24,
    "balances": {
      "current": "26289",
      "previous": "0"
    }
  },
  "blockNumber": "10114491",
  "created": "2020-05-22T08:00:00.422Z",
  "updated": "2020-05-22T08:00:01.536Z",
  "id": "5ec78680b0c6090011d5a909"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000066b10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `26289`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``