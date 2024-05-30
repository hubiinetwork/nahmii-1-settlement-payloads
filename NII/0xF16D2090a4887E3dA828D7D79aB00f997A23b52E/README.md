# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF16D2090a4887E3dA828D7D79aB00f997A23b52E`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001e79270c6950538580000000000000000000000000000000000000000000000000b8f4dd8f0c7be8a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b8f4dd8f0c7be8a0000000000000000000000000000000000000000000000014460f33ac1c81690058f4024cfd10033cc891ff299c94017eabf81da5defd2fca26993ebd6705ceb31d6a689ced430f5b3d2ea4326a92bfb1e4d65f16612ff1ee19eb5f1d5627e096f409829f6b6cd37c9bf1c33b3c93003cf14a9b694c8752e50b9cb0fd93571bc000000000000000000000000000000000000000000000000000000000000001cbbbb2d863f160e2d2714c4d6218a14de55f9ab182b471c53b00df10e23e8a8a474aa45ff582bbd9f17cb86244e482a300d1dc0d5825718a7e9f95b6dfa29ac5d453097a7cc358d7b4a7f579b24b2f5b6953348249fe3fad37387bae76908ec17000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af02000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095acf4df2dcc65cb7f2f0000000000000000000000000000000000000000000095ad0071713a4a87272100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002f594f3f3e9680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61aa6a4f5a35567e00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f5463314e54557a4d5330335a4755794c54566d596d4d7459546b7a595330355a47597a4e546b7a4e6a5130597a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f16d2090a4887e3da828d7d79ab00f997a23b52e000000000000000000000000000000000000000000000001e79270c695053858000000000000000000000000000000000000000000000001dc0322eda43d79ce00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x058f4024cfd10033cc891ff299c94017eabf81da5defd2fca26993ebd6705ceb",
      "signature": {
        "s": "0x6f409829f6b6cd37c9bf1c33b3c93003cf14a9b694c8752e50b9cb0fd93571bc",
        "r": "0x31d6a689ced430f5b3d2ea4326a92bfb1e4d65f16612ff1ee19eb5f1d5627e09",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbbbb2d863f160e2d2714c4d6218a14de55f9ab182b471c53b00df10e23e8a8a4",
      "signature": {
        "s": "0x453097a7cc358d7b4a7f579b24b2f5b6953348249fe3fad37387bae76908ec17",
        "r": "0x74aa45ff582bbd9f17cb86244e482a300d1dc0d5825718a7e9f95b6dfa29ac5d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "832970050234728074",
    "total": "23373949499737642640"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "832970050234728074",
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
            "amount": "27266208144608751609824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "832970050234728"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyOTc1NTUzMS03ZGUyLTVmYmMtYTkzYS05ZGYzNTkzNjQ0YzcifQ==",
    "nonce": 110338,
    "balances": {
      "current": "706823090800476145024815",
      "previous": "706823924603496429987617"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf16d2090a4887e3da828d7d79ab00f997a23b52e",
    "nonce": 46,
    "balances": {
      "current": "35133267641276643416",
      "previous": "34300297591041915342"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:45.481Z",
  "updated": "2022-05-04T08:52:45.554Z",
  "id": "62723edd3592fd001130b4bc"
}
```
* *stageAmount*: `35133267641276643416`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000b8f4dd8f0c7be8a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b8f4dd8f0c7be8a0000000000000000000000000000000000000000000000014460f33ac1c81690058f4024cfd10033cc891ff299c94017eabf81da5defd2fca26993ebd6705ceb31d6a689ced430f5b3d2ea4326a92bfb1e4d65f16612ff1ee19eb5f1d5627e096f409829f6b6cd37c9bf1c33b3c93003cf14a9b694c8752e50b9cb0fd93571bc000000000000000000000000000000000000000000000000000000000000001cbbbb2d863f160e2d2714c4d6218a14de55f9ab182b471c53b00df10e23e8a8a474aa45ff582bbd9f17cb86244e482a300d1dc0d5825718a7e9f95b6dfa29ac5d453097a7cc358d7b4a7f579b24b2f5b6953348249fe3fad37387bae76908ec17000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af02000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095acf4df2dcc65cb7f2f0000000000000000000000000000000000000000000095ad0071713a4a87272100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002f594f3f3e9680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61aa6a4f5a35567e00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f5463314e54557a4d5330335a4755794c54566d596d4d7459546b7a595330355a47597a4e546b7a4e6a5130597a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f16d2090a4887e3da828d7d79ab00f997a23b52e000000000000000000000000000000000000000000000001e79270c695053858000000000000000000000000000000000000000000000001dc0322eda43d79ce00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x058f4024cfd10033cc891ff299c94017eabf81da5defd2fca26993ebd6705ceb",
      "signature": {
        "s": "0x6f409829f6b6cd37c9bf1c33b3c93003cf14a9b694c8752e50b9cb0fd93571bc",
        "r": "0x31d6a689ced430f5b3d2ea4326a92bfb1e4d65f16612ff1ee19eb5f1d5627e09",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbbbb2d863f160e2d2714c4d6218a14de55f9ab182b471c53b00df10e23e8a8a4",
      "signature": {
        "s": "0x453097a7cc358d7b4a7f579b24b2f5b6953348249fe3fad37387bae76908ec17",
        "r": "0x74aa45ff582bbd9f17cb86244e482a300d1dc0d5825718a7e9f95b6dfa29ac5d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "832970050234728074",
    "total": "23373949499737642640"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "832970050234728074",
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
            "amount": "27266208144608751609824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "832970050234728"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyOTc1NTUzMS03ZGUyLTVmYmMtYTkzYS05ZGYzNTkzNjQ0YzcifQ==",
    "nonce": 110338,
    "balances": {
      "current": "706823090800476145024815",
      "previous": "706823924603496429987617"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf16d2090a4887e3da828d7d79ab00f997a23b52e",
    "nonce": 46,
    "balances": {
      "current": "35133267641276643416",
      "previous": "34300297591041915342"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:45.481Z",
  "updated": "2022-05-04T08:52:45.554Z",
  "id": "62723edd3592fd001130b4bc"
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
0x0f200f9b000000000000000000000000000000000000000000000001e79270c6950538580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `35133267641276643416`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`