# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd26fb8F0E0010DAC8bf620D15BB76f7753D918A0`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000a6f20eb695ff9a78c27f96d0622889b2937f36dac68279e2ecf85cc1602016f3a1f1ae8b5ba316f97ffa78b24fbc3a42788c6803dcf6c6c5e2e5000a392def6c146be668dd1441a11ac123cc2f46cac691959bec0367b69519b449e85377f212d000000000000000000000000000000000000000000000000000000000000001b55ce8810b7f9f2e556503098b510d919efb4abdb785e73c9402bd417cd09396fa088b708396ce07c2c33115c05e781d5b6696c6fe1f289e16fea61e69d544e291bf6ead8793b7278b2080b347307b406198d82453e6a63593d021d40d1938011000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000044b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c85dea67000000000000000000000000000000000000000000000000002386f2c85dea7200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000091c0e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d54426b4e325534595330795a5445784c5456685a546b74595467774e79316d597a51345a574e695a4445315a6a636966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d26fb8f0e0010dac8bf620d15bb76f7753d918a0000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6f20eb695ff9a78c27f96d0622889b2937f36dac68279e2ecf85cc1602016f3a",
      "signature": {
        "s": "0x46be668dd1441a11ac123cc2f46cac691959bec0367b69519b449e85377f212d",
        "r": "0x1f1ae8b5ba316f97ffa78b24fbc3a42788c6803dcf6c6c5e2e5000a392def6c1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x55ce8810b7f9f2e556503098b510d919efb4abdb785e73c9402bd417cd09396f",
      "signature": {
        "s": "0x1bf6ead8793b7278b2080b347307b406198d82453e6a63593d021d40d1938011",
        "r": "0xa088b708396ce07c2c33115c05e781d5b6696c6fe1f289e16fea61e69d544e29",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10",
    "total": "10"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10",
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
            "amount": "597006"
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
    "data": "eyJyZWYiOiI4MTBkN2U4YS0yZTExLTVhZTktYTgwNy1mYzQ4ZWNiZDE1ZjcifQ==",
    "nonce": 1099,
    "balances": {
      "current": "10000001486678631",
      "previous": "10000001486678642"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd26fb8f0e0010dac8bf620d15bb76f7753d918a0",
    "nonce": 20,
    "balances": {
      "current": "10",
      "previous": "0"
    }
  },
  "blockNumber": "10114519",
  "created": "2020-05-22T08:06:49.665Z",
  "updated": "2020-05-22T08:06:50.014Z",
  "id": "5ec78819005df800101bc38f"
}
```
* *stageAmount*: `10`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000a6f20eb695ff9a78c27f96d0622889b2937f36dac68279e2ecf85cc1602016f3a1f1ae8b5ba316f97ffa78b24fbc3a42788c6803dcf6c6c5e2e5000a392def6c146be668dd1441a11ac123cc2f46cac691959bec0367b69519b449e85377f212d000000000000000000000000000000000000000000000000000000000000001b55ce8810b7f9f2e556503098b510d919efb4abdb785e73c9402bd417cd09396fa088b708396ce07c2c33115c05e781d5b6696c6fe1f289e16fea61e69d544e291bf6ead8793b7278b2080b347307b406198d82453e6a63593d021d40d1938011000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000044b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c85dea67000000000000000000000000000000000000000000000000002386f2c85dea7200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000091c0e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d54426b4e325534595330795a5445784c5456685a546b74595467774e79316d597a51345a574e695a4445315a6a636966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d26fb8f0e0010dac8bf620d15bb76f7753d918a0000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6f20eb695ff9a78c27f96d0622889b2937f36dac68279e2ecf85cc1602016f3a",
      "signature": {
        "s": "0x46be668dd1441a11ac123cc2f46cac691959bec0367b69519b449e85377f212d",
        "r": "0x1f1ae8b5ba316f97ffa78b24fbc3a42788c6803dcf6c6c5e2e5000a392def6c1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x55ce8810b7f9f2e556503098b510d919efb4abdb785e73c9402bd417cd09396f",
      "signature": {
        "s": "0x1bf6ead8793b7278b2080b347307b406198d82453e6a63593d021d40d1938011",
        "r": "0xa088b708396ce07c2c33115c05e781d5b6696c6fe1f289e16fea61e69d544e29",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10",
    "total": "10"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10",
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
            "amount": "597006"
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
    "data": "eyJyZWYiOiI4MTBkN2U4YS0yZTExLTVhZTktYTgwNy1mYzQ4ZWNiZDE1ZjcifQ==",
    "nonce": 1099,
    "balances": {
      "current": "10000001486678631",
      "previous": "10000001486678642"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd26fb8f0e0010dac8bf620d15bb76f7753d918a0",
    "nonce": 20,
    "balances": {
      "current": "10",
      "previous": "0"
    }
  },
  "blockNumber": "10114519",
  "created": "2020-05-22T08:06:49.665Z",
  "updated": "2020-05-22T08:06:50.014Z",
  "id": "5ec78819005df800101bc38f"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``