# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE737adaC767F5d48DEE4F3b51c124b0c74200380`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000008c09f21cd4946cf0000000000000000000000000000000000000000000000000000000002dd71bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000002dd71bc0000000000000000000000000000000000000000000000000000000042dd10d9ff8301a910df6b61bd936ffe28fc264a970b711b1cf0c29a4435faf3f56132818d04f2a59266d9656c85e309b7cab33966f2a8d3ad806978e9c691869ae60f11201940d7f37747d8ba5b156492b54ca3a833674035fe9e7e886a04a1d37cdd07000000000000000000000000000000000000000000000000000000000000001cffd34f84a40b2cf8692414cef561f723ca8fb2ee4f6d5f222fb83569aa9eca8ce9600b8ef2a89fd10479d281d8afe91d9d2e6cf1f254c807ad2170d478a3d02d28755ee53b2d6830789bd94d631664720b261068470f2dcde7444cc60162153f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3ac000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003b9919aebb1896a1b8c1000000000000000000000000000000000000000000003b9919aebb18997fe64000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000bbc30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd2413a3cb9eae6fe60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d59544a6d4f444d31595330315954557a4c5455774d7a6774595464695969307a5a57466a4e6d566a4d474e684e6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000020000000000000000000000000e737adac767f5d48dee4f3b51c124b0c7420038000000000000000000000000000000000000000000000000008c09f21cd4946cf00000000000000000000000000000000000000000000000008c09f21ca6bd51300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xff8301a910df6b61bd936ffe28fc264a970b711b1cf0c29a4435faf3f5613281",
      "signature": {
        "s": "0x201940d7f37747d8ba5b156492b54ca3a833674035fe9e7e886a04a1d37cdd07",
        "r": "0x8d04f2a59266d9656c85e309b7cab33966f2a8d3ad806978e9c691869ae60f11",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xffd34f84a40b2cf8692414cef561f723ca8fb2ee4f6d5f222fb83569aa9eca8c",
      "signature": {
        "s": "0x28755ee53b2d6830789bd94d631664720b261068470f2dcde7444cc60162153f",
        "r": "0xe9600b8ef2a89fd10479d281d8afe91d9d2e6cf1f254c807ad2170d478a3d02d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "48067004",
    "total": "1121784025"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48067004",
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
            "amount": "27691162456142895804390"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48067"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmYTJmODM1YS01YTUzLTUwMzgtYTdiYi0zZWFjNmVjMGNhNjkifQ==",
    "nonce": 111532,
    "balances": {
      "current": "281443824954797805648065",
      "previous": "281443824954797853763136"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe737adac767f5d48dee4f3b51c124b0c74200380",
    "nonce": 32,
    "balances": {
      "current": "630678915358738127",
      "previous": "630678915310671123"
    }
  },
  "blockNumber": "14709980",
  "created": "2022-05-04T08:58:48.632Z",
  "updated": "2022-05-04T08:58:48.708Z",
  "id": "627240487832e20011830d24"
}
```
* *stageAmount*: `630678915358738127`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000002dd71bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000002dd71bc0000000000000000000000000000000000000000000000000000000042dd10d9ff8301a910df6b61bd936ffe28fc264a970b711b1cf0c29a4435faf3f56132818d04f2a59266d9656c85e309b7cab33966f2a8d3ad806978e9c691869ae60f11201940d7f37747d8ba5b156492b54ca3a833674035fe9e7e886a04a1d37cdd07000000000000000000000000000000000000000000000000000000000000001cffd34f84a40b2cf8692414cef561f723ca8fb2ee4f6d5f222fb83569aa9eca8ce9600b8ef2a89fd10479d281d8afe91d9d2e6cf1f254c807ad2170d478a3d02d28755ee53b2d6830789bd94d631664720b261068470f2dcde7444cc60162153f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3ac000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003b9919aebb1896a1b8c1000000000000000000000000000000000000000000003b9919aebb18997fe64000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000bbc30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd2413a3cb9eae6fe60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d59544a6d4f444d31595330315954557a4c5455774d7a6774595464695969307a5a57466a4e6d566a4d474e684e6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000020000000000000000000000000e737adac767f5d48dee4f3b51c124b0c7420038000000000000000000000000000000000000000000000000008c09f21cd4946cf00000000000000000000000000000000000000000000000008c09f21ca6bd51300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xff8301a910df6b61bd936ffe28fc264a970b711b1cf0c29a4435faf3f5613281",
      "signature": {
        "s": "0x201940d7f37747d8ba5b156492b54ca3a833674035fe9e7e886a04a1d37cdd07",
        "r": "0x8d04f2a59266d9656c85e309b7cab33966f2a8d3ad806978e9c691869ae60f11",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xffd34f84a40b2cf8692414cef561f723ca8fb2ee4f6d5f222fb83569aa9eca8c",
      "signature": {
        "s": "0x28755ee53b2d6830789bd94d631664720b261068470f2dcde7444cc60162153f",
        "r": "0xe9600b8ef2a89fd10479d281d8afe91d9d2e6cf1f254c807ad2170d478a3d02d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "48067004",
    "total": "1121784025"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48067004",
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
            "amount": "27691162456142895804390"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48067"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmYTJmODM1YS01YTUzLTUwMzgtYTdiYi0zZWFjNmVjMGNhNjkifQ==",
    "nonce": 111532,
    "balances": {
      "current": "281443824954797805648065",
      "previous": "281443824954797853763136"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe737adac767f5d48dee4f3b51c124b0c74200380",
    "nonce": 32,
    "balances": {
      "current": "630678915358738127",
      "previous": "630678915310671123"
    }
  },
  "blockNumber": "14709980",
  "created": "2022-05-04T08:58:48.632Z",
  "updated": "2022-05-04T08:58:48.708Z",
  "id": "627240487832e20011830d24"
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
0x0f200f9b00000000000000000000000000000000000000000000000008c09f21cd4946cf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `630678915358738127`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`