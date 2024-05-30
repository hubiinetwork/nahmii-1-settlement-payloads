# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0a24740dcB4BA8Fb8469ef4Cfe22eeEdcF069076`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000001427ce3849e9a000000000000000000000000000000000000000000000000000000000000c1be0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000c1be000000000000000000000000000000000000000000000000000000000011a98528c9cf9f4ae964e83a9468cb3194e271db5fd0573f5cb8f60b582c28a413410fb104fb92a160d658cecf019fc8fab157db8407efcbcd9bcd69259a1eb911f6fe7f74c19c887a0353f47481614ff5ca91f0f927bf72395319e55e5046f4a09551000000000000000000000000000000000000000000000000000000000000001b3390b287a34c9128e0ca5542d4cc9027802688ba3cc46fc26fc28bceb9dbe6506a232ce0a2c800c4ef377799129cca8cb1342174193dd4344239116cbabe686858705e1eda051f8bcb6bd78172889218c8b9f29f4b8dafe8f7db4ba7854c081a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b793000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021af08420a6b0472e5650000000000000000000000000000000000000000000021af08420a6b0473a75400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e3c4b396ac56322f440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d325530595441324d53316a4d4455344c5455784e6d5974596d55794e5330774e5468684f4445314d446c694e32556966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000000a24740dcb4ba8fb8469ef4cfe22eeedcf0690760000000000000000000000000000000000000000000000000001427ce3849e9a0000000000000000000000000000000000000000000000000001427ce383dcdc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x28c9cf9f4ae964e83a9468cb3194e271db5fd0573f5cb8f60b582c28a413410f",
      "signature": {
        "s": "0x7f74c19c887a0353f47481614ff5ca91f0f927bf72395319e55e5046f4a09551",
        "r": "0xb104fb92a160d658cecf019fc8fab157db8407efcbcd9bcd69259a1eb911f6fe",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3390b287a34c9128e0ca5542d4cc9027802688ba3cc46fc26fc28bceb9dbe650",
      "signature": {
        "s": "0x58705e1eda051f8bcb6bd78172889218c8b9f29f4b8dafe8f7db4ba7854c081a",
        "r": "0x6a232ce0a2c800c4ef377799129cca8cb1342174193dd4344239116cbabe6868",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "49598",
    "total": "1157509"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "49598",
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
            "amount": "27813417157199484038980"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "49"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzM2U0YTA2MS1jMDU4LTUxNmYtYmUyNS0wNThhODE1MDliN2UifQ==",
    "nonce": 112531,
    "balances": {
      "current": "159066869197152982328677",
      "previous": "159066869197152982378324"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0a24740dcb4ba8fb8469ef4cfe22eeedcf069076",
    "nonce": 29,
    "balances": {
      "current": "354579137207962",
      "previous": "354579137158364"
    }
  },
  "blockNumber": "14709997",
  "created": "2022-05-04T09:04:20.878Z",
  "updated": "2022-05-04T09:04:20.954Z",
  "id": "627241943592fd001130b7ab"
}
```
* *stageAmount*: `354579137207962`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000c1be0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000c1be000000000000000000000000000000000000000000000000000000000011a98528c9cf9f4ae964e83a9468cb3194e271db5fd0573f5cb8f60b582c28a413410fb104fb92a160d658cecf019fc8fab157db8407efcbcd9bcd69259a1eb911f6fe7f74c19c887a0353f47481614ff5ca91f0f927bf72395319e55e5046f4a09551000000000000000000000000000000000000000000000000000000000000001b3390b287a34c9128e0ca5542d4cc9027802688ba3cc46fc26fc28bceb9dbe6506a232ce0a2c800c4ef377799129cca8cb1342174193dd4344239116cbabe686858705e1eda051f8bcb6bd78172889218c8b9f29f4b8dafe8f7db4ba7854c081a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b793000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021af08420a6b0472e5650000000000000000000000000000000000000000000021af08420a6b0473a75400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e3c4b396ac56322f440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d325530595441324d53316a4d4455344c5455784e6d5974596d55794e5330774e5468684f4445314d446c694e32556966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000000a24740dcb4ba8fb8469ef4cfe22eeedcf0690760000000000000000000000000000000000000000000000000001427ce3849e9a0000000000000000000000000000000000000000000000000001427ce383dcdc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x28c9cf9f4ae964e83a9468cb3194e271db5fd0573f5cb8f60b582c28a413410f",
      "signature": {
        "s": "0x7f74c19c887a0353f47481614ff5ca91f0f927bf72395319e55e5046f4a09551",
        "r": "0xb104fb92a160d658cecf019fc8fab157db8407efcbcd9bcd69259a1eb911f6fe",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3390b287a34c9128e0ca5542d4cc9027802688ba3cc46fc26fc28bceb9dbe650",
      "signature": {
        "s": "0x58705e1eda051f8bcb6bd78172889218c8b9f29f4b8dafe8f7db4ba7854c081a",
        "r": "0x6a232ce0a2c800c4ef377799129cca8cb1342174193dd4344239116cbabe6868",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "49598",
    "total": "1157509"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "49598",
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
            "amount": "27813417157199484038980"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "49"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzM2U0YTA2MS1jMDU4LTUxNmYtYmUyNS0wNThhODE1MDliN2UifQ==",
    "nonce": 112531,
    "balances": {
      "current": "159066869197152982328677",
      "previous": "159066869197152982378324"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0a24740dcb4ba8fb8469ef4cfe22eeedcf069076",
    "nonce": 29,
    "balances": {
      "current": "354579137207962",
      "previous": "354579137158364"
    }
  },
  "blockNumber": "14709997",
  "created": "2022-05-04T09:04:20.878Z",
  "updated": "2022-05-04T09:04:20.954Z",
  "id": "627241943592fd001130b7ab"
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
0x0f200f9b0000000000000000000000000000000000000000000000000001427ce3849e9a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `354579137207962`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`