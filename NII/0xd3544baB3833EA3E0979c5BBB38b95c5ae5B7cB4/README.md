# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd3544baB3833EA3E0979c5BBB38b95c5ae5B7cB4`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000b2a1b9f93dd8a6b9900000000000000000000000000000000000000000000000000000003cf9c90c20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000003cf9c90c2000000000000000000000000000000000000000000000001b1857fd516a8ab1d95d8c3a72f9ccfb21c2fdc2d8944e632c28deedc1723b98bd813548add3c675caf4bd4dac2efda03aea81df1c4e2278e9bc6f16649b3804f853532108cae49aa6670517df21b510983fb9cae46ee7e419c2f7c3818015ce815cc0f379e932d45000000000000000000000000000000000000000000000000000000000000001b876b0eb292fff0156bb0e97653ad222e33e6a5d3fa98dd11b33b4e7637240305aff21d18d9cf372bc899f9805f857b01090b977ce9587ef007f0a987e90b66cb4a8ef9f11c36536078e2bf36ff2af7ea2b86d1cee4b7f1d702400d69e9cc55d9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b238000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004940493b69e8b9c099b1000000000000000000000000000000000000000000004940493b69ec8a56ec2100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000f9c1ae0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9a633fa92e476e99c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f5456684e575a6b4e4330304f4752684c5456684d6a63744f5451354d79316d5a474d7a5a44497a4e5445775a6a676966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000d3544bab3833ea3e0979c5bbb38b95c5ae5b7cb400000000000000000000000000000000000000000000000b2a1b9f93dd8a6b9900000000000000000000000000000000000000000000000b2a1b9f900deddad700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x95d8c3a72f9ccfb21c2fdc2d8944e632c28deedc1723b98bd813548add3c675c",
      "signature": {
        "s": "0x6670517df21b510983fb9cae46ee7e419c2f7c3818015ce815cc0f379e932d45",
        "r": "0xaf4bd4dac2efda03aea81df1c4e2278e9bc6f16649b3804f853532108cae49aa",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x876b0eb292fff0156bb0e97653ad222e33e6a5d3fa98dd11b33b4e7637240305",
      "signature": {
        "s": "0x4a8ef9f11c36536078e2bf36ff2af7ea2b86d1cee4b7f1d702400d69e9cc55d9",
        "r": "0xaff21d18d9cf372bc899f9805f857b01090b977ce9587ef007f0a987e90b66cb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16368046274",
    "total": "31238514943510227741"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16368046274",
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
            "amount": "27626752069686112217500"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16368046"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0OTVhNWZkNC00OGRhLTVhMjctOTQ5My1mZGMzZDIzNTEwZjgifQ==",
    "nonce": 111160,
    "balances": {
      "current": "345918621798038176307633",
      "previous": "345918621798054560721953"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3544bab3833ea3e0979c5bbb38b95c5ae5b7cb4",
    "nonce": 45,
    "balances": {
      "current": "205948379042195073945",
      "previous": "205948379025827027671"
    }
  },
  "blockNumber": "14709974",
  "created": "2022-05-04T08:56:51.715Z",
  "updated": "2022-05-04T08:56:51.811Z",
  "id": "62723fd37832e20011830ca8"
}
```
* *stageAmount*: `205948379042195073945`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000003cf9c90c20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000003cf9c90c2000000000000000000000000000000000000000000000001b1857fd516a8ab1d95d8c3a72f9ccfb21c2fdc2d8944e632c28deedc1723b98bd813548add3c675caf4bd4dac2efda03aea81df1c4e2278e9bc6f16649b3804f853532108cae49aa6670517df21b510983fb9cae46ee7e419c2f7c3818015ce815cc0f379e932d45000000000000000000000000000000000000000000000000000000000000001b876b0eb292fff0156bb0e97653ad222e33e6a5d3fa98dd11b33b4e7637240305aff21d18d9cf372bc899f9805f857b01090b977ce9587ef007f0a987e90b66cb4a8ef9f11c36536078e2bf36ff2af7ea2b86d1cee4b7f1d702400d69e9cc55d9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b238000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004940493b69e8b9c099b1000000000000000000000000000000000000000000004940493b69ec8a56ec2100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000f9c1ae0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9a633fa92e476e99c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f5456684e575a6b4e4330304f4752684c5456684d6a63744f5451354d79316d5a474d7a5a44497a4e5445775a6a676966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000d3544bab3833ea3e0979c5bbb38b95c5ae5b7cb400000000000000000000000000000000000000000000000b2a1b9f93dd8a6b9900000000000000000000000000000000000000000000000b2a1b9f900deddad700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x95d8c3a72f9ccfb21c2fdc2d8944e632c28deedc1723b98bd813548add3c675c",
      "signature": {
        "s": "0x6670517df21b510983fb9cae46ee7e419c2f7c3818015ce815cc0f379e932d45",
        "r": "0xaf4bd4dac2efda03aea81df1c4e2278e9bc6f16649b3804f853532108cae49aa",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x876b0eb292fff0156bb0e97653ad222e33e6a5d3fa98dd11b33b4e7637240305",
      "signature": {
        "s": "0x4a8ef9f11c36536078e2bf36ff2af7ea2b86d1cee4b7f1d702400d69e9cc55d9",
        "r": "0xaff21d18d9cf372bc899f9805f857b01090b977ce9587ef007f0a987e90b66cb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16368046274",
    "total": "31238514943510227741"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16368046274",
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
            "amount": "27626752069686112217500"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16368046"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0OTVhNWZkNC00OGRhLTVhMjctOTQ5My1mZGMzZDIzNTEwZjgifQ==",
    "nonce": 111160,
    "balances": {
      "current": "345918621798038176307633",
      "previous": "345918621798054560721953"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3544bab3833ea3e0979c5bbb38b95c5ae5b7cb4",
    "nonce": 45,
    "balances": {
      "current": "205948379042195073945",
      "previous": "205948379025827027671"
    }
  },
  "blockNumber": "14709974",
  "created": "2022-05-04T08:56:51.715Z",
  "updated": "2022-05-04T08:56:51.811Z",
  "id": "62723fd37832e20011830ca8"
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
0x0f200f9b00000000000000000000000000000000000000000000000b2a1b9f93dd8a6b990000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `205948379042195073945`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`