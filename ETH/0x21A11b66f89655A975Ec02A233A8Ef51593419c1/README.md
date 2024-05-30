# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x21A11b66f89655A975Ec02A233A8Ef51593419c1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000012000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000012a2bc1985cc5fc007aa25bdfa903b1092f31cf91345445ed2bb2f841c878634985b7b2dffa9760a5b88e76c56f6bd0889fefddac6f3f5cd11e7e40a7ac1d77e3342ee8ce1a1963aaeab3dc278bb7fc0d2c3cb133f11dc5d495b874d04fd899018000000000000000000000000000000000000000000000000000000000000001c2c68ca09251a3b6f6416c72e26a8fb579e83c9f08892ece4ffc36a504bcd1e60c2f98f1922bb0087cb88c491feca2d8dd0be173d87dd9ba8e38a88e8d38cfe8e7cdea6d6fa230c386695b7154bf9204bafda3c9fd5b2587f354011d93ccd2ba1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000088b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc76837a000000000000000000000000000000000000000000000000002386f2bc76838d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c260300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e5755315a54686d4d4330784f4455784c5455304e545574596a59334e69316b4d4449304e6a4e6d4d6d4d334e32496966513d3d000000000000000000000000000000000000000000000000000000000000001100000000000000000000000021a11b66f89655a975ec02a233a8ef51593419c10000000000000000000000000000000000000000000000000000000000000012000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa2bc1985cc5fc007aa25bdfa903b1092f31cf91345445ed2bb2f841c87863498",
      "signature": {
        "s": "0x42ee8ce1a1963aaeab3dc278bb7fc0d2c3cb133f11dc5d495b874d04fd899018",
        "r": "0x5b7b2dffa9760a5b88e76c56f6bd0889fefddac6f3f5cd11e7e40a7ac1d77e33",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2c68ca09251a3b6f6416c72e26a8fb579e83c9f08892ece4ffc36a504bcd1e60",
      "signature": {
        "s": "0x7cdea6d6fa230c386695b7154bf9204bafda3c9fd5b2587f354011d93ccd2ba1",
        "r": "0xc2f98f1922bb0087cb88c491feca2d8dd0be173d87dd9ba8e38a88e8d38cfe8e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18",
    "total": "18"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18",
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
            "amount": "796163"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNWU1ZThmMC0xODUxLTU0NTUtYjY3Ni1kMDI0NjNmMmM3N2IifQ==",
    "nonce": 2187,
    "balances": {
      "current": "10000001286964090",
      "previous": "10000001286964109"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x21a11b66f89655a975ec02a233a8ef51593419c1",
    "nonce": 17,
    "balances": {
      "current": "18",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:14:56.221Z",
  "updated": "2020-05-22T08:14:56.294Z",
  "id": "5ec78a00b0c6090011d5abaa"
}
```
* *stageAmount*: `18`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000012000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000012a2bc1985cc5fc007aa25bdfa903b1092f31cf91345445ed2bb2f841c878634985b7b2dffa9760a5b88e76c56f6bd0889fefddac6f3f5cd11e7e40a7ac1d77e3342ee8ce1a1963aaeab3dc278bb7fc0d2c3cb133f11dc5d495b874d04fd899018000000000000000000000000000000000000000000000000000000000000001c2c68ca09251a3b6f6416c72e26a8fb579e83c9f08892ece4ffc36a504bcd1e60c2f98f1922bb0087cb88c491feca2d8dd0be173d87dd9ba8e38a88e8d38cfe8e7cdea6d6fa230c386695b7154bf9204bafda3c9fd5b2587f354011d93ccd2ba1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000088b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc76837a000000000000000000000000000000000000000000000000002386f2bc76838d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c260300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e5755315a54686d4d4330784f4455784c5455304e545574596a59334e69316b4d4449304e6a4e6d4d6d4d334e32496966513d3d000000000000000000000000000000000000000000000000000000000000001100000000000000000000000021a11b66f89655a975ec02a233a8ef51593419c10000000000000000000000000000000000000000000000000000000000000012000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa2bc1985cc5fc007aa25bdfa903b1092f31cf91345445ed2bb2f841c87863498",
      "signature": {
        "s": "0x42ee8ce1a1963aaeab3dc278bb7fc0d2c3cb133f11dc5d495b874d04fd899018",
        "r": "0x5b7b2dffa9760a5b88e76c56f6bd0889fefddac6f3f5cd11e7e40a7ac1d77e33",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2c68ca09251a3b6f6416c72e26a8fb579e83c9f08892ece4ffc36a504bcd1e60",
      "signature": {
        "s": "0x7cdea6d6fa230c386695b7154bf9204bafda3c9fd5b2587f354011d93ccd2ba1",
        "r": "0xc2f98f1922bb0087cb88c491feca2d8dd0be173d87dd9ba8e38a88e8d38cfe8e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18",
    "total": "18"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18",
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
            "amount": "796163"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNWU1ZThmMC0xODUxLTU0NTUtYjY3Ni1kMDI0NjNmMmM3N2IifQ==",
    "nonce": 2187,
    "balances": {
      "current": "10000001286964090",
      "previous": "10000001286964109"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x21a11b66f89655a975ec02a233a8ef51593419c1",
    "nonce": 17,
    "balances": {
      "current": "18",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:14:56.221Z",
  "updated": "2020-05-22T08:14:56.294Z",
  "id": "5ec78a00b0c6090011d5abaa"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``