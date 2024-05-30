# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x79D194063dfd58528Ca0f551F0beE9a43e6f6D8a`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000028fe00000000000000000000000000000000000000000000000000000000000028fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000028fe00000000000000000000000000000000000000000000000000000000000028fea7329cd4868653a90d309caed03305c98e2d67c886029e2db82ff788623d8b09963b5876c7c7957624df585dd68361922546c803c281cddef14f8c82422767ea2d9d5ddc3cf13fc586e18e4da183465fc178ab577e24effc0d67eab28c08a04b000000000000000000000000000000000000000000000000000000000000001c4147629fbcfd5af793a5d9881db8955bbaa5f7942832133ede61f7e1253649ceb9e240af5f8061f27d40cbdc34d79df2e92a11f83b5245be347e000d1fd9ba477734b6085bebd4d8c6df7ad20f6d2b3e4f5444dcbdcb642ff63592eb623624fe000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000067c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5e245be000000000000000000000000000000000000000000000000002386f2c5e26ec600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009bdfe00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e575a6d5a6a67774d5330354e6a67784c5456684d4463744f4749344e79316a596d497a5a54466959546c6c4d6a676966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000079d194063dfd58528ca0f551f0bee9a43e6f6d8a00000000000000000000000000000000000000000000000000000000000028fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa7329cd4868653a90d309caed03305c98e2d67c886029e2db82ff788623d8b09",
      "signature": {
        "s": "0x2d9d5ddc3cf13fc586e18e4da183465fc178ab577e24effc0d67eab28c08a04b",
        "r": "0x963b5876c7c7957624df585dd68361922546c803c281cddef14f8c82422767ea",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4147629fbcfd5af793a5d9881db8955bbaa5f7942832133ede61f7e1253649ce",
      "signature": {
        "s": "0x7734b6085bebd4d8c6df7ad20f6d2b3e4f5444dcbdcb642ff63592eb623624fe",
        "r": "0xb9e240af5f8061f27d40cbdc34d79df2e92a11f83b5245be347e000d1fd9ba47",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10494",
    "total": "10494"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10494",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "638462"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NWZmZjgwMS05NjgxLTVhMDctOGI4Ny1jYmIzZTFiYTllMjgifQ==",
    "nonce": 1660,
    "balances": {
      "current": "10000001445021118",
      "previous": "10000001445031622"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x79d194063dfd58528ca0f551f0bee9a43e6f6d8a",
    "nonce": 10,
    "balances": {
      "current": "10494",
      "previous": "0"
    }
  },
  "blockNumber": "10114537",
  "created": "2020-05-22T08:11:10.108Z",
  "updated": "2020-05-22T08:11:10.183Z",
  "id": "5ec7891ee5756b00111b8186"
}
```
* *stageAmount*: `10494`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000028fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000028fe00000000000000000000000000000000000000000000000000000000000028fea7329cd4868653a90d309caed03305c98e2d67c886029e2db82ff788623d8b09963b5876c7c7957624df585dd68361922546c803c281cddef14f8c82422767ea2d9d5ddc3cf13fc586e18e4da183465fc178ab577e24effc0d67eab28c08a04b000000000000000000000000000000000000000000000000000000000000001c4147629fbcfd5af793a5d9881db8955bbaa5f7942832133ede61f7e1253649ceb9e240af5f8061f27d40cbdc34d79df2e92a11f83b5245be347e000d1fd9ba477734b6085bebd4d8c6df7ad20f6d2b3e4f5444dcbdcb642ff63592eb623624fe000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000067c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5e245be000000000000000000000000000000000000000000000000002386f2c5e26ec600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009bdfe00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e575a6d5a6a67774d5330354e6a67784c5456684d4463744f4749344e79316a596d497a5a54466959546c6c4d6a676966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000079d194063dfd58528ca0f551f0bee9a43e6f6d8a00000000000000000000000000000000000000000000000000000000000028fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa7329cd4868653a90d309caed03305c98e2d67c886029e2db82ff788623d8b09",
      "signature": {
        "s": "0x2d9d5ddc3cf13fc586e18e4da183465fc178ab577e24effc0d67eab28c08a04b",
        "r": "0x963b5876c7c7957624df585dd68361922546c803c281cddef14f8c82422767ea",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4147629fbcfd5af793a5d9881db8955bbaa5f7942832133ede61f7e1253649ce",
      "signature": {
        "s": "0x7734b6085bebd4d8c6df7ad20f6d2b3e4f5444dcbdcb642ff63592eb623624fe",
        "r": "0xb9e240af5f8061f27d40cbdc34d79df2e92a11f83b5245be347e000d1fd9ba47",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10494",
    "total": "10494"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10494",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "638462"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NWZmZjgwMS05NjgxLTVhMDctOGI4Ny1jYmIzZTFiYTllMjgifQ==",
    "nonce": 1660,
    "balances": {
      "current": "10000001445021118",
      "previous": "10000001445031622"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x79d194063dfd58528ca0f551f0bee9a43e6f6d8a",
    "nonce": 10,
    "balances": {
      "current": "10494",
      "previous": "0"
    }
  },
  "blockNumber": "10114537",
  "created": "2020-05-22T08:11:10.108Z",
  "updated": "2020-05-22T08:11:10.183Z",
  "id": "5ec7891ee5756b00111b8186"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000028fe0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10494`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``