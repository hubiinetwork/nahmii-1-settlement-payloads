# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9b6D023c8ae0D38AA560ad47De93c326637F6A6F`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000014370000000000000000000000000000000000000000000000000000000000001437000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000014370000000000000000000000000000000000000000000000000000000000001437abc7e780df949c483045d09b094465e3e9d1401444e4235922b2958d899d81568f7934cac401f84d6f153622ab82cc8661efbf5b5f615d01a715ad5988a480360bcddc0c01803f7a5f05880a68eac1eaf7ab983a2fb8b49d22e62c418158b215000000000000000000000000000000000000000000000000000000000000001b5446817cb5519039371f16540d4039614961420ebd0a54f8344b4911b1fed4b8ec4530849cc65c7d26c7d27e4c0e12d31e605235d59ab8050bd10b4d0ea9972b03af4efc91a13c56ff2fc5d82be710974c6904a4b606deda8f936ebe092543d2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000048d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c812ad24000000000000000000000000000000000000000000000000002386f2c812c16000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092f3a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6d45304d6a6c6a4e53307a5a4441334c54566a4e6a6374595441304e7930354f4459774d3251794e5451345a474d6966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000009b6d023c8ae0d38aa560ad47de93c326637f6a6f0000000000000000000000000000000000000000000000000000000000001437000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xabc7e780df949c483045d09b094465e3e9d1401444e4235922b2958d899d8156",
      "signature": {
        "s": "0x0bcddc0c01803f7a5f05880a68eac1eaf7ab983a2fb8b49d22e62c418158b215",
        "r": "0x8f7934cac401f84d6f153622ab82cc8661efbf5b5f615d01a715ad5988a48036",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5446817cb5519039371f16540d4039614961420ebd0a54f8344b4911b1fed4b8",
      "signature": {
        "s": "0x03af4efc91a13c56ff2fc5d82be710974c6904a4b606deda8f936ebe092543d2",
        "r": "0xec4530849cc65c7d26c7d27e4c0e12d31e605235d59ab8050bd10b4d0ea9972b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5175",
    "total": "5175"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5175",
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
            "amount": "601914"
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
    "data": "eyJyZWYiOiIwMmE0MjljNS0zZDA3LTVjNjctYTA0Ny05ODYwM2QyNTQ4ZGMifQ==",
    "nonce": 1165,
    "balances": {
      "current": "10000001481747748",
      "previous": "10000001481752928"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9b6d023c8ae0d38aa560ad47de93c326637f6a6f",
    "nonce": 10,
    "balances": {
      "current": "5175",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:14.520Z",
  "updated": "2020-05-22T08:07:14.588Z",
  "id": "5ec78832005df800101bc3a5"
}
```
* *stageAmount*: `5175`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000001437000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000014370000000000000000000000000000000000000000000000000000000000001437abc7e780df949c483045d09b094465e3e9d1401444e4235922b2958d899d81568f7934cac401f84d6f153622ab82cc8661efbf5b5f615d01a715ad5988a480360bcddc0c01803f7a5f05880a68eac1eaf7ab983a2fb8b49d22e62c418158b215000000000000000000000000000000000000000000000000000000000000001b5446817cb5519039371f16540d4039614961420ebd0a54f8344b4911b1fed4b8ec4530849cc65c7d26c7d27e4c0e12d31e605235d59ab8050bd10b4d0ea9972b03af4efc91a13c56ff2fc5d82be710974c6904a4b606deda8f936ebe092543d2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000048d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c812ad24000000000000000000000000000000000000000000000000002386f2c812c16000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092f3a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6d45304d6a6c6a4e53307a5a4441334c54566a4e6a6374595441304e7930354f4459774d3251794e5451345a474d6966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000009b6d023c8ae0d38aa560ad47de93c326637f6a6f0000000000000000000000000000000000000000000000000000000000001437000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xabc7e780df949c483045d09b094465e3e9d1401444e4235922b2958d899d8156",
      "signature": {
        "s": "0x0bcddc0c01803f7a5f05880a68eac1eaf7ab983a2fb8b49d22e62c418158b215",
        "r": "0x8f7934cac401f84d6f153622ab82cc8661efbf5b5f615d01a715ad5988a48036",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5446817cb5519039371f16540d4039614961420ebd0a54f8344b4911b1fed4b8",
      "signature": {
        "s": "0x03af4efc91a13c56ff2fc5d82be710974c6904a4b606deda8f936ebe092543d2",
        "r": "0xec4530849cc65c7d26c7d27e4c0e12d31e605235d59ab8050bd10b4d0ea9972b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5175",
    "total": "5175"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5175",
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
            "amount": "601914"
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
    "data": "eyJyZWYiOiIwMmE0MjljNS0zZDA3LTVjNjctYTA0Ny05ODYwM2QyNTQ4ZGMifQ==",
    "nonce": 1165,
    "balances": {
      "current": "10000001481747748",
      "previous": "10000001481752928"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9b6d023c8ae0d38aa560ad47de93c326637f6a6f",
    "nonce": 10,
    "balances": {
      "current": "5175",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:14.520Z",
  "updated": "2020-05-22T08:07:14.588Z",
  "id": "5ec78832005df800101bc3a5"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000014370000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5175`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``