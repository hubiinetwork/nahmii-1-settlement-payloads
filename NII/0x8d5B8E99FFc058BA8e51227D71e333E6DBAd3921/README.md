# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8d5B8E99FFc058BA8e51227D71e333E6DBAd3921`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000985dc33617965355c00000000000000000000000000000000000000000000000039cc853cb3e5fb4f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000039cc853cb3e5fb4f00000000000000000000000000000000000000000000000655e4c025c8d35bda5f437d896b4d367e945d15c733b6a1880e3fd69cacb9dc556519a55a072639f66b018ca7adc61a69b8e4eb5444cb0287c0c627af5bdee764a36d132c64e768223ac67f19488195ca0cc34a34c897e55b9e0f02c482e0820eb628902c6140ae0a000000000000000000000000000000000000000000000000000000000000001c0797c502f5d2b02db0f72373e33586011c90c7b86b7552bbb651220d6a7945482fb1827d45d4aef82419b3f8f60ed81839485a5b069a033bc803cb74a79ec2062ae64eef5464253fcd3bb94b56f1d1f4c4475a779922187cabbb57af05699c37000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afe4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000005184aef50a3358165b88000000000000000000000000000000000000000000005184e8d05b58cfbfe5ae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000ecbe8c3c38ed70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d788f252a53b4267700000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e6a426d4d444d794d4331694d7a6b774c5455304d5441744f5745344e4330314d54497a5a5464694d325a6d5a574d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008d5b8e99ffc058ba8e51227d71e333e6dbad392100000000000000000000000000000000000000000000000985dc33617965355c0000000000000000000000000000000000000000000000094c0fae24c57f3a0d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5f437d896b4d367e945d15c733b6a1880e3fd69cacb9dc556519a55a072639f6",
      "signature": {
        "s": "0x3ac67f19488195ca0cc34a34c897e55b9e0f02c482e0820eb628902c6140ae0a",
        "r": "0x6b018ca7adc61a69b8e4eb5444cb0287c0c627af5bdee764a36d132c64e76822",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0797c502f5d2b02db0f72373e33586011c90c7b86b7552bbb651220d6a794548",
      "signature": {
        "s": "0x2ae64eef5464253fcd3bb94b56f1d1f4c4475a779922187cabbb57af05699c37",
        "r": "0x2fb1827d45d4aef82419b3f8f60ed81839485a5b069a033bc803cb74a79ec206",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4164850251173591887",
    "total": "116869747498686831578"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4164850251173591887",
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
            "amount": "27587750430798919133040"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4164850251173591"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3NjBmMDMyMC1iMzkwLTU0MTAtOWE4NC01MTIzZTdiM2ZmZWMifQ==",
    "nonce": 110564,
    "balances": {
      "current": "384959262324118454164360",
      "previous": "384963431339219878929838"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8d5b8e99ffc058ba8e51227d71e333e6dbad3921",
    "nonce": 46,
    "balances": {
      "current": "175666337659048244572",
      "previous": "171501487407874652685"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:55.239Z",
  "updated": "2022-05-04T08:53:55.339Z",
  "id": "62723f233592fd001130b4ff"
}
```
* *stageAmount*: `175666337659048244572`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000039cc853cb3e5fb4f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000039cc853cb3e5fb4f00000000000000000000000000000000000000000000000655e4c025c8d35bda5f437d896b4d367e945d15c733b6a1880e3fd69cacb9dc556519a55a072639f66b018ca7adc61a69b8e4eb5444cb0287c0c627af5bdee764a36d132c64e768223ac67f19488195ca0cc34a34c897e55b9e0f02c482e0820eb628902c6140ae0a000000000000000000000000000000000000000000000000000000000000001c0797c502f5d2b02db0f72373e33586011c90c7b86b7552bbb651220d6a7945482fb1827d45d4aef82419b3f8f60ed81839485a5b069a033bc803cb74a79ec2062ae64eef5464253fcd3bb94b56f1d1f4c4475a779922187cabbb57af05699c37000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afe4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000005184aef50a3358165b88000000000000000000000000000000000000000000005184e8d05b58cfbfe5ae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000ecbe8c3c38ed70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d788f252a53b4267700000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e6a426d4d444d794d4331694d7a6b774c5455304d5441744f5745344e4330314d54497a5a5464694d325a6d5a574d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008d5b8e99ffc058ba8e51227d71e333e6dbad392100000000000000000000000000000000000000000000000985dc33617965355c0000000000000000000000000000000000000000000000094c0fae24c57f3a0d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5f437d896b4d367e945d15c733b6a1880e3fd69cacb9dc556519a55a072639f6",
      "signature": {
        "s": "0x3ac67f19488195ca0cc34a34c897e55b9e0f02c482e0820eb628902c6140ae0a",
        "r": "0x6b018ca7adc61a69b8e4eb5444cb0287c0c627af5bdee764a36d132c64e76822",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0797c502f5d2b02db0f72373e33586011c90c7b86b7552bbb651220d6a794548",
      "signature": {
        "s": "0x2ae64eef5464253fcd3bb94b56f1d1f4c4475a779922187cabbb57af05699c37",
        "r": "0x2fb1827d45d4aef82419b3f8f60ed81839485a5b069a033bc803cb74a79ec206",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4164850251173591887",
    "total": "116869747498686831578"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4164850251173591887",
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
            "amount": "27587750430798919133040"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4164850251173591"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3NjBmMDMyMC1iMzkwLTU0MTAtOWE4NC01MTIzZTdiM2ZmZWMifQ==",
    "nonce": 110564,
    "balances": {
      "current": "384959262324118454164360",
      "previous": "384963431339219878929838"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8d5b8e99ffc058ba8e51227d71e333e6dbad3921",
    "nonce": 46,
    "balances": {
      "current": "175666337659048244572",
      "previous": "171501487407874652685"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:55.239Z",
  "updated": "2022-05-04T08:53:55.339Z",
  "id": "62723f233592fd001130b4ff"
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
0x0f200f9b00000000000000000000000000000000000000000000000985dc33617965355c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `175666337659048244572`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`