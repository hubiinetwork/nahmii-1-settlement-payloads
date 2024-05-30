# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x931B96A1A897358E89Ea9E688c4273215B5b2972`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000bbe5000000000000000000000000000000000000000000000000000000000000bbe50000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000bbe5000000000000000000000000000000000000000000000000000000000000bbe5221ee0f14114bc087c65ec9a67560d655c590109e6bf09f614ff6ef1001b9f12f019d37b8bd0eab9f032d9716fde3d4183823a6a65239150534ddca9b8eed21153c5bb55ca86ca62b60ead634fd072a8caf2e355f1232eedeae58c73c583bfc3000000000000000000000000000000000000000000000000000000000000001cb2e49eef676ef6c5144f670354085a3caa1850e1818c130cfade5798427c8f457775ed4c5b05a5f7fba600f71f1a7dc382d56e655b5f3b08bb89be37f57b8c09253b06a8734292d7c789410b9227215f1f962a95319ef9c15529a0693219caeb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000022700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb30d4fb000000000000000000000000000000000000000000000000002386f2cb31911000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000863ce00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d446b33596a686a4e69316a4f574a694c54566b4d6a59745957526a4d79316a4d324e695a6d59344e32566b4e6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000931b96a1a897358e89ea9e688c4273215b5b2972000000000000000000000000000000000000000000000000000000000000bbe5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x221ee0f14114bc087c65ec9a67560d655c590109e6bf09f614ff6ef1001b9f12",
      "signature": {
        "s": "0x53c5bb55ca86ca62b60ead634fd072a8caf2e355f1232eedeae58c73c583bfc3",
        "r": "0xf019d37b8bd0eab9f032d9716fde3d4183823a6a65239150534ddca9b8eed211",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb2e49eef676ef6c5144f670354085a3caa1850e1818c130cfade5798427c8f45",
      "signature": {
        "s": "0x253b06a8734292d7c789410b9227215f1f962a95319ef9c15529a0693219caeb",
        "r": "0x7775ed4c5b05a5f7fba600f71f1a7dc382d56e655b5f3b08bb89be37f57b8c09",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "48101",
    "total": "48101"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48101",
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
            "amount": "549838"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "48"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMDk3YjhjNi1jOWJiLTVkMjYtYWRjMy1jM2NiZmY4N2VkNmMifQ==",
    "nonce": 551,
    "balances": {
      "current": "10000001534055675",
      "previous": "10000001534103824"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x931b96a1a897358e89ea9e688c4273215b5b2972",
    "nonce": 20,
    "balances": {
      "current": "48101",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:51.929Z",
  "updated": "2020-05-22T08:02:52.002Z",
  "id": "5ec7872be5756b00111b8026"
}
```
* *stageAmount*: `48101`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000bbe50000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000bbe5000000000000000000000000000000000000000000000000000000000000bbe5221ee0f14114bc087c65ec9a67560d655c590109e6bf09f614ff6ef1001b9f12f019d37b8bd0eab9f032d9716fde3d4183823a6a65239150534ddca9b8eed21153c5bb55ca86ca62b60ead634fd072a8caf2e355f1232eedeae58c73c583bfc3000000000000000000000000000000000000000000000000000000000000001cb2e49eef676ef6c5144f670354085a3caa1850e1818c130cfade5798427c8f457775ed4c5b05a5f7fba600f71f1a7dc382d56e655b5f3b08bb89be37f57b8c09253b06a8734292d7c789410b9227215f1f962a95319ef9c15529a0693219caeb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000022700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb30d4fb000000000000000000000000000000000000000000000000002386f2cb31911000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000863ce00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d446b33596a686a4e69316a4f574a694c54566b4d6a59745957526a4d79316a4d324e695a6d59344e32566b4e6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000931b96a1a897358e89ea9e688c4273215b5b2972000000000000000000000000000000000000000000000000000000000000bbe5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x221ee0f14114bc087c65ec9a67560d655c590109e6bf09f614ff6ef1001b9f12",
      "signature": {
        "s": "0x53c5bb55ca86ca62b60ead634fd072a8caf2e355f1232eedeae58c73c583bfc3",
        "r": "0xf019d37b8bd0eab9f032d9716fde3d4183823a6a65239150534ddca9b8eed211",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb2e49eef676ef6c5144f670354085a3caa1850e1818c130cfade5798427c8f45",
      "signature": {
        "s": "0x253b06a8734292d7c789410b9227215f1f962a95319ef9c15529a0693219caeb",
        "r": "0x7775ed4c5b05a5f7fba600f71f1a7dc382d56e655b5f3b08bb89be37f57b8c09",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "48101",
    "total": "48101"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48101",
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
            "amount": "549838"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "48"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMDk3YjhjNi1jOWJiLTVkMjYtYWRjMy1jM2NiZmY4N2VkNmMifQ==",
    "nonce": 551,
    "balances": {
      "current": "10000001534055675",
      "previous": "10000001534103824"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x931b96a1a897358e89ea9e688c4273215b5b2972",
    "nonce": 20,
    "balances": {
      "current": "48101",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:51.929Z",
  "updated": "2020-05-22T08:02:52.002Z",
  "id": "5ec7872be5756b00111b8026"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000bbe50000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `48101`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``