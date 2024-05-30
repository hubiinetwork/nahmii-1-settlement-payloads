# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x263b144DD2e01261b5Ae1DF7B46b340658698d9a`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000479400000000000000000000000000000000000000000000000000000000000047940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000479400000000000000000000000000000000000000000000000000000000000047944d35206db76b08b64e095bafadf5d04737d91779edcb4fdfdd45e7ff293ad6ebbde2cf74c634cd9c45ac07faf2c37c16477315d0745e38546197f4583825d1e97c973a00ffe9ad3f9ae86f669eba70a7b7aa30181df971421387ac928fabca2c000000000000000000000000000000000000000000000000000000000000001cfbbc37e3ae9b739799e6d9a01af58ca78ae27158cb84e7821c4cddc1bf7efbf43b8e752037e7833e4814a641bfdf2fed83c65430dafc9bfb63ab07f9e54e17140b970ad8be6f4b1bde7fc40839a486757667a17c6ac13413df760551f38de1b8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000ee00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cddb3317000000000000000000000000000000000000000000000000002386f2cddb7abd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b58c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d444669597a55334d4330775a6d5a6b4c5455354e575974595445304e53316b4d5441304d324978596a646c5a444d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000263b144dd2e01261b5ae1df7b46b340658698d9a0000000000000000000000000000000000000000000000000000000000004794000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4d35206db76b08b64e095bafadf5d04737d91779edcb4fdfdd45e7ff293ad6eb",
      "signature": {
        "s": "0x7c973a00ffe9ad3f9ae86f669eba70a7b7aa30181df971421387ac928fabca2c",
        "r": "0xbde2cf74c634cd9c45ac07faf2c37c16477315d0745e38546197f4583825d1e9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfbbc37e3ae9b739799e6d9a01af58ca78ae27158cb84e7821c4cddc1bf7efbf4",
      "signature": {
        "s": "0x0b970ad8be6f4b1bde7fc40839a486757667a17c6ac13413df760551f38de1b8",
        "r": "0x3b8e752037e7833e4814a641bfdf2fed83c65430dafc9bfb63ab07f9e54e1714",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18324",
    "total": "18324"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18324",
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
            "amount": "505228"
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
    "data": "eyJyZWYiOiJjMDFiYzU3MC0wZmZkLTU5NWYtYTE0NS1kMTA0M2IxYjdlZDMifQ==",
    "nonce": 238,
    "balances": {
      "current": "10000001578775319",
      "previous": "10000001578793661"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x263b144dd2e01261b5ae1df7b46b340658698d9a",
    "nonce": 20,
    "balances": {
      "current": "18324",
      "previous": "0"
    }
  },
  "blockNumber": "10114493",
  "created": "2020-05-22T08:00:34.098Z",
  "updated": "2020-05-22T08:00:34.175Z",
  "id": "5ec786a2005df800101bc261"
}
```
* *stageAmount*: `18324`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000047940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000479400000000000000000000000000000000000000000000000000000000000047944d35206db76b08b64e095bafadf5d04737d91779edcb4fdfdd45e7ff293ad6ebbde2cf74c634cd9c45ac07faf2c37c16477315d0745e38546197f4583825d1e97c973a00ffe9ad3f9ae86f669eba70a7b7aa30181df971421387ac928fabca2c000000000000000000000000000000000000000000000000000000000000001cfbbc37e3ae9b739799e6d9a01af58ca78ae27158cb84e7821c4cddc1bf7efbf43b8e752037e7833e4814a641bfdf2fed83c65430dafc9bfb63ab07f9e54e17140b970ad8be6f4b1bde7fc40839a486757667a17c6ac13413df760551f38de1b8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000ee00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cddb3317000000000000000000000000000000000000000000000000002386f2cddb7abd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b58c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d444669597a55334d4330775a6d5a6b4c5455354e575974595445304e53316b4d5441304d324978596a646c5a444d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000263b144dd2e01261b5ae1df7b46b340658698d9a0000000000000000000000000000000000000000000000000000000000004794000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4d35206db76b08b64e095bafadf5d04737d91779edcb4fdfdd45e7ff293ad6eb",
      "signature": {
        "s": "0x7c973a00ffe9ad3f9ae86f669eba70a7b7aa30181df971421387ac928fabca2c",
        "r": "0xbde2cf74c634cd9c45ac07faf2c37c16477315d0745e38546197f4583825d1e9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfbbc37e3ae9b739799e6d9a01af58ca78ae27158cb84e7821c4cddc1bf7efbf4",
      "signature": {
        "s": "0x0b970ad8be6f4b1bde7fc40839a486757667a17c6ac13413df760551f38de1b8",
        "r": "0x3b8e752037e7833e4814a641bfdf2fed83c65430dafc9bfb63ab07f9e54e1714",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18324",
    "total": "18324"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18324",
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
            "amount": "505228"
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
    "data": "eyJyZWYiOiJjMDFiYzU3MC0wZmZkLTU5NWYtYTE0NS1kMTA0M2IxYjdlZDMifQ==",
    "nonce": 238,
    "balances": {
      "current": "10000001578775319",
      "previous": "10000001578793661"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x263b144dd2e01261b5ae1df7b46b340658698d9a",
    "nonce": 20,
    "balances": {
      "current": "18324",
      "previous": "0"
    }
  },
  "blockNumber": "10114493",
  "created": "2020-05-22T08:00:34.098Z",
  "updated": "2020-05-22T08:00:34.175Z",
  "id": "5ec786a2005df800101bc261"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18324`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``