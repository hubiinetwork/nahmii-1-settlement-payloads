# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x80652F57b38020dfe1718E05FCB9F112058978Ea`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000015fe4bc8b104f6f140000000000000000000000000000000000000000000000000857cea924a2083bc30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000857cea924a2083bc30000000000000000000000000000000000000000000000ea1cd41dd5b763749bac2894b82e8d0b164893d82d6ae33187f66f44d96d9554d57882e9991c4d75e3be8eda0f40feb4821b1de337d16d532db468bf6c0236d92ef7ac855c387c4f1206217d6f452aa004f288a7f2ab804d4589cca4be0b02fb45cd2752cf28fa848a000000000000000000000000000000000000000000000000000000000000001c863ded0f6c80c298ea0efd37b94b784a0e4c66590750b3ff76db8aad03e282737f4861a606a12a6790abfe746ff378d0c980845f26a4dae2923d4249884220f44c7b8faee5d8a33c1f366d5fc6d9542c19efd6f37320da982b511e31f1327e96000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b29d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000474b1a059183774a087b00000000000000000000000000000000000000000000475373f6feebf9bd486500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000222c443e06b04270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da2660c9afe487e8ca0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e54646c5a6a56685a43316c4e57557a4c54566d4d325974596d4d784d4330324e5759795a6d51314e6d55335932456966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000080652f57b38020dfe1718e05fcb9f112058978ea00000000000000000000000000000000000000000000015fe4bc8b104f6f14000000000000000000000000000000000000000000000001578cede1ebad66d83d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xac2894b82e8d0b164893d82d6ae33187f66f44d96d9554d57882e9991c4d75e3",
      "signature": {
        "s": "0x06217d6f452aa004f288a7f2ab804d4589cca4be0b02fb45cd2752cf28fa848a",
        "r": "0xbe8eda0f40feb4821b1de337d16d532db468bf6c0236d92ef7ac855c387c4f12",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x863ded0f6c80c298ea0efd37b94b784a0e4c66590750b3ff76db8aad03e28273",
      "signature": {
        "s": "0x4c7b8faee5d8a33c1f366d5fc6d9542c19efd6f37320da982b511e31f1327e96",
        "r": "0x7f4861a606a12a6790abfe746ff378d0c980845f26a4dae2923d4249884220f4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "153901133090980903875",
    "total": "4318615431379901707419"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "153901133090980903875",
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
            "amount": "27635988054345404377290"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "153901133090980903"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjNTdlZjVhZC1lNWUzLTVmM2YtYmMxMC02NWYyZmQ1NmU3Y2EifQ==",
    "nonce": 111261,
    "balances": {
      "current": "336673401154086724307067",
      "previous": "336827456188310796191845"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x80652f57b38020dfe1718e05fcb9f112058978ea",
    "nonce": 46,
    "balances": {
      "current": "6491289371510490207232",
      "previous": "6337388238419509303357"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:23.207Z",
  "updated": "2022-05-04T08:57:23.311Z",
  "id": "62723ff37832e20011830cca"
}
```
* *stageAmount*: `6491289371510490207232`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000857cea924a2083bc30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000857cea924a2083bc30000000000000000000000000000000000000000000000ea1cd41dd5b763749bac2894b82e8d0b164893d82d6ae33187f66f44d96d9554d57882e9991c4d75e3be8eda0f40feb4821b1de337d16d532db468bf6c0236d92ef7ac855c387c4f1206217d6f452aa004f288a7f2ab804d4589cca4be0b02fb45cd2752cf28fa848a000000000000000000000000000000000000000000000000000000000000001c863ded0f6c80c298ea0efd37b94b784a0e4c66590750b3ff76db8aad03e282737f4861a606a12a6790abfe746ff378d0c980845f26a4dae2923d4249884220f44c7b8faee5d8a33c1f366d5fc6d9542c19efd6f37320da982b511e31f1327e96000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b29d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000474b1a059183774a087b00000000000000000000000000000000000000000000475373f6feebf9bd486500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000222c443e06b04270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da2660c9afe487e8ca0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e54646c5a6a56685a43316c4e57557a4c54566d4d325974596d4d784d4330324e5759795a6d51314e6d55335932456966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000080652f57b38020dfe1718e05fcb9f112058978ea00000000000000000000000000000000000000000000015fe4bc8b104f6f14000000000000000000000000000000000000000000000001578cede1ebad66d83d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xac2894b82e8d0b164893d82d6ae33187f66f44d96d9554d57882e9991c4d75e3",
      "signature": {
        "s": "0x06217d6f452aa004f288a7f2ab804d4589cca4be0b02fb45cd2752cf28fa848a",
        "r": "0xbe8eda0f40feb4821b1de337d16d532db468bf6c0236d92ef7ac855c387c4f12",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x863ded0f6c80c298ea0efd37b94b784a0e4c66590750b3ff76db8aad03e28273",
      "signature": {
        "s": "0x4c7b8faee5d8a33c1f366d5fc6d9542c19efd6f37320da982b511e31f1327e96",
        "r": "0x7f4861a606a12a6790abfe746ff378d0c980845f26a4dae2923d4249884220f4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "153901133090980903875",
    "total": "4318615431379901707419"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "153901133090980903875",
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
            "amount": "27635988054345404377290"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "153901133090980903"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjNTdlZjVhZC1lNWUzLTVmM2YtYmMxMC02NWYyZmQ1NmU3Y2EifQ==",
    "nonce": 111261,
    "balances": {
      "current": "336673401154086724307067",
      "previous": "336827456188310796191845"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x80652f57b38020dfe1718e05fcb9f112058978ea",
    "nonce": 46,
    "balances": {
      "current": "6491289371510490207232",
      "previous": "6337388238419509303357"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:23.207Z",
  "updated": "2022-05-04T08:57:23.311Z",
  "id": "62723ff37832e20011830cca"
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
0x0f200f9b00000000000000000000000000000000000000000000015fe4bc8b104f6f14000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6491289371510490207232`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`