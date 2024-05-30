# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x69De827466eb02D672b79139f0efF3cEe2358C79`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000170e000000000000000000000000000000000000000000000000000000000000170e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000170e000000000000000000000000000000000000000000000000000000000000170e4fcca4820fd543e1179d3d5315c311e48700fb8fe027acc112787a8ca6edc1a49e3b4c154804e2c62e3b3951d854415986d004aeef6738911e94a29d882d754d0166bd79d042b7b2e1efa7796801b6bcb24ec0ec63b4a4f25a8a8e16468788c8000000000000000000000000000000000000000000000000000000000000001b141d926c4fb59f7a8ed1d0d6181ee45db40bdf380e5004086da3995d12a3860738bf227882c43228084db4819b0fec01b41a268f84f39d9e011508262d8f4c7863714f285af5bc02a50faf08305696e69a919da743e5a6ba3852534b83ac2b4e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f6000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008c400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc62db11000000000000000000000000000000000000000000000000002386f2bc62f22400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2afe00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f4751334d4455324e5330794f446b324c54553359574d74596a5a6b4d69316b596a56694e32466d5a54566c4d47556966513d3d000000000000000000000000000000000000000000000000000000000000000900000000000000000000000069de827466eb02d672b79139f0eff3cee2358c79000000000000000000000000000000000000000000000000000000000000170e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4fcca4820fd543e1179d3d5315c311e48700fb8fe027acc112787a8ca6edc1a4",
      "signature": {
        "s": "0x0166bd79d042b7b2e1efa7796801b6bcb24ec0ec63b4a4f25a8a8e16468788c8",
        "r": "0x9e3b4c154804e2c62e3b3951d854415986d004aeef6738911e94a29d882d754d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x141d926c4fb59f7a8ed1d0d6181ee45db40bdf380e5004086da3995d12a38607",
      "signature": {
        "s": "0x63714f285af5bc02a50faf08305696e69a919da743e5a6ba3852534b83ac2b4e",
        "r": "0x38bf227882c43228084db4819b0fec01b41a268f84f39d9e011508262d8f4c78",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5902",
    "total": "5902"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5902",
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
            "amount": "797438"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyOGQ3MDU2NS0yODk2LTU3YWMtYjZkMi1kYjViN2FmZTVlMGUifQ==",
    "nonce": 2244,
    "balances": {
      "current": "10000001285675793",
      "previous": "10000001285681700"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x69de827466eb02d672b79139f0eff3cee2358c79",
    "nonce": 9,
    "balances": {
      "current": "5902",
      "previous": "0"
    }
  },
  "blockNumber": "10114550",
  "created": "2020-05-22T08:15:16.524Z",
  "updated": "2020-05-22T08:15:16.586Z",
  "id": "5ec78a14e5756b00111b824e"
}
```
* *stageAmount*: `5902`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000170e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000170e000000000000000000000000000000000000000000000000000000000000170e4fcca4820fd543e1179d3d5315c311e48700fb8fe027acc112787a8ca6edc1a49e3b4c154804e2c62e3b3951d854415986d004aeef6738911e94a29d882d754d0166bd79d042b7b2e1efa7796801b6bcb24ec0ec63b4a4f25a8a8e16468788c8000000000000000000000000000000000000000000000000000000000000001b141d926c4fb59f7a8ed1d0d6181ee45db40bdf380e5004086da3995d12a3860738bf227882c43228084db4819b0fec01b41a268f84f39d9e011508262d8f4c7863714f285af5bc02a50faf08305696e69a919da743e5a6ba3852534b83ac2b4e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f6000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008c400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc62db11000000000000000000000000000000000000000000000000002386f2bc62f22400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2afe00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f4751334d4455324e5330794f446b324c54553359574d74596a5a6b4d69316b596a56694e32466d5a54566c4d47556966513d3d000000000000000000000000000000000000000000000000000000000000000900000000000000000000000069de827466eb02d672b79139f0eff3cee2358c79000000000000000000000000000000000000000000000000000000000000170e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4fcca4820fd543e1179d3d5315c311e48700fb8fe027acc112787a8ca6edc1a4",
      "signature": {
        "s": "0x0166bd79d042b7b2e1efa7796801b6bcb24ec0ec63b4a4f25a8a8e16468788c8",
        "r": "0x9e3b4c154804e2c62e3b3951d854415986d004aeef6738911e94a29d882d754d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x141d926c4fb59f7a8ed1d0d6181ee45db40bdf380e5004086da3995d12a38607",
      "signature": {
        "s": "0x63714f285af5bc02a50faf08305696e69a919da743e5a6ba3852534b83ac2b4e",
        "r": "0x38bf227882c43228084db4819b0fec01b41a268f84f39d9e011508262d8f4c78",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5902",
    "total": "5902"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5902",
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
            "amount": "797438"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyOGQ3MDU2NS0yODk2LTU3YWMtYjZkMi1kYjViN2FmZTVlMGUifQ==",
    "nonce": 2244,
    "balances": {
      "current": "10000001285675793",
      "previous": "10000001285681700"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x69de827466eb02d672b79139f0eff3cee2358c79",
    "nonce": 9,
    "balances": {
      "current": "5902",
      "previous": "0"
    }
  },
  "blockNumber": "10114550",
  "created": "2020-05-22T08:15:16.524Z",
  "updated": "2020-05-22T08:15:16.586Z",
  "id": "5ec78a14e5756b00111b824e"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000170e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5902`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``