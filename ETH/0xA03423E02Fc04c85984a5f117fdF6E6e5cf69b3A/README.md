# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA03423E02Fc04c85984a5f117fdF6E6e5cf69b3A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000028450000000000000000000000000000000000000000000000000000000000002845000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000028450000000000000000000000000000000000000000000000000000000000002845f9505f55dd50386899a1104e5c6a07bc29d2a520131c5afe279c61689cf76d1c3b12edcb94743e42a80ebd3d3dd0f3200100c2986a60889fa7204f96fe0018b77037e45bc9e143faf9e37155f703b45f7f72c6073d32610aeb21be69c664de57000000000000000000000000000000000000000000000000000000000000001bc27b4e5f27be4575681f8cbb6f139d1b51621217db598866b4b8f77b8cc5bd9fa4c19dc2c887a71efdecb674bf3b239aee4804ea2e6713cc8736c715872e9eed4dbd20069eafe9e2a3af2992270550681d2011118048ae9da7b2804303f5853d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000009f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d1cfd8c5000000000000000000000000000000000000000000000000002386f2d1d0011400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006b2af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e7a6c6b4f4751325969307a4e57566d4c5455345a44597459546c684e53316a4d54646a593255325a6a6b7a4e6a456966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000a03423e02fc04c85984a5f117fdf6e6e5cf69b3a0000000000000000000000000000000000000000000000000000000000002845000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf9505f55dd50386899a1104e5c6a07bc29d2a520131c5afe279c61689cf76d1c",
      "signature": {
        "s": "0x7037e45bc9e143faf9e37155f703b45f7f72c6073d32610aeb21be69c664de57",
        "r": "0x3b12edcb94743e42a80ebd3d3dd0f3200100c2986a60889fa7204f96fe0018b7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc27b4e5f27be4575681f8cbb6f139d1b51621217db598866b4b8f77b8cc5bd9f",
      "signature": {
        "s": "0x4dbd20069eafe9e2a3af2992270550681d2011118048ae9da7b2804303f5853d",
        "r": "0xa4c19dc2c887a71efdecb674bf3b239aee4804ea2e6713cc8736c715872e9eed",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10309",
    "total": "10309"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10309",
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
            "amount": "438959"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNzlkOGQ2Yi0zNWVmLTU4ZDYtYTlhNS1jMTdjY2U2ZjkzNjEifQ==",
    "nonce": 159,
    "balances": {
      "current": "10000001645140165",
      "previous": "10000001645150484"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa03423e02fc04c85984a5f117fdf6e6e5cf69b3a",
    "nonce": 10,
    "balances": {
      "current": "10309",
      "previous": "0"
    }
  },
  "blockNumber": "10114491",
  "created": "2020-05-22T08:00:06.481Z",
  "updated": "2020-05-22T08:00:06.563Z",
  "id": "5ec78686005df800101bc245"
}
```
* *stageAmount*: `10309`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000002845000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000028450000000000000000000000000000000000000000000000000000000000002845f9505f55dd50386899a1104e5c6a07bc29d2a520131c5afe279c61689cf76d1c3b12edcb94743e42a80ebd3d3dd0f3200100c2986a60889fa7204f96fe0018b77037e45bc9e143faf9e37155f703b45f7f72c6073d32610aeb21be69c664de57000000000000000000000000000000000000000000000000000000000000001bc27b4e5f27be4575681f8cbb6f139d1b51621217db598866b4b8f77b8cc5bd9fa4c19dc2c887a71efdecb674bf3b239aee4804ea2e6713cc8736c715872e9eed4dbd20069eafe9e2a3af2992270550681d2011118048ae9da7b2804303f5853d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000009f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d1cfd8c5000000000000000000000000000000000000000000000000002386f2d1d0011400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006b2af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e7a6c6b4f4751325969307a4e57566d4c5455345a44597459546c684e53316a4d54646a593255325a6a6b7a4e6a456966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000a03423e02fc04c85984a5f117fdf6e6e5cf69b3a0000000000000000000000000000000000000000000000000000000000002845000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf9505f55dd50386899a1104e5c6a07bc29d2a520131c5afe279c61689cf76d1c",
      "signature": {
        "s": "0x7037e45bc9e143faf9e37155f703b45f7f72c6073d32610aeb21be69c664de57",
        "r": "0x3b12edcb94743e42a80ebd3d3dd0f3200100c2986a60889fa7204f96fe0018b7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc27b4e5f27be4575681f8cbb6f139d1b51621217db598866b4b8f77b8cc5bd9f",
      "signature": {
        "s": "0x4dbd20069eafe9e2a3af2992270550681d2011118048ae9da7b2804303f5853d",
        "r": "0xa4c19dc2c887a71efdecb674bf3b239aee4804ea2e6713cc8736c715872e9eed",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10309",
    "total": "10309"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10309",
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
            "amount": "438959"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNzlkOGQ2Yi0zNWVmLTU4ZDYtYTlhNS1jMTdjY2U2ZjkzNjEifQ==",
    "nonce": 159,
    "balances": {
      "current": "10000001645140165",
      "previous": "10000001645150484"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa03423e02fc04c85984a5f117fdf6e6e5cf69b3a",
    "nonce": 10,
    "balances": {
      "current": "10309",
      "previous": "0"
    }
  },
  "blockNumber": "10114491",
  "created": "2020-05-22T08:00:06.481Z",
  "updated": "2020-05-22T08:00:06.563Z",
  "id": "5ec78686005df800101bc245"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000028450000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10309`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``