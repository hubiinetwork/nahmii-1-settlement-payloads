# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8dF252dA894DB4aB205c1B4B8769Eec0522f49af`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000002b081c2bbf37a6b000000000000000000000000000000000000000000000000001f56798ce296af0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000001f56798ce296af000000000000000000000000000000000000000000000000029f5a596e72a708dc806c4faebba62909e6545dfed6f3967afa1c5eeb56b429be6f4c14ade80f1bd6452e592767f1f2710b02d5d271162410c152b635b63c90d41146f10d761c1a3e900f537b7b8e5104553e43a23b40cd2e8fd5c7526870fae31b65e018e89c46000000000000000000000000000000000000000000000000000000000000001c713e4bca50c0df54e6fedc8132463f60635d296930a89d7b9ff31f09475166c475105f6a93377bee59b3ae3c27a93a1f17ec8d7e53c90d1ff5c6c23cb45f717e5202833a6a671c0054e250c3e9c1cc4a800b4bb8843ac282184713af6afa91da000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3ef000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039f6619a85bdf443a5f70000000000000000000000000000000000000000000039f661b9e43d420ee95700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000805c0e8acb10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd8f2965f5658e90030000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979597a686a4e545a6a4e693168597a4a6a4c54566d59544174596d45344d5331694d3259334d6d5131597a41774f44516966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000008df252da894db4ab205c1b4b8769eec0522f49af00000000000000000000000000000000000000000000000002b081c2bbf37a6b00000000000000000000000000000000000000000000000002912b492f10e3bc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdc806c4faebba62909e6545dfed6f3967afa1c5eeb56b429be6f4c14ade80f1b",
      "signature": {
        "s": "0x3e900f537b7b8e5104553e43a23b40cd2e8fd5c7526870fae31b65e018e89c46",
        "r": "0xd6452e592767f1f2710b02d5d271162410c152b635b63c90d41146f10d761c1a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x713e4bca50c0df54e6fedc8132463f60635d296930a89d7b9ff31f09475166c4",
      "signature": {
        "s": "0x5202833a6a671c0054e250c3e9c1cc4a800b4bb8843ac282184713af6afa91da",
        "r": "0x75105f6a93377bee59b3ae3c27a93a1f17ec8d7e53c90d1ff5c6c23cb45f717e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8820804332721839",
    "total": "188969049524446984"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8820804332721839",
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
            "amount": "27698878743164151042051"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8820804332721"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyYzhjNTZjNi1hYzJjLTVmYTAtYmE4MS1iM2Y3MmQ1YzAwODQifQ==",
    "nonce": 111599,
    "balances": {
      "current": "273719821646521312716279",
      "previous": "273719830476146449770839"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8df252da894db4ab205c1b4b8769eec0522f49af",
    "nonce": 29,
    "balances": {
      "current": "193797457353865835",
      "previous": "184976653021143996"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:11.096Z",
  "updated": "2022-05-04T08:59:11.198Z",
  "id": "6272405f7832e20011830d3d"
}
```
* *stageAmount*: `193797457353865835`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000001f56798ce296af0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000001f56798ce296af000000000000000000000000000000000000000000000000029f5a596e72a708dc806c4faebba62909e6545dfed6f3967afa1c5eeb56b429be6f4c14ade80f1bd6452e592767f1f2710b02d5d271162410c152b635b63c90d41146f10d761c1a3e900f537b7b8e5104553e43a23b40cd2e8fd5c7526870fae31b65e018e89c46000000000000000000000000000000000000000000000000000000000000001c713e4bca50c0df54e6fedc8132463f60635d296930a89d7b9ff31f09475166c475105f6a93377bee59b3ae3c27a93a1f17ec8d7e53c90d1ff5c6c23cb45f717e5202833a6a671c0054e250c3e9c1cc4a800b4bb8843ac282184713af6afa91da000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3ef000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039f6619a85bdf443a5f70000000000000000000000000000000000000000000039f661b9e43d420ee95700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000805c0e8acb10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd8f2965f5658e90030000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694979597a686a4e545a6a4e693168597a4a6a4c54566d59544174596d45344d5331694d3259334d6d5131597a41774f44516966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000008df252da894db4ab205c1b4b8769eec0522f49af00000000000000000000000000000000000000000000000002b081c2bbf37a6b00000000000000000000000000000000000000000000000002912b492f10e3bc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdc806c4faebba62909e6545dfed6f3967afa1c5eeb56b429be6f4c14ade80f1b",
      "signature": {
        "s": "0x3e900f537b7b8e5104553e43a23b40cd2e8fd5c7526870fae31b65e018e89c46",
        "r": "0xd6452e592767f1f2710b02d5d271162410c152b635b63c90d41146f10d761c1a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x713e4bca50c0df54e6fedc8132463f60635d296930a89d7b9ff31f09475166c4",
      "signature": {
        "s": "0x5202833a6a671c0054e250c3e9c1cc4a800b4bb8843ac282184713af6afa91da",
        "r": "0x75105f6a93377bee59b3ae3c27a93a1f17ec8d7e53c90d1ff5c6c23cb45f717e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8820804332721839",
    "total": "188969049524446984"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8820804332721839",
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
            "amount": "27698878743164151042051"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8820804332721"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyYzhjNTZjNi1hYzJjLTVmYTAtYmE4MS1iM2Y3MmQ1YzAwODQifQ==",
    "nonce": 111599,
    "balances": {
      "current": "273719821646521312716279",
      "previous": "273719830476146449770839"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8df252da894db4ab205c1b4b8769eec0522f49af",
    "nonce": 29,
    "balances": {
      "current": "193797457353865835",
      "previous": "184976653021143996"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:11.096Z",
  "updated": "2022-05-04T08:59:11.198Z",
  "id": "6272405f7832e20011830d3d"
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
0x0f200f9b00000000000000000000000000000000000000000000000002b081c2bbf37a6b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `193797457353865835`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`