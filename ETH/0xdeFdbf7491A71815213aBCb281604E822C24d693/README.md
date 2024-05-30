# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdeFdbf7491A71815213aBCb281604E822C24d693`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000047f500000000000000000000000000000000000000000000000000000000000047f5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047f500000000000000000000000000000000000000000000000000000000000047f54e5d25a91154c1eecba67bf0f9140f367c82fd961a1f30ad9d38543e4c552edfdb377fd8bd6bc1af867e3a92027494d90871de62999e7935e918b04e5cc675cb16152b89e11b3dfbdc0ca3be5c2053a2640c01e49c5306190ce1bd0ad601ba09000000000000000000000000000000000000000000000000000000000000001bd4c83ba8e20a005a285a9db4d3988f7f7a148b820be2462d5f274fa8afb5ea2d826d4b55df7aef841e6533a9e30cc23ff3fe73d0aec729f65612137a17e986567fa68a3d43788a7de86b74d4e9d1a02e1584efbeccc6264091642775b659183b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55cb000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002cf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf23df0000000000000000000000000000000000000000000000000002386f2caf285f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008739900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d3256694f545a6d595330344f57526b4c5456694d5451744f446b77597930305a6d526c4f545577593249794e32456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000defdbf7491a71815213abcb281604e822c24d69300000000000000000000000000000000000000000000000000000000000047f5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4e5d25a91154c1eecba67bf0f9140f367c82fd961a1f30ad9d38543e4c552edf",
      "signature": {
        "s": "0x16152b89e11b3dfbdc0ca3be5c2053a2640c01e49c5306190ce1bd0ad601ba09",
        "r": "0xdb377fd8bd6bc1af867e3a92027494d90871de62999e7935e918b04e5cc675cb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd4c83ba8e20a005a285a9db4d3988f7f7a148b820be2462d5f274fa8afb5ea2d",
      "signature": {
        "s": "0x7fa68a3d43788a7de86b74d4e9d1a02e1584efbeccc6264091642775b659183b",
        "r": "0x826d4b55df7aef841e6533a9e30cc23ff3fe73d0aec729f65612137a17e98656",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18421",
    "total": "18421"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18421",
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
            "amount": "553881"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxM2ViOTZmYS04OWRkLTViMTQtODkwYy00ZmRlOTUwY2IyN2EifQ==",
    "nonce": 719,
    "balances": {
      "current": "10000001529953776",
      "previous": "10000001529972215"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdefdbf7491a71815213abcb281604e822c24d693",
    "nonce": 20,
    "balances": {
      "current": "18421",
      "previous": "0"
    }
  },
  "blockNumber": "10114507",
  "created": "2020-05-22T08:04:13.913Z",
  "updated": "2020-05-22T08:04:13.988Z",
  "id": "5ec7877d005df800101bc306"
}
```
* *stageAmount*: `18421`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000047f5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047f500000000000000000000000000000000000000000000000000000000000047f54e5d25a91154c1eecba67bf0f9140f367c82fd961a1f30ad9d38543e4c552edfdb377fd8bd6bc1af867e3a92027494d90871de62999e7935e918b04e5cc675cb16152b89e11b3dfbdc0ca3be5c2053a2640c01e49c5306190ce1bd0ad601ba09000000000000000000000000000000000000000000000000000000000000001bd4c83ba8e20a005a285a9db4d3988f7f7a148b820be2462d5f274fa8afb5ea2d826d4b55df7aef841e6533a9e30cc23ff3fe73d0aec729f65612137a17e986567fa68a3d43788a7de86b74d4e9d1a02e1584efbeccc6264091642775b659183b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55cb000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002cf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf23df0000000000000000000000000000000000000000000000000002386f2caf285f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008739900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d3256694f545a6d595330344f57526b4c5456694d5451744f446b77597930305a6d526c4f545577593249794e32456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000defdbf7491a71815213abcb281604e822c24d69300000000000000000000000000000000000000000000000000000000000047f5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4e5d25a91154c1eecba67bf0f9140f367c82fd961a1f30ad9d38543e4c552edf",
      "signature": {
        "s": "0x16152b89e11b3dfbdc0ca3be5c2053a2640c01e49c5306190ce1bd0ad601ba09",
        "r": "0xdb377fd8bd6bc1af867e3a92027494d90871de62999e7935e918b04e5cc675cb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd4c83ba8e20a005a285a9db4d3988f7f7a148b820be2462d5f274fa8afb5ea2d",
      "signature": {
        "s": "0x7fa68a3d43788a7de86b74d4e9d1a02e1584efbeccc6264091642775b659183b",
        "r": "0x826d4b55df7aef841e6533a9e30cc23ff3fe73d0aec729f65612137a17e98656",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18421",
    "total": "18421"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18421",
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
            "amount": "553881"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxM2ViOTZmYS04OWRkLTViMTQtODkwYy00ZmRlOTUwY2IyN2EifQ==",
    "nonce": 719,
    "balances": {
      "current": "10000001529953776",
      "previous": "10000001529972215"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdefdbf7491a71815213abcb281604e822c24d693",
    "nonce": 20,
    "balances": {
      "current": "18421",
      "previous": "0"
    }
  },
  "blockNumber": "10114507",
  "created": "2020-05-22T08:04:13.913Z",
  "updated": "2020-05-22T08:04:13.988Z",
  "id": "5ec7877d005df800101bc306"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047f50000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18421`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``