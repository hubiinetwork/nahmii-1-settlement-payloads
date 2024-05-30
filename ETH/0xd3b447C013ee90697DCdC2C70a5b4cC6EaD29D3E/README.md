# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd3b447C013ee90697DCdC2C70a5b4cC6EaD29D3E`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000aa47000000000000000000000000000000000000000000000000000000000000aa470000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000aa47000000000000000000000000000000000000000000000000000000000000aa47be50107c2d56472e0bebe613fe4986eda6175b37576145e71a37a6588f175c1660c96bd5f7a7b4242dfb7b5b4d6d3eb23630ffb67e639b9cf3aeebe65022bde82bf0059570928bcd39c93b421a4e4f381fec2522a2b3923befa36caaba8bcf60000000000000000000000000000000000000000000000000000000000000001c853d391d42a483aac09c6ba4613ccd6165efd32a412e26a1e9ff84464f40d7d07caf75bcb6cfb554276a40827fb78b94758dcac37a2ab96749f1898259e22c810120f977443ec090499c9e72be6d0b633decb4ae12be02ed831fca1926e377cd000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004a300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c800963f000000000000000000000000000000000000000000000000002386f2c80140b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000933d800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f57566d4e6d4669597930794e544a6a4c5455324d324574595759344d793033595445305a6a46684e7a51354d7a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d3b447c013ee90697dcdc2c70a5b4cc6ead29d3e000000000000000000000000000000000000000000000000000000000000aa47000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbe50107c2d56472e0bebe613fe4986eda6175b37576145e71a37a6588f175c16",
      "signature": {
        "s": "0x2bf0059570928bcd39c93b421a4e4f381fec2522a2b3923befa36caaba8bcf60",
        "r": "0x60c96bd5f7a7b4242dfb7b5b4d6d3eb23630ffb67e639b9cf3aeebe65022bde8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x853d391d42a483aac09c6ba4613ccd6165efd32a412e26a1e9ff84464f40d7d0",
      "signature": {
        "s": "0x0120f977443ec090499c9e72be6d0b633decb4ae12be02ed831fca1926e377cd",
        "r": "0x7caf75bcb6cfb554276a40827fb78b94758dcac37a2ab96749f1898259e22c81",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "43591",
    "total": "43591"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "43591",
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
            "amount": "603096"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "43"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOWVmNmFiYy0yNTJjLTU2M2EtYWY4My03YTE0ZjFhNzQ5MzMifQ==",
    "nonce": 1187,
    "balances": {
      "current": "10000001480562239",
      "previous": "10000001480605873"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3b447c013ee90697dcdc2c70a5b4cc6ead29d3e",
    "nonce": 20,
    "balances": {
      "current": "43591",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:28.683Z",
  "updated": "2020-05-22T08:07:28.752Z",
  "id": "5ec78840e5756b00111b80f2"
}
```
* *stageAmount*: `43591`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000aa470000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000aa47000000000000000000000000000000000000000000000000000000000000aa47be50107c2d56472e0bebe613fe4986eda6175b37576145e71a37a6588f175c1660c96bd5f7a7b4242dfb7b5b4d6d3eb23630ffb67e639b9cf3aeebe65022bde82bf0059570928bcd39c93b421a4e4f381fec2522a2b3923befa36caaba8bcf60000000000000000000000000000000000000000000000000000000000000001c853d391d42a483aac09c6ba4613ccd6165efd32a412e26a1e9ff84464f40d7d07caf75bcb6cfb554276a40827fb78b94758dcac37a2ab96749f1898259e22c810120f977443ec090499c9e72be6d0b633decb4ae12be02ed831fca1926e377cd000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004a300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c800963f000000000000000000000000000000000000000000000000002386f2c80140b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000933d800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f57566d4e6d4669597930794e544a6a4c5455324d324574595759344d793033595445305a6a46684e7a51354d7a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d3b447c013ee90697dcdc2c70a5b4cc6ead29d3e000000000000000000000000000000000000000000000000000000000000aa47000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbe50107c2d56472e0bebe613fe4986eda6175b37576145e71a37a6588f175c16",
      "signature": {
        "s": "0x2bf0059570928bcd39c93b421a4e4f381fec2522a2b3923befa36caaba8bcf60",
        "r": "0x60c96bd5f7a7b4242dfb7b5b4d6d3eb23630ffb67e639b9cf3aeebe65022bde8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x853d391d42a483aac09c6ba4613ccd6165efd32a412e26a1e9ff84464f40d7d0",
      "signature": {
        "s": "0x0120f977443ec090499c9e72be6d0b633decb4ae12be02ed831fca1926e377cd",
        "r": "0x7caf75bcb6cfb554276a40827fb78b94758dcac37a2ab96749f1898259e22c81",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "43591",
    "total": "43591"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "43591",
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
            "amount": "603096"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "43"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOWVmNmFiYy0yNTJjLTU2M2EtYWY4My03YTE0ZjFhNzQ5MzMifQ==",
    "nonce": 1187,
    "balances": {
      "current": "10000001480562239",
      "previous": "10000001480605873"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3b447c013ee90697dcdc2c70a5b4cc6ead29d3e",
    "nonce": 20,
    "balances": {
      "current": "43591",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:28.683Z",
  "updated": "2020-05-22T08:07:28.752Z",
  "id": "5ec78840e5756b00111b80f2"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000aa470000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `43591`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``