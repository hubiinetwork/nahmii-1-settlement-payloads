# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbD8511ec3AE39e8266280Dc10552642e498F9C2b`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000050d75d9bf858a077d000000000000000000000000000000000000000000000003d8e6d305eb064efc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000003d8e6d305eb064efc0000000000000000000000000000000000000000000000050d75d9bf858a077ddd117695f476c6ce6fa321c5ae7286f113a61871e7be67576ed6a246672c5e5632afec7cc291896d90d16cdfa10c140ec65197cec3fa70f26588dc1fb4eef74f6ade83d6c8cec6dc0941ded3c2629202a32aeae61905fe21d501c8bb30037e9f000000000000000000000000000000000000000000000000000000000000001b24f083905bb426adc6c0d10e05d8c0bce86a5a62a8f411aa168257b56ce49cbaafa98dfc84efa8e7debfe76557a5c42a5ec942ddbc785b1976b3e5a25fbf9e5f1b1d1e8afb2fc2b0868cafde6bbe286b84818b606b8c2112e70724728c51d73f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c6eb410000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001485a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000026b2e4046efe591d07800000000000000000000000000000000000000000000026f08233c79a926358c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000fc2283d88e16180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004045c535c81a8eb885c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e57566a4d324d314d7930784e7a67354c54566c5a544d74596a526b4d4330314e7a426859544d774e4452684d6d496966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000bd8511ec3ae39e8266280dc10552642e498f9c2b0000000000000000000000000000000000000000000000050d75d9bf858a077d000000000000000000000000000000000000000000000001348f06b99a83b88100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdd117695f476c6ce6fa321c5ae7286f113a61871e7be67576ed6a246672c5e56",
      "signature": {
        "s": "0x6ade83d6c8cec6dc0941ded3c2629202a32aeae61905fe21d501c8bb30037e9f",
        "r": "0x32afec7cc291896d90d16cdfa10c140ec65197cec3fa70f26588dc1fb4eef74f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x24f083905bb426adc6c0d10e05d8c0bce86a5a62a8f411aa168257b56ce49cba",
      "signature": {
        "s": "0x1b1d1e8afb2fc2b0868cafde6bbe286b84818b606b8c2112e70724728c51d73f",
        "r": "0xafa98dfc84efa8e7debfe76557a5c42a5ec942ddbc785b1976b3e5a25fbf9e5f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "70969643800335896316",
    "total": "93203641079918364541"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "70969643800335896316",
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
            "amount": "18969905670559929960540"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "70969643800335896"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNWVjM2M1My0xNzg5LTVlZTMtYjRkMC01NzBhYTMwNDRhMmIifQ==",
    "nonce": 84058,
    "balances": {
      "current": "11421867323346629283960",
      "previous": "11492907936790765516172"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbd8511ec3ae39e8266280dc10552642e498f9c2b",
    "nonce": 2,
    "balances": {
      "current": "93203641079918364541",
      "previous": "22233997279582468225"
    }
  },
  "blockNumber": "13036353",
  "created": "2021-08-16T12:46:33.882Z",
  "updated": "2021-08-16T12:46:33.954Z",
  "id": "611a5e294b9bda00102879c6"
}
```
* *stageAmount*: `93203641079918364541`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000003d8e6d305eb064efc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000003d8e6d305eb064efc0000000000000000000000000000000000000000000000050d75d9bf858a077ddd117695f476c6ce6fa321c5ae7286f113a61871e7be67576ed6a246672c5e5632afec7cc291896d90d16cdfa10c140ec65197cec3fa70f26588dc1fb4eef74f6ade83d6c8cec6dc0941ded3c2629202a32aeae61905fe21d501c8bb30037e9f000000000000000000000000000000000000000000000000000000000000001b24f083905bb426adc6c0d10e05d8c0bce86a5a62a8f411aa168257b56ce49cbaafa98dfc84efa8e7debfe76557a5c42a5ec942ddbc785b1976b3e5a25fbf9e5f1b1d1e8afb2fc2b0868cafde6bbe286b84818b606b8c2112e70724728c51d73f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c6eb410000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001485a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000026b2e4046efe591d07800000000000000000000000000000000000000000000026f08233c79a926358c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000fc2283d88e16180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004045c535c81a8eb885c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e57566a4d324d314d7930784e7a67354c54566c5a544d74596a526b4d4330314e7a426859544d774e4452684d6d496966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000bd8511ec3ae39e8266280dc10552642e498f9c2b0000000000000000000000000000000000000000000000050d75d9bf858a077d000000000000000000000000000000000000000000000001348f06b99a83b88100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdd117695f476c6ce6fa321c5ae7286f113a61871e7be67576ed6a246672c5e56",
      "signature": {
        "s": "0x6ade83d6c8cec6dc0941ded3c2629202a32aeae61905fe21d501c8bb30037e9f",
        "r": "0x32afec7cc291896d90d16cdfa10c140ec65197cec3fa70f26588dc1fb4eef74f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x24f083905bb426adc6c0d10e05d8c0bce86a5a62a8f411aa168257b56ce49cba",
      "signature": {
        "s": "0x1b1d1e8afb2fc2b0868cafde6bbe286b84818b606b8c2112e70724728c51d73f",
        "r": "0xafa98dfc84efa8e7debfe76557a5c42a5ec942ddbc785b1976b3e5a25fbf9e5f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "70969643800335896316",
    "total": "93203641079918364541"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "70969643800335896316",
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
            "amount": "18969905670559929960540"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "70969643800335896"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkNWVjM2M1My0xNzg5LTVlZTMtYjRkMC01NzBhYTMwNDRhMmIifQ==",
    "nonce": 84058,
    "balances": {
      "current": "11421867323346629283960",
      "previous": "11492907936790765516172"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbd8511ec3ae39e8266280dc10552642e498f9c2b",
    "nonce": 2,
    "balances": {
      "current": "93203641079918364541",
      "previous": "22233997279582468225"
    }
  },
  "blockNumber": "13036353",
  "created": "2021-08-16T12:46:33.882Z",
  "updated": "2021-08-16T12:46:33.954Z",
  "id": "611a5e294b9bda00102879c6"
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
0x0f200f9b0000000000000000000000000000000000000000000000050d75d9bf858a077d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `93203641079918364541`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`