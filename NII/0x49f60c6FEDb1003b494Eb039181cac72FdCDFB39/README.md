# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x49f60c6FEDb1003b494Eb039181cac72FdCDFB39`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000020e5f5f6098e6c3470000000000000000000000000000000000000000000000006b2269ac4cd0328e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000006b2269ac4cd0328e0000000000000000000000000000000000000000000000020e5f5f6098e6c3475352208bf106ab2ade6445f6108d0a160b167aecdae2ee135b9077dcc0b731ea81ee2a383555b424145cef5d554a77fa1e9bad231c62945cc4d725d0d9d97455011a69ff0b04067cab5a91612203811c45f44055bd981bb31a2234c42dab4637000000000000000000000000000000000000000000000000000000000000001c95e4ebefcc08befdf69a37fb4fce5bdacc408c56425e207a195b81a8d265b47c27108c9ec44c5d85668667fbf2d042c18905cb21943a658d5e24e87dbcf2fd60180081d86218ddcca7d39312932096eaeaea2a59deb6fa45ac49ed6df366df0b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000139a6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026b487c5fd450d91e7700000000000000000000000000000000000000000000026b4f303d41abdc9bbd500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001b6d296367a1d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c4ecb4343937ae2eb00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d574e6c4e7a59785953316b4f5463354c54557a59544d74596a466c597930324e4459335957566c597a497a4d6a676966513d3d000000000000000000000000000000000000000000000000000000000000000500000000000000000000000049f60c6fedb1003b494eb039181cac72fdcdfb390000000000000000000000000000000000000000000000020e5f5f6098e6c347000000000000000000000000000000000000000000000001a33cf5b44c1690b900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5352208bf106ab2ade6445f6108d0a160b167aecdae2ee135b9077dcc0b731ea",
      "signature": {
        "s": "0x011a69ff0b04067cab5a91612203811c45f44055bd981bb31a2234c42dab4637",
        "r": "0x81ee2a383555b424145cef5d554a77fa1e9bad231c62945cc4d725d0d9d97455",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x95e4ebefcc08befdf69a37fb4fce5bdacc408c56425e207a195b81a8d265b47c",
      "signature": {
        "s": "0x180081d86218ddcca7d39312932096eaeaea2a59deb6fa45ac49ed6df366df0b",
        "r": "0x27108c9ec44c5d85668667fbf2d042c18905cb21943a658d5e24e87dbcf2fd60",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7719848900010455694",
    "total": "37929139455224365895"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7719848900010455694",
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
            "amount": "17799717602165118611120"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7719848900010455"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjMWNlNzYxYS1kOTc5LTUzYTMtYjFlYy02NDY3YWVlYzIzMjgifQ==",
    "nonce": 80294,
    "balances": {
      "current": "182780123786552791918448",
      "previous": "182787851355301702384597"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x49f60c6fedb1003b494eb039181cac72fdcdfb39",
    "nonce": 5,
    "balances": {
      "current": "37929139455224365895",
      "previous": "30209290555213910201"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:44.898Z",
  "updated": "2021-07-05T11:14:44.984Z",
  "id": "60e2e9a4cc369000105e3028"
}
```
* *stageAmount*: `37929139455224365895`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000006b2269ac4cd0328e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000006b2269ac4cd0328e0000000000000000000000000000000000000000000000020e5f5f6098e6c3475352208bf106ab2ade6445f6108d0a160b167aecdae2ee135b9077dcc0b731ea81ee2a383555b424145cef5d554a77fa1e9bad231c62945cc4d725d0d9d97455011a69ff0b04067cab5a91612203811c45f44055bd981bb31a2234c42dab4637000000000000000000000000000000000000000000000000000000000000001c95e4ebefcc08befdf69a37fb4fce5bdacc408c56425e207a195b81a8d265b47c27108c9ec44c5d85668667fbf2d042c18905cb21943a658d5e24e87dbcf2fd60180081d86218ddcca7d39312932096eaeaea2a59deb6fa45ac49ed6df366df0b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000139a6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026b487c5fd450d91e7700000000000000000000000000000000000000000000026b4f303d41abdc9bbd500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001b6d296367a1d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c4ecb4343937ae2eb00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d574e6c4e7a59785953316b4f5463354c54557a59544d74596a466c597930324e4459335957566c597a497a4d6a676966513d3d000000000000000000000000000000000000000000000000000000000000000500000000000000000000000049f60c6fedb1003b494eb039181cac72fdcdfb390000000000000000000000000000000000000000000000020e5f5f6098e6c347000000000000000000000000000000000000000000000001a33cf5b44c1690b900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5352208bf106ab2ade6445f6108d0a160b167aecdae2ee135b9077dcc0b731ea",
      "signature": {
        "s": "0x011a69ff0b04067cab5a91612203811c45f44055bd981bb31a2234c42dab4637",
        "r": "0x81ee2a383555b424145cef5d554a77fa1e9bad231c62945cc4d725d0d9d97455",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x95e4ebefcc08befdf69a37fb4fce5bdacc408c56425e207a195b81a8d265b47c",
      "signature": {
        "s": "0x180081d86218ddcca7d39312932096eaeaea2a59deb6fa45ac49ed6df366df0b",
        "r": "0x27108c9ec44c5d85668667fbf2d042c18905cb21943a658d5e24e87dbcf2fd60",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7719848900010455694",
    "total": "37929139455224365895"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7719848900010455694",
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
            "amount": "17799717602165118611120"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7719848900010455"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjMWNlNzYxYS1kOTc5LTUzYTMtYjFlYy02NDY3YWVlYzIzMjgifQ==",
    "nonce": 80294,
    "balances": {
      "current": "182780123786552791918448",
      "previous": "182787851355301702384597"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x49f60c6fedb1003b494eb039181cac72fdcdfb39",
    "nonce": 5,
    "balances": {
      "current": "37929139455224365895",
      "previous": "30209290555213910201"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:44.898Z",
  "updated": "2021-07-05T11:14:44.984Z",
  "id": "60e2e9a4cc369000105e3028"
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
0x0f200f9b0000000000000000000000000000000000000000000000020e5f5f6098e6c3470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `37929139455224365895`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`