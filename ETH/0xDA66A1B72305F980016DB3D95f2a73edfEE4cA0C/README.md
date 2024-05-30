# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xDA66A1B72305F980016DB3D95f2a73edfEE4cA0C`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000002d2a0000000000000000000000000000000000000000000000000000000000002d2a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000002d2a0000000000000000000000000000000000000000000000000000000000002d2aac90a854e9a5e77b5a77636a163b6c050bef04d4ebbe7769aca16b021ad1b6f16842ecd6e455270e23f0f8a5471de1b8fd5e02d14377c76e25daf6a09c90cd2e10eb704e0d13e6cf11d5390ac490c9aaa39ae02cca7746bf5ee2c8a9f9aea7fe000000000000000000000000000000000000000000000000000000000000001cd182f79b9594f32fcb9bff6edafd59c48b9ded1ba375e016f39bdf876024885a809bccff51809ba06107b629f476dbca09ac764b917680b97e83afdb67567a3e6d7f157e192180d069fc50e9ec3117380b4974004b5c6e228fb606205be5cdea000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005e300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c66fbf38000000000000000000000000000000000000000000000000002386f2c66fec6d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000999f500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978596d4d774d6d457a4e43316d4d475a6b4c54566a4d574974596a5531596930784e4745354d44526a4e324d325a44516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da66a1b72305f980016db3d95f2a73edfee4ca0c0000000000000000000000000000000000000000000000000000000000002d2a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xac90a854e9a5e77b5a77636a163b6c050bef04d4ebbe7769aca16b021ad1b6f1",
      "signature": {
        "s": "0x10eb704e0d13e6cf11d5390ac490c9aaa39ae02cca7746bf5ee2c8a9f9aea7fe",
        "r": "0x6842ecd6e455270e23f0f8a5471de1b8fd5e02d14377c76e25daf6a09c90cd2e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd182f79b9594f32fcb9bff6edafd59c48b9ded1ba375e016f39bdf876024885a",
      "signature": {
        "s": "0x6d7f157e192180d069fc50e9ec3117380b4974004b5c6e228fb606205be5cdea",
        "r": "0x809bccff51809ba06107b629f476dbca09ac764b917680b97e83afdb67567a3e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11562",
    "total": "11562"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11562",
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
            "amount": "629237"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "11"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxYmMwMmEzNC1mMGZkLTVjMWItYjU1Yi0xNGE5MDRjN2M2ZDQifQ==",
    "nonce": 1507,
    "balances": {
      "current": "10000001454292792",
      "previous": "10000001454304365"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda66a1b72305f980016db3d95f2a73edfee4ca0c",
    "nonce": 20,
    "balances": {
      "current": "11562",
      "previous": "0"
    }
  },
  "blockNumber": "10114531",
  "created": "2020-05-22T08:10:03.517Z",
  "updated": "2020-05-22T08:10:03.601Z",
  "id": "5ec788dbe5756b00111b814c"
}
```
* *stageAmount*: `11562`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000002d2a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000002d2a0000000000000000000000000000000000000000000000000000000000002d2aac90a854e9a5e77b5a77636a163b6c050bef04d4ebbe7769aca16b021ad1b6f16842ecd6e455270e23f0f8a5471de1b8fd5e02d14377c76e25daf6a09c90cd2e10eb704e0d13e6cf11d5390ac490c9aaa39ae02cca7746bf5ee2c8a9f9aea7fe000000000000000000000000000000000000000000000000000000000000001cd182f79b9594f32fcb9bff6edafd59c48b9ded1ba375e016f39bdf876024885a809bccff51809ba06107b629f476dbca09ac764b917680b97e83afdb67567a3e6d7f157e192180d069fc50e9ec3117380b4974004b5c6e228fb606205be5cdea000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005e300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c66fbf38000000000000000000000000000000000000000000000000002386f2c66fec6d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000999f500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978596d4d774d6d457a4e43316d4d475a6b4c54566a4d574974596a5531596930784e4745354d44526a4e324d325a44516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000da66a1b72305f980016db3d95f2a73edfee4ca0c0000000000000000000000000000000000000000000000000000000000002d2a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xac90a854e9a5e77b5a77636a163b6c050bef04d4ebbe7769aca16b021ad1b6f1",
      "signature": {
        "s": "0x10eb704e0d13e6cf11d5390ac490c9aaa39ae02cca7746bf5ee2c8a9f9aea7fe",
        "r": "0x6842ecd6e455270e23f0f8a5471de1b8fd5e02d14377c76e25daf6a09c90cd2e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd182f79b9594f32fcb9bff6edafd59c48b9ded1ba375e016f39bdf876024885a",
      "signature": {
        "s": "0x6d7f157e192180d069fc50e9ec3117380b4974004b5c6e228fb606205be5cdea",
        "r": "0x809bccff51809ba06107b629f476dbca09ac764b917680b97e83afdb67567a3e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11562",
    "total": "11562"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11562",
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
            "amount": "629237"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "11"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxYmMwMmEzNC1mMGZkLTVjMWItYjU1Yi0xNGE5MDRjN2M2ZDQifQ==",
    "nonce": 1507,
    "balances": {
      "current": "10000001454292792",
      "previous": "10000001454304365"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xda66a1b72305f980016db3d95f2a73edfee4ca0c",
    "nonce": 20,
    "balances": {
      "current": "11562",
      "previous": "0"
    }
  },
  "blockNumber": "10114531",
  "created": "2020-05-22T08:10:03.517Z",
  "updated": "2020-05-22T08:10:03.601Z",
  "id": "5ec788dbe5756b00111b814c"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000002d2a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `11562`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``