# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x377aa084c119c3Cc8ef4f4CD39a6e59f399205be`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000a54ce72000000000000000000000000000000000000000000000000000000000a54ce72000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000a54ce72000000000000000000000000000000000000000000000000000000000a54ce7298c2d8d4c6e55828e7cdf5a6669dd6c22c96b8f33bdb8b1973c5145b77e5e549c6efcfa4132fe811b176dd09e10a1f0654b99cd7333b0d93a778aee1785ba2c1439c6d70707782ad40f6af91ee97aae85b4a2241e9e5e1c7a0df197c2c94c7e7000000000000000000000000000000000000000000000000000000000000001c8f70486855c09005c5bba68d0e50b7ced2d8303cc10443681e889d203d1ecc64b225523f3dddfb6e1c77a11b1766398b10d9c4a415bf0f3d63de76f13d86503d2951530d097fc5f81d22e4ccacb308e296eb9b8aec180f147515f1b0435560a6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56960000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000197800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17df04d474cc000000000000000000000000000000000000000000000000002e17df0f2be85000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002a512000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a25916687000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596a673459546b354f43316d4d7a45774c545532596d4d74596d466b4d6931685a446b7a4e3251784e47557a4f546b6966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000377aa084c119c3cc8ef4f4cd39a6e59f399205be000000000000000000000000000000000000000000000000000000000a54ce72000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x98c2d8d4c6e55828e7cdf5a6669dd6c22c96b8f33bdb8b1973c5145b77e5e549",
      "signature": {
        "s": "0x439c6d70707782ad40f6af91ee97aae85b4a2241e9e5e1c7a0df197c2c94c7e7",
        "r": "0xc6efcfa4132fe811b176dd09e10a1f0654b99cd7333b0d93a778aee1785ba2c1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8f70486855c09005c5bba68d0e50b7ced2d8303cc10443681e889d203d1ecc64",
      "signature": {
        "s": "0x2951530d097fc5f81d22e4ccacb308e296eb9b8aec180f147515f1b0435560a6",
        "r": "0xb225523f3dddfb6e1c77a11b1766398b10d9c4a415bf0f3d63de76f13d86503d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "173330034",
    "total": "173330034"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "173330034",
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
            "amount": "43579958919"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "173330"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4Yjg4YTk5OC1mMzEwLTU2YmMtYmFkMi1hZDkzN2QxNGUzOTkifQ==",
    "nonce": 6520,
    "balances": {
      "current": "12974095554868428",
      "previous": "12974095728371792"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x377aa084c119c3cc8ef4f4cd39a6e59f399205be",
    "nonce": 11,
    "balances": {
      "current": "173330034",
      "previous": "0"
    }
  },
  "blockNumber": "10114710",
  "created": "2020-05-22T08:49:48.664Z",
  "updated": "2020-05-22T08:49:48.730Z",
  "id": "5ec7922cb0c6090011d5b14e"
}
```
* *stageAmount*: `173330034`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000a54ce72000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000a54ce72000000000000000000000000000000000000000000000000000000000a54ce7298c2d8d4c6e55828e7cdf5a6669dd6c22c96b8f33bdb8b1973c5145b77e5e549c6efcfa4132fe811b176dd09e10a1f0654b99cd7333b0d93a778aee1785ba2c1439c6d70707782ad40f6af91ee97aae85b4a2241e9e5e1c7a0df197c2c94c7e7000000000000000000000000000000000000000000000000000000000000001c8f70486855c09005c5bba68d0e50b7ced2d8303cc10443681e889d203d1ecc64b225523f3dddfb6e1c77a11b1766398b10d9c4a415bf0f3d63de76f13d86503d2951530d097fc5f81d22e4ccacb308e296eb9b8aec180f147515f1b0435560a6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56960000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000197800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17df04d474cc000000000000000000000000000000000000000000000000002e17df0f2be85000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002a512000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a25916687000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596a673459546b354f43316d4d7a45774c545532596d4d74596d466b4d6931685a446b7a4e3251784e47557a4f546b6966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000377aa084c119c3cc8ef4f4cd39a6e59f399205be000000000000000000000000000000000000000000000000000000000a54ce72000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x98c2d8d4c6e55828e7cdf5a6669dd6c22c96b8f33bdb8b1973c5145b77e5e549",
      "signature": {
        "s": "0x439c6d70707782ad40f6af91ee97aae85b4a2241e9e5e1c7a0df197c2c94c7e7",
        "r": "0xc6efcfa4132fe811b176dd09e10a1f0654b99cd7333b0d93a778aee1785ba2c1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8f70486855c09005c5bba68d0e50b7ced2d8303cc10443681e889d203d1ecc64",
      "signature": {
        "s": "0x2951530d097fc5f81d22e4ccacb308e296eb9b8aec180f147515f1b0435560a6",
        "r": "0xb225523f3dddfb6e1c77a11b1766398b10d9c4a415bf0f3d63de76f13d86503d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "173330034",
    "total": "173330034"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "173330034",
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
            "amount": "43579958919"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "173330"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4Yjg4YTk5OC1mMzEwLTU2YmMtYmFkMi1hZDkzN2QxNGUzOTkifQ==",
    "nonce": 6520,
    "balances": {
      "current": "12974095554868428",
      "previous": "12974095728371792"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x377aa084c119c3cc8ef4f4cd39a6e59f399205be",
    "nonce": 11,
    "balances": {
      "current": "173330034",
      "previous": "0"
    }
  },
  "blockNumber": "10114710",
  "created": "2020-05-22T08:49:48.664Z",
  "updated": "2020-05-22T08:49:48.730Z",
  "id": "5ec7922cb0c6090011d5b14e"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000a54ce72000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `173330034`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`