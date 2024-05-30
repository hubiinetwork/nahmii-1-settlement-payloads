# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6e14696C618160ba75F7D7d5342Dbc733Fc0d69E`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000005bdff26a813e50826000000000000000000000000000000000000000000000000ad4360f9a21b48b90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000ad4360f9a21b48b9000000000000000000000000000000000000000000000005bdff26a813e50826d802c330031659a1ad884d38a5ceab1400a0af13c6f790c283938140b944a3a5b29211b1b7dc1892407ff1b7dfe8574cac4517c9a12c255472504854c233a3a051702d2bb8775746051e73a247fe349f3e5619b5f5cf3664a084f3346efec758000000000000000000000000000000000000000000000000000000000000001bccd21014ae2217c24fa2222d25736542076e26693bf86c7de77f79abf31c3a54f5012c2078d8fb248de26147b824a9e7d28a8f1a072ecc9db1337b118b4004c92322c1274c001c20925cab03d97d00afea7a27c73e3abfb71fbea8eca6020eef000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b612000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000031f86977062efe74855b0000000000000000000000000000000000000000000031f916e6c222bb9a959300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000002c5afa1b0ac77f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df9a6817511891529f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e546b785a54426a5979303459324e6a4c54566a4e44557459545a6b597931685a57466b4e7a5a6a4e5745344e32556966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000006e14696c618160ba75f7d7d5342dbc733fc0d69e000000000000000000000000000000000000000000000005bdff26a813e5082600000000000000000000000000000000000000000000000510bbc5ae71c9bf6d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd802c330031659a1ad884d38a5ceab1400a0af13c6f790c283938140b944a3a5",
      "signature": {
        "s": "0x51702d2bb8775746051e73a247fe349f3e5619b5f5cf3664a084f3346efec758",
        "r": "0xb29211b1b7dc1892407ff1b7dfe8574cac4517c9a12c255472504854c233a3a0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xccd21014ae2217c24fa2222d25736542076e26693bf86c7de77f79abf31c3a54",
      "signature": {
        "s": "0x2322c1274c001c20925cab03d97d00afea7a27c73e3abfb71fbea8eca6020eef",
        "r": "0xf5012c2078d8fb248de26147b824a9e7d28a8f1a072ecc9db1337b118b4004c9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "12484929217283967161",
    "total": "105924424264107493414"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12484929217283967161",
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
            "amount": "27736582511301946856095"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12484929217283967"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzNTkxZTBjYy04Y2NjLTVjNDUtYTZkYy1hZWFkNzZjNWE4N2UifQ==",
    "nonce": 112146,
    "balances": {
      "current": "235978349740587702584667",
      "previous": "235990847154734203835795"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6e14696c618160ba75f7d7d5342dbc733fc0d69e",
    "nonce": 9,
    "balances": {
      "current": "105924424264107493414",
      "previous": "93439495046823526253"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:15.577Z",
  "updated": "2022-05-04T09:02:15.641Z",
  "id": "627241177832e20011830df5"
}
```
* *stageAmount*: `105924424264107493414`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000ad4360f9a21b48b90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000ad4360f9a21b48b9000000000000000000000000000000000000000000000005bdff26a813e50826d802c330031659a1ad884d38a5ceab1400a0af13c6f790c283938140b944a3a5b29211b1b7dc1892407ff1b7dfe8574cac4517c9a12c255472504854c233a3a051702d2bb8775746051e73a247fe349f3e5619b5f5cf3664a084f3346efec758000000000000000000000000000000000000000000000000000000000000001bccd21014ae2217c24fa2222d25736542076e26693bf86c7de77f79abf31c3a54f5012c2078d8fb248de26147b824a9e7d28a8f1a072ecc9db1337b118b4004c92322c1274c001c20925cab03d97d00afea7a27c73e3abfb71fbea8eca6020eef000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b612000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000031f86977062efe74855b0000000000000000000000000000000000000000000031f916e6c222bb9a959300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000002c5afa1b0ac77f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df9a6817511891529f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e546b785a54426a5979303459324e6a4c54566a4e44557459545a6b597931685a57466b4e7a5a6a4e5745344e32556966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000006e14696c618160ba75f7d7d5342dbc733fc0d69e000000000000000000000000000000000000000000000005bdff26a813e5082600000000000000000000000000000000000000000000000510bbc5ae71c9bf6d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd802c330031659a1ad884d38a5ceab1400a0af13c6f790c283938140b944a3a5",
      "signature": {
        "s": "0x51702d2bb8775746051e73a247fe349f3e5619b5f5cf3664a084f3346efec758",
        "r": "0xb29211b1b7dc1892407ff1b7dfe8574cac4517c9a12c255472504854c233a3a0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xccd21014ae2217c24fa2222d25736542076e26693bf86c7de77f79abf31c3a54",
      "signature": {
        "s": "0x2322c1274c001c20925cab03d97d00afea7a27c73e3abfb71fbea8eca6020eef",
        "r": "0xf5012c2078d8fb248de26147b824a9e7d28a8f1a072ecc9db1337b118b4004c9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "12484929217283967161",
    "total": "105924424264107493414"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12484929217283967161",
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
            "amount": "27736582511301946856095"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12484929217283967"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzNTkxZTBjYy04Y2NjLTVjNDUtYTZkYy1hZWFkNzZjNWE4N2UifQ==",
    "nonce": 112146,
    "balances": {
      "current": "235978349740587702584667",
      "previous": "235990847154734203835795"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6e14696c618160ba75f7d7d5342dbc733fc0d69e",
    "nonce": 9,
    "balances": {
      "current": "105924424264107493414",
      "previous": "93439495046823526253"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:15.577Z",
  "updated": "2022-05-04T09:02:15.641Z",
  "id": "627241177832e20011830df5"
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
0x0f200f9b000000000000000000000000000000000000000000000005bdff26a813e508260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `105924424264107493414`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`