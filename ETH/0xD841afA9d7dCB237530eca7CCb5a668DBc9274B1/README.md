# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD841afA9d7dCB237530eca7CCb5a668DBc9274B1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000008dcda86337b9886252519823f4d796ae5205523b77edbf0d7fb776c2fd2e682276e53b5e76ed5c9b260e69a8196038131ff557d8e32e2930de6dfadd5bfb62e122769cfe276084aa5c3b00685003ce8b4fa47a6bdfa8d89b0dc32a1551f4e2a65000000000000000000000000000000000000000000000000000000000000001b2b25418d2e320ddd695dff7c59829bbf6efdbad9a28d2c88fc8d1348054f9a55156d0f6108b1de4afee2c8c0aa95fc59189ab74a141d21da3bcb2601704645465dc9a07497342b4ed83c8ccfce5086cc3f7b58eb2a5f3022d938eeab7174104f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005e900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6600ccc000000000000000000000000000000000000000000000000002386f2c6600cd500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099dfa00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d324668596a49774e69316a4d4463354c5455774d6a51744f54686b5a4330354e5441354d6a646c4d4745324e32516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d841afa9d7dcb237530eca7ccb5a668dbc9274b10000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdcda86337b9886252519823f4d796ae5205523b77edbf0d7fb776c2fd2e68227",
      "signature": {
        "s": "0x2769cfe276084aa5c3b00685003ce8b4fa47a6bdfa8d89b0dc32a1551f4e2a65",
        "r": "0x6e53b5e76ed5c9b260e69a8196038131ff557d8e32e2930de6dfadd5bfb62e12",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2b25418d2e320ddd695dff7c59829bbf6efdbad9a28d2c88fc8d1348054f9a55",
      "signature": {
        "s": "0x5dc9a07497342b4ed83c8ccfce5086cc3f7b58eb2a5f3022d938eeab7174104f",
        "r": "0x156d0f6108b1de4afee2c8c0aa95fc59189ab74a141d21da3bcb260170464546",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8",
    "total": "8"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8",
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
            "amount": "630266"
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
    "data": "eyJyZWYiOiI5M2FhYjIwNi1jMDc5LTUwMjQtOThkZC05NTA5MjdlMGE2N2QifQ==",
    "nonce": 1513,
    "balances": {
      "current": "10000001453264076",
      "previous": "10000001453264085"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd841afa9d7dcb237530eca7ccb5a668dbc9274b1",
    "nonce": 20,
    "balances": {
      "current": "8",
      "previous": "0"
    }
  },
  "blockNumber": "10114531",
  "created": "2020-05-22T08:10:07.745Z",
  "updated": "2020-05-22T08:10:07.831Z",
  "id": "5ec788dfb0c6090011d5aac9"
}
```
* *stageAmount*: `8`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000008dcda86337b9886252519823f4d796ae5205523b77edbf0d7fb776c2fd2e682276e53b5e76ed5c9b260e69a8196038131ff557d8e32e2930de6dfadd5bfb62e122769cfe276084aa5c3b00685003ce8b4fa47a6bdfa8d89b0dc32a1551f4e2a65000000000000000000000000000000000000000000000000000000000000001b2b25418d2e320ddd695dff7c59829bbf6efdbad9a28d2c88fc8d1348054f9a55156d0f6108b1de4afee2c8c0aa95fc59189ab74a141d21da3bcb2601704645465dc9a07497342b4ed83c8ccfce5086cc3f7b58eb2a5f3022d938eeab7174104f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005e900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6600ccc000000000000000000000000000000000000000000000000002386f2c6600cd500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099dfa00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d324668596a49774e69316a4d4463354c5455774d6a51744f54686b5a4330354e5441354d6a646c4d4745324e32516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d841afa9d7dcb237530eca7ccb5a668dbc9274b10000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdcda86337b9886252519823f4d796ae5205523b77edbf0d7fb776c2fd2e68227",
      "signature": {
        "s": "0x2769cfe276084aa5c3b00685003ce8b4fa47a6bdfa8d89b0dc32a1551f4e2a65",
        "r": "0x6e53b5e76ed5c9b260e69a8196038131ff557d8e32e2930de6dfadd5bfb62e12",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2b25418d2e320ddd695dff7c59829bbf6efdbad9a28d2c88fc8d1348054f9a55",
      "signature": {
        "s": "0x5dc9a07497342b4ed83c8ccfce5086cc3f7b58eb2a5f3022d938eeab7174104f",
        "r": "0x156d0f6108b1de4afee2c8c0aa95fc59189ab74a141d21da3bcb260170464546",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8",
    "total": "8"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8",
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
            "amount": "630266"
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
    "data": "eyJyZWYiOiI5M2FhYjIwNi1jMDc5LTUwMjQtOThkZC05NTA5MjdlMGE2N2QifQ==",
    "nonce": 1513,
    "balances": {
      "current": "10000001453264076",
      "previous": "10000001453264085"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd841afa9d7dcb237530eca7ccb5a668dbc9274b1",
    "nonce": 20,
    "balances": {
      "current": "8",
      "previous": "0"
    }
  },
  "blockNumber": "10114531",
  "created": "2020-05-22T08:10:07.745Z",
  "updated": "2020-05-22T08:10:07.831Z",
  "id": "5ec788dfb0c6090011d5aac9"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``