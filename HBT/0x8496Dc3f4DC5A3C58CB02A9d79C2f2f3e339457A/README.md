# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8496Dc3f4DC5A3C58CB02A9d79C2f2f3e339457A`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001745dd77000000000000000000000000000000000000000000000000000000001745dd77000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001745dd77000000000000000000000000000000000000000000000000000000001745dd772ebb7a46b99f0e0d247d81b36c5466919ec6e221b7364a00b7c4b124a78e3deba8be1a9d71689bcb147d27f5f3b466fd2beaa4f4d66525171f9348baa522603a77c7f91ff6332de469f78b38c492b911e3a277113387a1c24c4a5c704865740f000000000000000000000000000000000000000000000000000000000000001b90526d08ffaaf228678afcbe962b417657d83531608aaa92dc93dd05e2fe9e6abc2976e31f11dde38178bfe550720cab642aa4978ab891de5d01cf9184119f6131287963b06d112021eab03fbd214de58cf7670f38cca546e7cf9a01b30d3a11000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56960000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000196b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e19ea84e16000000000000000000000000000000000000000000000000002e17e1b5f420c300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005f536000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a24e71e77000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a5451784e47497959533079593245344c5455334e545974595463304e53316b4f4449344d4751354f544177597a676966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000008496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a000000000000000000000000000000000000000000000000000000001745dd77000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2ebb7a46b99f0e0d247d81b36c5466919ec6e221b7364a00b7c4b124a78e3deb",
      "signature": {
        "s": "0x77c7f91ff6332de469f78b38c492b911e3a277113387a1c24c4a5c704865740f",
        "r": "0xa8be1a9d71689bcb147d27f5f3b466fd2beaa4f4d66525171f9348baa522603a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x90526d08ffaaf228678afcbe962b417657d83531608aaa92dc93dd05e2fe9e6a",
      "signature": {
        "s": "0x31287963b06d112021eab03fbd214de58cf7670f38cca546e7cf9a01b30d3a11",
        "r": "0xbc2976e31f11dde38178bfe550720cab642aa4978ab891de5d01cf9184119f61",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "390454647",
    "total": "390454647"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "390454647",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "43568799351"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "390454"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZTQxNGIyYS0yY2E4LTU3NTYtYTc0NS1kODI4MGQ5OTAwYzgifQ==",
    "nonce": 6507,
    "balances": {
      "current": "12974106725600790",
      "previous": "12974107116445891"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a",
    "nonce": 10,
    "balances": {
      "current": "390454647",
      "previous": "0"
    }
  },
  "blockNumber": "10114710",
  "created": "2020-05-22T08:49:43.076Z",
  "updated": "2020-05-22T08:49:43.154Z",
  "id": "5ec79227e5756b00111b87c2"
}
```
* *stageAmount*: `390454647`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001745dd77000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001745dd77000000000000000000000000000000000000000000000000000000001745dd772ebb7a46b99f0e0d247d81b36c5466919ec6e221b7364a00b7c4b124a78e3deba8be1a9d71689bcb147d27f5f3b466fd2beaa4f4d66525171f9348baa522603a77c7f91ff6332de469f78b38c492b911e3a277113387a1c24c4a5c704865740f000000000000000000000000000000000000000000000000000000000000001b90526d08ffaaf228678afcbe962b417657d83531608aaa92dc93dd05e2fe9e6abc2976e31f11dde38178bfe550720cab642aa4978ab891de5d01cf9184119f6131287963b06d112021eab03fbd214de58cf7670f38cca546e7cf9a01b30d3a11000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56960000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000196b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e19ea84e16000000000000000000000000000000000000000000000000002e17e1b5f420c300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005f536000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a24e71e77000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a5451784e47497959533079593245344c5455334e545974595463304e53316b4f4449344d4751354f544177597a676966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000008496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a000000000000000000000000000000000000000000000000000000001745dd77000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2ebb7a46b99f0e0d247d81b36c5466919ec6e221b7364a00b7c4b124a78e3deb",
      "signature": {
        "s": "0x77c7f91ff6332de469f78b38c492b911e3a277113387a1c24c4a5c704865740f",
        "r": "0xa8be1a9d71689bcb147d27f5f3b466fd2beaa4f4d66525171f9348baa522603a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x90526d08ffaaf228678afcbe962b417657d83531608aaa92dc93dd05e2fe9e6a",
      "signature": {
        "s": "0x31287963b06d112021eab03fbd214de58cf7670f38cca546e7cf9a01b30d3a11",
        "r": "0xbc2976e31f11dde38178bfe550720cab642aa4978ab891de5d01cf9184119f61",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "390454647",
    "total": "390454647"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "390454647",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "43568799351"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "390454"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZTQxNGIyYS0yY2E4LTU3NTYtYTc0NS1kODI4MGQ5OTAwYzgifQ==",
    "nonce": 6507,
    "balances": {
      "current": "12974106725600790",
      "previous": "12974107116445891"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a",
    "nonce": 10,
    "balances": {
      "current": "390454647",
      "previous": "0"
    }
  },
  "blockNumber": "10114710",
  "created": "2020-05-22T08:49:43.076Z",
  "updated": "2020-05-22T08:49:43.154Z",
  "id": "5ec79227e5756b00111b87c2"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000001745dd77000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `390454647`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`