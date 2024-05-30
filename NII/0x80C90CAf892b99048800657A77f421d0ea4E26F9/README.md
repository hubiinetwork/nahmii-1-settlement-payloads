# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x80C90CAf892b99048800657A77f421d0ea4E26F9`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000040805cc68990e70000000000000000000000000000000000000000000000000001877d4bd73ade0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000001877d4bd73ade000000000000000000000000000000000000000000000000002ae9930468ddca0994e2a86f6afcd79be4cbbbbb5d73a27add017ba7ceb5e6cf3cab457cf50f411831bf09fee091b651c95e5f64615c08087c601397d13cffc4ad357c778b32cc792206ada854d2198473adcac4e35ecce087e067c75af3fa4d2ab1a7232e99e9000000000000000000000000000000000000000000000000000000000000001b9d498b215c4f95ad04fe3695d62ed3cbff41425e904423174abe0f9997e63d13e42e67a24a5d4995850179d03b43897eb50de173c4e4f19e56331293a4ef177a5f03063e6ac3ca49627ae35664e49ecc3552b7e2bd1a04d00199a52f19cc5959000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ba0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac72000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a852c2aa5be1a26d9f7000000000000000000000000000000000000000000009a852c2c2d9f9ea4f3dd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000006438a6df080000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4dd790be7961c49e50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6d55784d7a4d794d6930315a57526b4c545578595751745957526b4d433033593255784d7a59345a4468685a54556966513d3d000000000000000000000000000000000000000000000000000000000000002d00000000000000000000000080c90caf892b99048800657a77f421d0ea4e26f90000000000000000000000000000000000000000000000000040805cc68990e7000000000000000000000000000000000000000000000000003ef8df7ab2560900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0994e2a86f6afcd79be4cbbbbb5d73a27add017ba7ceb5e6cf3cab457cf50f41",
      "signature": {
        "s": "0x792206ada854d2198473adcac4e35ecce087e067c75af3fa4d2ab1a7232e99e9",
        "r": "0x1831bf09fee091b651c95e5f64615c08087c601397d13cffc4ad357c778b32cc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9d498b215c4f95ad04fe3695d62ed3cbff41425e904423174abe0f9997e63d13",
      "signature": {
        "s": "0x5f03063e6ac3ca49627ae35664e49ecc3552b7e2bd1a04d00199a52f19cc5959",
        "r": "0xe42e67a24a5d4995850179d03b43897eb50de173c4e4f19e56331293a4ef177a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "430447189768926",
    "total": "12078766665293258"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "430447189768926",
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
            "amount": "27243353052639146035685"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "430447189768"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZmUxMzMyMi01ZWRkLTUxYWQtYWRkMC03Y2UxMzY4ZDhhZTUifQ==",
    "nonce": 109682,
    "balances": {
      "current": "729701037862051325073911",
      "previous": "729701038292928962032605"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x80c90caf892b99048800657a77f421d0ea4e26f9",
    "nonce": 45,
    "balances": {
      "current": "18155534465732839",
      "previous": "17725087275963913"
    }
  },
  "blockNumber": "14709946",
  "created": "2022-05-04T08:49:22.284Z",
  "updated": "2022-05-04T08:49:22.355Z",
  "id": "62723e12bbd75600116d0462"
}
```
* *stageAmount*: `18155534465732839`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000001877d4bd73ade0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000001877d4bd73ade000000000000000000000000000000000000000000000000002ae9930468ddca0994e2a86f6afcd79be4cbbbbb5d73a27add017ba7ceb5e6cf3cab457cf50f411831bf09fee091b651c95e5f64615c08087c601397d13cffc4ad357c778b32cc792206ada854d2198473adcac4e35ecce087e067c75af3fa4d2ab1a7232e99e9000000000000000000000000000000000000000000000000000000000000001b9d498b215c4f95ad04fe3695d62ed3cbff41425e904423174abe0f9997e63d13e42e67a24a5d4995850179d03b43897eb50de173c4e4f19e56331293a4ef177a5f03063e6ac3ca49627ae35664e49ecc3552b7e2bd1a04d00199a52f19cc5959000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ba0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac72000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a852c2aa5be1a26d9f7000000000000000000000000000000000000000000009a852c2c2d9f9ea4f3dd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000006438a6df080000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4dd790be7961c49e50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6d55784d7a4d794d6930315a57526b4c545578595751745957526b4d433033593255784d7a59345a4468685a54556966513d3d000000000000000000000000000000000000000000000000000000000000002d00000000000000000000000080c90caf892b99048800657a77f421d0ea4e26f90000000000000000000000000000000000000000000000000040805cc68990e7000000000000000000000000000000000000000000000000003ef8df7ab2560900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0994e2a86f6afcd79be4cbbbbb5d73a27add017ba7ceb5e6cf3cab457cf50f41",
      "signature": {
        "s": "0x792206ada854d2198473adcac4e35ecce087e067c75af3fa4d2ab1a7232e99e9",
        "r": "0x1831bf09fee091b651c95e5f64615c08087c601397d13cffc4ad357c778b32cc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9d498b215c4f95ad04fe3695d62ed3cbff41425e904423174abe0f9997e63d13",
      "signature": {
        "s": "0x5f03063e6ac3ca49627ae35664e49ecc3552b7e2bd1a04d00199a52f19cc5959",
        "r": "0xe42e67a24a5d4995850179d03b43897eb50de173c4e4f19e56331293a4ef177a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "430447189768926",
    "total": "12078766665293258"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "430447189768926",
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
            "amount": "27243353052639146035685"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "430447189768"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZmUxMzMyMi01ZWRkLTUxYWQtYWRkMC03Y2UxMzY4ZDhhZTUifQ==",
    "nonce": 109682,
    "balances": {
      "current": "729701037862051325073911",
      "previous": "729701038292928962032605"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x80c90caf892b99048800657a77f421d0ea4e26f9",
    "nonce": 45,
    "balances": {
      "current": "18155534465732839",
      "previous": "17725087275963913"
    }
  },
  "blockNumber": "14709946",
  "created": "2022-05-04T08:49:22.284Z",
  "updated": "2022-05-04T08:49:22.355Z",
  "id": "62723e12bbd75600116d0462"
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
0x0f200f9b0000000000000000000000000000000000000000000000000040805cc68990e70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18155534465732839`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`