# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4a1a89E96e1a70786509A5e18E2b7d64F6f75a35`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000240e600000000000000000000000000000000000000000000000000000000000240e6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000240e600000000000000000000000000000000000000000000000000000000000240e69e972c4f1ba726a783c636f0363fc88365a0dbc2b3bc9d87d5bd871f94203370f9bb6fa50e0633d55b0c6c60783effa3b1ab54d13395677edac57eebce57605d48051ac2a9964db1ed25415f80863838a12ad09e7d394d6f27faef0b09f5bcac000000000000000000000000000000000000000000000000000000000000001caaeb951d00be8721eb09ba2ce0f1c46f323eb74c54c96ad9d6987a814fa5d980f2dae2b34e1ad9e5400c7625a554f2ca4980d1ebbcf635d5c49916229217045620f5afd9da9436c2cc08a9bbf0165a66febf15084cc310efa0b89ad217687504000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cded9f8a000000000000000000000000000000000000000000000000002386f2cdefe10300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000009300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b0db00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d3256684d5467784d5331694f544d794c545533597a67744f574d325969316a5a446b7a4e6a67345a5755784e6d516966513d3d00000000000000000000000000000000000000000000000000000000000000120000000000000000000000004a1a89e96e1a70786509a5e18e2b7d64f6f75a3500000000000000000000000000000000000000000000000000000000000240e6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9e972c4f1ba726a783c636f0363fc88365a0dbc2b3bc9d87d5bd871f94203370",
      "signature": {
        "s": "0x48051ac2a9964db1ed25415f80863838a12ad09e7d394d6f27faef0b09f5bcac",
        "r": "0xf9bb6fa50e0633d55b0c6c60783effa3b1ab54d13395677edac57eebce57605d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xaaeb951d00be8721eb09ba2ce0f1c46f323eb74c54c96ad9d6987a814fa5d980",
      "signature": {
        "s": "0x20f5afd9da9436c2cc08a9bbf0165a66febf15084cc310efa0b89ad217687504",
        "r": "0xf2dae2b34e1ad9e5400c7625a554f2ca4980d1ebbcf635d5c499162292170456",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "147686",
    "total": "147686"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "147686",
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
            "amount": "504027"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "147"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmM2VhMTgxMS1iOTMyLTU3YzgtOWM2Yi1jZDkzNjg4ZWUxNmQifQ==",
    "nonce": 224,
    "balances": {
      "current": "10000001579982730",
      "previous": "10000001580130563"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4a1a89e96e1a70786509a5e18e2b7d64f6f75a35",
    "nonce": 18,
    "balances": {
      "current": "147686",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:31.276Z",
  "updated": "2020-05-22T08:00:31.356Z",
  "id": "5ec7869f005df800101bc25c"
}
```
* *stageAmount*: `147686`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000240e6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000240e600000000000000000000000000000000000000000000000000000000000240e69e972c4f1ba726a783c636f0363fc88365a0dbc2b3bc9d87d5bd871f94203370f9bb6fa50e0633d55b0c6c60783effa3b1ab54d13395677edac57eebce57605d48051ac2a9964db1ed25415f80863838a12ad09e7d394d6f27faef0b09f5bcac000000000000000000000000000000000000000000000000000000000000001caaeb951d00be8721eb09ba2ce0f1c46f323eb74c54c96ad9d6987a814fa5d980f2dae2b34e1ad9e5400c7625a554f2ca4980d1ebbcf635d5c49916229217045620f5afd9da9436c2cc08a9bbf0165a66febf15084cc310efa0b89ad217687504000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cded9f8a000000000000000000000000000000000000000000000000002386f2cdefe10300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000009300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b0db00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d3256684d5467784d5331694f544d794c545533597a67744f574d325969316a5a446b7a4e6a67345a5755784e6d516966513d3d00000000000000000000000000000000000000000000000000000000000000120000000000000000000000004a1a89e96e1a70786509a5e18e2b7d64f6f75a3500000000000000000000000000000000000000000000000000000000000240e6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9e972c4f1ba726a783c636f0363fc88365a0dbc2b3bc9d87d5bd871f94203370",
      "signature": {
        "s": "0x48051ac2a9964db1ed25415f80863838a12ad09e7d394d6f27faef0b09f5bcac",
        "r": "0xf9bb6fa50e0633d55b0c6c60783effa3b1ab54d13395677edac57eebce57605d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xaaeb951d00be8721eb09ba2ce0f1c46f323eb74c54c96ad9d6987a814fa5d980",
      "signature": {
        "s": "0x20f5afd9da9436c2cc08a9bbf0165a66febf15084cc310efa0b89ad217687504",
        "r": "0xf2dae2b34e1ad9e5400c7625a554f2ca4980d1ebbcf635d5c499162292170456",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "147686",
    "total": "147686"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "147686",
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
            "amount": "504027"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "147"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmM2VhMTgxMS1iOTMyLTU3YzgtOWM2Yi1jZDkzNjg4ZWUxNmQifQ==",
    "nonce": 224,
    "balances": {
      "current": "10000001579982730",
      "previous": "10000001580130563"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4a1a89e96e1a70786509a5e18e2b7d64f6f75a35",
    "nonce": 18,
    "balances": {
      "current": "147686",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:31.276Z",
  "updated": "2020-05-22T08:00:31.356Z",
  "id": "5ec7869f005df800101bc25c"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000240e60000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `147686`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``