# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xff873Ec0a781F1925b878B1e2b8985DD51FDF7Aa`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000b6d6f16f35a8bc454000000000000000000000000000000000000000000000000455bd5d2db1ab80f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000455bd5d2db1ab80f0000000000000000000000000000000000000000000000079a46003d3fb19a784f600ff151dae20904e06b94c65c3f591be7f41046df88296ed4e2fdfd14f53a3ce52e670a0574734c2aae0e3c2b9d101566bf7fde23477d63844a36b7c3f9321b1f1a06f4ba5bc0e098ab60c0fc4aa8ef606f0e1e94d009bfa2dbe4c840ee0f000000000000000000000000000000000000000000000000000000000000001b4c5d396e26dc56bfb491dc7d4e058284166595b33f4a09cc0a6b6f161feca1d7bfbf0d2bb0766766b534f57a26e6b0be4130a3222c9c2adcd05a084f3b47945d0c993c2541e0368b9b1f6dcd9c417472052cc2fe2410ab84e10176b18206238a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0f0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004ba2dd048ea2e72e859b000000000000000000000000000000000000000000004ba3227225f42d83612d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000011c17e6b3a23830000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d90a0d291522d21b260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a6a4a694e5441355a53316b4d7a59344c5456684d6a67745957466d5953316a4f54417a4f54526a5a5442684d574d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000ff873ec0a781f1925b878b1e2b8985dd51fdf7aa00000000000000000000000000000000000000000000000b6d6f16f35a8bc45400000000000000000000000000000000000000000000000b281341207f710c4500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f600ff151dae20904e06b94c65c3f591be7f41046df88296ed4e2fdfd14f53a",
      "signature": {
        "s": "0x1b1f1a06f4ba5bc0e098ab60c0fc4aa8ef606f0e1e94d009bfa2dbe4c840ee0f",
        "r": "0x3ce52e670a0574734c2aae0e3c2b9d101566bf7fde23477d63844a36b7c3f932",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4c5d396e26dc56bfb491dc7d4e058284166595b33f4a09cc0a6b6f161feca1d7",
      "signature": {
        "s": "0x0c993c2541e0368b9b1f6dcd9c417472052cc2fe2410ab84e10176b18206238a",
        "r": "0xbfbf0d2bb0766766b534f57a26e6b0be4130a3222c9c2adcd05a084f3b47945d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4997823313093507087",
    "total": "140243781509239118456"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4997823313093507087",
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
            "amount": "27615500158629030533926"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4997823313093507"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZjJiNTA5ZS1kMzY4LTVhMjgtYWFmYS1jOTAzOTRjZTBhMWMifQ==",
    "nonce": 110832,
    "balances": {
      "current": "357181784766176941737371",
      "previous": "357186787587313348337965"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xff873ec0a781f1925b878b1e2b8985dd51fdf7aa",
    "nonce": 46,
    "balances": {
      "current": "210799731517806068820",
      "previous": "205801908204712561733"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:15.875Z",
  "updated": "2022-05-04T08:55:15.941Z",
  "id": "62723f737832e20011830c36"
}
```
* *stageAmount*: `210799731517806068820`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000455bd5d2db1ab80f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000455bd5d2db1ab80f0000000000000000000000000000000000000000000000079a46003d3fb19a784f600ff151dae20904e06b94c65c3f591be7f41046df88296ed4e2fdfd14f53a3ce52e670a0574734c2aae0e3c2b9d101566bf7fde23477d63844a36b7c3f9321b1f1a06f4ba5bc0e098ab60c0fc4aa8ef606f0e1e94d009bfa2dbe4c840ee0f000000000000000000000000000000000000000000000000000000000000001b4c5d396e26dc56bfb491dc7d4e058284166595b33f4a09cc0a6b6f161feca1d7bfbf0d2bb0766766b534f57a26e6b0be4130a3222c9c2adcd05a084f3b47945d0c993c2541e0368b9b1f6dcd9c417472052cc2fe2410ab84e10176b18206238a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0f0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004ba2dd048ea2e72e859b000000000000000000000000000000000000000000004ba3227225f42d83612d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000011c17e6b3a23830000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d90a0d291522d21b260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a6a4a694e5441355a53316b4d7a59344c5456684d6a67745957466d5953316a4f54417a4f54526a5a5442684d574d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000ff873ec0a781f1925b878b1e2b8985dd51fdf7aa00000000000000000000000000000000000000000000000b6d6f16f35a8bc45400000000000000000000000000000000000000000000000b281341207f710c4500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f600ff151dae20904e06b94c65c3f591be7f41046df88296ed4e2fdfd14f53a",
      "signature": {
        "s": "0x1b1f1a06f4ba5bc0e098ab60c0fc4aa8ef606f0e1e94d009bfa2dbe4c840ee0f",
        "r": "0x3ce52e670a0574734c2aae0e3c2b9d101566bf7fde23477d63844a36b7c3f932",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4c5d396e26dc56bfb491dc7d4e058284166595b33f4a09cc0a6b6f161feca1d7",
      "signature": {
        "s": "0x0c993c2541e0368b9b1f6dcd9c417472052cc2fe2410ab84e10176b18206238a",
        "r": "0xbfbf0d2bb0766766b534f57a26e6b0be4130a3222c9c2adcd05a084f3b47945d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4997823313093507087",
    "total": "140243781509239118456"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4997823313093507087",
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
            "amount": "27615500158629030533926"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4997823313093507"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZjJiNTA5ZS1kMzY4LTVhMjgtYWFmYS1jOTAzOTRjZTBhMWMifQ==",
    "nonce": 110832,
    "balances": {
      "current": "357181784766176941737371",
      "previous": "357186787587313348337965"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xff873ec0a781f1925b878b1e2b8985dd51fdf7aa",
    "nonce": 46,
    "balances": {
      "current": "210799731517806068820",
      "previous": "205801908204712561733"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:15.875Z",
  "updated": "2022-05-04T08:55:15.941Z",
  "id": "62723f737832e20011830c36"
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
0x0f200f9b00000000000000000000000000000000000000000000000b6d6f16f35a8bc4540000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `210799731517806068820`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`