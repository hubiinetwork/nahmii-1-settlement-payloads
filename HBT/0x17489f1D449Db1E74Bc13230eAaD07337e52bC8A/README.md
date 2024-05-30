# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x17489f1D449Db1E74Bc13230eAaD07337e52bC8A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000058dcc2568d00000000000000000000000000000000000000000000000000000058dcc2568d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000058dcc2568d00000000000000000000000000000000000000000000000000000058dcc2568dc4c26dc45952eb4457dac257be6e441348a99af6c271e722bef9e64233d273eeedb5e3293cffc9eaa775417ff732dd9b81481c70c394cde5c704b8865fda16045f91c4c6fc455943d48d15c0eaa8c3bca830ec5949207649fad4096e20f70f5b000000000000000000000000000000000000000000000000000000000000001c62cb5a9c6d7482f0b3f5e332cd8c433f0cc10fab22da7af40f1ba3757ac36cede75dc40317e038ee9beacba909addd881a73efc1a10b92858898fd8235f9ccd81e5b4982ea0697660596b673f7df9c9347794a2f4afbfee1d7fe30e061a971d5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5663000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014da00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2242846792cc000000000000000000000000000000000000000000000000002e229b77e9980600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000016bfaead000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000077d6aa4a2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e474934597a6c6c4d69316b4f574d334c5455305a4449744f4455335a69316d4d6a64684d6a67324e6d55304e44516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000017489f1d449db1e74bc13230eaad07337e52bc8a00000000000000000000000000000000000000000000000000000058dcc2568d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc4c26dc45952eb4457dac257be6e441348a99af6c271e722bef9e64233d273ee",
      "signature": {
        "s": "0x5f91c4c6fc455943d48d15c0eaa8c3bca830ec5949207649fad4096e20f70f5b",
        "r": "0xedb5e3293cffc9eaa775417ff732dd9b81481c70c394cde5c704b8865fda1604",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x62cb5a9c6d7482f0b3f5e332cd8c433f0cc10fab22da7af40f1ba3757ac36ced",
      "signature": {
        "s": "0x1e5b4982ea0697660596b673f7df9c9347794a2f4afbfee1d7fe30e061a971d5",
        "r": "0xe75dc40317e038ee9beacba909addd881a73efc1a10b92858898fd8235f9ccd8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "381660845709",
    "total": "381660845709"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "381660845709",
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
            "amount": "32168912034"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "381660845"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNGI4YzllMi1kOWM3LTU0ZDItODU3Zi1mMjdhMjg2NmU0NDQifQ==",
    "nonce": 5338,
    "balances": {
      "current": "12985518013256396",
      "previous": "12985900055762950"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x17489f1d449db1e74bc13230eaad07337e52bc8a",
    "nonce": 22,
    "balances": {
      "current": "381660845709",
      "previous": "0"
    }
  },
  "blockNumber": "10114659",
  "created": "2020-05-22T08:40:20.982Z",
  "updated": "2020-05-22T08:40:21.048Z",
  "id": "5ec78ff4005df800101bc930"
}
```
* *stageAmount*: `381660845709`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000058dcc2568d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000058dcc2568d00000000000000000000000000000000000000000000000000000058dcc2568dc4c26dc45952eb4457dac257be6e441348a99af6c271e722bef9e64233d273eeedb5e3293cffc9eaa775417ff732dd9b81481c70c394cde5c704b8865fda16045f91c4c6fc455943d48d15c0eaa8c3bca830ec5949207649fad4096e20f70f5b000000000000000000000000000000000000000000000000000000000000001c62cb5a9c6d7482f0b3f5e332cd8c433f0cc10fab22da7af40f1ba3757ac36cede75dc40317e038ee9beacba909addd881a73efc1a10b92858898fd8235f9ccd81e5b4982ea0697660596b673f7df9c9347794a2f4afbfee1d7fe30e061a971d5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5663000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014da00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2242846792cc000000000000000000000000000000000000000000000000002e229b77e9980600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000016bfaead000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000077d6aa4a2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e474934597a6c6c4d69316b4f574d334c5455305a4449744f4455335a69316d4d6a64684d6a67324e6d55304e44516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000017489f1d449db1e74bc13230eaad07337e52bc8a00000000000000000000000000000000000000000000000000000058dcc2568d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc4c26dc45952eb4457dac257be6e441348a99af6c271e722bef9e64233d273ee",
      "signature": {
        "s": "0x5f91c4c6fc455943d48d15c0eaa8c3bca830ec5949207649fad4096e20f70f5b",
        "r": "0xedb5e3293cffc9eaa775417ff732dd9b81481c70c394cde5c704b8865fda1604",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x62cb5a9c6d7482f0b3f5e332cd8c433f0cc10fab22da7af40f1ba3757ac36ced",
      "signature": {
        "s": "0x1e5b4982ea0697660596b673f7df9c9347794a2f4afbfee1d7fe30e061a971d5",
        "r": "0xe75dc40317e038ee9beacba909addd881a73efc1a10b92858898fd8235f9ccd8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "381660845709",
    "total": "381660845709"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "381660845709",
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
            "amount": "32168912034"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "381660845"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNGI4YzllMi1kOWM3LTU0ZDItODU3Zi1mMjdhMjg2NmU0NDQifQ==",
    "nonce": 5338,
    "balances": {
      "current": "12985518013256396",
      "previous": "12985900055762950"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x17489f1d449db1e74bc13230eaad07337e52bc8a",
    "nonce": 22,
    "balances": {
      "current": "381660845709",
      "previous": "0"
    }
  },
  "blockNumber": "10114659",
  "created": "2020-05-22T08:40:20.982Z",
  "updated": "2020-05-22T08:40:21.048Z",
  "id": "5ec78ff4005df800101bc930"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000058dcc2568d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `381660845709`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`