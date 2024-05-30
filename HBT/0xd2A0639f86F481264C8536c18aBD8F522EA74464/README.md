# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd2A0639f86F481264C8536c18aBD8F522EA74464`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000fc454e4000000000000000000000000000000000000000000000000000000000fc454e4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000fc454e4000000000000000000000000000000000000000000000000000000000fc454e49fbd03b3ab1b285bfec9d9dee5cc406e6a206310264760dcafca9e3526eb6934e9aaf2f609e674e9708bd871d853323678b943dc6c240737be7cf079a5279b5151a6b970e9230e54aa3cf0802d2c5eedd28902ecd97666e8531590bd5df9a614000000000000000000000000000000000000000000000000000000000000001c8974b04bfbf7a2a2ffcd09183bdff33f0daf63bcc07e2e3e672d28ad6e30d0416b0f9556a8921ce674fe17fc79e07a292b13b6a8b5fd4159e078a5758b3298cc03f54f68c698c5b2aae5aae58f75d795a5296f595a6e58488f1c88aa12f307ff000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a2100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e170a28a38cb0000000000000000000000000000000000000000000000000002e170a386beae100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000004094d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a5c0176cd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e3259794e54526d4f4331694f5459774c5456694e54597459546b334e5330774e6d4d794d446b304f444a694f57596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d2a0639f86f481264c8536c18abd8f522ea74464000000000000000000000000000000000000000000000000000000000fc454e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9fbd03b3ab1b285bfec9d9dee5cc406e6a206310264760dcafca9e3526eb6934",
      "signature": {
        "s": "0x51a6b970e9230e54aa3cf0802d2c5eedd28902ecd97666e8531590bd5df9a614",
        "r": "0xe9aaf2f609e674e9708bd871d853323678b943dc6c240737be7cf079a5279b51",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8974b04bfbf7a2a2ffcd09183bdff33f0daf63bcc07e2e3e672d28ad6e30d041",
      "signature": {
        "s": "0x03f54f68c698c5b2aae5aae58f75d795a5296f595a6e58488f1c88aa12f307ff",
        "r": "0x6b0f9556a8921ce674fe17fc79e07a292b13b6a8b5fd4159e078a5758b3298cc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "264525028",
    "total": "264525028"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "264525028",
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
            "amount": "44493272781"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "264525"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzN2YyNTRmOC1iOTYwLTViNTYtYTk3NS0wNmMyMDk0ODJiOWYifQ==",
    "nonce": 6689,
    "balances": {
      "current": "12973181327609008",
      "previous": "12973181592398561"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd2a0639f86f481264c8536c18abd8f522ea74464",
    "nonce": 22,
    "balances": {
      "current": "264525028",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:51:00.802Z",
  "updated": "2020-05-22T08:51:00.872Z",
  "id": "5ec79274b0c6090011d5b181"
}
```
* *stageAmount*: `264525028`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000fc454e4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000fc454e4000000000000000000000000000000000000000000000000000000000fc454e49fbd03b3ab1b285bfec9d9dee5cc406e6a206310264760dcafca9e3526eb6934e9aaf2f609e674e9708bd871d853323678b943dc6c240737be7cf079a5279b5151a6b970e9230e54aa3cf0802d2c5eedd28902ecd97666e8531590bd5df9a614000000000000000000000000000000000000000000000000000000000000001c8974b04bfbf7a2a2ffcd09183bdff33f0daf63bcc07e2e3e672d28ad6e30d0416b0f9556a8921ce674fe17fc79e07a292b13b6a8b5fd4159e078a5758b3298cc03f54f68c698c5b2aae5aae58f75d795a5296f595a6e58488f1c88aa12f307ff000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a2100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e170a28a38cb0000000000000000000000000000000000000000000000000002e170a386beae100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000004094d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a5c0176cd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e3259794e54526d4f4331694f5459774c5456694e54597459546b334e5330774e6d4d794d446b304f444a694f57596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d2a0639f86f481264c8536c18abd8f522ea74464000000000000000000000000000000000000000000000000000000000fc454e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9fbd03b3ab1b285bfec9d9dee5cc406e6a206310264760dcafca9e3526eb6934",
      "signature": {
        "s": "0x51a6b970e9230e54aa3cf0802d2c5eedd28902ecd97666e8531590bd5df9a614",
        "r": "0xe9aaf2f609e674e9708bd871d853323678b943dc6c240737be7cf079a5279b51",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8974b04bfbf7a2a2ffcd09183bdff33f0daf63bcc07e2e3e672d28ad6e30d041",
      "signature": {
        "s": "0x03f54f68c698c5b2aae5aae58f75d795a5296f595a6e58488f1c88aa12f307ff",
        "r": "0x6b0f9556a8921ce674fe17fc79e07a292b13b6a8b5fd4159e078a5758b3298cc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "264525028",
    "total": "264525028"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "264525028",
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
            "amount": "44493272781"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "264525"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzN2YyNTRmOC1iOTYwLTViNTYtYTk3NS0wNmMyMDk0ODJiOWYifQ==",
    "nonce": 6689,
    "balances": {
      "current": "12973181327609008",
      "previous": "12973181592398561"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd2a0639f86f481264c8536c18abd8f522ea74464",
    "nonce": 22,
    "balances": {
      "current": "264525028",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:51:00.802Z",
  "updated": "2020-05-22T08:51:00.872Z",
  "id": "5ec79274b0c6090011d5b181"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000fc454e4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `264525028`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`