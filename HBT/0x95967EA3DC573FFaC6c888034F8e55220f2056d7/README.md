# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x95967EA3DC573FFaC6c888034F8e55220f2056d7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000002330b73f000000000000000000000000000000000000000000000000000000002330b73f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002330b73f000000000000000000000000000000000000000000000000000000002330b73f3ca3fda1c3de37e0ec2ba287f08bf028b89c3cf42908b341967b1dcb4ad4693ab58452794373b032a6d8750aec9fc1ae99c87d0f29c14f85c886833bd83a40b77a5b6ab5ead98d7719cbba385e78d80ea8d9a5f12ba3e9e8d693f0c0c9e4b52a000000000000000000000000000000000000000000000000000000000000001c19f1811fce7560b3f5baf8fd620bf0eebd836458a7ff5d4b0bb51aa7f9ed348d4f5cb8e39d8353e49c67fb77dcdc9444f569861f4239b83aad3262c2078e20f036f41326508c7a6322aed25bf081c9ae61b2819c39a9750cc401886013fc0a07000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5681000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017da00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0f6b918636000000000000000000000000000000000000000000000000002e1b0f8ecb3fb000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000009023b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000954c72d1b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e54566a596d46684d69316c5a5467334c54566c4d5449744f4467314f5330774e6a4d354d7a426a4e7a686c596d556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000095967ea3dc573ffac6c888034f8e55220f2056d7000000000000000000000000000000000000000000000000000000002330b73f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3ca3fda1c3de37e0ec2ba287f08bf028b89c3cf42908b341967b1dcb4ad4693a",
      "signature": {
        "s": "0x7a5b6ab5ead98d7719cbba385e78d80ea8d9a5f12ba3e9e8d693f0c0c9e4b52a",
        "r": "0xb58452794373b032a6d8750aec9fc1ae99c87d0f29c14f85c886833bd83a40b7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x19f1811fce7560b3f5baf8fd620bf0eebd836458a7ff5d4b0bb51aa7f9ed348d",
      "signature": {
        "s": "0x36f41326508c7a6322aed25bf081c9ae61b2819c39a9750cc401886013fc0a07",
        "r": "0x4f5cb8e39d8353e49c67fb77dcdc9444f569861f4239b83aad3262c2078e20f0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "590395199",
    "total": "590395199"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "590395199",
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
            "amount": "40077045019"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "590395"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2NTVjYmFhMi1lZTg3LTVlMTItODg1OS0wNjM5MzBjNzhlYmUifQ==",
    "nonce": 6106,
    "balances": {
      "current": "12977601971848758",
      "previous": "12977602562834352"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x95967ea3dc573ffac6c888034f8e55220f2056d7",
    "nonce": 22,
    "balances": {
      "current": "590395199",
      "previous": "0"
    }
  },
  "blockNumber": "10114689",
  "created": "2020-05-22T08:46:31.692Z",
  "updated": "2020-05-22T08:46:31.769Z",
  "id": "5ec79167e5756b00111b8742"
}
```
* *stageAmount*: `590395199`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000002330b73f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002330b73f000000000000000000000000000000000000000000000000000000002330b73f3ca3fda1c3de37e0ec2ba287f08bf028b89c3cf42908b341967b1dcb4ad4693ab58452794373b032a6d8750aec9fc1ae99c87d0f29c14f85c886833bd83a40b77a5b6ab5ead98d7719cbba385e78d80ea8d9a5f12ba3e9e8d693f0c0c9e4b52a000000000000000000000000000000000000000000000000000000000000001c19f1811fce7560b3f5baf8fd620bf0eebd836458a7ff5d4b0bb51aa7f9ed348d4f5cb8e39d8353e49c67fb77dcdc9444f569861f4239b83aad3262c2078e20f036f41326508c7a6322aed25bf081c9ae61b2819c39a9750cc401886013fc0a07000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5681000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017da00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0f6b918636000000000000000000000000000000000000000000000000002e1b0f8ecb3fb000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000009023b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000954c72d1b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e54566a596d46684d69316c5a5467334c54566c4d5449744f4467314f5330774e6a4d354d7a426a4e7a686c596d556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000095967ea3dc573ffac6c888034f8e55220f2056d7000000000000000000000000000000000000000000000000000000002330b73f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3ca3fda1c3de37e0ec2ba287f08bf028b89c3cf42908b341967b1dcb4ad4693a",
      "signature": {
        "s": "0x7a5b6ab5ead98d7719cbba385e78d80ea8d9a5f12ba3e9e8d693f0c0c9e4b52a",
        "r": "0xb58452794373b032a6d8750aec9fc1ae99c87d0f29c14f85c886833bd83a40b7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x19f1811fce7560b3f5baf8fd620bf0eebd836458a7ff5d4b0bb51aa7f9ed348d",
      "signature": {
        "s": "0x36f41326508c7a6322aed25bf081c9ae61b2819c39a9750cc401886013fc0a07",
        "r": "0x4f5cb8e39d8353e49c67fb77dcdc9444f569861f4239b83aad3262c2078e20f0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "590395199",
    "total": "590395199"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "590395199",
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
            "amount": "40077045019"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "590395"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2NTVjYmFhMi1lZTg3LTVlMTItODg1OS0wNjM5MzBjNzhlYmUifQ==",
    "nonce": 6106,
    "balances": {
      "current": "12977601971848758",
      "previous": "12977602562834352"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x95967ea3dc573ffac6c888034f8e55220f2056d7",
    "nonce": 22,
    "balances": {
      "current": "590395199",
      "previous": "0"
    }
  },
  "blockNumber": "10114689",
  "created": "2020-05-22T08:46:31.692Z",
  "updated": "2020-05-22T08:46:31.769Z",
  "id": "5ec79167e5756b00111b8742"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000002330b73f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `590395199`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`