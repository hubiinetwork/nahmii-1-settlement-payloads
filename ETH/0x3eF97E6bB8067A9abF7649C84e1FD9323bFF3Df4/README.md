# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3eF97E6bB8067A9abF7649C84e1FD9323bFF3Df4`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000908800000000000000000000000000000000000000000000000000000000000090880000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000908800000000000000000000000000000000000000000000000000000000000090887999db1b6fb457413ceda2f47391b8a301bb7053bcab7cdc85bc25d5e826a850f05c886f4dcf1b6169670f6ac6e54d29975f252aaa1f8240defa7b57e6113c3b1ed3e3484ccb3d27f0e7c58a80c1fd26941647c2884526b27add5ffe00114766000000000000000000000000000000000000000000000000000000000000001cf448eb1f95bce05d1ec42aa22ee846cbfcba7e86abdeae087a5f761a090bc0e3747449590bf675a7e0a7243d3aeae652df442b82e4655f35c8bf24f1cbc3eaa5354db1facf6b7cdda6c230b52ddd1d6c13bb1b52ecd9b6cec7e24ef9fa31c2b8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e2000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005d900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c67179ab000000000000000000000000000000000000000000000000002386f2c6720a5800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009998400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e5749314f5451345a4331694e47566c4c54566d5954597459544a694e6930304e5449334d4441304e54526d5a44596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000003ef97e6bb8067a9abf7649c84e1fd9323bff3df40000000000000000000000000000000000000000000000000000000000009088000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7999db1b6fb457413ceda2f47391b8a301bb7053bcab7cdc85bc25d5e826a850",
      "signature": {
        "s": "0x1ed3e3484ccb3d27f0e7c58a80c1fd26941647c2884526b27add5ffe00114766",
        "r": "0xf05c886f4dcf1b6169670f6ac6e54d29975f252aaa1f8240defa7b57e6113c3b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf448eb1f95bce05d1ec42aa22ee846cbfcba7e86abdeae087a5f761a090bc0e3",
      "signature": {
        "s": "0x354db1facf6b7cdda6c230b52ddd1d6c13bb1b52ecd9b6cec7e24ef9fa31c2b8",
        "r": "0x747449590bf675a7e0a7243d3aeae652df442b82e4655f35c8bf24f1cbc3eaa5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "37000",
    "total": "37000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "37000",
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
            "amount": "629124"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "37"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NWI1OTQ4ZC1iNGVlLTVmYTYtYTJiNi00NTI3MDA0NTRmZDYifQ==",
    "nonce": 1497,
    "balances": {
      "current": "10000001454406059",
      "previous": "10000001454443096"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ef97e6bb8067a9abf7649c84e1fd9323bff3df4",
    "nonce": 20,
    "balances": {
      "current": "37000",
      "previous": "0"
    }
  },
  "blockNumber": "10114530",
  "created": "2020-05-22T08:09:58.498Z",
  "updated": "2020-05-22T08:09:58.569Z",
  "id": "5ec788d6b0c6090011d5aac3"
}
```
* *stageAmount*: `37000`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000090880000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000908800000000000000000000000000000000000000000000000000000000000090887999db1b6fb457413ceda2f47391b8a301bb7053bcab7cdc85bc25d5e826a850f05c886f4dcf1b6169670f6ac6e54d29975f252aaa1f8240defa7b57e6113c3b1ed3e3484ccb3d27f0e7c58a80c1fd26941647c2884526b27add5ffe00114766000000000000000000000000000000000000000000000000000000000000001cf448eb1f95bce05d1ec42aa22ee846cbfcba7e86abdeae087a5f761a090bc0e3747449590bf675a7e0a7243d3aeae652df442b82e4655f35c8bf24f1cbc3eaa5354db1facf6b7cdda6c230b52ddd1d6c13bb1b52ecd9b6cec7e24ef9fa31c2b8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e2000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005d900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c67179ab000000000000000000000000000000000000000000000000002386f2c6720a5800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009998400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e5749314f5451345a4331694e47566c4c54566d5954597459544a694e6930304e5449334d4441304e54526d5a44596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000003ef97e6bb8067a9abf7649c84e1fd9323bff3df40000000000000000000000000000000000000000000000000000000000009088000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7999db1b6fb457413ceda2f47391b8a301bb7053bcab7cdc85bc25d5e826a850",
      "signature": {
        "s": "0x1ed3e3484ccb3d27f0e7c58a80c1fd26941647c2884526b27add5ffe00114766",
        "r": "0xf05c886f4dcf1b6169670f6ac6e54d29975f252aaa1f8240defa7b57e6113c3b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf448eb1f95bce05d1ec42aa22ee846cbfcba7e86abdeae087a5f761a090bc0e3",
      "signature": {
        "s": "0x354db1facf6b7cdda6c230b52ddd1d6c13bb1b52ecd9b6cec7e24ef9fa31c2b8",
        "r": "0x747449590bf675a7e0a7243d3aeae652df442b82e4655f35c8bf24f1cbc3eaa5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "37000",
    "total": "37000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "37000",
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
            "amount": "629124"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "37"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NWI1OTQ4ZC1iNGVlLTVmYTYtYTJiNi00NTI3MDA0NTRmZDYifQ==",
    "nonce": 1497,
    "balances": {
      "current": "10000001454406059",
      "previous": "10000001454443096"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ef97e6bb8067a9abf7649c84e1fd9323bff3df4",
    "nonce": 20,
    "balances": {
      "current": "37000",
      "previous": "0"
    }
  },
  "blockNumber": "10114530",
  "created": "2020-05-22T08:09:58.498Z",
  "updated": "2020-05-22T08:09:58.569Z",
  "id": "5ec788d6b0c6090011d5aac3"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000090880000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `37000`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``