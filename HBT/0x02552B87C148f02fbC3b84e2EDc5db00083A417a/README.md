# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x02552B87C148f02fbC3b84e2EDc5db00083A417a`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000564b11c250000000000000000000000000000000000000000000000000000000564b11c25000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000564b11c250000000000000000000000000000000000000000000000000000000564b11c25879e69a170974b5ede7bc568e2699ec4935fae99e6ee76d85cc80e5d93d365918fe36d4dbc5ca3ec9f429e95267b915873ac9cc3beb46532cc7da208723a7f0c6a0b11c6b5af3cb9fdd35f18769aaa39068eeceb1f585490ee1128bcc65c4ff4000000000000000000000000000000000000000000000000000000000000001c3670af88fd4ec9a06da8da9294c564857ce5586f8a2f34680bb09d50dd32fb8868b66ce57db01722bdead84f06f47b8442eda3cc7f95fe6fbfba114faad10012525b8fba3541e277621d7344611547db41376f2b54bdbdfe1d2b49a46bbf82e6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5665000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014f900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e21363e97a8da000000000000000000000000000000000000000000000000002e213ba4aa3a0400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001617505000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007c206994e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e47566d5a5451784e5331684d4452684c54566d4d444d74595449784e5330344f5755334f5445355a6d597a4e546b6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000002552b87c148f02fbc3b84e2edc5db00083a417a0000000000000000000000000000000000000000000000000000000564b11c25000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x879e69a170974b5ede7bc568e2699ec4935fae99e6ee76d85cc80e5d93d36591",
      "signature": {
        "s": "0x6a0b11c6b5af3cb9fdd35f18769aaa39068eeceb1f585490ee1128bcc65c4ff4",
        "r": "0x8fe36d4dbc5ca3ec9f429e95267b915873ac9cc3beb46532cc7da208723a7f0c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3670af88fd4ec9a06da8da9294c564857ce5586f8a2f34680bb09d50dd32fb88",
      "signature": {
        "s": "0x525b8fba3541e277621d7344611547db41376f2b54bdbdfe1d2b49a46bbf82e6",
        "r": "0x68b66ce57db01722bdead84f06f47b8442eda3cc7f95fe6fbfba114faad10012",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "23164165157",
    "total": "23164165157"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23164165157",
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
            "amount": "33319983438"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "23164165"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2NGVmZTQxNS1hMDRhLTVmMDMtYTIxNS04OWU3OTE5ZmYzNTkifQ==",
    "nonce": 5369,
    "balances": {
      "current": "12984365790767322",
      "previous": "12984388978096644"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02552b87c148f02fbc3b84e2edc5db00083a417a",
    "nonce": 22,
    "balances": {
      "current": "23164165157",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:39.395Z",
  "updated": "2020-05-22T08:40:39.563Z",
  "id": "5ec79007b0c6090011d5afb9"
}
```
* *stageAmount*: `23164165157`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000564b11c25000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000564b11c250000000000000000000000000000000000000000000000000000000564b11c25879e69a170974b5ede7bc568e2699ec4935fae99e6ee76d85cc80e5d93d365918fe36d4dbc5ca3ec9f429e95267b915873ac9cc3beb46532cc7da208723a7f0c6a0b11c6b5af3cb9fdd35f18769aaa39068eeceb1f585490ee1128bcc65c4ff4000000000000000000000000000000000000000000000000000000000000001c3670af88fd4ec9a06da8da9294c564857ce5586f8a2f34680bb09d50dd32fb8868b66ce57db01722bdead84f06f47b8442eda3cc7f95fe6fbfba114faad10012525b8fba3541e277621d7344611547db41376f2b54bdbdfe1d2b49a46bbf82e6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5665000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014f900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e21363e97a8da000000000000000000000000000000000000000000000000002e213ba4aa3a0400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001617505000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007c206994e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e47566d5a5451784e5331684d4452684c54566d4d444d74595449784e5330344f5755334f5445355a6d597a4e546b6966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000002552b87c148f02fbc3b84e2edc5db00083a417a0000000000000000000000000000000000000000000000000000000564b11c25000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x879e69a170974b5ede7bc568e2699ec4935fae99e6ee76d85cc80e5d93d36591",
      "signature": {
        "s": "0x6a0b11c6b5af3cb9fdd35f18769aaa39068eeceb1f585490ee1128bcc65c4ff4",
        "r": "0x8fe36d4dbc5ca3ec9f429e95267b915873ac9cc3beb46532cc7da208723a7f0c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3670af88fd4ec9a06da8da9294c564857ce5586f8a2f34680bb09d50dd32fb88",
      "signature": {
        "s": "0x525b8fba3541e277621d7344611547db41376f2b54bdbdfe1d2b49a46bbf82e6",
        "r": "0x68b66ce57db01722bdead84f06f47b8442eda3cc7f95fe6fbfba114faad10012",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "23164165157",
    "total": "23164165157"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23164165157",
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
            "amount": "33319983438"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "23164165"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2NGVmZTQxNS1hMDRhLTVmMDMtYTIxNS04OWU3OTE5ZmYzNTkifQ==",
    "nonce": 5369,
    "balances": {
      "current": "12984365790767322",
      "previous": "12984388978096644"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02552b87c148f02fbc3b84e2edc5db00083a417a",
    "nonce": 22,
    "balances": {
      "current": "23164165157",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:39.395Z",
  "updated": "2020-05-22T08:40:39.563Z",
  "id": "5ec79007b0c6090011d5afb9"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000564b11c25000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `23164165157`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`