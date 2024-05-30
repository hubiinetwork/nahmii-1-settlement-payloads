# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3f845aA152497fDC41C18c6de0F4578D213Bd4D2`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000620cfd0000000000000000000000000000000000000000000000000000000000620cfd0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000620cfd0000000000000000000000000000000000000000000000000000000000620cfd00f642485c7ab23feba7e6b2e86d741922379db9581c7a0b28a200e07de3208da1fc4f53e00c879af989aa7f16ce7a76cf3baf181bb24dabaff8194f016827a00144be081ad4ef392fff9f0f6f796ef8b242be667625a1c0b7b34483a0d759383000000000000000000000000000000000000000000000000000000000000001b563aefbf347025fb1ed5c8602ca59291a97f2a249d368a7827a67807a42397ef80b96f660b7133b043bf5db3ed896d5810615b69bd75b9bde0ddc94b8032490c71ba5298a494a205d22740f78037f9c2f7cdd472b8c4b1fed68250c83766c881000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d3d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b8840dec745000000000000000000000000000000000000000000000000002e0b88470128b200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000001919d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d4d6770fc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e6d4d7a4e324d784d4330784e545a6d4c5455335a5455744f445577597931684e57466d4e6a557959546b304d57556966513d3d000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000003f845aa152497fdc41c18c6de0f4578d213bd4d2000000000000000000000000000000000000000000000000000000000620cfd0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f642485c7ab23feba7e6b2e86d741922379db9581c7a0b28a200e07de3208da",
      "signature": {
        "s": "0x144be081ad4ef392fff9f0f6f796ef8b242be667625a1c0b7b34483a0d759383",
        "r": "0x1fc4f53e00c879af989aa7f16ce7a76cf3baf181bb24dabaff8194f016827a00",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x563aefbf347025fb1ed5c8602ca59291a97f2a249d368a7827a67807a42397ef",
      "signature": {
        "s": "0x71ba5298a494a205d22740f78037f9c2f7cdd472b8c4b1fed68250c83766c881",
        "r": "0x80b96f660b7133b043bf5db3ed896d5810615b69bd75b9bde0ddc94b8032490c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "102813648",
    "total": "102813648"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "102813648",
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
            "amount": "57133199612"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "102813"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NmMzN2MxMC0xNTZmLTU3ZTUtODUwYy1hNWFmNjUyYTk0MWUifQ==",
    "nonce": 7485,
    "balances": {
      "current": "12960528760489797",
      "previous": "12960528863406258"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3f845aa152497fdc41c18c6de0f4578d213bd4d2",
    "nonce": 14,
    "balances": {
      "current": "102813648",
      "previous": "0"
    }
  },
  "blockNumber": "10114741",
  "created": "2020-05-22T08:57:10.134Z",
  "updated": "2020-05-22T08:57:10.191Z",
  "id": "5ec793e6b0c6090011d5b294"
}
```
* *stageAmount*: `102813648`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000620cfd0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000620cfd0000000000000000000000000000000000000000000000000000000000620cfd00f642485c7ab23feba7e6b2e86d741922379db9581c7a0b28a200e07de3208da1fc4f53e00c879af989aa7f16ce7a76cf3baf181bb24dabaff8194f016827a00144be081ad4ef392fff9f0f6f796ef8b242be667625a1c0b7b34483a0d759383000000000000000000000000000000000000000000000000000000000000001b563aefbf347025fb1ed5c8602ca59291a97f2a249d368a7827a67807a42397ef80b96f660b7133b043bf5db3ed896d5810615b69bd75b9bde0ddc94b8032490c71ba5298a494a205d22740f78037f9c2f7cdd472b8c4b1fed68250c83766c881000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d3d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b8840dec745000000000000000000000000000000000000000000000000002e0b88470128b200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000001919d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d4d6770fc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e6d4d7a4e324d784d4330784e545a6d4c5455335a5455744f445577597931684e57466d4e6a557959546b304d57556966513d3d000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000003f845aa152497fdc41c18c6de0f4578d213bd4d2000000000000000000000000000000000000000000000000000000000620cfd0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0f642485c7ab23feba7e6b2e86d741922379db9581c7a0b28a200e07de3208da",
      "signature": {
        "s": "0x144be081ad4ef392fff9f0f6f796ef8b242be667625a1c0b7b34483a0d759383",
        "r": "0x1fc4f53e00c879af989aa7f16ce7a76cf3baf181bb24dabaff8194f016827a00",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x563aefbf347025fb1ed5c8602ca59291a97f2a249d368a7827a67807a42397ef",
      "signature": {
        "s": "0x71ba5298a494a205d22740f78037f9c2f7cdd472b8c4b1fed68250c83766c881",
        "r": "0x80b96f660b7133b043bf5db3ed896d5810615b69bd75b9bde0ddc94b8032490c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "102813648",
    "total": "102813648"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "102813648",
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
            "amount": "57133199612"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "102813"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NmMzN2MxMC0xNTZmLTU3ZTUtODUwYy1hNWFmNjUyYTk0MWUifQ==",
    "nonce": 7485,
    "balances": {
      "current": "12960528760489797",
      "previous": "12960528863406258"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3f845aa152497fdc41c18c6de0f4578d213bd4d2",
    "nonce": 14,
    "balances": {
      "current": "102813648",
      "previous": "0"
    }
  },
  "blockNumber": "10114741",
  "created": "2020-05-22T08:57:10.134Z",
  "updated": "2020-05-22T08:57:10.191Z",
  "id": "5ec793e6b0c6090011d5b294"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000620cfd0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `102813648`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`