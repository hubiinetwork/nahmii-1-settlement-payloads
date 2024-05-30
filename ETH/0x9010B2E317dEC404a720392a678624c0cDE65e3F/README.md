# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9010B2E317dEC404a720392a678624c0cDE65e3F`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002f16b000000000000000000000000000000000000000000000000000000000002f16b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002f16b000000000000000000000000000000000000000000000000000000000002f16b99d3921e175a0331a30346b904bf5309e021d81ed2013dffc22c554ae0e0fa55c4fae97a0992605b3de15f6b8bba118e68c00b58ec6092da84f1e6bbfed4f8f233e6180486ced0e0a1aeeef9d9f2207051086340e11b82530345523e82dc94ce000000000000000000000000000000000000000000000000000000000000001c035e4befca3126aca4cca748b7a3f2e85f9c452ef888fba0e8615d0257d7709b713e0fc9434b899c211e792376e0e309b7b24de394380e2a2b7f51fdad907b2973ad41d8e4a3af112121564e5cb265e3a368c0a95d5e76b14b34460d1daacf53000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000060c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6559603000000000000000000000000000000000000000000000000002386f2c658882e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009a09900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a5456684f4445795a693078597a59784c54566859574d74596d4978595330784e6d55335a546b3259546c6c5a47556966513d3d000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000009010b2e317dec404a720392a678624c0cde65e3f000000000000000000000000000000000000000000000000000000000002f16b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x99d3921e175a0331a30346b904bf5309e021d81ed2013dffc22c554ae0e0fa55",
      "signature": {
        "s": "0x33e6180486ced0e0a1aeeef9d9f2207051086340e11b82530345523e82dc94ce",
        "r": "0xc4fae97a0992605b3de15f6b8bba118e68c00b58ec6092da84f1e6bbfed4f8f2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x035e4befca3126aca4cca748b7a3f2e85f9c452ef888fba0e8615d0257d7709b",
      "signature": {
        "s": "0x73ad41d8e4a3af112121564e5cb265e3a368c0a95d5e76b14b34460d1daacf53",
        "r": "0x713e0fc9434b899c211e792376e0e309b7b24de394380e2a2b7f51fdad907b29",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "192875",
    "total": "192875"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "192875",
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
            "amount": "630937"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "192"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTVhODEyZi0xYzYxLTVhYWMtYmIxYS0xNmU3ZTk2YTllZGUifQ==",
    "nonce": 1548,
    "balances": {
      "current": "10000001452578307",
      "previous": "10000001452771374"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9010b2e317dec404a720392a678624c0cde65e3f",
    "nonce": 12,
    "balances": {
      "current": "192875",
      "previous": "0"
    }
  },
  "blockNumber": "10114532",
  "created": "2020-05-22T08:10:24.707Z",
  "updated": "2020-05-22T08:10:24.770Z",
  "id": "5ec788f0e5756b00111b815a"
}
```
* *stageAmount*: `192875`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002f16b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002f16b000000000000000000000000000000000000000000000000000000000002f16b99d3921e175a0331a30346b904bf5309e021d81ed2013dffc22c554ae0e0fa55c4fae97a0992605b3de15f6b8bba118e68c00b58ec6092da84f1e6bbfed4f8f233e6180486ced0e0a1aeeef9d9f2207051086340e11b82530345523e82dc94ce000000000000000000000000000000000000000000000000000000000000001c035e4befca3126aca4cca748b7a3f2e85f9c452ef888fba0e8615d0257d7709b713e0fc9434b899c211e792376e0e309b7b24de394380e2a2b7f51fdad907b2973ad41d8e4a3af112121564e5cb265e3a368c0a95d5e76b14b34460d1daacf53000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000060c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6559603000000000000000000000000000000000000000000000000002386f2c658882e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009a09900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a5456684f4445795a693078597a59784c54566859574d74596d4978595330784e6d55335a546b3259546c6c5a47556966513d3d000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000009010b2e317dec404a720392a678624c0cde65e3f000000000000000000000000000000000000000000000000000000000002f16b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x99d3921e175a0331a30346b904bf5309e021d81ed2013dffc22c554ae0e0fa55",
      "signature": {
        "s": "0x33e6180486ced0e0a1aeeef9d9f2207051086340e11b82530345523e82dc94ce",
        "r": "0xc4fae97a0992605b3de15f6b8bba118e68c00b58ec6092da84f1e6bbfed4f8f2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x035e4befca3126aca4cca748b7a3f2e85f9c452ef888fba0e8615d0257d7709b",
      "signature": {
        "s": "0x73ad41d8e4a3af112121564e5cb265e3a368c0a95d5e76b14b34460d1daacf53",
        "r": "0x713e0fc9434b899c211e792376e0e309b7b24de394380e2a2b7f51fdad907b29",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "192875",
    "total": "192875"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "192875",
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
            "amount": "630937"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "192"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTVhODEyZi0xYzYxLTVhYWMtYmIxYS0xNmU3ZTk2YTllZGUifQ==",
    "nonce": 1548,
    "balances": {
      "current": "10000001452578307",
      "previous": "10000001452771374"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9010b2e317dec404a720392a678624c0cde65e3f",
    "nonce": 12,
    "balances": {
      "current": "192875",
      "previous": "0"
    }
  },
  "blockNumber": "10114532",
  "created": "2020-05-22T08:10:24.707Z",
  "updated": "2020-05-22T08:10:24.770Z",
  "id": "5ec788f0e5756b00111b815a"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000002f16b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `192875`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``