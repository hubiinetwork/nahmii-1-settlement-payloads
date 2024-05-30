# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1266Bc91e136333D977c5aC56eA9Cda1deb32C01`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000005285f400000000000000000000000000000000000000000000000000000000005285f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000005285f400000000000000000000000000000000000000000000000000000000005285f4c1118ba3a57c0448cfb5b589f554c4f140f61befbf7baadf5e528d04678c8ac8ef2f1adf1cd3d6236e3d47eb6b4264e462456d9f19a9ffd14c4d2e86ac072a31344889da7bf8d2599da91f79b40ca49e0061f56eddf60e1865d9452cd18ff296000000000000000000000000000000000000000000000000000000000000001b8c79da106c442a6e896ca71c79cf5a0ebc08af652f73a37da1bd431f8b504b054c95b760de792dc4af2eee3e231e1c7e4d5d1ca99a6e3a33132d52c1d35fb65f14d24e5a6a9a8fff0e9b9640b97272496b54fa0ec07d89d9564ce6d4bfffb275000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2eba05138000000000000000000000000000000000000000000000000002386f2ebf2ec4c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000015200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000018d600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d7a526a4f5451355a6930314d7a5a6d4c545533597a51744f4441334d79303059324d335a4467794d4451305a54556966513d3d00000000000000000000000000000000000000000000000000000000000000180000000000000000000000001266bc91e136333d977c5ac56ea9cda1deb32c0100000000000000000000000000000000000000000000000000000000005285f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc1118ba3a57c0448cfb5b589f554c4f140f61befbf7baadf5e528d04678c8ac8",
      "signature": {
        "s": "0x344889da7bf8d2599da91f79b40ca49e0061f56eddf60e1865d9452cd18ff296",
        "r": "0xef2f1adf1cd3d6236e3d47eb6b4264e462456d9f19a9ffd14c4d2e86ac072a31",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8c79da106c442a6e896ca71c79cf5a0ebc08af652f73a37da1bd431f8b504b05",
      "signature": {
        "s": "0x14d24e5a6a9a8fff0e9b9640b97272496b54fa0ec07d89d9564ce6d4bfffb275",
        "r": "0x4c95b760de792dc4af2eee3e231e1c7e4d5d1ca99a6e3a33132d52c1d35fb65f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5408244",
    "total": "5408244"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5408244",
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
            "amount": "6358"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5408"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMzRjOTQ5Zi01MzZmLTU3YzQtODA3My00Y2M3ZDgyMDQ0ZTUifQ==",
    "nonce": 10,
    "balances": {
      "current": "10000002078232888",
      "previous": "10000002083646540"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1266bc91e136333d977c5ac56ea9cda1deb32c01",
    "nonce": 24,
    "balances": {
      "current": "5408244",
      "previous": "0"
    }
  },
  "blockNumber": "10114486",
  "created": "2020-05-22T07:59:07.475Z",
  "updated": "2020-05-22T07:59:07.545Z",
  "id": "5ec7864be5756b00111b7f75"
}
```
* *stageAmount*: `5408244`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000005285f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000005285f400000000000000000000000000000000000000000000000000000000005285f4c1118ba3a57c0448cfb5b589f554c4f140f61befbf7baadf5e528d04678c8ac8ef2f1adf1cd3d6236e3d47eb6b4264e462456d9f19a9ffd14c4d2e86ac072a31344889da7bf8d2599da91f79b40ca49e0061f56eddf60e1865d9452cd18ff296000000000000000000000000000000000000000000000000000000000000001b8c79da106c442a6e896ca71c79cf5a0ebc08af652f73a37da1bd431f8b504b054c95b760de792dc4af2eee3e231e1c7e4d5d1ca99a6e3a33132d52c1d35fb65f14d24e5a6a9a8fff0e9b9640b97272496b54fa0ec07d89d9564ce6d4bfffb275000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2eba05138000000000000000000000000000000000000000000000000002386f2ebf2ec4c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000015200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000018d600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d7a526a4f5451355a6930314d7a5a6d4c545533597a51744f4441334d79303059324d335a4467794d4451305a54556966513d3d00000000000000000000000000000000000000000000000000000000000000180000000000000000000000001266bc91e136333d977c5ac56ea9cda1deb32c0100000000000000000000000000000000000000000000000000000000005285f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc1118ba3a57c0448cfb5b589f554c4f140f61befbf7baadf5e528d04678c8ac8",
      "signature": {
        "s": "0x344889da7bf8d2599da91f79b40ca49e0061f56eddf60e1865d9452cd18ff296",
        "r": "0xef2f1adf1cd3d6236e3d47eb6b4264e462456d9f19a9ffd14c4d2e86ac072a31",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8c79da106c442a6e896ca71c79cf5a0ebc08af652f73a37da1bd431f8b504b05",
      "signature": {
        "s": "0x14d24e5a6a9a8fff0e9b9640b97272496b54fa0ec07d89d9564ce6d4bfffb275",
        "r": "0x4c95b760de792dc4af2eee3e231e1c7e4d5d1ca99a6e3a33132d52c1d35fb65f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5408244",
    "total": "5408244"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5408244",
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
            "amount": "6358"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5408"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMzRjOTQ5Zi01MzZmLTU3YzQtODA3My00Y2M3ZDgyMDQ0ZTUifQ==",
    "nonce": 10,
    "balances": {
      "current": "10000002078232888",
      "previous": "10000002083646540"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1266bc91e136333d977c5ac56ea9cda1deb32c01",
    "nonce": 24,
    "balances": {
      "current": "5408244",
      "previous": "0"
    }
  },
  "blockNumber": "10114486",
  "created": "2020-05-22T07:59:07.475Z",
  "updated": "2020-05-22T07:59:07.545Z",
  "id": "5ec7864be5756b00111b7f75"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000005285f40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5408244`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``