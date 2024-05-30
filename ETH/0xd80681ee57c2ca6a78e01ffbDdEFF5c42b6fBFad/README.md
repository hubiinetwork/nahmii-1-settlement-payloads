# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd80681ee57c2ca6a78e01ffbDdEFF5c42b6fBFad`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000140810000000000000000000000000000000000000000000000000000000000014081000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000140810000000000000000000000000000000000000000000000000000000000014081ab4e9b61285a2a95dd005dc0c8690537a2bff48644db98c15e1f982ddc7f626aa93526064b05375df3dd9b18c6d64fdb085fd7050e94c33aa5532e64b4d50d304e9c99978423294ff59eebd01827620f2551a03a5c4cbeabc3fecd09a0c3c17f000000000000000000000000000000000000000000000000000000000000001c59c30fb9f6453d28670fadf890fc9c4f0300b1a623369deaae5a3d83eaa0b5b88a9db24cd11165558b405e3370dde6ae84fad1c9fb9bac0c6e8ffae55298453003e7a1e6982b8bc8e50df098d771cfd684c3571351f2305b1595b9a5a29bb65e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000062100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c618bae2000000000000000000000000000000000000000000000000002386f2c619fbb500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009b02400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6a6b304e544a6a4d79316a5a6d5a6a4c54566b4e6a4d74596d4a6a4e4330354e6d4e6c4e574d7a595463774d7a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d80681ee57c2ca6a78e01ffbddeff5c42b6fbfad0000000000000000000000000000000000000000000000000000000000014081000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xab4e9b61285a2a95dd005dc0c8690537a2bff48644db98c15e1f982ddc7f626a",
      "signature": {
        "s": "0x4e9c99978423294ff59eebd01827620f2551a03a5c4cbeabc3fecd09a0c3c17f",
        "r": "0xa93526064b05375df3dd9b18c6d64fdb085fd7050e94c33aa5532e64b4d50d30",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x59c30fb9f6453d28670fadf890fc9c4f0300b1a623369deaae5a3d83eaa0b5b8",
      "signature": {
        "s": "0x03e7a1e6982b8bc8e50df098d771cfd684c3571351f2305b1595b9a5a29bb65e",
        "r": "0x8a9db24cd11165558b405e3370dde6ae84fad1c9fb9bac0c6e8ffae552984530",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "82049",
    "total": "82049"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "82049",
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
            "amount": "634916"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "82"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzZjk0NTJjMy1jZmZjLTVkNjMtYmJjNC05NmNlNWMzYTcwMzIifQ==",
    "nonce": 1569,
    "balances": {
      "current": "10000001448590050",
      "previous": "10000001448672181"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd80681ee57c2ca6a78e01ffbddeff5c42b6fbfad",
    "nonce": 20,
    "balances": {
      "current": "82049",
      "previous": "0"
    }
  },
  "blockNumber": "10114534",
  "created": "2020-05-22T08:10:36.785Z",
  "updated": "2020-05-22T08:10:36.850Z",
  "id": "5ec788fc005df800101bc439"
}
```
* *stageAmount*: `82049`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000014081000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000140810000000000000000000000000000000000000000000000000000000000014081ab4e9b61285a2a95dd005dc0c8690537a2bff48644db98c15e1f982ddc7f626aa93526064b05375df3dd9b18c6d64fdb085fd7050e94c33aa5532e64b4d50d304e9c99978423294ff59eebd01827620f2551a03a5c4cbeabc3fecd09a0c3c17f000000000000000000000000000000000000000000000000000000000000001c59c30fb9f6453d28670fadf890fc9c4f0300b1a623369deaae5a3d83eaa0b5b88a9db24cd11165558b405e3370dde6ae84fad1c9fb9bac0c6e8ffae55298453003e7a1e6982b8bc8e50df098d771cfd684c3571351f2305b1595b9a5a29bb65e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000062100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c618bae2000000000000000000000000000000000000000000000000002386f2c619fbb500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009b02400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6a6b304e544a6a4d79316a5a6d5a6a4c54566b4e6a4d74596d4a6a4e4330354e6d4e6c4e574d7a595463774d7a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d80681ee57c2ca6a78e01ffbddeff5c42b6fbfad0000000000000000000000000000000000000000000000000000000000014081000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xab4e9b61285a2a95dd005dc0c8690537a2bff48644db98c15e1f982ddc7f626a",
      "signature": {
        "s": "0x4e9c99978423294ff59eebd01827620f2551a03a5c4cbeabc3fecd09a0c3c17f",
        "r": "0xa93526064b05375df3dd9b18c6d64fdb085fd7050e94c33aa5532e64b4d50d30",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x59c30fb9f6453d28670fadf890fc9c4f0300b1a623369deaae5a3d83eaa0b5b8",
      "signature": {
        "s": "0x03e7a1e6982b8bc8e50df098d771cfd684c3571351f2305b1595b9a5a29bb65e",
        "r": "0x8a9db24cd11165558b405e3370dde6ae84fad1c9fb9bac0c6e8ffae552984530",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "82049",
    "total": "82049"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "82049",
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
            "amount": "634916"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "82"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzZjk0NTJjMy1jZmZjLTVkNjMtYmJjNC05NmNlNWMzYTcwMzIifQ==",
    "nonce": 1569,
    "balances": {
      "current": "10000001448590050",
      "previous": "10000001448672181"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd80681ee57c2ca6a78e01ffbddeff5c42b6fbfad",
    "nonce": 20,
    "balances": {
      "current": "82049",
      "previous": "0"
    }
  },
  "blockNumber": "10114534",
  "created": "2020-05-22T08:10:36.785Z",
  "updated": "2020-05-22T08:10:36.850Z",
  "id": "5ec788fc005df800101bc439"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000140810000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `82049`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``