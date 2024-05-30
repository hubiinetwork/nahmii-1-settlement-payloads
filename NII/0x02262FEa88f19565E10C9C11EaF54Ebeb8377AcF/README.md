# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x02262FEa88f19565E10C9C11EaF54Ebeb8377AcF`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001bed55af804c8da6500000000000000000000000000000000000000000000000000000000578e5cb00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000578e5cb0000000000000000000000000000000000000000000000000e53e09242990844d9f706a7c03bc72e2202a775fc363c00eca0e5a75791c3b8aac31c374a758b97e3d2df7695bbdb49d019e2af3d60dbd0e80f4506a7887bcc91ca365998f0c6ba1090e1b98e689324a755a410fb784670668b9ae1b71640ae0395bdf7d49a41c29000000000000000000000000000000000000000000000000000000000000001b2558734b2a8e2d4762ac34859042f539b3b33a3f367ff6d7e13804791f38f27f5481e10b1a504d6e4c7f8f987d7f6fc5c4a03f8b645eb4281f39557ace925fdf5de014aa600a99c4261d9cdf5e3d4320fdd4186a3979813cbec5b3a5b57639ac000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0a7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004c59e6b213933accc12d000000000000000000000000000000000000000000004c59e6b21393927187f000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000166a130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8db3d941b4a1f2eec0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f5755334e4749334e43316a4e4445304c5456685a6d4974596a6b795a6930784e4749794d5441334d5749324d44596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000002262fea88f19565e10c9c11eaf54ebeb8377acf000000000000000000000000000000000000000000000001bed55af804c8da65000000000000000000000000000000000000000000000001bed55af7ad3a7db500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9f706a7c03bc72e2202a775fc363c00eca0e5a75791c3b8aac31c374a758b97e",
      "signature": {
        "s": "0x090e1b98e689324a755a410fb784670668b9ae1b71640ae0395bdf7d49a41c29",
        "r": "0x3d2df7695bbdb49d019e2af3d60dbd0e80f4506a7887bcc91ca365998f0c6ba1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2558734b2a8e2d4762ac34859042f539b3b33a3f367ff6d7e13804791f38f27f",
      "signature": {
        "s": "0x5de014aa600a99c4261d9cdf5e3d4320fdd4186a3979813cbec5b3a5b57639ac",
        "r": "0x5481e10b1a504d6e4c7f8f987d7f6fc5c4a03f8b645eb4281f39557ace925fdf",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1468947632",
    "total": "16518650534162367565"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1468947632",
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
            "amount": "27612127080182303370988"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1468947"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmOWU3NGI3NC1jNDE0LTVhZmItYjkyZi0xNGIyMTA3MWI2MDYifQ==",
    "nonce": 110759,
    "balances": {
      "current": "360558236291350831874349",
      "previous": "360558236291352302290928"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02262fea88f19565e10c9c11eaf54ebeb8377acf",
    "nonce": 46,
    "balances": {
      "current": "32197741132233890405",
      "previous": "32197741130764942773"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:54:52.740Z",
  "updated": "2022-05-04T08:54:52.810Z",
  "id": "62723f5c3592fd001130b543"
}
```
* *stageAmount*: `32197741132233890405`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000578e5cb00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000578e5cb0000000000000000000000000000000000000000000000000e53e09242990844d9f706a7c03bc72e2202a775fc363c00eca0e5a75791c3b8aac31c374a758b97e3d2df7695bbdb49d019e2af3d60dbd0e80f4506a7887bcc91ca365998f0c6ba1090e1b98e689324a755a410fb784670668b9ae1b71640ae0395bdf7d49a41c29000000000000000000000000000000000000000000000000000000000000001b2558734b2a8e2d4762ac34859042f539b3b33a3f367ff6d7e13804791f38f27f5481e10b1a504d6e4c7f8f987d7f6fc5c4a03f8b645eb4281f39557ace925fdf5de014aa600a99c4261d9cdf5e3d4320fdd4186a3979813cbec5b3a5b57639ac000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0a7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004c59e6b213933accc12d000000000000000000000000000000000000000000004c59e6b21393927187f000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000166a130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8db3d941b4a1f2eec0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f5755334e4749334e43316a4e4445304c5456685a6d4974596a6b795a6930784e4749794d5441334d5749324d44596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000002262fea88f19565e10c9c11eaf54ebeb8377acf000000000000000000000000000000000000000000000001bed55af804c8da65000000000000000000000000000000000000000000000001bed55af7ad3a7db500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9f706a7c03bc72e2202a775fc363c00eca0e5a75791c3b8aac31c374a758b97e",
      "signature": {
        "s": "0x090e1b98e689324a755a410fb784670668b9ae1b71640ae0395bdf7d49a41c29",
        "r": "0x3d2df7695bbdb49d019e2af3d60dbd0e80f4506a7887bcc91ca365998f0c6ba1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2558734b2a8e2d4762ac34859042f539b3b33a3f367ff6d7e13804791f38f27f",
      "signature": {
        "s": "0x5de014aa600a99c4261d9cdf5e3d4320fdd4186a3979813cbec5b3a5b57639ac",
        "r": "0x5481e10b1a504d6e4c7f8f987d7f6fc5c4a03f8b645eb4281f39557ace925fdf",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1468947632",
    "total": "16518650534162367565"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1468947632",
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
            "amount": "27612127080182303370988"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1468947"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmOWU3NGI3NC1jNDE0LTVhZmItYjkyZi0xNGIyMTA3MWI2MDYifQ==",
    "nonce": 110759,
    "balances": {
      "current": "360558236291350831874349",
      "previous": "360558236291352302290928"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02262fea88f19565e10c9c11eaf54ebeb8377acf",
    "nonce": 46,
    "balances": {
      "current": "32197741132233890405",
      "previous": "32197741130764942773"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:54:52.740Z",
  "updated": "2022-05-04T08:54:52.810Z",
  "id": "62723f5c3592fd001130b543"
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
0x0f200f9b000000000000000000000000000000000000000000000001bed55af804c8da650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `32197741132233890405`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`