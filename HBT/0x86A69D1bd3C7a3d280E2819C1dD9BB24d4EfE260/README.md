# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x86A69D1bd3C7a3d280E2819C1dD9BB24d4EfE260`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000007e23bf30000000000000000000000000000000000000000000000000000000007e23bf3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000007e23bf30000000000000000000000000000000000000000000000000000000007e23bf381f2a16cae452fb2333ac1465b006acbee7914a87df1940452e2259f9cfefcbd9d4899b1905636e380d4f42ee87b73d0285623c73c95fde1578f326f8eed7c87329565a58c7314a6a742b62c21f03ebbf02dfc8de3e970b68395223c2485a098000000000000000000000000000000000000000000000000000000000000001b4bfbc51da717213b8a36b7225b072ea81a3da3e7d0f4b2770e623f755631ed5f847ad08fb5832e59b21606214374a4ae003673e80fdfeaabfa1ee5843406e5f46528d4c5252217dec6ddaba354add4e926d9ad802a73fe080e4c765662cd95ff000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5676000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016f400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b448db75990000000000000000000000000000000000000000000000000002e1b44959b9a2d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000204aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009473081b9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a597a4e6c4d6d51794f433079595755344c5455794d544974595745314d5330784d4467355a5468694d6a5a6a4d47496966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000086a69d1bd3c7a3d280e2819c1dd9bb24d4efe2600000000000000000000000000000000000000000000000000000000007e23bf3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x81f2a16cae452fb2333ac1465b006acbee7914a87df1940452e2259f9cfefcbd",
      "signature": {
        "s": "0x329565a58c7314a6a742b62c21f03ebbf02dfc8de3e970b68395223c2485a098",
        "r": "0x9d4899b1905636e380d4f42ee87b73d0285623c73c95fde1578f326f8eed7c87",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4bfbc51da717213b8a36b7225b072ea81a3da3e7d0f4b2770e623f755631ed5f",
      "signature": {
        "s": "0x6528d4c5252217dec6ddaba354add4e926d9ad802a73fe080e4c765662cd95ff",
        "r": "0x847ad08fb5832e59b21606214374a4ae003673e80fdfeaabfa1ee5843406e5f4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "132266995",
    "total": "132266995"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "132266995",
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
            "amount": "39849066937"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "132266"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYzNlMmQyOC0yYWU4LTUyMTItYWE1MS0xMDg5ZThiMjZjMGIifQ==",
    "nonce": 5876,
    "balances": {
      "current": "12977830178019728",
      "previous": "12977830310418989"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x86a69d1bd3c7a3d280e2819c1dd9bb24d4efe260",
    "nonce": 22,
    "balances": {
      "current": "132266995",
      "previous": "0"
    }
  },
  "blockNumber": "10114678",
  "created": "2020-05-22T08:44:39.424Z",
  "updated": "2020-05-22T08:44:39.496Z",
  "id": "5ec790f7e5756b00111b86fa"
}
```
* *stageAmount*: `132266995`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000007e23bf3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000007e23bf30000000000000000000000000000000000000000000000000000000007e23bf381f2a16cae452fb2333ac1465b006acbee7914a87df1940452e2259f9cfefcbd9d4899b1905636e380d4f42ee87b73d0285623c73c95fde1578f326f8eed7c87329565a58c7314a6a742b62c21f03ebbf02dfc8de3e970b68395223c2485a098000000000000000000000000000000000000000000000000000000000000001b4bfbc51da717213b8a36b7225b072ea81a3da3e7d0f4b2770e623f755631ed5f847ad08fb5832e59b21606214374a4ae003673e80fdfeaabfa1ee5843406e5f46528d4c5252217dec6ddaba354add4e926d9ad802a73fe080e4c765662cd95ff000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5676000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016f400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b448db75990000000000000000000000000000000000000000000000000002e1b44959b9a2d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000204aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009473081b9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a597a4e6c4d6d51794f433079595755344c5455794d544974595745314d5330784d4467355a5468694d6a5a6a4d47496966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000086a69d1bd3c7a3d280e2819c1dd9bb24d4efe2600000000000000000000000000000000000000000000000000000000007e23bf3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x81f2a16cae452fb2333ac1465b006acbee7914a87df1940452e2259f9cfefcbd",
      "signature": {
        "s": "0x329565a58c7314a6a742b62c21f03ebbf02dfc8de3e970b68395223c2485a098",
        "r": "0x9d4899b1905636e380d4f42ee87b73d0285623c73c95fde1578f326f8eed7c87",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4bfbc51da717213b8a36b7225b072ea81a3da3e7d0f4b2770e623f755631ed5f",
      "signature": {
        "s": "0x6528d4c5252217dec6ddaba354add4e926d9ad802a73fe080e4c765662cd95ff",
        "r": "0x847ad08fb5832e59b21606214374a4ae003673e80fdfeaabfa1ee5843406e5f4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "132266995",
    "total": "132266995"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "132266995",
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
            "amount": "39849066937"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "132266"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYzNlMmQyOC0yYWU4LTUyMTItYWE1MS0xMDg5ZThiMjZjMGIifQ==",
    "nonce": 5876,
    "balances": {
      "current": "12977830178019728",
      "previous": "12977830310418989"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x86a69d1bd3c7a3d280e2819c1dd9bb24d4efe260",
    "nonce": 22,
    "balances": {
      "current": "132266995",
      "previous": "0"
    }
  },
  "blockNumber": "10114678",
  "created": "2020-05-22T08:44:39.424Z",
  "updated": "2020-05-22T08:44:39.496Z",
  "id": "5ec790f7e5756b00111b86fa"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000007e23bf3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `132266995`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`