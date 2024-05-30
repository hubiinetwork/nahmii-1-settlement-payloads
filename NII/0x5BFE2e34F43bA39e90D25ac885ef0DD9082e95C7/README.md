# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5BFE2e34F43bA39e90D25ac885ef0DD9082e95C7`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000002d58db9917b729362f400000000000000000000000000000000000000000000001133b9f08adf4b81e00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001133b9f08adf4b81e00000000000000000000000000000000000000000000001e2b4d7a9b8a89c617b7c0606838f682c73fa1342af9cf60e555cc7c2dd0d6ca4e1f2fbaded221021c44b0a860b14866b12066860a91dfe63c05ecb3cef62cc5172283219817982def750d499ad729478a4c08f0155b981062a28ecfdd2c61fc68f98faf0ec0d31e626000000000000000000000000000000000000000000000000000000000000001c59c91368d7ec58a679f461c7889b61672ad9cad351af04ba65b403b5b4eb470cc0d8c4308f36319afea9565c1592fad1484bc61ca85ef00fa5d8e52dcbaf2545605750a48414529f8e0ee10efdf0170659bcb77cf25bbcd113901f211e238bb1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b283000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000047fad42a44fa3343959d00000000000000000000000000000000000000000000480c0c4b9020dbff8d1f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000004675a9bc97075a20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9f96fd70fef1599290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a49344d47566c4e79316b595449304c545578595467745954426b4d7930784e6a45304f44466d596a4a69596a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005bfe2e34f43ba39e90d25ac885ef0dd9082e95c70000000000000000000000000000000000000000000002d58db9917b729362f40000000000000000000000000000000000000000000002c459ffa0f09347e11400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c0606838f682c73fa1342af9cf60e555cc7c2dd0d6ca4e1f2fbaded221021c4",
      "signature": {
        "s": "0x50d499ad729478a4c08f0155b981062a28ecfdd2c61fc68f98faf0ec0d31e626",
        "r": "0x4b0a860b14866b12066860a91dfe63c05ecb3cef62cc5172283219817982def7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x59c91368d7ec58a679f461c7889b61672ad9cad351af04ba65b403b5b4eb470c",
      "signature": {
        "s": "0x605750a48414529f8e0ee10efdf0170659bcb77cf25bbcd113901f211e238bb1",
        "r": "0xc0d8c4308f36319afea9565c1592fad1484bc61ca85ef00fa5d8e52dcbaf2545",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "317321923898930594272",
    "total": "8904361714185391595899"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "317321923898930594272",
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
            "amount": "27632749699444493359401"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "317321923898930594"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNzI4MGVlNy1kYTI0LTUxYTgtYTBkMy0xNjE0ODFmYjJiYjkifQ==",
    "nonce": 111235,
    "balances": {
      "current": "339914994409898653226397",
      "previous": "340232633655721482751263"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bfe2e34f43ba39e90d25ac885ef0dd9082e95c7",
    "nonce": 46,
    "balances": {
      "current": "13384101807028853498612",
      "previous": "13066779883129922904340"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:15.444Z",
  "updated": "2022-05-04T08:57:15.509Z",
  "id": "62723feb3592fd001130b5e6"
}
```
* *stageAmount*: `13384101807028853498612`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000001133b9f08adf4b81e00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001133b9f08adf4b81e00000000000000000000000000000000000000000000001e2b4d7a9b8a89c617b7c0606838f682c73fa1342af9cf60e555cc7c2dd0d6ca4e1f2fbaded221021c44b0a860b14866b12066860a91dfe63c05ecb3cef62cc5172283219817982def750d499ad729478a4c08f0155b981062a28ecfdd2c61fc68f98faf0ec0d31e626000000000000000000000000000000000000000000000000000000000000001c59c91368d7ec58a679f461c7889b61672ad9cad351af04ba65b403b5b4eb470cc0d8c4308f36319afea9565c1592fad1484bc61ca85ef00fa5d8e52dcbaf2545605750a48414529f8e0ee10efdf0170659bcb77cf25bbcd113901f211e238bb1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b283000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000047fad42a44fa3343959d00000000000000000000000000000000000000000000480c0c4b9020dbff8d1f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000004675a9bc97075a20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9f96fd70fef1599290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a49344d47566c4e79316b595449304c545578595467745954426b4d7930784e6a45304f44466d596a4a69596a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005bfe2e34f43ba39e90d25ac885ef0dd9082e95c70000000000000000000000000000000000000000000002d58db9917b729362f40000000000000000000000000000000000000000000002c459ffa0f09347e11400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c0606838f682c73fa1342af9cf60e555cc7c2dd0d6ca4e1f2fbaded221021c4",
      "signature": {
        "s": "0x50d499ad729478a4c08f0155b981062a28ecfdd2c61fc68f98faf0ec0d31e626",
        "r": "0x4b0a860b14866b12066860a91dfe63c05ecb3cef62cc5172283219817982def7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x59c91368d7ec58a679f461c7889b61672ad9cad351af04ba65b403b5b4eb470c",
      "signature": {
        "s": "0x605750a48414529f8e0ee10efdf0170659bcb77cf25bbcd113901f211e238bb1",
        "r": "0xc0d8c4308f36319afea9565c1592fad1484bc61ca85ef00fa5d8e52dcbaf2545",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "317321923898930594272",
    "total": "8904361714185391595899"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "317321923898930594272",
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
            "amount": "27632749699444493359401"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "317321923898930594"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNzI4MGVlNy1kYTI0LTUxYTgtYTBkMy0xNjE0ODFmYjJiYjkifQ==",
    "nonce": 111235,
    "balances": {
      "current": "339914994409898653226397",
      "previous": "340232633655721482751263"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bfe2e34f43ba39e90d25ac885ef0dd9082e95c7",
    "nonce": 46,
    "balances": {
      "current": "13384101807028853498612",
      "previous": "13066779883129922904340"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:15.444Z",
  "updated": "2022-05-04T08:57:15.509Z",
  "id": "62723feb3592fd001130b5e6"
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
0x0f200f9b0000000000000000000000000000000000000000000002d58db9917b729362f40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13384101807028853498612`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`