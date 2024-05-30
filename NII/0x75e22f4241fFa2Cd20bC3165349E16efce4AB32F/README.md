# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x75e22f4241fFa2Cd20bC3165349E16efce4AB32F`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000009c2c6abf8847b700000000000000000000000000000000000000000000000000000000004b1cd70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004b1cd70000000000000000000000000000000000000000000000000000000006d8f96528fdd30b2647c4aa0e8c21e949ef85375b099181d2dd715599d6a26eb3db36542bf05e73ae5af9be0cea710a57c02bb3e13b6e1a15637f165bcc9705c4c5ecca1dd4b1597462cca52b2fcf0061dd626acac42d9492665f7758f8d9905657a28e000000000000000000000000000000000000000000000000000000000000001be884d1c1a5d704861cfc102b391585896e9460626fcd8a8d4d1658e9a3a0538f7b3ef1bddda1ec48889b2aa8c30b35bb6ae766b071a3a6aae84775c7044adabc610e3939a2407245606da656ffec265730b00dc1a73e4aae3a2ee3cf62c97fce000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b389000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bcfa9538ae48bc273c2000000000000000000000000000000000000000000003bcfa9538ae48c0da3d300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000133a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd161f7ec2b885bdc50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e5751334d7a49774f5330794e4463324c5456695a6a59744f475932595330325a44566d4e6a6c6c4d7a5a6a4e574d6966513d3d000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000075e22f4241ffa2cd20bc3165349e16efce4ab32f000000000000000000000000000000000000000000000000009c2c6abf8847b7000000000000000000000000000000000000000000000000009c2c6abf3d2ae000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x28fdd30b2647c4aa0e8c21e949ef85375b099181d2dd715599d6a26eb3db3654",
      "signature": {
        "s": "0x1dd4b1597462cca52b2fcf0061dd626acac42d9492665f7758f8d9905657a28e",
        "r": "0x2bf05e73ae5af9be0cea710a57c02bb3e13b6e1a15637f165bcc9705c4c5ecca",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe884d1c1a5d704861cfc102b391585896e9460626fcd8a8d4d1658e9a3a0538f",
      "signature": {
        "s": "0x610e3939a2407245606da656ffec265730b00dc1a73e4aae3a2ee3cf62c97fce",
        "r": "0x7b3ef1bddda1ec48889b2aa8c30b35bb6ae766b071a3a6aae84775c7044adabc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4922583",
    "total": "114882917"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4922583",
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
            "amount": "27690156986805933948357"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4922"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNWQ3MzIwOS0yNDc2LTViZjYtOGY2YS02ZDVmNjllMzZjNWMifQ==",
    "nonce": 111497,
    "balances": {
      "current": "282450299761096623551426",
      "previous": "282450299761096628478931"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x75e22f4241ffa2cd20bc3165349e16efce4ab32f",
    "nonce": 30,
    "balances": {
      "current": "43958933358397367",
      "previous": "43958933353474784"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:37.131Z",
  "updated": "2022-05-04T08:58:37.220Z",
  "id": "6272403d3592fd001130b64b"
}
```
* *stageAmount*: `43958933358397367`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000004b1cd70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004b1cd70000000000000000000000000000000000000000000000000000000006d8f96528fdd30b2647c4aa0e8c21e949ef85375b099181d2dd715599d6a26eb3db36542bf05e73ae5af9be0cea710a57c02bb3e13b6e1a15637f165bcc9705c4c5ecca1dd4b1597462cca52b2fcf0061dd626acac42d9492665f7758f8d9905657a28e000000000000000000000000000000000000000000000000000000000000001be884d1c1a5d704861cfc102b391585896e9460626fcd8a8d4d1658e9a3a0538f7b3ef1bddda1ec48889b2aa8c30b35bb6ae766b071a3a6aae84775c7044adabc610e3939a2407245606da656ffec265730b00dc1a73e4aae3a2ee3cf62c97fce000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b389000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bcfa9538ae48bc273c2000000000000000000000000000000000000000000003bcfa9538ae48c0da3d300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000133a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd161f7ec2b885bdc50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e5751334d7a49774f5330794e4463324c5456695a6a59744f475932595330325a44566d4e6a6c6c4d7a5a6a4e574d6966513d3d000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000075e22f4241ffa2cd20bc3165349e16efce4ab32f000000000000000000000000000000000000000000000000009c2c6abf8847b7000000000000000000000000000000000000000000000000009c2c6abf3d2ae000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x28fdd30b2647c4aa0e8c21e949ef85375b099181d2dd715599d6a26eb3db3654",
      "signature": {
        "s": "0x1dd4b1597462cca52b2fcf0061dd626acac42d9492665f7758f8d9905657a28e",
        "r": "0x2bf05e73ae5af9be0cea710a57c02bb3e13b6e1a15637f165bcc9705c4c5ecca",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe884d1c1a5d704861cfc102b391585896e9460626fcd8a8d4d1658e9a3a0538f",
      "signature": {
        "s": "0x610e3939a2407245606da656ffec265730b00dc1a73e4aae3a2ee3cf62c97fce",
        "r": "0x7b3ef1bddda1ec48889b2aa8c30b35bb6ae766b071a3a6aae84775c7044adabc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4922583",
    "total": "114882917"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4922583",
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
            "amount": "27690156986805933948357"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4922"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNWQ3MzIwOS0yNDc2LTViZjYtOGY2YS02ZDVmNjllMzZjNWMifQ==",
    "nonce": 111497,
    "balances": {
      "current": "282450299761096623551426",
      "previous": "282450299761096628478931"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x75e22f4241ffa2cd20bc3165349e16efce4ab32f",
    "nonce": 30,
    "balances": {
      "current": "43958933358397367",
      "previous": "43958933353474784"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:37.131Z",
  "updated": "2022-05-04T08:58:37.220Z",
  "id": "6272403d3592fd001130b64b"
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
0x0f200f9b000000000000000000000000000000000000000000000000009c2c6abf8847b70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `43958933358397367`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`