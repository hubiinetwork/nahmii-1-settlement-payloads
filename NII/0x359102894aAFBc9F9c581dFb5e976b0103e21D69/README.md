# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x359102894aAFBc9F9c581dFb5e976b0103e21D69`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000470de4df82000000000000000000000000000000000000000000000000000000470de4df8200000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000470de4df82000000000000000000000000000000000000000000000000000000470de4df8200007eed520f16bdc5c14c0fea83c930288911f95f88859eea7e3f426eaed870943ece4919b8e3fd1e20e55b8394e8f86871180fad0f898730e2dc0bc8f03e63224728396c145ed31a76a750354248ef06fcff418f6a2e29d91ad176d6749a99947f000000000000000000000000000000000000000000000000000000000000001bcb4481b5e4927c6c51f900ed2feb29a9750a78c844d067aa4a923a281f53a2da8a4df0e1e466a291464de8c024484bf3927809cc591729de2cff9f336717e511756439880cdb1c4b916423f055d256c42fb9c090b8687197aeb811a608df9ad0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000d8fe5b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002c0000000000000000000000003a8c0d0eb29e3cc41cf4c0d0affd4603c2e08008000000000000000000000000000000000000000000000014df14836d47ee3776000000000000000000000000000000000000000000000014df5ba382c455777600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000012309ce540000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000047d5fb9d5bc0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6d59314d7a4e6d595331685932566a4c5451784e445174596a63325a5330325a575a6a5a6d5a6d596a4a6b4f44416966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000359102894aafbc9f9c581dfb5e976b0103e21d6900000000000000000000000000000000000000000000000000470de4df820000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7eed520f16bdc5c14c0fea83c930288911f95f88859eea7e3f426eaed870943e",
      "signature": {
        "s": "0x28396c145ed31a76a750354248ef06fcff418f6a2e29d91ad176d6749a99947f",
        "r": "0xce4919b8e3fd1e20e55b8394e8f86871180fad0f898730e2dc0bc8f03e632247",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcb4481b5e4927c6c51f900ed2feb29a9750a78c844d067aa4a923a281f53a2da",
      "signature": {
        "s": "0x756439880cdb1c4b916423f055d256c42fb9c090b8687197aeb811a608df9ad0",
        "r": "0x8a4df0e1e466a291464de8c024484bf3927809cc591729de2cff9f336717e511",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "20000000000000000",
    "total": "20000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20000000000000000",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "20220000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "20000000000000"
      }
    },
    "wallet": "0x3a8c0d0eb29e3cc41cf4c0d0affd4603c2e08008",
    "data": "eyJyZWYiOiI0NmY1MzNmYS1hY2VjLTQxNDQtYjc2ZS02ZWZjZmZmYjJkODAifQ==",
    "nonce": 44,
    "balances": {
      "current": "385009498949564643190",
      "previous": "385029518949564643190"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x359102894aafbc9f9c581dfb5e976b0103e21d69",
    "nonce": 1,
    "balances": {
      "current": "20000000000000000",
      "previous": "0"
    }
  },
  "blockNumber": "14220891",
  "created": "2022-02-17T02:22:58.898Z",
  "updated": "2022-02-17T02:22:59.103Z",
  "id": "620db182f840e300116e9409"
}
```
* *stageAmount*: `20000000000000000`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000470de4df8200000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000470de4df82000000000000000000000000000000000000000000000000000000470de4df8200007eed520f16bdc5c14c0fea83c930288911f95f88859eea7e3f426eaed870943ece4919b8e3fd1e20e55b8394e8f86871180fad0f898730e2dc0bc8f03e63224728396c145ed31a76a750354248ef06fcff418f6a2e29d91ad176d6749a99947f000000000000000000000000000000000000000000000000000000000000001bcb4481b5e4927c6c51f900ed2feb29a9750a78c844d067aa4a923a281f53a2da8a4df0e1e466a291464de8c024484bf3927809cc591729de2cff9f336717e511756439880cdb1c4b916423f055d256c42fb9c090b8687197aeb811a608df9ad0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000d8fe5b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002c0000000000000000000000003a8c0d0eb29e3cc41cf4c0d0affd4603c2e08008000000000000000000000000000000000000000000000014df14836d47ee3776000000000000000000000000000000000000000000000014df5ba382c455777600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000012309ce540000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000047d5fb9d5bc0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6d59314d7a4e6d595331685932566a4c5451784e445174596a63325a5330325a575a6a5a6d5a6d596a4a6b4f44416966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000359102894aafbc9f9c581dfb5e976b0103e21d6900000000000000000000000000000000000000000000000000470de4df820000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7eed520f16bdc5c14c0fea83c930288911f95f88859eea7e3f426eaed870943e",
      "signature": {
        "s": "0x28396c145ed31a76a750354248ef06fcff418f6a2e29d91ad176d6749a99947f",
        "r": "0xce4919b8e3fd1e20e55b8394e8f86871180fad0f898730e2dc0bc8f03e632247",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcb4481b5e4927c6c51f900ed2feb29a9750a78c844d067aa4a923a281f53a2da",
      "signature": {
        "s": "0x756439880cdb1c4b916423f055d256c42fb9c090b8687197aeb811a608df9ad0",
        "r": "0x8a4df0e1e466a291464de8c024484bf3927809cc591729de2cff9f336717e511",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "20000000000000000",
    "total": "20000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20000000000000000",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "20220000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "20000000000000"
      }
    },
    "wallet": "0x3a8c0d0eb29e3cc41cf4c0d0affd4603c2e08008",
    "data": "eyJyZWYiOiI0NmY1MzNmYS1hY2VjLTQxNDQtYjc2ZS02ZWZjZmZmYjJkODAifQ==",
    "nonce": 44,
    "balances": {
      "current": "385009498949564643190",
      "previous": "385029518949564643190"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x359102894aafbc9f9c581dfb5e976b0103e21d69",
    "nonce": 1,
    "balances": {
      "current": "20000000000000000",
      "previous": "0"
    }
  },
  "blockNumber": "14220891",
  "created": "2022-02-17T02:22:58.898Z",
  "updated": "2022-02-17T02:22:59.103Z",
  "id": "620db182f840e300116e9409"
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
0x0f200f9b00000000000000000000000000000000000000000000000000470de4df8200000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `20000000000000000`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`