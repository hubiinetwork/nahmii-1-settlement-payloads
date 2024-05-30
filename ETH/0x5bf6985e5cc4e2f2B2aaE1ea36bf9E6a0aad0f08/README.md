# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5bf6985e5cc4e2f2B2aaE1ea36bf9E6a0aad0f08`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000004b891e00000000000000000000000000000000000000000000000000000000004b891e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004b891e00000000000000000000000000000000000000000000000000000000004b891ecee71022f15e3a79b9b16485616baab68142f126e1714a6da4b720c380650560e69d7f9c25879085432d45218af94159bc90b7e5d7bdd67333cc78b577e5f8773f9a97e42a1fadd522217a2f117a406dbccaf841e5c8e2ae761c74e0db230b16000000000000000000000000000000000000000000000000000000000000001c3ab3ccdcca82a0380fec8ad9875250323717369ef421a11d09481196873a66952a05cce3cbf3f9b696f41e74841a501226ad4f313e27e6aec8f80bfb85b38c362ab15c88c79a094aacefcb37af30bf86f1135a98576f6ff43566306216080b05000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000c300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d046582e000000000000000000000000000000000000000000000000002386f2d091f4a200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000135600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007174900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493459575a6c59544d334d5330325a444a6a4c54557a5a5441744f4755774d7930794d4751344d324668593259355a54516966513d3d00000000000000000000000000000000000000000000000000000000000000180000000000000000000000005bf6985e5cc4e2f2b2aae1ea36bf9e6a0aad0f0800000000000000000000000000000000000000000000000000000000004b891e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcee71022f15e3a79b9b16485616baab68142f126e1714a6da4b720c380650560",
      "signature": {
        "s": "0x3f9a97e42a1fadd522217a2f117a406dbccaf841e5c8e2ae761c74e0db230b16",
        "r": "0xe69d7f9c25879085432d45218af94159bc90b7e5d7bdd67333cc78b577e5f877",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3ab3ccdcca82a0380fec8ad9875250323717369ef421a11d09481196873a6695",
      "signature": {
        "s": "0x2ab15c88c79a094aacefcb37af30bf86f1135a98576f6ff43566306216080b05",
        "r": "0x2a05cce3cbf3f9b696f41e74841a501226ad4f313e27e6aec8f80bfb85b38c36",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4950302",
    "total": "4950302"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4950302",
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
            "amount": "464713"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4950"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YWZlYTM3MS02ZDJjLTUzZTAtOGUwMy0yMGQ4M2FhY2Y5ZTQifQ==",
    "nonce": 195,
    "balances": {
      "current": "10000001619351598",
      "previous": "10000001624306850"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bf6985e5cc4e2f2b2aae1ea36bf9e6a0aad0f08",
    "nonce": 24,
    "balances": {
      "current": "4950302",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:18.798Z",
  "updated": "2020-05-22T08:00:18.864Z",
  "id": "5ec78692b0c6090011d5a915"
}
```
* *stageAmount*: `4950302`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000004b891e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004b891e00000000000000000000000000000000000000000000000000000000004b891ecee71022f15e3a79b9b16485616baab68142f126e1714a6da4b720c380650560e69d7f9c25879085432d45218af94159bc90b7e5d7bdd67333cc78b577e5f8773f9a97e42a1fadd522217a2f117a406dbccaf841e5c8e2ae761c74e0db230b16000000000000000000000000000000000000000000000000000000000000001c3ab3ccdcca82a0380fec8ad9875250323717369ef421a11d09481196873a66952a05cce3cbf3f9b696f41e74841a501226ad4f313e27e6aec8f80bfb85b38c362ab15c88c79a094aacefcb37af30bf86f1135a98576f6ff43566306216080b05000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000c300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d046582e000000000000000000000000000000000000000000000000002386f2d091f4a200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000135600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007174900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493459575a6c59544d334d5330325a444a6a4c54557a5a5441744f4755774d7930794d4751344d324668593259355a54516966513d3d00000000000000000000000000000000000000000000000000000000000000180000000000000000000000005bf6985e5cc4e2f2b2aae1ea36bf9e6a0aad0f0800000000000000000000000000000000000000000000000000000000004b891e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcee71022f15e3a79b9b16485616baab68142f126e1714a6da4b720c380650560",
      "signature": {
        "s": "0x3f9a97e42a1fadd522217a2f117a406dbccaf841e5c8e2ae761c74e0db230b16",
        "r": "0xe69d7f9c25879085432d45218af94159bc90b7e5d7bdd67333cc78b577e5f877",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3ab3ccdcca82a0380fec8ad9875250323717369ef421a11d09481196873a6695",
      "signature": {
        "s": "0x2ab15c88c79a094aacefcb37af30bf86f1135a98576f6ff43566306216080b05",
        "r": "0x2a05cce3cbf3f9b696f41e74841a501226ad4f313e27e6aec8f80bfb85b38c36",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4950302",
    "total": "4950302"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4950302",
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
            "amount": "464713"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4950"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4YWZlYTM3MS02ZDJjLTUzZTAtOGUwMy0yMGQ4M2FhY2Y5ZTQifQ==",
    "nonce": 195,
    "balances": {
      "current": "10000001619351598",
      "previous": "10000001624306850"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bf6985e5cc4e2f2b2aae1ea36bf9e6a0aad0f08",
    "nonce": 24,
    "balances": {
      "current": "4950302",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:18.798Z",
  "updated": "2020-05-22T08:00:18.864Z",
  "id": "5ec78692b0c6090011d5a915"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000004b891e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4950302`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``