# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x41746F1837B46AdDA5Be5F85fd84EDc8C2Dd820f`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000004cd3762639d393d4000000000000000000000000000000000000000000000000069b07e988a2b13f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000069b07e988a2b13f0000000000000000000000000000000000000000000000004cd3762639d393d4dbb9af9c29eeea19d99b32f299f548ec712c9f38eb4282c098b1909376f57630c694acd55ce1fe11d57c70de526a4e265a970bb421105c457640232dc7dec1d719882caba286d118e497590a6f28f9ec8405d61f67919871f1c87dfbfec636b1000000000000000000000000000000000000000000000000000000000000001c9bf63aa850a379d7cfa9ef62770436540f351cc9c7afe83b3cf8bf1bd68b4d280aed55ec349fdeb69ec00d43c7cdde10036eac89e5ea22645a1debdd7ce9e9ff2086f3df4ea85e92ace0e3b20ef9e2ed263307226f21f9147e0f96490857c647000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b597000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000033e9aa58343b0dd1ba1e0000000000000000000000000000000000000000000033e9b0f4ed0bfd3f558600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000001b0e766caea290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df1b3ca53576aa8c9a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c596a63335a5463774e5330314e5745344c545578595441744f545268596930314f5455305a5441774e7a55314d6d516966513d3d000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000041746f1837b46adda5be5f85fd84edc8c2dd820f0000000000000000000000000000000000000000000000004cd3762639d393d400000000000000000000000000000000000000000000000046386e3cb130e29500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdbb9af9c29eeea19d99b32f299f548ec712c9f38eb4282c098b1909376f57630",
      "signature": {
        "s": "0x19882caba286d118e497590a6f28f9ec8405d61f67919871f1c87dfbfec636b1",
        "r": "0xc694acd55ce1fe11d57c70de526a4e265a970bb421105c457640232dc7dec1d7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9bf63aa850a379d7cfa9ef62770436540f351cc9c7afe83b3cf8bf1bd68b4d28",
      "signature": {
        "s": "0x2086f3df4ea85e92ace0e3b20ef9e2ed263307226f21f9147e0f96490857c647",
        "r": "0x0aed55ec349fdeb69ec00d43c7cdde10036eac89e5ea22645a1debdd7ce9e9ff",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "475982885218857279",
    "total": "5535898273519473620"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "475982885218857279",
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
            "amount": "27727418967972125510810"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "475982885218857"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlYjc3ZTcwNS01NWE4LTUxYTAtOTRhYi01OTU0ZTAwNzU1MmQifQ==",
    "nonce": 112023,
    "balances": {
      "current": "245151056613738869275166",
      "previous": "245151533072606973351302"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x41746f1837b46adda5be5f85fd84edc8c2dd820f",
    "nonce": 12,
    "balances": {
      "current": "5535898273519473620",
      "previous": "5059915388300616341"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:01:37.367Z",
  "updated": "2022-05-04T09:01:37.455Z",
  "id": "627240f1bbd75600116d0765"
}
```
* *stageAmount*: `5535898273519473620`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000069b07e988a2b13f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000069b07e988a2b13f0000000000000000000000000000000000000000000000004cd3762639d393d4dbb9af9c29eeea19d99b32f299f548ec712c9f38eb4282c098b1909376f57630c694acd55ce1fe11d57c70de526a4e265a970bb421105c457640232dc7dec1d719882caba286d118e497590a6f28f9ec8405d61f67919871f1c87dfbfec636b1000000000000000000000000000000000000000000000000000000000000001c9bf63aa850a379d7cfa9ef62770436540f351cc9c7afe83b3cf8bf1bd68b4d280aed55ec349fdeb69ec00d43c7cdde10036eac89e5ea22645a1debdd7ce9e9ff2086f3df4ea85e92ace0e3b20ef9e2ed263307226f21f9147e0f96490857c647000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b597000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000033e9aa58343b0dd1ba1e0000000000000000000000000000000000000000000033e9b0f4ed0bfd3f558600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000001b0e766caea290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df1b3ca53576aa8c9a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c596a63335a5463774e5330314e5745344c545578595441744f545268596930314f5455305a5441774e7a55314d6d516966513d3d000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000041746f1837b46adda5be5f85fd84edc8c2dd820f0000000000000000000000000000000000000000000000004cd3762639d393d400000000000000000000000000000000000000000000000046386e3cb130e29500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdbb9af9c29eeea19d99b32f299f548ec712c9f38eb4282c098b1909376f57630",
      "signature": {
        "s": "0x19882caba286d118e497590a6f28f9ec8405d61f67919871f1c87dfbfec636b1",
        "r": "0xc694acd55ce1fe11d57c70de526a4e265a970bb421105c457640232dc7dec1d7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9bf63aa850a379d7cfa9ef62770436540f351cc9c7afe83b3cf8bf1bd68b4d28",
      "signature": {
        "s": "0x2086f3df4ea85e92ace0e3b20ef9e2ed263307226f21f9147e0f96490857c647",
        "r": "0x0aed55ec349fdeb69ec00d43c7cdde10036eac89e5ea22645a1debdd7ce9e9ff",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "475982885218857279",
    "total": "5535898273519473620"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "475982885218857279",
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
            "amount": "27727418967972125510810"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "475982885218857"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlYjc3ZTcwNS01NWE4LTUxYTAtOTRhYi01OTU0ZTAwNzU1MmQifQ==",
    "nonce": 112023,
    "balances": {
      "current": "245151056613738869275166",
      "previous": "245151533072606973351302"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x41746f1837b46adda5be5f85fd84edc8c2dd820f",
    "nonce": 12,
    "balances": {
      "current": "5535898273519473620",
      "previous": "5059915388300616341"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:01:37.367Z",
  "updated": "2022-05-04T09:01:37.455Z",
  "id": "627240f1bbd75600116d0765"
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
0x0f200f9b0000000000000000000000000000000000000000000000004cd3762639d393d40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5535898273519473620`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`