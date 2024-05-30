# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7bc167d23d28c671bf3Fe88A750eD9C6108c6CB1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000165e500000000000000000000000000000000000000000000000000000000000165e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000165e500000000000000000000000000000000000000000000000000000000000165e534cd366f1119f0b9313560f7827e91acae15ff518782974bba84c9dec588ec63c61b4579c637b1e24652beeca44381142a3114691084999b23cb9078950ed51e1fa7653a933ad731287b261d1c836d416a15068672a226bda53df556c1c148b2000000000000000000000000000000000000000000000000000000000000001cda1219475d5f91aaea21e68df754d85cbd72a9de81122b5b94407b81491d4f3fa0b3c18b80c37cf19017d520e7bdf18f7ca8790e4d8ba877d61092da2914db1d645c6f6fa2e451fdfe4b69efa07558c5c2fbc5d9935c8d8cbac038cbd39ecb47000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb8b39cb000000000000000000000000000000000000000000000000002386f2cb8ca00b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000084cd000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a6d4d7a597a67304e79316b4d5467794c5456684e54497459544e6b4f53316d5a6a4a695a6a42694e3249785a54676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007bc167d23d28c671bf3fe88a750ed9c6108c6cb100000000000000000000000000000000000000000000000000000000000165e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x34cd366f1119f0b9313560f7827e91acae15ff518782974bba84c9dec588ec63",
      "signature": {
        "s": "0x1fa7653a933ad731287b261d1c836d416a15068672a226bda53df556c1c148b2",
        "r": "0xc61b4579c637b1e24652beeca44381142a3114691084999b23cb9078950ed51e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xda1219475d5f91aaea21e68df754d85cbd72a9de81122b5b94407b81491d4f3f",
      "signature": {
        "s": "0x645c6f6fa2e451fdfe4b69efa07558c5c2fbc5d9935c8d8cbac038cbd39ecb47",
        "r": "0xa0b3c18b80c37cf19017d520e7bdf18f7ca8790e4d8ba877d61092da2914db1d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "91621",
    "total": "91621"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "91621",
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
            "amount": "543952"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "91"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZmMzYzg0Ny1kMTgyLTVhNTItYTNkOS1mZjJiZjBiN2IxZTgifQ==",
    "nonce": 480,
    "balances": {
      "current": "10000001539979723",
      "previous": "10000001540071435"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7bc167d23d28c671bf3fe88a750ed9c6108c6cb1",
    "nonce": 20,
    "balances": {
      "current": "91621",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:19.077Z",
  "updated": "2020-05-22T08:02:19.151Z",
  "id": "5ec7870be5756b00111b8014"
}
```
* *stageAmount*: `91621`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000165e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000165e500000000000000000000000000000000000000000000000000000000000165e534cd366f1119f0b9313560f7827e91acae15ff518782974bba84c9dec588ec63c61b4579c637b1e24652beeca44381142a3114691084999b23cb9078950ed51e1fa7653a933ad731287b261d1c836d416a15068672a226bda53df556c1c148b2000000000000000000000000000000000000000000000000000000000000001cda1219475d5f91aaea21e68df754d85cbd72a9de81122b5b94407b81491d4f3fa0b3c18b80c37cf19017d520e7bdf18f7ca8790e4d8ba877d61092da2914db1d645c6f6fa2e451fdfe4b69efa07558c5c2fbc5d9935c8d8cbac038cbd39ecb47000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb8b39cb000000000000000000000000000000000000000000000000002386f2cb8ca00b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000084cd000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a6d4d7a597a67304e79316b4d5467794c5456684e54497459544e6b4f53316d5a6a4a695a6a42694e3249785a54676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007bc167d23d28c671bf3fe88a750ed9c6108c6cb100000000000000000000000000000000000000000000000000000000000165e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x34cd366f1119f0b9313560f7827e91acae15ff518782974bba84c9dec588ec63",
      "signature": {
        "s": "0x1fa7653a933ad731287b261d1c836d416a15068672a226bda53df556c1c148b2",
        "r": "0xc61b4579c637b1e24652beeca44381142a3114691084999b23cb9078950ed51e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xda1219475d5f91aaea21e68df754d85cbd72a9de81122b5b94407b81491d4f3f",
      "signature": {
        "s": "0x645c6f6fa2e451fdfe4b69efa07558c5c2fbc5d9935c8d8cbac038cbd39ecb47",
        "r": "0xa0b3c18b80c37cf19017d520e7bdf18f7ca8790e4d8ba877d61092da2914db1d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "91621",
    "total": "91621"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "91621",
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
            "amount": "543952"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "91"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZmMzYzg0Ny1kMTgyLTVhNTItYTNkOS1mZjJiZjBiN2IxZTgifQ==",
    "nonce": 480,
    "balances": {
      "current": "10000001539979723",
      "previous": "10000001540071435"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7bc167d23d28c671bf3fe88a750ed9c6108c6cb1",
    "nonce": 20,
    "balances": {
      "current": "91621",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:19.077Z",
  "updated": "2020-05-22T08:02:19.151Z",
  "id": "5ec7870be5756b00111b8014"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000165e50000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `91621`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``