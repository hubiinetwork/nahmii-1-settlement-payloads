# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4241a5e76d299a9dd53711e2c577Ffc2357bED2C`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000c307604e7ca17bd4000000000000000000000000000000000000000000000000049fb8bd2d1cb1310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000049fb8bd2d1cb13100000000000000000000000000000000000000000000000081c0614ab3e96752112935e6853d967455dafd39de79d24bdd4d7b305e280e4bb7c4b08314a15c4659d8250cf2a1273bf199e9aa8943df0c1b901a49ed14857e92699bb4aff119574d04296b3d749b6e4a2487abdb78fe41b1e9074daef027be528c24b84f2c82be000000000000000000000000000000000000000000000000000000000000001c0a0ec942131ac5daa25fd32b16c95ae9b334e494d2c13374c35aaa88e37af8a731f95953bf6df15b6b27b7e530da83ba0a2388aa86f5ce4ba3b42e3172076f4e53e6cc1ecc018ff9bc9cd412ad00a8ba3ae824827f10a90ad5dd8abf6f01f16f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af0f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095aca7e50193373df4bf0000000000000000000000000000000000000000000095acac85e958c5ef69b200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000012f086194c3c20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61aba54b3339eb09d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d6a5a695a6d4e6d5a53316d5a6d4d7a4c54566b596a4174596a5a695969316d5a6d5a684e6d4e68596d466c4d32516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004241a5e76d299a9dd53711e2c577ffc2357bed2c000000000000000000000000000000000000000000000000c307604e7ca17bd4000000000000000000000000000000000000000000000000be67a7914f84caa300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x112935e6853d967455dafd39de79d24bdd4d7b305e280e4bb7c4b08314a15c46",
      "signature": {
        "s": "0x4d04296b3d749b6e4a2487abdb78fe41b1e9074daef027be528c24b84f2c82be",
        "r": "0x59d8250cf2a1273bf199e9aa8943df0c1b901a49ed14857e92699bb4aff11957",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0a0ec942131ac5daa25fd32b16c95ae9b334e494d2c13374c35aaa88e37af8a7",
      "signature": {
        "s": "0x53e6cc1ecc018ff9bc9cd412ad00a8ba3ae824827f10a90ad5dd8abf6f01f16f",
        "r": "0x31f95953bf6df15b6b27b7e530da83ba0a2388aa86f5ce4ba3b42e3172076f4e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "333188020093890865",
    "total": "9349579799895041874"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "333188020093890865",
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
            "amount": "27266213685862013513885"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "333188020093890"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMjZiZmNmZS1mZmMzLTVkYjAtYjZiYi1mZmZhNmNhYmFlM2QifQ==",
    "nonce": 110351,
    "balances": {
      "current": "706817544005960979051711",
      "previous": "706817877527169093036466"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4241a5e76d299a9dd53711e2c577ffc2357bed2c",
    "nonce": 46,
    "balances": {
      "current": "14053307052447595476",
      "previous": "13720119032353704611"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:50.830Z",
  "updated": "2022-05-04T08:52:50.920Z",
  "id": "62723ee23592fd001130b4be"
}
```
* *stageAmount*: `14053307052447595476`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000049fb8bd2d1cb1310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000049fb8bd2d1cb13100000000000000000000000000000000000000000000000081c0614ab3e96752112935e6853d967455dafd39de79d24bdd4d7b305e280e4bb7c4b08314a15c4659d8250cf2a1273bf199e9aa8943df0c1b901a49ed14857e92699bb4aff119574d04296b3d749b6e4a2487abdb78fe41b1e9074daef027be528c24b84f2c82be000000000000000000000000000000000000000000000000000000000000001c0a0ec942131ac5daa25fd32b16c95ae9b334e494d2c13374c35aaa88e37af8a731f95953bf6df15b6b27b7e530da83ba0a2388aa86f5ce4ba3b42e3172076f4e53e6cc1ecc018ff9bc9cd412ad00a8ba3ae824827f10a90ad5dd8abf6f01f16f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af0f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095aca7e50193373df4bf0000000000000000000000000000000000000000000095acac85e958c5ef69b200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000012f086194c3c20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61aba54b3339eb09d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d6a5a695a6d4e6d5a53316d5a6d4d7a4c54566b596a4174596a5a695969316d5a6d5a684e6d4e68596d466c4d32516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004241a5e76d299a9dd53711e2c577ffc2357bed2c000000000000000000000000000000000000000000000000c307604e7ca17bd4000000000000000000000000000000000000000000000000be67a7914f84caa300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x112935e6853d967455dafd39de79d24bdd4d7b305e280e4bb7c4b08314a15c46",
      "signature": {
        "s": "0x4d04296b3d749b6e4a2487abdb78fe41b1e9074daef027be528c24b84f2c82be",
        "r": "0x59d8250cf2a1273bf199e9aa8943df0c1b901a49ed14857e92699bb4aff11957",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0a0ec942131ac5daa25fd32b16c95ae9b334e494d2c13374c35aaa88e37af8a7",
      "signature": {
        "s": "0x53e6cc1ecc018ff9bc9cd412ad00a8ba3ae824827f10a90ad5dd8abf6f01f16f",
        "r": "0x31f95953bf6df15b6b27b7e530da83ba0a2388aa86f5ce4ba3b42e3172076f4e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "333188020093890865",
    "total": "9349579799895041874"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "333188020093890865",
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
            "amount": "27266213685862013513885"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "333188020093890"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMjZiZmNmZS1mZmMzLTVkYjAtYjZiYi1mZmZhNmNhYmFlM2QifQ==",
    "nonce": 110351,
    "balances": {
      "current": "706817544005960979051711",
      "previous": "706817877527169093036466"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4241a5e76d299a9dd53711e2c577ffc2357bed2c",
    "nonce": 46,
    "balances": {
      "current": "14053307052447595476",
      "previous": "13720119032353704611"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:50.830Z",
  "updated": "2022-05-04T08:52:50.920Z",
  "id": "62723ee23592fd001130b4be"
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
0x0f200f9b000000000000000000000000000000000000000000000000c307604e7ca17bd40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14053307052447595476`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`