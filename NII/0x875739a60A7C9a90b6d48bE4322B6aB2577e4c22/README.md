# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x875739a60A7C9a90b6d48bE4322B6aB2577e4c22`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000155019a25bbda4b4870000000000000000000000000000000000000000000000000000000465b421110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000465b4211100000000000000000000000000000000000000000000000a62801b9e97b8f117df633c317cfe0bf07e76cda1f077a89117d8dc99745e5574b26447c23cb108c6f9deceb97467d166020002aac5ac064bc997bc07018e3a9ea0ac65ac773f4851001bf78292776deb6d51fc4b89f519f90c4d54e7be9346be8d8a32bcc2923142000000000000000000000000000000000000000000000000000000000000001c664d7cb133e56c9e8f6870555661aecc39e9fd8d8a2a0f8f0414f78d9e05da03a59817311def013be2fcbf6a7032259569e569362b7a88550ececa1473f7eb344fa1edf6fa5cca0d568c7dc130f576a6bf870da59045394b83ba7db33d317c8c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b255000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000490ac3b9aacb6708a4b500000000000000000000000000000000000000000000490ac3b9aacfcddcf3e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001202e1c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9b3e40f7ae1bbe42b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f545a6a4e5451325a533030593251304c54553359544d74596d4e6d4d79316d4d544d354d6a4669595455775a444d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000875739a60a7c9a90b6d48be4322b6ab2577e4c220000000000000000000000000000000000000000000000155019a25bbda4b4870000000000000000000000000000000000000000000000155019a25757f0937600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdf633c317cfe0bf07e76cda1f077a89117d8dc99745e5574b26447c23cb108c6",
      "signature": {
        "s": "0x001bf78292776deb6d51fc4b89f519f90c4d54e7be9346be8d8a32bcc2923142",
        "r": "0xf9deceb97467d166020002aac5ac064bc997bc07018e3a9ea0ac65ac773f4851",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x664d7cb133e56c9e8f6870555661aecc39e9fd8d8a2a0f8f0414f78d9e05da03",
      "signature": {
        "s": "0x4fa1edf6fa5cca0d568c7dc130f576a6bf870da59045394b83ba7db33d317c8c",
        "r": "0xa59817311def013be2fcbf6a7032259569e569362b7a88550ececa1473f7eb34",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18886172945",
    "total": "191565144117795680535"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18886172945",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27627738380991125513259"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "18886172"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlOTZjNTQ2ZS00Y2Q0LTU3YTMtYmNmMy1mMTM5MjFiYTUwZDMifQ==",
    "nonce": 111189,
    "balances": {
      "current": "344931324181719867237557",
      "previous": "344931324181738772296674"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x875739a60a7c9a90b6d48be4322b6ab2577e4c22",
    "nonce": 46,
    "balances": {
      "current": "393153448460259996807",
      "previous": "393153448441373823862"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:00.762Z",
  "updated": "2022-05-04T08:57:00.905Z",
  "id": "62723fdc3592fd001130b5d5"
}
```
* *stageAmount*: `393153448460259996807`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000465b421110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000465b4211100000000000000000000000000000000000000000000000a62801b9e97b8f117df633c317cfe0bf07e76cda1f077a89117d8dc99745e5574b26447c23cb108c6f9deceb97467d166020002aac5ac064bc997bc07018e3a9ea0ac65ac773f4851001bf78292776deb6d51fc4b89f519f90c4d54e7be9346be8d8a32bcc2923142000000000000000000000000000000000000000000000000000000000000001c664d7cb133e56c9e8f6870555661aecc39e9fd8d8a2a0f8f0414f78d9e05da03a59817311def013be2fcbf6a7032259569e569362b7a88550ececa1473f7eb344fa1edf6fa5cca0d568c7dc130f576a6bf870da59045394b83ba7db33d317c8c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b255000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000490ac3b9aacb6708a4b500000000000000000000000000000000000000000000490ac3b9aacfcddcf3e200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001202e1c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9b3e40f7ae1bbe42b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f545a6a4e5451325a533030593251304c54553359544d74596d4e6d4d79316d4d544d354d6a4669595455775a444d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000875739a60a7c9a90b6d48be4322b6ab2577e4c220000000000000000000000000000000000000000000000155019a25bbda4b4870000000000000000000000000000000000000000000000155019a25757f0937600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdf633c317cfe0bf07e76cda1f077a89117d8dc99745e5574b26447c23cb108c6",
      "signature": {
        "s": "0x001bf78292776deb6d51fc4b89f519f90c4d54e7be9346be8d8a32bcc2923142",
        "r": "0xf9deceb97467d166020002aac5ac064bc997bc07018e3a9ea0ac65ac773f4851",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x664d7cb133e56c9e8f6870555661aecc39e9fd8d8a2a0f8f0414f78d9e05da03",
      "signature": {
        "s": "0x4fa1edf6fa5cca0d568c7dc130f576a6bf870da59045394b83ba7db33d317c8c",
        "r": "0xa59817311def013be2fcbf6a7032259569e569362b7a88550ececa1473f7eb34",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18886172945",
    "total": "191565144117795680535"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18886172945",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27627738380991125513259"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "18886172"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlOTZjNTQ2ZS00Y2Q0LTU3YTMtYmNmMy1mMTM5MjFiYTUwZDMifQ==",
    "nonce": 111189,
    "balances": {
      "current": "344931324181719867237557",
      "previous": "344931324181738772296674"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x875739a60a7c9a90b6d48be4322b6ab2577e4c22",
    "nonce": 46,
    "balances": {
      "current": "393153448460259996807",
      "previous": "393153448441373823862"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:00.762Z",
  "updated": "2022-05-04T08:57:00.905Z",
  "id": "62723fdc3592fd001130b5d5"
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
0x0f200f9b0000000000000000000000000000000000000000000000155019a25bbda4b4870000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `393153448460259996807`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`