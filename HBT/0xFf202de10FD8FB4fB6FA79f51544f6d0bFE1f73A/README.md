# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFf202de10FD8FB4fB6FA79f51544f6d0bFE1f73A`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000f8b375e3e0000000000000000000000000000000000000000000000000000000f8b375e3e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000f8b375e3e0000000000000000000000000000000000000000000000000000000f8b375e3e86bb592a698416d1f2c0a4908577fd09e846ef322e156971c3daae544ea1732d7e51225b6d3f8af78555905ec8399c01c4474d387ba08ee245ce6721f53e42c608985442887bf0adf4359393638d82d4c319b440a29bd4164272b60075c5c2c5000000000000000000000000000000000000000000000000000000000000001c6095c1e86e3898f7afe68ee14771cdf3cd17c62e45ce812918ab3caabb89d90d8759c2487e071062bb74d8d5f79be541cc5bb85fcf4df8af962c7637562316d825783508915287458160145340e812f93cc0dc3a3930375c4c090be3d221a62e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56650000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000152500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1dcaf73c6cf1000000000000000000000000000000000000000000000000002e1dda866e791a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003faadeb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008a1df8f92000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d325a685a4456694e69316a59574e6b4c54566a4e4463744f5441784d7930304e6d45794d7a5130597a67795a44556966513d3d000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000ff202de10fd8fb4fb6fa79f51544f6d0bfe1f73a0000000000000000000000000000000000000000000000000000000f8b375e3e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x86bb592a698416d1f2c0a4908577fd09e846ef322e156971c3daae544ea1732d",
      "signature": {
        "s": "0x08985442887bf0adf4359393638d82d4c319b440a29bd4164272b60075c5c2c5",
        "r": "0x7e51225b6d3f8af78555905ec8399c01c4474d387ba08ee245ce6721f53e42c6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6095c1e86e3898f7afe68ee14771cdf3cd17c62e45ce812918ab3caabb89d90d",
      "signature": {
        "s": "0x25783508915287458160145340e812f93cc0dc3a3930375c4c090be3d221a62e",
        "r": "0x8759c2487e071062bb74d8d5f79be541cc5bb85fcf4df8af962c7637562316d8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "66760171070",
    "total": "66760171070"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "66760171070",
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
            "amount": "37075521426"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "66760171"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiM2ZhZDViNi1jYWNkLTVjNDctOTAxMy00NmEyMzQ0YzgyZDUifQ==",
    "nonce": 5413,
    "balances": {
      "current": "12980606497221873",
      "previous": "12980673324153114"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xff202de10fd8fb4fb6fa79f51544f6d0bfe1f73a",
    "nonce": 26,
    "balances": {
      "current": "66760171070",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:53.115Z",
  "updated": "2020-05-22T08:40:53.229Z",
  "id": "5ec79015005df800101bc94c"
}
```
* *stageAmount*: `66760171070`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000f8b375e3e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000f8b375e3e0000000000000000000000000000000000000000000000000000000f8b375e3e86bb592a698416d1f2c0a4908577fd09e846ef322e156971c3daae544ea1732d7e51225b6d3f8af78555905ec8399c01c4474d387ba08ee245ce6721f53e42c608985442887bf0adf4359393638d82d4c319b440a29bd4164272b60075c5c2c5000000000000000000000000000000000000000000000000000000000000001c6095c1e86e3898f7afe68ee14771cdf3cd17c62e45ce812918ab3caabb89d90d8759c2487e071062bb74d8d5f79be541cc5bb85fcf4df8af962c7637562316d825783508915287458160145340e812f93cc0dc3a3930375c4c090be3d221a62e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56650000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000152500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1dcaf73c6cf1000000000000000000000000000000000000000000000000002e1dda866e791a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003faadeb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008a1df8f92000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d325a685a4456694e69316a59574e6b4c54566a4e4463744f5441784d7930304e6d45794d7a5130597a67795a44556966513d3d000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000ff202de10fd8fb4fb6fa79f51544f6d0bfe1f73a0000000000000000000000000000000000000000000000000000000f8b375e3e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x86bb592a698416d1f2c0a4908577fd09e846ef322e156971c3daae544ea1732d",
      "signature": {
        "s": "0x08985442887bf0adf4359393638d82d4c319b440a29bd4164272b60075c5c2c5",
        "r": "0x7e51225b6d3f8af78555905ec8399c01c4474d387ba08ee245ce6721f53e42c6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6095c1e86e3898f7afe68ee14771cdf3cd17c62e45ce812918ab3caabb89d90d",
      "signature": {
        "s": "0x25783508915287458160145340e812f93cc0dc3a3930375c4c090be3d221a62e",
        "r": "0x8759c2487e071062bb74d8d5f79be541cc5bb85fcf4df8af962c7637562316d8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "66760171070",
    "total": "66760171070"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "66760171070",
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
            "amount": "37075521426"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "66760171"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiM2ZhZDViNi1jYWNkLTVjNDctOTAxMy00NmEyMzQ0YzgyZDUifQ==",
    "nonce": 5413,
    "balances": {
      "current": "12980606497221873",
      "previous": "12980673324153114"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xff202de10fd8fb4fb6fa79f51544f6d0bfe1f73a",
    "nonce": 26,
    "balances": {
      "current": "66760171070",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:53.115Z",
  "updated": "2020-05-22T08:40:53.229Z",
  "id": "5ec79015005df800101bc94c"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000f8b375e3e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `66760171070`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`