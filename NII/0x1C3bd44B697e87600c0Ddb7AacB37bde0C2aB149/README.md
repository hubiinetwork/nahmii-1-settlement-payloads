# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1C3bd44B697e87600c0Ddb7AacB37bde0C2aB149`.

The ordered steps of contract function invocations are included below and in
the corresponding [steps.json](./steps.json). Please read [the general recipe
for settling Nahmii 1 balance](../../README.md) before starting on the first
step of settlement.

## Ordered steps
### Step 1
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001a055690d9db800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001a055690d9db8000000000000000000000000000000000000000000000000000340aad21b3b700000ad54133a5b1fc4f0191d75a789bc42eb5aa4833eeff460c9b82ceb535af318c91f0713d0accc2f4eb80f0b9b08f68f5caa36905cb2af82232583668da9fd118e5053d7d5478023f40ed8e98c5653004ae4f950f2421241a423aec2169cd54b95000000000000000000000000000000000000000000000000000000000000001b92e1eb1eb2f195f16a3362db46ce70cad6a40e42391878386d07ee0e5d7b26838b073a108e2b2550dc489b4b0d60c2ec17a6f8ffd08028cfd603c6e618a63ec77df440a01324101e13041ac883aeed98686937f7b4bf12db05fd1497b5fb0220000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000b93465000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000120000000000000000000000008d16a4008108492be0314300ac75601e84302dbd000000000000000000000000000000000000000000000032fbdeed2f6be75b5b0000000000000000000000000000000000000000000000349c9eeb1458e25b5b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000006a94d74f4300000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d529ae9e8600000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977596d51784d54526a4e43316c5a6d526b4c54526c4e7a6b74596a6b784d693168596a426a4e54466b4d544d77596d596966513d3d00000000000000000000000000000000000000000000000000000000000000020000000000000000000000001c3bd44b697e87600c0ddb7aacb37bde0c2ab14900000000000000000000000000000000000000000000000340aad21b3b700000000000000000000000000000000000000000000000000001a055690d9db8000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad54133a5b1fc4f0191d75a789bc42eb5aa4833eeff460c9b82ceb535af318c9",
      "signature": {
        "s": "0x5053d7d5478023f40ed8e98c5653004ae4f950f2421241a423aec2169cd54b95",
        "r": "0x1f0713d0accc2f4eb80f0b9b08f68f5caa36905cb2af82232583668da9fd118e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x92e1eb1eb2f195f16a3362db46ce70cad6a40e42391878386d07ee0e5d7b2683",
      "signature": {
        "s": "0x7df440a01324101e13041ac883aeed98686937f7b4bf12db05fd1497b5fb0220",
        "r": "0x8b073a108e2b2550dc489b4b0d60c2ec17a6f8ffd08028cfd603c6e618a63ec7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "30000000000000000000",
    "total": "60000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "30000000000000000000",
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
            "amount": "60000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "30000000000000000"
      }
    },
    "wallet": "0x8d16a4008108492be0314300ac75601e84302dbd",
    "data": "eyJyZWYiOiIwYmQxMTRjNC1lZmRkLTRlNzktYjkxMi1hYjBjNTFkMTMwYmYifQ==",
    "nonce": 18,
    "balances": {
      "current": "940486408021756828507",
      "previous": "970516408021756828507"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1c3bd44b697e87600c0ddb7aacb37bde0c2ab149",
    "nonce": 2,
    "balances": {
      "current": "60000000000000000000",
      "previous": "30000000000000000000"
    }
  },
  "blockNumber": "12137573",
  "created": "2021-03-30T01:05:22.120Z",
  "updated": "2021-03-30T01:05:22.278Z",
  "id": "606279524bedf50010a99d49"
}
```
* *standard*: `ERC20`
### Step 2
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000340aad21b3b7000000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `60000000000000000000`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`