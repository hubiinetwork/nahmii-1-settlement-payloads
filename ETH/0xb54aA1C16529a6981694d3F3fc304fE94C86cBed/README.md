# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb54aA1C16529a6981694d3F3fc304fE94C86cBed`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001896000000000000000000000000000000000000000000000000000000000000189600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001896000000000000000000000000000000000000000000000000000000000000189652a3e5e7a3c12ecdf0c3b5cd6f0582536afe38b42e4492a3ff40dcf3e54a80bab6162bcd7a8e75508921c310c0d6de5c347b367640b8fe7b11b101953f89e0832739de9c836c9c545e012e8a21fab8256e2a9c200ecd9df7b268f14df88daf5e000000000000000000000000000000000000000000000000000000000000001b8bd9fffbcd73aca19cd2f7d28f8e9ade148a3740920d89c2b2eba0eee4f9e1b181e0b0575eb2d748f95b9971b6feb61fb91c4f2041dc3646c13bc69f8b0a361604a454a42e3bd30906626d629a1c1673544f19ea42a41902d7c580f74ddc5f0b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000061d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c61b419d000000000000000000000000000000000000000000000000002386f2c61b5a3900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009af8100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e54566a4f446b7a4e5330314e324d304c5455774f4449744f5745335a6930355a5455304e6a63794e4749785957556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b54aa1c16529a6981694d3f3fc304fe94c86cbed0000000000000000000000000000000000000000000000000000000000001896000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x52a3e5e7a3c12ecdf0c3b5cd6f0582536afe38b42e4492a3ff40dcf3e54a80ba",
      "signature": {
        "s": "0x2739de9c836c9c545e012e8a21fab8256e2a9c200ecd9df7b268f14df88daf5e",
        "r": "0xb6162bcd7a8e75508921c310c0d6de5c347b367640b8fe7b11b101953f89e083",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8bd9fffbcd73aca19cd2f7d28f8e9ade148a3740920d89c2b2eba0eee4f9e1b1",
      "signature": {
        "s": "0x04a454a42e3bd30906626d629a1c1673544f19ea42a41902d7c580f74ddc5f0b",
        "r": "0x81e0b0575eb2d748f95b9971b6feb61fb91c4f2041dc3646c13bc69f8b0a3616",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6294",
    "total": "6294"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6294",
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
            "amount": "634753"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NTVjODkzNS01N2M0LTUwODItOWE3Zi05ZTU0NjcyNGIxYWUifQ==",
    "nonce": 1565,
    "balances": {
      "current": "10000001448755613",
      "previous": "10000001448761913"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb54aa1c16529a6981694d3f3fc304fe94c86cbed",
    "nonce": 20,
    "balances": {
      "current": "6294",
      "previous": "0"
    }
  },
  "blockNumber": "10114533",
  "created": "2020-05-22T08:10:34.950Z",
  "updated": "2020-05-22T08:10:35.032Z",
  "id": "5ec788fab0c6090011d5aad6"
}
```
* *stageAmount*: `6294`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000189600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001896000000000000000000000000000000000000000000000000000000000000189652a3e5e7a3c12ecdf0c3b5cd6f0582536afe38b42e4492a3ff40dcf3e54a80bab6162bcd7a8e75508921c310c0d6de5c347b367640b8fe7b11b101953f89e0832739de9c836c9c545e012e8a21fab8256e2a9c200ecd9df7b268f14df88daf5e000000000000000000000000000000000000000000000000000000000000001b8bd9fffbcd73aca19cd2f7d28f8e9ade148a3740920d89c2b2eba0eee4f9e1b181e0b0575eb2d748f95b9971b6feb61fb91c4f2041dc3646c13bc69f8b0a361604a454a42e3bd30906626d629a1c1673544f19ea42a41902d7c580f74ddc5f0b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000061d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c61b419d000000000000000000000000000000000000000000000000002386f2c61b5a3900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009af8100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e54566a4f446b7a4e5330314e324d304c5455774f4449744f5745335a6930355a5455304e6a63794e4749785957556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b54aa1c16529a6981694d3f3fc304fe94c86cbed0000000000000000000000000000000000000000000000000000000000001896000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x52a3e5e7a3c12ecdf0c3b5cd6f0582536afe38b42e4492a3ff40dcf3e54a80ba",
      "signature": {
        "s": "0x2739de9c836c9c545e012e8a21fab8256e2a9c200ecd9df7b268f14df88daf5e",
        "r": "0xb6162bcd7a8e75508921c310c0d6de5c347b367640b8fe7b11b101953f89e083",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8bd9fffbcd73aca19cd2f7d28f8e9ade148a3740920d89c2b2eba0eee4f9e1b1",
      "signature": {
        "s": "0x04a454a42e3bd30906626d629a1c1673544f19ea42a41902d7c580f74ddc5f0b",
        "r": "0x81e0b0575eb2d748f95b9971b6feb61fb91c4f2041dc3646c13bc69f8b0a3616",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6294",
    "total": "6294"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6294",
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
            "amount": "634753"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NTVjODkzNS01N2M0LTUwODItOWE3Zi05ZTU0NjcyNGIxYWUifQ==",
    "nonce": 1565,
    "balances": {
      "current": "10000001448755613",
      "previous": "10000001448761913"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb54aa1c16529a6981694d3f3fc304fe94c86cbed",
    "nonce": 20,
    "balances": {
      "current": "6294",
      "previous": "0"
    }
  },
  "blockNumber": "10114533",
  "created": "2020-05-22T08:10:34.950Z",
  "updated": "2020-05-22T08:10:35.032Z",
  "id": "5ec788fab0c6090011d5aad6"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000018960000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6294`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``