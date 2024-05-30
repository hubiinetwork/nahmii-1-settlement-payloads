# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb3bC37A32F0b5413254f1315Efb7a93688166114`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b2800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b28ebf1e4185cbb4f6f2702aafd008239bdee6c808af3c8059a9c84f89ac10523b2bf4b9f9c1c3a14aa342a93041c897361a7913da24851cf4b2bed95547b76b5887c9159238c85aa9fee1f770159e083dc900692298b179f940c4a1ba4ddbc257b000000000000000000000000000000000000000000000000000000000000001bfb42b46b7f20dbd1d3eda5fe8a09fa9abb5e5cac52dc0bdda32a096371d4f27e2e62cf317679e987bd0025e5d57d38aa7ffa3b41ae574595dfc73f31c89c9dcb5455c96f52a4d174f2ba43e1a4197cab1c090ae65be464347daa4f59b6949b86000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000029200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb023257000000000000000000000000000000000000000000000000002386f2cb027d9200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000013000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086f9200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d57466c4d5456684e5330774e3251324c545579596a637459544d354e69303159575532596d4e6c4d3259334e6d496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b3bc37a32f0b5413254f1315efb7a936881661140000000000000000000000000000000000000000000000000000000000004b28000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xebf1e4185cbb4f6f2702aafd008239bdee6c808af3c8059a9c84f89ac10523b2",
      "signature": {
        "s": "0x7c9159238c85aa9fee1f770159e083dc900692298b179f940c4a1ba4ddbc257b",
        "r": "0xbf4b9f9c1c3a14aa342a93041c897361a7913da24851cf4b2bed95547b76b588",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfb42b46b7f20dbd1d3eda5fe8a09fa9abb5e5cac52dc0bdda32a096371d4f27e",
      "signature": {
        "s": "0x5455c96f52a4d174f2ba43e1a4197cab1c090ae65be464347daa4f59b6949b86",
        "r": "0x2e62cf317679e987bd0025e5d57d38aa7ffa3b41ae574595dfc73f31c89c9dcb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19240",
    "total": "19240"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19240",
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
            "amount": "552850"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMWFlMTVhNS0wN2Q2LTUyYjctYTM5Ni01YWU2YmNlM2Y3NmIifQ==",
    "nonce": 658,
    "balances": {
      "current": "10000001530999383",
      "previous": "10000001531018642"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3bc37a32f0b5413254f1315efb7a93688166114",
    "nonce": 20,
    "balances": {
      "current": "19240",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:49.352Z",
  "updated": "2020-05-22T08:03:49.432Z",
  "id": "5ec78765b0c6090011d5a9ab"
}
```
* *stageAmount*: `19240`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004b2800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b28ebf1e4185cbb4f6f2702aafd008239bdee6c808af3c8059a9c84f89ac10523b2bf4b9f9c1c3a14aa342a93041c897361a7913da24851cf4b2bed95547b76b5887c9159238c85aa9fee1f770159e083dc900692298b179f940c4a1ba4ddbc257b000000000000000000000000000000000000000000000000000000000000001bfb42b46b7f20dbd1d3eda5fe8a09fa9abb5e5cac52dc0bdda32a096371d4f27e2e62cf317679e987bd0025e5d57d38aa7ffa3b41ae574595dfc73f31c89c9dcb5455c96f52a4d174f2ba43e1a4197cab1c090ae65be464347daa4f59b6949b86000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000029200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb023257000000000000000000000000000000000000000000000000002386f2cb027d9200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000013000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086f9200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d57466c4d5456684e5330774e3251324c545579596a637459544d354e69303159575532596d4e6c4d3259334e6d496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b3bc37a32f0b5413254f1315efb7a936881661140000000000000000000000000000000000000000000000000000000000004b28000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xebf1e4185cbb4f6f2702aafd008239bdee6c808af3c8059a9c84f89ac10523b2",
      "signature": {
        "s": "0x7c9159238c85aa9fee1f770159e083dc900692298b179f940c4a1ba4ddbc257b",
        "r": "0xbf4b9f9c1c3a14aa342a93041c897361a7913da24851cf4b2bed95547b76b588",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfb42b46b7f20dbd1d3eda5fe8a09fa9abb5e5cac52dc0bdda32a096371d4f27e",
      "signature": {
        "s": "0x5455c96f52a4d174f2ba43e1a4197cab1c090ae65be464347daa4f59b6949b86",
        "r": "0x2e62cf317679e987bd0025e5d57d38aa7ffa3b41ae574595dfc73f31c89c9dcb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19240",
    "total": "19240"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19240",
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
            "amount": "552850"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMWFlMTVhNS0wN2Q2LTUyYjctYTM5Ni01YWU2YmNlM2Y3NmIifQ==",
    "nonce": 658,
    "balances": {
      "current": "10000001530999383",
      "previous": "10000001531018642"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3bc37a32f0b5413254f1315efb7a93688166114",
    "nonce": 20,
    "balances": {
      "current": "19240",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:49.352Z",
  "updated": "2020-05-22T08:03:49.432Z",
  "id": "5ec78765b0c6090011d5a9ab"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `19240`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``