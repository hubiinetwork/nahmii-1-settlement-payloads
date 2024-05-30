# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x05E6B955d226931c64A26DE1E0D0E9AE232ee4dc`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000007c2b3033000000000000000000000000000000000000000000000000000000007c2b3033000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000007c2b3033000000000000000000000000000000000000000000000000000000007c2b30336085026302aa0f77ff706846a206c311e1a0a09c24fd94e4c4258865c7c7459437cc818fa58da70f46413edd50b709bf571479577debabe98dee5e91b37bd7d7561dc043c422367057bd62859779c8e025d92b67c32ce5e57118603440a44a1e000000000000000000000000000000000000000000000000000000000000001c8fd6a58723f02532f48a55ebd8fd1bd6802d3805a4c840494a0a2d4f5f3957ec85fdbd3f6913f4449e12c7224743a0f787a36834b9b12cfd39fbadfca2ab97d51d422e2b2928d67c6b0a46e7c8a170269b9565f1e36debc1ea815f1ad1f80692000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5676000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016ef00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b460a7c908f000000000000000000000000000000000000000000000000002e1b4686c78a4700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001fc985000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000946cf207e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6a63304e44597a596930784d7a457a4c54566b5a6a5174595745304e69316c595455325a474d355a4452694f44596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000005e6b955d226931c64a26de1e0d0e9ae232ee4dc000000000000000000000000000000000000000000000000000000007c2b3033000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6085026302aa0f77ff706846a206c311e1a0a09c24fd94e4c4258865c7c74594",
      "signature": {
        "s": "0x561dc043c422367057bd62859779c8e025d92b67c32ce5e57118603440a44a1e",
        "r": "0x37cc818fa58da70f46413edd50b709bf571479577debabe98dee5e91b37bd7d7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8fd6a58723f02532f48a55ebd8fd1bd6802d3805a4c840494a0a2d4f5f3957ec",
      "signature": {
        "s": "0x1d422e2b2928d67c6b0a46e7c8a170269b9565f1e36debc1ea815f1ad1f80692",
        "r": "0x85fdbd3f6913f4449e12c7224743a0f787a36834b9b12cfd39fbadfca2ab97d5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2083205171",
    "total": "2083205171"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2083205171",
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
            "amount": "39842685054"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2083205"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2Mjc0NDYzYi0xMzEzLTVkZjQtYWE0Ni1lYTU2ZGM5ZDRiODYifQ==",
    "nonce": 5871,
    "balances": {
      "current": "12977836566286479",
      "previous": "12977838651574855"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x05e6b955d226931c64a26de1e0d0e9ae232ee4dc",
    "nonce": 22,
    "balances": {
      "current": "2083205171",
      "previous": "0"
    }
  },
  "blockNumber": "10114678",
  "created": "2020-05-22T08:44:35.334Z",
  "updated": "2020-05-22T08:44:35.476Z",
  "id": "5ec790f3b0c6090011d5b063"
}
```
* *stageAmount*: `2083205171`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000007c2b3033000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000007c2b3033000000000000000000000000000000000000000000000000000000007c2b30336085026302aa0f77ff706846a206c311e1a0a09c24fd94e4c4258865c7c7459437cc818fa58da70f46413edd50b709bf571479577debabe98dee5e91b37bd7d7561dc043c422367057bd62859779c8e025d92b67c32ce5e57118603440a44a1e000000000000000000000000000000000000000000000000000000000000001c8fd6a58723f02532f48a55ebd8fd1bd6802d3805a4c840494a0a2d4f5f3957ec85fdbd3f6913f4449e12c7224743a0f787a36834b9b12cfd39fbadfca2ab97d51d422e2b2928d67c6b0a46e7c8a170269b9565f1e36debc1ea815f1ad1f80692000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5676000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016ef00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b460a7c908f000000000000000000000000000000000000000000000000002e1b4686c78a4700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001fc985000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000946cf207e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6a63304e44597a596930784d7a457a4c54566b5a6a5174595745304e69316c595455325a474d355a4452694f44596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000005e6b955d226931c64a26de1e0d0e9ae232ee4dc000000000000000000000000000000000000000000000000000000007c2b3033000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6085026302aa0f77ff706846a206c311e1a0a09c24fd94e4c4258865c7c74594",
      "signature": {
        "s": "0x561dc043c422367057bd62859779c8e025d92b67c32ce5e57118603440a44a1e",
        "r": "0x37cc818fa58da70f46413edd50b709bf571479577debabe98dee5e91b37bd7d7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8fd6a58723f02532f48a55ebd8fd1bd6802d3805a4c840494a0a2d4f5f3957ec",
      "signature": {
        "s": "0x1d422e2b2928d67c6b0a46e7c8a170269b9565f1e36debc1ea815f1ad1f80692",
        "r": "0x85fdbd3f6913f4449e12c7224743a0f787a36834b9b12cfd39fbadfca2ab97d5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2083205171",
    "total": "2083205171"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2083205171",
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
            "amount": "39842685054"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2083205"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2Mjc0NDYzYi0xMzEzLTVkZjQtYWE0Ni1lYTU2ZGM5ZDRiODYifQ==",
    "nonce": 5871,
    "balances": {
      "current": "12977836566286479",
      "previous": "12977838651574855"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x05e6b955d226931c64a26de1e0d0e9ae232ee4dc",
    "nonce": 22,
    "balances": {
      "current": "2083205171",
      "previous": "0"
    }
  },
  "blockNumber": "10114678",
  "created": "2020-05-22T08:44:35.334Z",
  "updated": "2020-05-22T08:44:35.476Z",
  "id": "5ec790f3b0c6090011d5b063"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000007c2b3033000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2083205171`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`