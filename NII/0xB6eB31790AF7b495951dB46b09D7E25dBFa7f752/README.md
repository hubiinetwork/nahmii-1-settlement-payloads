# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB6eB31790AF7b495951dB46b09D7E25dBFa7f752`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001169cd2811c8c2038000000000000000000000000000000000000000000000000069b07e9ae28a9a30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000069b07e9ae28a9a3000000000000000000000000000000000000000000000000b95bf8b3dc68d7de4d65727b43384624d9ee16c183fad82af19847b57c9cf83a10878f9f48f74f6ae9d5d7dd5ad68e7345a36423d9a1514814014c00933681b256363ba245ac1edb26d8097cfb75b0844d94b0eb4a29d3bc0ab0026f4e08780e3acc670a7c685fc5000000000000000000000000000000000000000000000000000000000000001c1dc58a28b1a723b37b01d0dbc22e5c520fa9588dabc54d995d79934cf4d331d2ee5cc9d531715f86a6ce668dee14fa68b14a47f49021e25d79fc95cbf308fabc103de8ba7ad008c4c8c846ef1ffdc7e739987c829827d25d4ffcd0be976a981d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2cb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000046905d03043322744242000000000000000000000000000000000000000000004690639fbd043771712f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000001b0e766d4854a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da5622a50046d249d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a4759354d3249784d53316d5a6d4e6b4c54566c593259744f44597a4f433034595755784d7a417759544d345a54596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000b6eb31790af7b495951db46b09d7e25dbfa7f752000000000000000000000000000000000000000000000001169cd2811c8c20380000000000000000000000000000000000000000000000011001ca976e63769500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4d65727b43384624d9ee16c183fad82af19847b57c9cf83a10878f9f48f74f6a",
      "signature": {
        "s": "0x26d8097cfb75b0844d94b0eb4a29d3bc0ab0026f4e08780e3acc670a7c685fc5",
        "r": "0xe9d5d7dd5ad68e7345a36423d9a1514814014c00933681b256363ba245ac1edb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1dc58a28b1a723b37b01d0dbc22e5c520fa9588dabc54d995d79934cf4d331d2",
      "signature": {
        "s": "0x103de8ba7ad008c4c8c846ef1ffdc7e739987c829827d25d4ffcd0be976a981d",
        "r": "0xee5cc9d531715f86a6ce668dee14fa68b14a47f49021e25d79fc95cbf308fabc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "475982885848394147",
    "total": "13356542571278030814"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "475982885848394147",
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
            "amount": "27639429327073985055190"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "475982885848394"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwZGY5M2IxMS1mZmNkLTVlY2YtODYzOC04YWUxMzAwYTM4ZTYifQ==",
    "nonce": 111307,
    "balances": {
      "current": "333228687152777465709122",
      "previous": "333229163611646199951663"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6eb31790af7b495951db46b09d7e25dbfa7f752",
    "nonce": 46,
    "balances": {
      "current": "20076152690882388024",
      "previous": "19600169805033993877"
    }
  },
  "blockNumber": "14709976",
  "created": "2022-05-04T08:57:37.772Z",
  "updated": "2022-05-04T08:57:37.859Z",
  "id": "627240017832e20011830cd8"
}
```
* *stageAmount*: `20076152690882388024`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000069b07e9ae28a9a30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000069b07e9ae28a9a3000000000000000000000000000000000000000000000000b95bf8b3dc68d7de4d65727b43384624d9ee16c183fad82af19847b57c9cf83a10878f9f48f74f6ae9d5d7dd5ad68e7345a36423d9a1514814014c00933681b256363ba245ac1edb26d8097cfb75b0844d94b0eb4a29d3bc0ab0026f4e08780e3acc670a7c685fc5000000000000000000000000000000000000000000000000000000000000001c1dc58a28b1a723b37b01d0dbc22e5c520fa9588dabc54d995d79934cf4d331d2ee5cc9d531715f86a6ce668dee14fa68b14a47f49021e25d79fc95cbf308fabc103de8ba7ad008c4c8c846ef1ffdc7e739987c829827d25d4ffcd0be976a981d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2cb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000046905d03043322744242000000000000000000000000000000000000000000004690639fbd043771712f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000001b0e766d4854a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da5622a50046d249d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a4759354d3249784d53316d5a6d4e6b4c54566c593259744f44597a4f433034595755784d7a417759544d345a54596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000b6eb31790af7b495951db46b09d7e25dbfa7f752000000000000000000000000000000000000000000000001169cd2811c8c20380000000000000000000000000000000000000000000000011001ca976e63769500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4d65727b43384624d9ee16c183fad82af19847b57c9cf83a10878f9f48f74f6a",
      "signature": {
        "s": "0x26d8097cfb75b0844d94b0eb4a29d3bc0ab0026f4e08780e3acc670a7c685fc5",
        "r": "0xe9d5d7dd5ad68e7345a36423d9a1514814014c00933681b256363ba245ac1edb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1dc58a28b1a723b37b01d0dbc22e5c520fa9588dabc54d995d79934cf4d331d2",
      "signature": {
        "s": "0x103de8ba7ad008c4c8c846ef1ffdc7e739987c829827d25d4ffcd0be976a981d",
        "r": "0xee5cc9d531715f86a6ce668dee14fa68b14a47f49021e25d79fc95cbf308fabc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "475982885848394147",
    "total": "13356542571278030814"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "475982885848394147",
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
            "amount": "27639429327073985055190"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "475982885848394"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwZGY5M2IxMS1mZmNkLTVlY2YtODYzOC04YWUxMzAwYTM4ZTYifQ==",
    "nonce": 111307,
    "balances": {
      "current": "333228687152777465709122",
      "previous": "333229163611646199951663"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6eb31790af7b495951db46b09d7e25dbfa7f752",
    "nonce": 46,
    "balances": {
      "current": "20076152690882388024",
      "previous": "19600169805033993877"
    }
  },
  "blockNumber": "14709976",
  "created": "2022-05-04T08:57:37.772Z",
  "updated": "2022-05-04T08:57:37.859Z",
  "id": "627240017832e20011830cd8"
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
0x0f200f9b000000000000000000000000000000000000000000000001169cd2811c8c20380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `20076152690882388024`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`