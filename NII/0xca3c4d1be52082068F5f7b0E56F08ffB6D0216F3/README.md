# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xca3c4d1be52082068F5f7b0E56F08ffB6D0216F3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000009cb7d4ce0b5ae117c00000000000000000000000000000000000000000000000000000004a9adb0a00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000004a9adb0a00000000000000000000000000000000000000000000000000000006cd20937bc0b0548667e898d52f3ce31287590fa52a212154738911ad9e42a89acf3f720800ac765624c4d32fccdaf1280236edfcc4430252a8edee9a13bbee62ee5cf20cf6671317c5fe195fa283c8f88bc153aaffc40f96c9b64595bad512f981952b066000000000000000000000000000000000000000000000000000000000000001bb536538c7c9476d15e47ee6024d3158472b700c12c4d68f16d581a295810d8f28ec03e8fcb58b7b145ae865d07134b82b2437351db21fb8542355ccc3b9193170fd7eaab0997c21f0006748ddbf98fabcb06bbe12ddb60debb4fbc91e5a17847000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b46d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039ae9d0aae7d40dc462d0000000000000000000000000000000000000000000039ae9d0aae81ebbb8bb600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000013194e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dda184134ffeabd1d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e446b784e6a6c6b4e4330314e54677a4c54566d4e574d744f47466c4d4330334e544a695a6a4a6c4d6d526b4f44636966513d3d0000000000000000000000000000000000000000000000000000000000000027000000000000000000000000ca3c4d1be52082068f5f7b0e56f08ffb6d0216f3000000000000000000000000000000000000000000000009cb7d4ce0b5ae117c000000000000000000000000000000000000000000000009cb7d4cdc0c0060dc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0b0548667e898d52f3ce31287590fa52a212154738911ad9e42a89acf3f72080",
      "signature": {
        "s": "0x6671317c5fe195fa283c8f88bc153aaffc40f96c9b64595bad512f981952b066",
        "r": "0x0ac765624c4d32fccdaf1280236edfcc4430252a8edee9a13bbee62ee5cf20cf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb536538c7c9476d15e47ee6024d3158472b700c12c4d68f16d581a295810d8f2",
      "signature": {
        "s": "0x0fd7eaab0997c21f0006748ddbf98fabcb06bbe12ddb60debb4fbc91e5a17847",
        "r": "0x8ec03e8fcb58b7b145ae865d07134b82b2437351db21fb8542355ccc3b919317",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "20026601632",
    "total": "467380287420"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20026601632",
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
            "amount": "27700201303209365197270"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "20026601"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhNDkxNjlkNC01NTgzLTVmNWMtOGFlMC03NTJiZjJlMmRkODcifQ==",
    "nonce": 111725,
    "balances": {
      "current": "272395939041261943277101",
      "previous": "272395939041281989905334"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca3c4d1be52082068f5f7b0e56f08ffb6d0216f3",
    "nonce": 39,
    "balances": {
      "current": "180683657153178636668",
      "previous": "180683657133152035036"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:49.966Z",
  "updated": "2022-05-04T08:59:50.079Z",
  "id": "627240853592fd001130b691"
}
```
* *stageAmount*: `180683657153178636668`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000004a9adb0a00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000004a9adb0a00000000000000000000000000000000000000000000000000000006cd20937bc0b0548667e898d52f3ce31287590fa52a212154738911ad9e42a89acf3f720800ac765624c4d32fccdaf1280236edfcc4430252a8edee9a13bbee62ee5cf20cf6671317c5fe195fa283c8f88bc153aaffc40f96c9b64595bad512f981952b066000000000000000000000000000000000000000000000000000000000000001bb536538c7c9476d15e47ee6024d3158472b700c12c4d68f16d581a295810d8f28ec03e8fcb58b7b145ae865d07134b82b2437351db21fb8542355ccc3b9193170fd7eaab0997c21f0006748ddbf98fabcb06bbe12ddb60debb4fbc91e5a17847000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b46d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039ae9d0aae7d40dc462d0000000000000000000000000000000000000000000039ae9d0aae81ebbb8bb600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000013194e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dda184134ffeabd1d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e446b784e6a6c6b4e4330314e54677a4c54566d4e574d744f47466c4d4330334e544a695a6a4a6c4d6d526b4f44636966513d3d0000000000000000000000000000000000000000000000000000000000000027000000000000000000000000ca3c4d1be52082068f5f7b0e56f08ffb6d0216f3000000000000000000000000000000000000000000000009cb7d4ce0b5ae117c000000000000000000000000000000000000000000000009cb7d4cdc0c0060dc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0b0548667e898d52f3ce31287590fa52a212154738911ad9e42a89acf3f72080",
      "signature": {
        "s": "0x6671317c5fe195fa283c8f88bc153aaffc40f96c9b64595bad512f981952b066",
        "r": "0x0ac765624c4d32fccdaf1280236edfcc4430252a8edee9a13bbee62ee5cf20cf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb536538c7c9476d15e47ee6024d3158472b700c12c4d68f16d581a295810d8f2",
      "signature": {
        "s": "0x0fd7eaab0997c21f0006748ddbf98fabcb06bbe12ddb60debb4fbc91e5a17847",
        "r": "0x8ec03e8fcb58b7b145ae865d07134b82b2437351db21fb8542355ccc3b919317",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "20026601632",
    "total": "467380287420"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20026601632",
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
            "amount": "27700201303209365197270"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "20026601"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhNDkxNjlkNC01NTgzLTVmNWMtOGFlMC03NTJiZjJlMmRkODcifQ==",
    "nonce": 111725,
    "balances": {
      "current": "272395939041261943277101",
      "previous": "272395939041281989905334"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca3c4d1be52082068f5f7b0e56f08ffb6d0216f3",
    "nonce": 39,
    "balances": {
      "current": "180683657153178636668",
      "previous": "180683657133152035036"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:49.966Z",
  "updated": "2022-05-04T08:59:50.079Z",
  "id": "627240853592fd001130b691"
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
0x0f200f9b000000000000000000000000000000000000000000000009cb7d4ce0b5ae117c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `180683657153178636668`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`