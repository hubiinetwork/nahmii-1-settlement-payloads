# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa955d4ee192F65E3b77dE1A10c46795EC7905714`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002447161188a55b5d14000000000000000000000000000000000000000000000000dc2fb26d57f3323b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f3323b00000000000000000000000000000000000000000000001822a46216080ab78e40feec4dce996e759f7eeba8ba032f2569520e2ab3c975818a57b3ffa23fd7cb887d179441999c374d6ba4921d5a210942fd5ac75844074fd1d06f3a80cbbb64704b06d1167643435648d98214e312d2580fa9d5ad5eaf4384aa2562a42ad4ab000000000000000000000000000000000000000000000000000000000000001b0805ff17c3e12428060035c64df98e09421b1ff5425d485132b831898aad3fc365b2faf8d92de9e93c3bfaf20dd8fff086f0f5ccd49570012b746fec6df610e1041d383ab83ce26d739bcc0d8d6538491331326fd6b65d18753d5081cfbb3616000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6af000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030267e8ebc2734a11a090000000000000000000000000000000000000000000030275af6ccb5f040512e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac04ea0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0118ff6a7cd11a91e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f5441794e7a51354d53316b4d7a4a694c5455305a5745744f4456694d43307a4e47466b4d3251355a54637a4e6a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a955d4ee192f65e3b77de1a10c46795ec790571400000000000000000000000000000000000000000000002447161188a55b5d140000000000000000000000000000000000000000000000236ae65f1b4d682ad900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x40feec4dce996e759f7eeba8ba032f2569520e2ab3c975818a57b3ffa23fd7cb",
      "signature": {
        "s": "0x704b06d1167643435648d98214e312d2580fa9d5ad5eaf4384aa2562a42ad4ab",
        "r": "0x887d179441999c374d6ba4921d5a210942fd5ac75844074fd1d06f3a80cbbb64",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0805ff17c3e12428060035c64df98e09421b1ff5425d485132b831898aad3fc3",
      "signature": {
        "s": "0x041d383ab83ce26d739bcc0d8d6538491331326fd6b65d18753d5081cfbb3616",
        "r": "0x65b2faf8d92de9e93c3bfaf20dd8fff086f0f5ccd49570012b746fec6df610e1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15866096194946282043",
    "total": "445218085709263058830"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946282043",
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
            "amount": "27745168588080040487198"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946282"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiOTAyNzQ5MS1kMzJiLTU0ZWEtODViMC0zNGFkM2Q5ZTczNjcifQ==",
    "nonce": 112303,
    "balances": {
      "current": "227383686885715977771529",
      "previous": "227399568848007118999854"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa955d4ee192f65e3b77de1a10c46795ec7905714",
    "nonce": 46,
    "balances": {
      "current": "669205087558311828756",
      "previous": "653338991363365546713"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:03:03.502Z",
  "updated": "2022-05-04T09:03:03.578Z",
  "id": "627241477832e20011830e23"
}
```
* *stageAmount*: `669205087558311828756`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000dc2fb26d57f3323b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f3323b00000000000000000000000000000000000000000000001822a46216080ab78e40feec4dce996e759f7eeba8ba032f2569520e2ab3c975818a57b3ffa23fd7cb887d179441999c374d6ba4921d5a210942fd5ac75844074fd1d06f3a80cbbb64704b06d1167643435648d98214e312d2580fa9d5ad5eaf4384aa2562a42ad4ab000000000000000000000000000000000000000000000000000000000000001b0805ff17c3e12428060035c64df98e09421b1ff5425d485132b831898aad3fc365b2faf8d92de9e93c3bfaf20dd8fff086f0f5ccd49570012b746fec6df610e1041d383ab83ce26d739bcc0d8d6538491331326fd6b65d18753d5081cfbb3616000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6af000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030267e8ebc2734a11a090000000000000000000000000000000000000000000030275af6ccb5f040512e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac04ea0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0118ff6a7cd11a91e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f5441794e7a51354d53316b4d7a4a694c5455305a5745744f4456694d43307a4e47466b4d3251355a54637a4e6a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a955d4ee192f65e3b77de1a10c46795ec790571400000000000000000000000000000000000000000000002447161188a55b5d140000000000000000000000000000000000000000000000236ae65f1b4d682ad900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x40feec4dce996e759f7eeba8ba032f2569520e2ab3c975818a57b3ffa23fd7cb",
      "signature": {
        "s": "0x704b06d1167643435648d98214e312d2580fa9d5ad5eaf4384aa2562a42ad4ab",
        "r": "0x887d179441999c374d6ba4921d5a210942fd5ac75844074fd1d06f3a80cbbb64",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0805ff17c3e12428060035c64df98e09421b1ff5425d485132b831898aad3fc3",
      "signature": {
        "s": "0x041d383ab83ce26d739bcc0d8d6538491331326fd6b65d18753d5081cfbb3616",
        "r": "0x65b2faf8d92de9e93c3bfaf20dd8fff086f0f5ccd49570012b746fec6df610e1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15866096194946282043",
    "total": "445218085709263058830"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946282043",
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
            "amount": "27745168588080040487198"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946282"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiOTAyNzQ5MS1kMzJiLTU0ZWEtODViMC0zNGFkM2Q5ZTczNjcifQ==",
    "nonce": 112303,
    "balances": {
      "current": "227383686885715977771529",
      "previous": "227399568848007118999854"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa955d4ee192f65e3b77de1a10c46795ec7905714",
    "nonce": 46,
    "balances": {
      "current": "669205087558311828756",
      "previous": "653338991363365546713"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:03:03.502Z",
  "updated": "2022-05-04T09:03:03.578Z",
  "id": "627241477832e20011830e23"
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
0x0f200f9b00000000000000000000000000000000000000000000002447161188a55b5d140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669205087558311828756`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`