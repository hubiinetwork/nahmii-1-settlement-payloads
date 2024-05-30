# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe82846429b6295dBb4bA548a7c21B988C651090B`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000488e2c1fa0504dc948000000000000000000000000000000000000000000000001b85f64daafe145f70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001b85f64daafe145f70000000000000000000000000000000000000000000000304548c42c0f8dd094e9d39f54f2467323c0e856b78c5b41cc549096d3f63152efb5b40a2beb7f3b684a5a405b454101af8e3472cdc01900d16bce1061a1f067e18b09ab2cb9bcc6ca4f5499efda6e0ab548d5fe71d580b10ce6b288d510baa233eca308eb6f4aeed1000000000000000000000000000000000000000000000000000000000000001bdae87289836825615eee33ac5a0a52e4aa76186aeccca730bfcf38ca2bc9ec8e0709931c2790c4c356bb53a4dade726bac5d58a83802f433643491810b03ff83678120bd54945cb0dc045f80597c158a30f4383808f0835f066bb53c00af737d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b715000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002f5dafbdde8f2707f948000000000000000000000000000000000000000000002f5f688dffac9e4147c300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000070bc42c75808840000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e044eaf61c0f9379a10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d57526c4e444a6a4e6931694f446c694c54566d4f444d74596a6b794e7930774e6a4131595451344d6a51784d54416966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e82846429b6295dbb4ba548a7c21b988c651090b0000000000000000000000000000000000000000000000488e2c1fa0504dc948000000000000000000000000000000000000000000000046d5ccbac5a06c835100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe9d39f54f2467323c0e856b78c5b41cc549096d3f63152efb5b40a2beb7f3b68",
      "signature": {
        "s": "0x4f5499efda6e0ab548d5fe71d580b10ce6b288d510baa233eca308eb6f4aeed1",
        "r": "0x4a5a405b454101af8e3472cdc01900d16bce1061a1f067e18b09ab2cb9bcc6ca",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xdae87289836825615eee33ac5a0a52e4aa76186aeccca730bfcf38ca2bc9ec8e",
      "signature": {
        "s": "0x678120bd54945cb0dc045f80597c158a30f4383808f0835f066bb53c00af737d",
        "r": "0x0709931c2790c4c356bb53a4dade726bac5d58a83802f433643491810b03ff83",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "31732192389892228599",
    "total": "890436171418517229716"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31732192389892228599",
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
            "amount": "27748869138998675863969"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31732192389892228"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMWRlNDJjNi1iODliLTVmODMtYjkyNy0wNjA1YTQ4MjQxMTAifQ==",
    "nonce": 112405,
    "balances": {
      "current": "223679435416161965570376",
      "previous": "223711199340744247691203"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe82846429b6295dbb4ba548a7c21b988c651090b",
    "nonce": 46,
    "balances": {
      "current": "1338410171332851255624",
      "previous": "1306677978942959027025"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:37.643Z",
  "updated": "2022-05-04T09:03:37.731Z",
  "id": "627241697832e20011830e46"
}
```
* *stageAmount*: `1338410171332851255624`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001b85f64daafe145f70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001b85f64daafe145f70000000000000000000000000000000000000000000000304548c42c0f8dd094e9d39f54f2467323c0e856b78c5b41cc549096d3f63152efb5b40a2beb7f3b684a5a405b454101af8e3472cdc01900d16bce1061a1f067e18b09ab2cb9bcc6ca4f5499efda6e0ab548d5fe71d580b10ce6b288d510baa233eca308eb6f4aeed1000000000000000000000000000000000000000000000000000000000000001bdae87289836825615eee33ac5a0a52e4aa76186aeccca730bfcf38ca2bc9ec8e0709931c2790c4c356bb53a4dade726bac5d58a83802f433643491810b03ff83678120bd54945cb0dc045f80597c158a30f4383808f0835f066bb53c00af737d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b715000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002f5dafbdde8f2707f948000000000000000000000000000000000000000000002f5f688dffac9e4147c300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000070bc42c75808840000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e044eaf61c0f9379a10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d57526c4e444a6a4e6931694f446c694c54566d4f444d74596a6b794e7930774e6a4131595451344d6a51784d54416966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e82846429b6295dbb4ba548a7c21b988c651090b0000000000000000000000000000000000000000000000488e2c1fa0504dc948000000000000000000000000000000000000000000000046d5ccbac5a06c835100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe9d39f54f2467323c0e856b78c5b41cc549096d3f63152efb5b40a2beb7f3b68",
      "signature": {
        "s": "0x4f5499efda6e0ab548d5fe71d580b10ce6b288d510baa233eca308eb6f4aeed1",
        "r": "0x4a5a405b454101af8e3472cdc01900d16bce1061a1f067e18b09ab2cb9bcc6ca",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xdae87289836825615eee33ac5a0a52e4aa76186aeccca730bfcf38ca2bc9ec8e",
      "signature": {
        "s": "0x678120bd54945cb0dc045f80597c158a30f4383808f0835f066bb53c00af737d",
        "r": "0x0709931c2790c4c356bb53a4dade726bac5d58a83802f433643491810b03ff83",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "31732192389892228599",
    "total": "890436171418517229716"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31732192389892228599",
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
            "amount": "27748869138998675863969"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31732192389892228"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMWRlNDJjNi1iODliLTVmODMtYjkyNy0wNjA1YTQ4MjQxMTAifQ==",
    "nonce": 112405,
    "balances": {
      "current": "223679435416161965570376",
      "previous": "223711199340744247691203"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe82846429b6295dbb4ba548a7c21b988c651090b",
    "nonce": 46,
    "balances": {
      "current": "1338410171332851255624",
      "previous": "1306677978942959027025"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:37.643Z",
  "updated": "2022-05-04T09:03:37.731Z",
  "id": "627241697832e20011830e46"
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
0x0f200f9b0000000000000000000000000000000000000000000000488e2c1fa0504dc9480000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1338410171332851255624`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`