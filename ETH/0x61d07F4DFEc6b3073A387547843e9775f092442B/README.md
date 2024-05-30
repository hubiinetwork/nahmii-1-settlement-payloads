# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x61d07F4DFEc6b3073A387547843e9775f092442B`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000030fb19000000000000000000000000000000000000000000000000000000000030fb190000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000030fb19000000000000000000000000000000000000000000000000000000000030fb19f060721fe55093c96f6dcba629e90c53aa4edbbafbcf56a6fcbbdc361c0f13b440576d368628758c7ce76d56684445625caa4a248fb3e0d6251c52272a37b0491cfd31b1e5815dee59a2699c83a87ffc4b4abd8b2425fa95efd278a99470f6cd000000000000000000000000000000000000000000000000000000000000001bba0ceb459831ad36a62ab56ed92002279595ff410baaebfcce11be587f5edfc4428bb28dc1a1108f5fa313a7797cf4f77006d3add8bcaf369dba678200abe7692b0e9c0f7525ce7a9e283f62c0a88b52324e7b84668c842373993a77049da50f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000043200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c895595e000000000000000000000000000000000000000000000000002386f2c8c6610100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000c8a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000090de000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e54517a4f4759334d53316d4d47566b4c54557a4f5445744f4445774e6930345a6d59784d4459334d546868597a416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000061d07f4dfec6b3073a387547843e9775f092442b000000000000000000000000000000000000000000000000000000000030fb19000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf060721fe55093c96f6dcba629e90c53aa4edbbafbcf56a6fcbbdc361c0f13b4",
      "signature": {
        "s": "0x1cfd31b1e5815dee59a2699c83a87ffc4b4abd8b2425fa95efd278a99470f6cd",
        "r": "0x40576d368628758c7ce76d56684445625caa4a248fb3e0d6251c52272a37b049",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xba0ceb459831ad36a62ab56ed92002279595ff410baaebfcce11be587f5edfc4",
      "signature": {
        "s": "0x2b0e9c0f7525ce7a9e283f62c0a88b52324e7b84668c842373993a77049da50f",
        "r": "0x428bb28dc1a1108f5fa313a7797cf4f77006d3add8bcaf369dba678200abe769",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3210009",
    "total": "3210009"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3210009",
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
            "amount": "593376"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3210"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NTQzOGY3MS1mMGVkLTUzOTEtODEwNi04ZmYxMDY3MThhYzAifQ==",
    "nonce": 1074,
    "balances": {
      "current": "10000001490311518",
      "previous": "10000001493524737"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61d07f4dfec6b3073a387547843e9775f092442b",
    "nonce": 20,
    "balances": {
      "current": "3210009",
      "previous": "0"
    }
  },
  "blockNumber": "10114517",
  "created": "2020-05-22T08:06:36.311Z",
  "updated": "2020-05-22T08:06:37.385Z",
  "id": "5ec7880c005df800101bc384"
}
```
* *stageAmount*: `3210009`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000030fb190000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000030fb19000000000000000000000000000000000000000000000000000000000030fb19f060721fe55093c96f6dcba629e90c53aa4edbbafbcf56a6fcbbdc361c0f13b440576d368628758c7ce76d56684445625caa4a248fb3e0d6251c52272a37b0491cfd31b1e5815dee59a2699c83a87ffc4b4abd8b2425fa95efd278a99470f6cd000000000000000000000000000000000000000000000000000000000000001bba0ceb459831ad36a62ab56ed92002279595ff410baaebfcce11be587f5edfc4428bb28dc1a1108f5fa313a7797cf4f77006d3add8bcaf369dba678200abe7692b0e9c0f7525ce7a9e283f62c0a88b52324e7b84668c842373993a77049da50f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000043200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c895595e000000000000000000000000000000000000000000000000002386f2c8c6610100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000c8a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000090de000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e54517a4f4759334d53316d4d47566b4c54557a4f5445744f4445774e6930345a6d59784d4459334d546868597a416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000061d07f4dfec6b3073a387547843e9775f092442b000000000000000000000000000000000000000000000000000000000030fb19000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf060721fe55093c96f6dcba629e90c53aa4edbbafbcf56a6fcbbdc361c0f13b4",
      "signature": {
        "s": "0x1cfd31b1e5815dee59a2699c83a87ffc4b4abd8b2425fa95efd278a99470f6cd",
        "r": "0x40576d368628758c7ce76d56684445625caa4a248fb3e0d6251c52272a37b049",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xba0ceb459831ad36a62ab56ed92002279595ff410baaebfcce11be587f5edfc4",
      "signature": {
        "s": "0x2b0e9c0f7525ce7a9e283f62c0a88b52324e7b84668c842373993a77049da50f",
        "r": "0x428bb28dc1a1108f5fa313a7797cf4f77006d3add8bcaf369dba678200abe769",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3210009",
    "total": "3210009"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3210009",
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
            "amount": "593376"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3210"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NTQzOGY3MS1mMGVkLTUzOTEtODEwNi04ZmYxMDY3MThhYzAifQ==",
    "nonce": 1074,
    "balances": {
      "current": "10000001490311518",
      "previous": "10000001493524737"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61d07f4dfec6b3073a387547843e9775f092442b",
    "nonce": 20,
    "balances": {
      "current": "3210009",
      "previous": "0"
    }
  },
  "blockNumber": "10114517",
  "created": "2020-05-22T08:06:36.311Z",
  "updated": "2020-05-22T08:06:37.385Z",
  "id": "5ec7880c005df800101bc384"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000030fb190000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3210009`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``