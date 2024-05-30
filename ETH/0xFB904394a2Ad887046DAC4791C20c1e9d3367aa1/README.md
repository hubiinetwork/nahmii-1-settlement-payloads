# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFB904394a2Ad887046DAC4791C20c1e9d3367aa1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000028cc00000000000000000000000000000000000000000000000000000000000028cc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000028cc00000000000000000000000000000000000000000000000000000000000028ccf66434030c28fa9ee13ad24b9b4f984f149895944c82d8a1aae6d7e9ba51930491bab00113af081ca79cad8b9dad42f9f0562400281d06acbad121c15425c6244223e546200b8da10e7a14afd65ec56b7cfdad56d3cc8e8598c2aa548a71d0be000000000000000000000000000000000000000000000000000000000000001c2aea4ca1c2788ef4e4f891bd61a7ca617b2c5c0ddc479f69c3e9da4d041b1d5b755d563747db1d3f9c6f6228b3dcd452f03b6ce829d8c459a9a1736f5e3dff3e62901d6ca74241b23e4432995ee1b6b46e774b9df12d095ce1a10111429b7a6d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000047c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c820a1e0000000000000000000000000000000000000000000000000002386f2c820cab600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092bb200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a6d517a4f4467355969316d5a6a59774c5455324f4467744f546468596930775a6a52684e4745344f5745324d44416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000fb904394a2ad887046dac4791c20c1e9d3367aa100000000000000000000000000000000000000000000000000000000000028cc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf66434030c28fa9ee13ad24b9b4f984f149895944c82d8a1aae6d7e9ba519304",
      "signature": {
        "s": "0x4223e546200b8da10e7a14afd65ec56b7cfdad56d3cc8e8598c2aa548a71d0be",
        "r": "0x91bab00113af081ca79cad8b9dad42f9f0562400281d06acbad121c15425c624",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2aea4ca1c2788ef4e4f891bd61a7ca617b2c5c0ddc479f69c3e9da4d041b1d5b",
      "signature": {
        "s": "0x62901d6ca74241b23e4432995ee1b6b46e774b9df12d095ce1a10111429b7a6d",
        "r": "0x755d563747db1d3f9c6f6228b3dcd452f03b6ce829d8c459a9a1736f5e3dff3e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10444",
    "total": "10444"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10444",
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
            "amount": "601010"
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
    "data": "eyJyZWYiOiJkZmQzODg5Yi1mZjYwLTU2ODgtOTdhYi0wZjRhNGE4OWE2MDAifQ==",
    "nonce": 1148,
    "balances": {
      "current": "10000001482662368",
      "previous": "10000001482672822"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfb904394a2ad887046dac4791c20c1e9d3367aa1",
    "nonce": 20,
    "balances": {
      "current": "10444",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:06.233Z",
  "updated": "2020-05-22T08:07:06.304Z",
  "id": "5ec7882a005df800101bc39e"
}
```
* *stageAmount*: `10444`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000028cc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000028cc00000000000000000000000000000000000000000000000000000000000028ccf66434030c28fa9ee13ad24b9b4f984f149895944c82d8a1aae6d7e9ba51930491bab00113af081ca79cad8b9dad42f9f0562400281d06acbad121c15425c6244223e546200b8da10e7a14afd65ec56b7cfdad56d3cc8e8598c2aa548a71d0be000000000000000000000000000000000000000000000000000000000000001c2aea4ca1c2788ef4e4f891bd61a7ca617b2c5c0ddc479f69c3e9da4d041b1d5b755d563747db1d3f9c6f6228b3dcd452f03b6ce829d8c459a9a1736f5e3dff3e62901d6ca74241b23e4432995ee1b6b46e774b9df12d095ce1a10111429b7a6d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000047c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c820a1e0000000000000000000000000000000000000000000000000002386f2c820cab600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092bb200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a6d517a4f4467355969316d5a6a59774c5455324f4467744f546468596930775a6a52684e4745344f5745324d44416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000fb904394a2ad887046dac4791c20c1e9d3367aa100000000000000000000000000000000000000000000000000000000000028cc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf66434030c28fa9ee13ad24b9b4f984f149895944c82d8a1aae6d7e9ba519304",
      "signature": {
        "s": "0x4223e546200b8da10e7a14afd65ec56b7cfdad56d3cc8e8598c2aa548a71d0be",
        "r": "0x91bab00113af081ca79cad8b9dad42f9f0562400281d06acbad121c15425c624",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2aea4ca1c2788ef4e4f891bd61a7ca617b2c5c0ddc479f69c3e9da4d041b1d5b",
      "signature": {
        "s": "0x62901d6ca74241b23e4432995ee1b6b46e774b9df12d095ce1a10111429b7a6d",
        "r": "0x755d563747db1d3f9c6f6228b3dcd452f03b6ce829d8c459a9a1736f5e3dff3e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10444",
    "total": "10444"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10444",
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
            "amount": "601010"
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
    "data": "eyJyZWYiOiJkZmQzODg5Yi1mZjYwLTU2ODgtOTdhYi0wZjRhNGE4OWE2MDAifQ==",
    "nonce": 1148,
    "balances": {
      "current": "10000001482662368",
      "previous": "10000001482672822"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfb904394a2ad887046dac4791c20c1e9d3367aa1",
    "nonce": 20,
    "balances": {
      "current": "10444",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:06.233Z",
  "updated": "2020-05-22T08:07:06.304Z",
  "id": "5ec7882a005df800101bc39e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000028cc0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10444`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``