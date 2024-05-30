# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAd67A06237c0B7eb3A86B401877F96fF4e9e765B`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001659a400000000000000000000000000000000000000000000000000000000001659a400000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001659a400000000000000000000000000000000000000000000000000000000001659a400b8a496f77f5bb3708bb3799714b12b3fce0d1826c406e5670790ed8a747ea28c85827936b2cc36df92c4bf5d09b3c6d203978a7f5cabc5cf9c21d249d10bac4d68b6c2ebb2f8552f77cc206a27d9db051528d12504527c2f4d1abb6554fb49d4000000000000000000000000000000000000000000000000000000000000001be3bf3940318a1cb6c5a703be2b6b660eb036a61e96308eda33836b68ba6cbb9fc5c95b40a13c5c4560ef90fff794f4fc948a3aab1d7e19400493d60b3f77a4d671db665883815fed323d32c7ad9477308d4490802d2efe3269c5a3a1b5ef2c19000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5681000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017d800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0fa8947eaa000000000000000000000000000000000000000000000000002e1b0fbef3db6700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005b8bd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000954b792a5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e7a55335932466b4f5330774f5755784c545577595449744f544e6a4f43307a4d3259314d546b795a4459785954636966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000ad67a06237c0b7eb3a86b401877f96ff4e9e765b000000000000000000000000000000000000000000000000000000001659a400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb8a496f77f5bb3708bb3799714b12b3fce0d1826c406e5670790ed8a747ea28c",
      "signature": {
        "s": "0x68b6c2ebb2f8552f77cc206a27d9db051528d12504527c2f4d1abb6554fb49d4",
        "r": "0x85827936b2cc36df92c4bf5d09b3c6d203978a7f5cabc5cf9c21d249d10bac4d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe3bf3940318a1cb6c5a703be2b6b660eb036a61e96308eda33836b68ba6cbb9f",
      "signature": {
        "s": "0x71db665883815fed323d32c7ad9477308d4490802d2efe3269c5a3a1b5ef2c19",
        "r": "0xc5c95b40a13c5c4560ef90fff794f4fc948a3aab1d7e19400493d60b3f77a4d6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "374973440",
    "total": "374973440"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "374973440",
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
            "amount": "40076022437"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "374973"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NzU3Y2FkOS0wOWUxLTUwYTItOTNjOC0zM2Y1MTkyZDYxYTcifQ==",
    "nonce": 6104,
    "balances": {
      "current": "12977602995453610",
      "previous": "12977603370802023"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xad67a06237c0b7eb3a86b401877f96ff4e9e765b",
    "nonce": 22,
    "balances": {
      "current": "374973440",
      "previous": "0"
    }
  },
  "blockNumber": "10114689",
  "created": "2020-05-22T08:46:28.713Z",
  "updated": "2020-05-22T08:46:28.793Z",
  "id": "5ec79164e5756b00111b8741"
}
```
* *stageAmount*: `374973440`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001659a400000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001659a400000000000000000000000000000000000000000000000000000000001659a400b8a496f77f5bb3708bb3799714b12b3fce0d1826c406e5670790ed8a747ea28c85827936b2cc36df92c4bf5d09b3c6d203978a7f5cabc5cf9c21d249d10bac4d68b6c2ebb2f8552f77cc206a27d9db051528d12504527c2f4d1abb6554fb49d4000000000000000000000000000000000000000000000000000000000000001be3bf3940318a1cb6c5a703be2b6b660eb036a61e96308eda33836b68ba6cbb9fc5c95b40a13c5c4560ef90fff794f4fc948a3aab1d7e19400493d60b3f77a4d671db665883815fed323d32c7ad9477308d4490802d2efe3269c5a3a1b5ef2c19000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5681000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017d800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0fa8947eaa000000000000000000000000000000000000000000000000002e1b0fbef3db6700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005b8bd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000954b792a5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e7a55335932466b4f5330774f5755784c545577595449744f544e6a4f43307a4d3259314d546b795a4459785954636966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000ad67a06237c0b7eb3a86b401877f96ff4e9e765b000000000000000000000000000000000000000000000000000000001659a400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb8a496f77f5bb3708bb3799714b12b3fce0d1826c406e5670790ed8a747ea28c",
      "signature": {
        "s": "0x68b6c2ebb2f8552f77cc206a27d9db051528d12504527c2f4d1abb6554fb49d4",
        "r": "0x85827936b2cc36df92c4bf5d09b3c6d203978a7f5cabc5cf9c21d249d10bac4d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe3bf3940318a1cb6c5a703be2b6b660eb036a61e96308eda33836b68ba6cbb9f",
      "signature": {
        "s": "0x71db665883815fed323d32c7ad9477308d4490802d2efe3269c5a3a1b5ef2c19",
        "r": "0xc5c95b40a13c5c4560ef90fff794f4fc948a3aab1d7e19400493d60b3f77a4d6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "374973440",
    "total": "374973440"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "374973440",
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
            "amount": "40076022437"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "374973"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NzU3Y2FkOS0wOWUxLTUwYTItOTNjOC0zM2Y1MTkyZDYxYTcifQ==",
    "nonce": 6104,
    "balances": {
      "current": "12977602995453610",
      "previous": "12977603370802023"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xad67a06237c0b7eb3a86b401877f96ff4e9e765b",
    "nonce": 22,
    "balances": {
      "current": "374973440",
      "previous": "0"
    }
  },
  "blockNumber": "10114689",
  "created": "2020-05-22T08:46:28.713Z",
  "updated": "2020-05-22T08:46:28.793Z",
  "id": "5ec79164e5756b00111b8741"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000001659a400000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `374973440`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`