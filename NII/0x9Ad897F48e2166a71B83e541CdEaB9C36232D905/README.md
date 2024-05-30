# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9Ad897F48e2166a71B83e541CdEaB9C36232D905`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000985dc34310d69acc200000000000000000000000000000000000000000000000039cc853cb3e730130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000039cc853cb3e7301300000000000000000000000000000000000000000000000655e4c025c8f5ddcf90caf476f5b00058a667344b8292e5e2c158a74eee643e98b9a8f31ffc77546b7ae266deed4517597c2b3b926aad67ca46fbc54e3691ae37d6d62fd62ca6613069a92671ec860d25d18f6b4adc6309390f6b6719555777da0422ce525607a196000000000000000000000000000000000000000000000000000000000000001ccef5cc4018dd504877dc94e0bf905fcc26271f239e1f1c830683fcc8780660ed95bdb1ba9116e08b014c6a66aee3325bc9ecf42a3e55dd40863691f785ff86765de37655467af5f1a2301ce13ba0c895fdb4e5746591c8b659125f650cc8a56e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae6b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009625c2a6ca1911ec48f4000000000000000000000000000000000000000000009625fc821b3e8997082d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000ecbe8c3c38f260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5fbc18dc95152d1140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a474a6a4e6d45324d43316b4e446b324c54566d4d446b7459574d35595330324f44426a597a426a5954417a597a496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009ad897f48e2166a71b83e541cdeab9c36232d90500000000000000000000000000000000000000000000000985dc34310d69acc20000000000000000000000000000000000000000000000094c0faef459827caf00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x90caf476f5b00058a667344b8292e5e2c158a74eee643e98b9a8f31ffc77546b",
      "signature": {
        "s": "0x69a92671ec860d25d18f6b4adc6309390f6b6719555777da0422ce525607a196",
        "r": "0x7ae266deed4517597c2b3b926aad67ca46fbc54e3691ae37d6d62fd62ca66130",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcef5cc4018dd504877dc94e0bf905fcc26271f239e1f1c830683fcc8780660ed",
      "signature": {
        "s": "0x5de37655467af5f1a2301ce13ba0c895fdb4e5746591c8b659125f650cc8a56e",
        "r": "0x95bdb1ba9116e08b014c6a66aee3325bc9ecf42a3e55dd40863691f785ff8676",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4164850251173670931",
    "total": "116869747498689093071"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4164850251173670931",
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
            "amount": "27263981933538825130260"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4164850251173670"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwZGJjNmE2MC1kNDk2LTVmMDktYWM5YS02ODBjYzBjYTAzYzIifQ==",
    "nonce": 110187,
    "balances": {
      "current": "709051528081472551143668",
      "previous": "709055697096573975988269"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9ad897f48e2166a71b83e541cdeab9c36232d905",
    "nonce": 46,
    "balances": {
      "current": "175666338550589795522",
      "previous": "171501488299416124591"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:58.693Z",
  "updated": "2022-05-04T08:51:58.815Z",
  "id": "62723eaebbd75600116d050e"
}
```
* *stageAmount*: `175666338550589795522`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000039cc853cb3e730130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000039cc853cb3e7301300000000000000000000000000000000000000000000000655e4c025c8f5ddcf90caf476f5b00058a667344b8292e5e2c158a74eee643e98b9a8f31ffc77546b7ae266deed4517597c2b3b926aad67ca46fbc54e3691ae37d6d62fd62ca6613069a92671ec860d25d18f6b4adc6309390f6b6719555777da0422ce525607a196000000000000000000000000000000000000000000000000000000000000001ccef5cc4018dd504877dc94e0bf905fcc26271f239e1f1c830683fcc8780660ed95bdb1ba9116e08b014c6a66aee3325bc9ecf42a3e55dd40863691f785ff86765de37655467af5f1a2301ce13ba0c895fdb4e5746591c8b659125f650cc8a56e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae6b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009625c2a6ca1911ec48f4000000000000000000000000000000000000000000009625fc821b3e8997082d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000ecbe8c3c38f260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5fbc18dc95152d1140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a474a6a4e6d45324d43316b4e446b324c54566d4d446b7459574d35595330324f44426a597a426a5954417a597a496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009ad897f48e2166a71b83e541cdeab9c36232d90500000000000000000000000000000000000000000000000985dc34310d69acc20000000000000000000000000000000000000000000000094c0faef459827caf00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x90caf476f5b00058a667344b8292e5e2c158a74eee643e98b9a8f31ffc77546b",
      "signature": {
        "s": "0x69a92671ec860d25d18f6b4adc6309390f6b6719555777da0422ce525607a196",
        "r": "0x7ae266deed4517597c2b3b926aad67ca46fbc54e3691ae37d6d62fd62ca66130",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcef5cc4018dd504877dc94e0bf905fcc26271f239e1f1c830683fcc8780660ed",
      "signature": {
        "s": "0x5de37655467af5f1a2301ce13ba0c895fdb4e5746591c8b659125f650cc8a56e",
        "r": "0x95bdb1ba9116e08b014c6a66aee3325bc9ecf42a3e55dd40863691f785ff8676",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4164850251173670931",
    "total": "116869747498689093071"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4164850251173670931",
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
            "amount": "27263981933538825130260"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4164850251173670"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwZGJjNmE2MC1kNDk2LTVmMDktYWM5YS02ODBjYzBjYTAzYzIifQ==",
    "nonce": 110187,
    "balances": {
      "current": "709051528081472551143668",
      "previous": "709055697096573975988269"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9ad897f48e2166a71b83e541cdeab9c36232d905",
    "nonce": 46,
    "balances": {
      "current": "175666338550589795522",
      "previous": "171501488299416124591"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:58.693Z",
  "updated": "2022-05-04T08:51:58.815Z",
  "id": "62723eaebbd75600116d050e"
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
0x0f200f9b00000000000000000000000000000000000000000000000985dc34310d69acc20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `175666338550589795522`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`