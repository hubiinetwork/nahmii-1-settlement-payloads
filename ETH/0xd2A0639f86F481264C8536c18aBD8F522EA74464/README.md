# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd2A0639f86F481264C8536c18aBD8F522EA74464`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000e500000000000000000000000000000000000000000000000000000000000000e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000e500000000000000000000000000000000000000000000000000000000000000e5053112d7bb338c33e6a4e5d76fee2c595e144157af2ddbc66f214c3f367f9a501b567ef1c0e1031ab34e7a39ad51b756019cec4a0631853fff9c7c8c90e8a43b76b4cdf8e239d2df1724fa0e20fbc7b15998563d5904e6b47fb8f45856f4585ab000000000000000000000000000000000000000000000000000000000000001bf125d459ac8bc3796a49b2519526d534df46e49c063415220598b52678ad4e996ba68e3d7b76df489e644fbe43bda158ac483e47531016c4ca3d0d63f6ed41c20775714dedf60b08ad6af828f27954fd65f9854ff729e8e9634c09925eb061bb000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000056300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7316f59000000000000000000000000000000000000000000000000002386f2c7317dac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009689100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6a566b4e5446684e6930314e324d784c5455775a4451744f57526b5a5330314f5745344d4759784d6a6b324f57516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d2a0639f86f481264c8536c18abd8f522ea744640000000000000000000000000000000000000000000000000000000000000e50000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x53112d7bb338c33e6a4e5d76fee2c595e144157af2ddbc66f214c3f367f9a501",
      "signature": {
        "s": "0x6b4cdf8e239d2df1724fa0e20fbc7b15998563d5904e6b47fb8f45856f4585ab",
        "r": "0xb567ef1c0e1031ab34e7a39ad51b756019cec4a0631853fff9c7c8c90e8a43b7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf125d459ac8bc3796a49b2519526d534df46e49c063415220598b52678ad4e99",
      "signature": {
        "s": "0x0775714dedf60b08ad6af828f27954fd65f9854ff729e8e9634c09925eb061bb",
        "r": "0x6ba68e3d7b76df489e644fbe43bda158ac483e47531016c4ca3d0d63f6ed41c2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3664",
    "total": "3664"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3664",
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
            "amount": "616593"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MjVkNTFhNi01N2MxLTUwZDQtOWRkZS01OWE4MGYxMjk2OWQifQ==",
    "nonce": 1379,
    "balances": {
      "current": "10000001466986329",
      "previous": "10000001466989996"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd2a0639f86f481264c8536c18abd8f522ea74464",
    "nonce": 20,
    "balances": {
      "current": "3664",
      "previous": "0"
    }
  },
  "blockNumber": "10114528",
  "created": "2020-05-22T08:08:53.864Z",
  "updated": "2020-05-22T08:08:55.930Z",
  "id": "5ec78895b0c6090011d5aa9a"
}
```
* *stageAmount*: `3664`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000e500000000000000000000000000000000000000000000000000000000000000e5053112d7bb338c33e6a4e5d76fee2c595e144157af2ddbc66f214c3f367f9a501b567ef1c0e1031ab34e7a39ad51b756019cec4a0631853fff9c7c8c90e8a43b76b4cdf8e239d2df1724fa0e20fbc7b15998563d5904e6b47fb8f45856f4585ab000000000000000000000000000000000000000000000000000000000000001bf125d459ac8bc3796a49b2519526d534df46e49c063415220598b52678ad4e996ba68e3d7b76df489e644fbe43bda158ac483e47531016c4ca3d0d63f6ed41c20775714dedf60b08ad6af828f27954fd65f9854ff729e8e9634c09925eb061bb000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000056300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7316f59000000000000000000000000000000000000000000000000002386f2c7317dac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009689100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6a566b4e5446684e6930314e324d784c5455775a4451744f57526b5a5330314f5745344d4759784d6a6b324f57516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d2a0639f86f481264c8536c18abd8f522ea744640000000000000000000000000000000000000000000000000000000000000e50000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x53112d7bb338c33e6a4e5d76fee2c595e144157af2ddbc66f214c3f367f9a501",
      "signature": {
        "s": "0x6b4cdf8e239d2df1724fa0e20fbc7b15998563d5904e6b47fb8f45856f4585ab",
        "r": "0xb567ef1c0e1031ab34e7a39ad51b756019cec4a0631853fff9c7c8c90e8a43b7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf125d459ac8bc3796a49b2519526d534df46e49c063415220598b52678ad4e99",
      "signature": {
        "s": "0x0775714dedf60b08ad6af828f27954fd65f9854ff729e8e9634c09925eb061bb",
        "r": "0x6ba68e3d7b76df489e644fbe43bda158ac483e47531016c4ca3d0d63f6ed41c2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3664",
    "total": "3664"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3664",
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
            "amount": "616593"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MjVkNTFhNi01N2MxLTUwZDQtOWRkZS01OWE4MGYxMjk2OWQifQ==",
    "nonce": 1379,
    "balances": {
      "current": "10000001466986329",
      "previous": "10000001466989996"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd2a0639f86f481264c8536c18abd8f522ea74464",
    "nonce": 20,
    "balances": {
      "current": "3664",
      "previous": "0"
    }
  },
  "blockNumber": "10114528",
  "created": "2020-05-22T08:08:53.864Z",
  "updated": "2020-05-22T08:08:55.930Z",
  "id": "5ec78895b0c6090011d5aa9a"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000e500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3664`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``