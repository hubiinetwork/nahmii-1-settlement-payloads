# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD062Abd54F36Dc1eABF862bc494156C009142C5B`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000165400000000000000000000000000000000000000000000000000000000000016540000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000165400000000000000000000000000000000000000000000000000000000000016549d2dfe50be4df7b838da0638a3a77ad78c54bd268888143de2b83da6a432b469d6e102cca4b6030f9519e554d1b79bcf9c8ba9929c49ea4fc10bd8dec5305abb5546a402015134fb2f0a9d606dc37ad473650dfab5e07a52783676a5f4c313ab000000000000000000000000000000000000000000000000000000000000001b47e0b80a57ccd94712d97bbcce2b9d4b5e746f627dc88de625ece6113e057003159681329825ec90c7b9f5e492973e9eb7229a38e5f22cf2327bfa8c9d525667181fe05f0ec9a33a08ddb7ea52f4fa786354db5f7515c4d6052aeff06bdb498e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005f200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c65f1fe4000000000000000000000000000000000000000000000000002386f2c65f363d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099e3300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a517a4d444e684e79316a5a6a63774c54566d5a4467744f44457a4d79307a5932566a5954466a5a6d59344e44636966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d062abd54f36dc1eabf862bc494156c009142c5b0000000000000000000000000000000000000000000000000000000000001654000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9d2dfe50be4df7b838da0638a3a77ad78c54bd268888143de2b83da6a432b469",
      "signature": {
        "s": "0x5546a402015134fb2f0a9d606dc37ad473650dfab5e07a52783676a5f4c313ab",
        "r": "0xd6e102cca4b6030f9519e554d1b79bcf9c8ba9929c49ea4fc10bd8dec5305abb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x47e0b80a57ccd94712d97bbcce2b9d4b5e746f627dc88de625ece6113e057003",
      "signature": {
        "s": "0x181fe05f0ec9a33a08ddb7ea52f4fa786354db5f7515c4d6052aeff06bdb498e",
        "r": "0x159681329825ec90c7b9f5e492973e9eb7229a38e5f22cf2327bfa8c9d525667",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5716",
    "total": "5716"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5716",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "630323"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NjQzMDNhNy1jZjcwLTVmZDgtODEzMy0zY2VjYTFjZmY4NDcifQ==",
    "nonce": 1522,
    "balances": {
      "current": "10000001453203428",
      "previous": "10000001453209149"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd062abd54f36dc1eabf862bc494156c009142c5b",
    "nonce": 20,
    "balances": {
      "current": "5716",
      "previous": "0"
    }
  },
  "blockNumber": "10114532",
  "created": "2020-05-22T08:10:10.665Z",
  "updated": "2020-05-22T08:10:10.736Z",
  "id": "5ec788e2005df800101bc429"
}
```
* *stageAmount*: `5716`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000016540000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000165400000000000000000000000000000000000000000000000000000000000016549d2dfe50be4df7b838da0638a3a77ad78c54bd268888143de2b83da6a432b469d6e102cca4b6030f9519e554d1b79bcf9c8ba9929c49ea4fc10bd8dec5305abb5546a402015134fb2f0a9d606dc37ad473650dfab5e07a52783676a5f4c313ab000000000000000000000000000000000000000000000000000000000000001b47e0b80a57ccd94712d97bbcce2b9d4b5e746f627dc88de625ece6113e057003159681329825ec90c7b9f5e492973e9eb7229a38e5f22cf2327bfa8c9d525667181fe05f0ec9a33a08ddb7ea52f4fa786354db5f7515c4d6052aeff06bdb498e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005f200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c65f1fe4000000000000000000000000000000000000000000000000002386f2c65f363d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000099e3300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a517a4d444e684e79316a5a6a63774c54566d5a4467744f44457a4d79307a5932566a5954466a5a6d59344e44636966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d062abd54f36dc1eabf862bc494156c009142c5b0000000000000000000000000000000000000000000000000000000000001654000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9d2dfe50be4df7b838da0638a3a77ad78c54bd268888143de2b83da6a432b469",
      "signature": {
        "s": "0x5546a402015134fb2f0a9d606dc37ad473650dfab5e07a52783676a5f4c313ab",
        "r": "0xd6e102cca4b6030f9519e554d1b79bcf9c8ba9929c49ea4fc10bd8dec5305abb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x47e0b80a57ccd94712d97bbcce2b9d4b5e746f627dc88de625ece6113e057003",
      "signature": {
        "s": "0x181fe05f0ec9a33a08ddb7ea52f4fa786354db5f7515c4d6052aeff06bdb498e",
        "r": "0x159681329825ec90c7b9f5e492973e9eb7229a38e5f22cf2327bfa8c9d525667",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5716",
    "total": "5716"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5716",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "630323"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NjQzMDNhNy1jZjcwLTVmZDgtODEzMy0zY2VjYTFjZmY4NDcifQ==",
    "nonce": 1522,
    "balances": {
      "current": "10000001453203428",
      "previous": "10000001453209149"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd062abd54f36dc1eabf862bc494156c009142c5b",
    "nonce": 20,
    "balances": {
      "current": "5716",
      "previous": "0"
    }
  },
  "blockNumber": "10114532",
  "created": "2020-05-22T08:10:10.665Z",
  "updated": "2020-05-22T08:10:10.736Z",
  "id": "5ec788e2005df800101bc429"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000016540000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5716`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``