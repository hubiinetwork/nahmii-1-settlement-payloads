# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3a0496ce53aeD6F1E7Bd4077BEB8DDFEF3E57414`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000011e400000000000000000000000000000000000000000000000000000000000011e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000011e400000000000000000000000000000000000000000000000000000000000011e4831ca1c9e4337472fb9c99fcfe86a40ed2c665c9b555b15a1fadd7b564ad9b194fe112e47def63c7103b92166959e704a2c5c38ef9519f4216e1919ca71e4e4648793c9fd2b6432491b4520338838bdfb9a5a159915eed8e247d9ffeca31213f000000000000000000000000000000000000000000000000000000000000001b18148d9078e85c59bffa451713d16309c69ff763a320c3547e7c0ed4058d3ef0ea33ec7359c2118fcfdf3adb6ecd3746cc35c7b4622faa28f4d7eac1166b7db213db1c679a94f7faf78b8ee15ec5dd71dce99ceeba4b47a86f7354d9f20f117b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000048c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c812c160000000000000000000000000000000000000000000000000002386f2c812d34800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092f3500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e3255354e5459335953307a595746684c5455774f545974596a45334e53316d4e7a517a4f544d334d6d51334f57556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000003a0496ce53aed6f1e7bd4077beb8ddfef3e5741400000000000000000000000000000000000000000000000000000000000011e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x831ca1c9e4337472fb9c99fcfe86a40ed2c665c9b555b15a1fadd7b564ad9b19",
      "signature": {
        "s": "0x48793c9fd2b6432491b4520338838bdfb9a5a159915eed8e247d9ffeca31213f",
        "r": "0x4fe112e47def63c7103b92166959e704a2c5c38ef9519f4216e1919ca71e4e46",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x18148d9078e85c59bffa451713d16309c69ff763a320c3547e7c0ed4058d3ef0",
      "signature": {
        "s": "0x13db1c679a94f7faf78b8ee15ec5dd71dce99ceeba4b47a86f7354d9f20f117b",
        "r": "0xea33ec7359c2118fcfdf3adb6ecd3746cc35c7b4622faa28f4d7eac1166b7db2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4580",
    "total": "4580"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4580",
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
            "amount": "601909"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjN2U5NTY3YS0zYWFhLTUwOTYtYjE3NS1mNzQzOTM3MmQ3OWUifQ==",
    "nonce": 1164,
    "balances": {
      "current": "10000001481752928",
      "previous": "10000001481757512"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3a0496ce53aed6f1e7bd4077beb8ddfef3e57414",
    "nonce": 20,
    "balances": {
      "current": "4580",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:14.340Z",
  "updated": "2020-05-22T08:07:14.414Z",
  "id": "5ec78832e5756b00111b80ea"
}
```
* *stageAmount*: `4580`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000011e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000011e400000000000000000000000000000000000000000000000000000000000011e4831ca1c9e4337472fb9c99fcfe86a40ed2c665c9b555b15a1fadd7b564ad9b194fe112e47def63c7103b92166959e704a2c5c38ef9519f4216e1919ca71e4e4648793c9fd2b6432491b4520338838bdfb9a5a159915eed8e247d9ffeca31213f000000000000000000000000000000000000000000000000000000000000001b18148d9078e85c59bffa451713d16309c69ff763a320c3547e7c0ed4058d3ef0ea33ec7359c2118fcfdf3adb6ecd3746cc35c7b4622faa28f4d7eac1166b7db213db1c679a94f7faf78b8ee15ec5dd71dce99ceeba4b47a86f7354d9f20f117b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000048c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c812c160000000000000000000000000000000000000000000000000002386f2c812d34800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092f3500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e3255354e5459335953307a595746684c5455774f545974596a45334e53316d4e7a517a4f544d334d6d51334f57556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000003a0496ce53aed6f1e7bd4077beb8ddfef3e5741400000000000000000000000000000000000000000000000000000000000011e4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x831ca1c9e4337472fb9c99fcfe86a40ed2c665c9b555b15a1fadd7b564ad9b19",
      "signature": {
        "s": "0x48793c9fd2b6432491b4520338838bdfb9a5a159915eed8e247d9ffeca31213f",
        "r": "0x4fe112e47def63c7103b92166959e704a2c5c38ef9519f4216e1919ca71e4e46",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x18148d9078e85c59bffa451713d16309c69ff763a320c3547e7c0ed4058d3ef0",
      "signature": {
        "s": "0x13db1c679a94f7faf78b8ee15ec5dd71dce99ceeba4b47a86f7354d9f20f117b",
        "r": "0xea33ec7359c2118fcfdf3adb6ecd3746cc35c7b4622faa28f4d7eac1166b7db2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4580",
    "total": "4580"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4580",
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
            "amount": "601909"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjN2U5NTY3YS0zYWFhLTUwOTYtYjE3NS1mNzQzOTM3MmQ3OWUifQ==",
    "nonce": 1164,
    "balances": {
      "current": "10000001481752928",
      "previous": "10000001481757512"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3a0496ce53aed6f1e7bd4077beb8ddfef3e57414",
    "nonce": 20,
    "balances": {
      "current": "4580",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:14.340Z",
  "updated": "2020-05-22T08:07:14.414Z",
  "id": "5ec78832e5756b00111b80ea"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000011e40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4580`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``