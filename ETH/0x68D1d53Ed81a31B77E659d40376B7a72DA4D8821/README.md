# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x68D1d53Ed81a31B77E659d40376B7a72DA4D8821`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000005f000000000000000000000000000000000000000000000000000000000000005f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000005f000000000000000000000000000000000000000000000000000000000000005f85fc20059d1b6dc8eb565274d5fb6f109b99c7e614db4cc24378a6d947144b49cfa9a76f5514b235e314baa9a0e370952dffd63b06ae2b602ca97d62c4bdf9e2202ff38221d040515da2bdc0eef7a0b6410e3e77b7970df0d87484cef0ae0a58000000000000000000000000000000000000000000000000000000000000001bae772416902d5e21111199b365d890de5bdb7bab8ada4a0c9854e2d4d4d4fbf419de06ea70ded3ffbd701072a8b07845d3a35be77ba914b0af89be61ba31814a30bbb373460b42948f36f1bf5ef0c42de57d8a990deafc795d0a1176b34bdc6d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc4ede66000000000000000000000000000000000000000000000000002386f2bc4edec600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c303700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a6d51334f574d334d7930305a5455354c5455784f5441744f4755344f53307a597a45784d545133596a426d596d596966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000068d1d53ed81a31b77e659d40376b7a72da4d8821000000000000000000000000000000000000000000000000000000000000005f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x85fc20059d1b6dc8eb565274d5fb6f109b99c7e614db4cc24378a6d947144b49",
      "signature": {
        "s": "0x202ff38221d040515da2bdc0eef7a0b6410e3e77b7970df0d87484cef0ae0a58",
        "r": "0xcfa9a76f5514b235e314baa9a0e370952dffd63b06ae2b602ca97d62c4bdf9e2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xae772416902d5e21111199b365d890de5bdb7bab8ada4a0c9854e2d4d4d4fbf4",
      "signature": {
        "s": "0x30bbb373460b42948f36f1bf5ef0c42de57d8a990deafc795d0a1176b34bdc6d",
        "r": "0x19de06ea70ded3ffbd701072a8b07845d3a35be77ba914b0af89be61ba31814a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "95",
    "total": "95"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "95",
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
            "amount": "798775"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZmQ3OWM3My00ZTU5LTUxOTAtOGU4OS0zYzExMTQ3YjBmYmYifQ==",
    "nonce": 2400,
    "balances": {
      "current": "10000001284365926",
      "previous": "10000001284366022"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x68d1d53ed81a31b77e659d40376b7a72da4d8821",
    "nonce": 3,
    "balances": {
      "current": "95",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:17.027Z",
  "updated": "2020-05-22T08:16:17.092Z",
  "id": "5ec78a51b0c6090011d5abee"
}
```
* *stageAmount*: `95`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000005f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000005f000000000000000000000000000000000000000000000000000000000000005f85fc20059d1b6dc8eb565274d5fb6f109b99c7e614db4cc24378a6d947144b49cfa9a76f5514b235e314baa9a0e370952dffd63b06ae2b602ca97d62c4bdf9e2202ff38221d040515da2bdc0eef7a0b6410e3e77b7970df0d87484cef0ae0a58000000000000000000000000000000000000000000000000000000000000001bae772416902d5e21111199b365d890de5bdb7bab8ada4a0c9854e2d4d4d4fbf419de06ea70ded3ffbd701072a8b07845d3a35be77ba914b0af89be61ba31814a30bbb373460b42948f36f1bf5ef0c42de57d8a990deafc795d0a1176b34bdc6d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc4ede66000000000000000000000000000000000000000000000000002386f2bc4edec600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c303700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a6d51334f574d334d7930305a5455354c5455784f5441744f4755344f53307a597a45784d545133596a426d596d596966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000068d1d53ed81a31b77e659d40376b7a72da4d8821000000000000000000000000000000000000000000000000000000000000005f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x85fc20059d1b6dc8eb565274d5fb6f109b99c7e614db4cc24378a6d947144b49",
      "signature": {
        "s": "0x202ff38221d040515da2bdc0eef7a0b6410e3e77b7970df0d87484cef0ae0a58",
        "r": "0xcfa9a76f5514b235e314baa9a0e370952dffd63b06ae2b602ca97d62c4bdf9e2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xae772416902d5e21111199b365d890de5bdb7bab8ada4a0c9854e2d4d4d4fbf4",
      "signature": {
        "s": "0x30bbb373460b42948f36f1bf5ef0c42de57d8a990deafc795d0a1176b34bdc6d",
        "r": "0x19de06ea70ded3ffbd701072a8b07845d3a35be77ba914b0af89be61ba31814a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "95",
    "total": "95"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "95",
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
            "amount": "798775"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZmQ3OWM3My00ZTU5LTUxOTAtOGU4OS0zYzExMTQ3YjBmYmYifQ==",
    "nonce": 2400,
    "balances": {
      "current": "10000001284365926",
      "previous": "10000001284366022"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x68d1d53ed81a31b77e659d40376b7a72da4d8821",
    "nonce": 3,
    "balances": {
      "current": "95",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:17.027Z",
  "updated": "2020-05-22T08:16:17.092Z",
  "id": "5ec78a51b0c6090011d5abee"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000005f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `95`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``