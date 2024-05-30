# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x66277d6E9b84Bbc150E58C55095897E79d56dfb8`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000079e49c35531c1e8170000000000000000000000000000000000000000000000002e3d3763c31f51dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000002e3d3763c31f51dd0000000000000000000000000000000000000000000000051183cceb0729b44190bf7c1935e09e0aefdeb352c7736540b134967b1c83b3e6884eff739f20e11eb2c14cbfbda81d7d41927c1611aeb3b6be85925d2266f208a8347ca77dd985e752315833b3ea1c4287091326cbc9d6de8880a5577fa00e3793223a96422ef540000000000000000000000000000000000000000000000000000000000000001cfc67e6c788476707026f668b1caf6971aa05910bd1e02fa9912b1f8c2831c669ee2bd4dc770c5669cc314c7dbc4bb9ded880fd09de207c6acb4c3d854bf10e474fa04e95441b68e4986fab9266970be10d72ff805014b87832a7e84bc1775f87000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae71000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009624a7332f6eb6e57d3f000000000000000000000000000000000000000000009624d57c3d2649d474d200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000bd653cfcfa5b60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5fc0a0b82e7065b1e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e5451304f5459314d53307a595451794c5455355a5445744f44566d4d6931684e6a4d344d6a67355a6a55785a6a456966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000066277d6e9b84bbc150e58c55095897e79d56dfb80000000000000000000000000000000000000000000000079e49c35531c1e817000000000000000000000000000000000000000000000007700c8bf16ea2963a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x90bf7c1935e09e0aefdeb352c7736540b134967b1c83b3e6884eff739f20e11e",
      "signature": {
        "s": "0x52315833b3ea1c4287091326cbc9d6de8880a5577fa00e3793223a96422ef540",
        "r": "0xb2c14cbfbda81d7d41927c1611aeb3b6be85925d2266f208a8347ca77dd985e7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfc67e6c788476707026f668b1caf6971aa05910bd1e02fa9912b1f8c2831c669",
      "signature": {
        "s": "0x4fa04e95441b68e4986fab9266970be10d72ff805014b87832a7e84bc1775f87",
        "r": "0xee2bd4dc770c5669cc314c7dbc4bb9ded880fd09de207c6acb4c3d854bf10e47",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3331880200938934749",
    "total": "93495797998951183425"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3331880200938934749",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27264002337973182290718"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3331880200938934"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNTQ0OTY1MS0zYTQyLTU5ZTEtODVmMi1hNjM4Mjg5ZjUxZjEifQ==",
    "nonce": 110193,
    "balances": {
      "current": "709031103242681033522495",
      "previous": "709034438454762173396178"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x66277d6e9b84bbc150e58c55095897e79d56dfb8",
    "nonce": 46,
    "balances": {
      "current": "140533070817933781015",
      "previous": "137201190616994846266"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:52:00.691Z",
  "updated": "2022-05-04T08:52:00.791Z",
  "id": "62723eb0bbd75600116d0511"
}
```
* *stageAmount*: `140533070817933781015`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000002e3d3763c31f51dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000002e3d3763c31f51dd0000000000000000000000000000000000000000000000051183cceb0729b44190bf7c1935e09e0aefdeb352c7736540b134967b1c83b3e6884eff739f20e11eb2c14cbfbda81d7d41927c1611aeb3b6be85925d2266f208a8347ca77dd985e752315833b3ea1c4287091326cbc9d6de8880a5577fa00e3793223a96422ef540000000000000000000000000000000000000000000000000000000000000001cfc67e6c788476707026f668b1caf6971aa05910bd1e02fa9912b1f8c2831c669ee2bd4dc770c5669cc314c7dbc4bb9ded880fd09de207c6acb4c3d854bf10e474fa04e95441b68e4986fab9266970be10d72ff805014b87832a7e84bc1775f87000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae71000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009624a7332f6eb6e57d3f000000000000000000000000000000000000000000009624d57c3d2649d474d200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000bd653cfcfa5b60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5fc0a0b82e7065b1e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e5451304f5459314d53307a595451794c5455355a5445744f44566d4d6931684e6a4d344d6a67355a6a55785a6a456966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000066277d6e9b84bbc150e58c55095897e79d56dfb80000000000000000000000000000000000000000000000079e49c35531c1e817000000000000000000000000000000000000000000000007700c8bf16ea2963a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x90bf7c1935e09e0aefdeb352c7736540b134967b1c83b3e6884eff739f20e11e",
      "signature": {
        "s": "0x52315833b3ea1c4287091326cbc9d6de8880a5577fa00e3793223a96422ef540",
        "r": "0xb2c14cbfbda81d7d41927c1611aeb3b6be85925d2266f208a8347ca77dd985e7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfc67e6c788476707026f668b1caf6971aa05910bd1e02fa9912b1f8c2831c669",
      "signature": {
        "s": "0x4fa04e95441b68e4986fab9266970be10d72ff805014b87832a7e84bc1775f87",
        "r": "0xee2bd4dc770c5669cc314c7dbc4bb9ded880fd09de207c6acb4c3d854bf10e47",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3331880200938934749",
    "total": "93495797998951183425"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3331880200938934749",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27264002337973182290718"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3331880200938934"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNTQ0OTY1MS0zYTQyLTU5ZTEtODVmMi1hNjM4Mjg5ZjUxZjEifQ==",
    "nonce": 110193,
    "balances": {
      "current": "709031103242681033522495",
      "previous": "709034438454762173396178"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x66277d6e9b84bbc150e58c55095897e79d56dfb8",
    "nonce": 46,
    "balances": {
      "current": "140533070817933781015",
      "previous": "137201190616994846266"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:52:00.691Z",
  "updated": "2022-05-04T08:52:00.791Z",
  "id": "62723eb0bbd75600116d0511"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000079e49c35531c1e8170000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `140533070817933781015`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`