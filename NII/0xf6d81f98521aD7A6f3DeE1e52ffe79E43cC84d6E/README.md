# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf6d81f98521aD7A6f3DeE1e52ffe79E43cC84d6E`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000004a544459b313354b100000000000000000000000000000000000000000000000100e8594039a3ba7a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000100e8594039a3ba7a000000000000000000000000000000000000000000000004a544459b313354b11f836c88684251683dc92bdaedb63dc385afd60131507ef3e90bedce5bb2ab475b5ae67b28936863891483ea08da9ae262c842bf26f3e419a9b26bb8c6bd71827915f759dfcbe6d3fa483e77fd5382c8de3da8750981414e57801c210629ccfe000000000000000000000000000000000000000000000000000000000000001b78689d33eba72301a8c4190f030c541670d5301b84696bebd6e7abd81e8f159939cbfa2402dfc3d1b983b8297eda39757f615f166341ab058521351076dadabe4530ab7df91a8c7886c89f774c1d487938299872099960e2ede9c529db9fe5fd000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bac19100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011505000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000024875ea89d2269f33ccf0000000000000000000000000000000000000000000024885fd2bb15229f93e300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000041c4b27f089c9a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000323036c42cb564e822e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e6a4e684d6d4d7a4e7930324e324d354c5455345a4441744f474d324e7930774d6a6c694f475a685a4463325a44596966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000f6d81f98521ad7a6f3dee1e52ffe79e43cc84d6e000000000000000000000000000000000000000000000004a544459b313354b1000000000000000000000000000000000000000000000003a45bec5af78f9a3700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1f836c88684251683dc92bdaedb63dc385afd60131507ef3e90bedce5bb2ab47",
      "signature": {
        "s": "0x7915f759dfcbe6d3fa483e77fd5382c8de3da8750981414e57801c210629ccfe",
        "r": "0x5b5ae67b28936863891483ea08da9ae262c842bf26f3e419a9b26bb8c6bd7182",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x78689d33eba72301a8c4190f030c541670d5301b84696bebd6e7abd81e8f1599",
      "signature": {
        "s": "0x4530ab7df91a8c7886c89f774c1d487938299872099960e2ede9c529db9fe5fd",
        "r": "0x39cbfa2402dfc3d1b983b8297eda39757f615f166341ab058521351076dadabe",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18512144400686234234",
    "total": "85695696142360335537"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18512144400686234234",
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
            "amount": "14812982136709462262318"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "18512144400686234"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNjNhMmMzNy02N2M5LTU4ZDAtOGM2Ny0wMjliOGZhZDc2ZDYifQ==",
    "nonce": 70917,
    "balances": {
      "current": "172502324707664801774799",
      "previous": "172520855364209888695267"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf6d81f98521ad7a6f3dee1e52ffe79e43cc84d6e",
    "nonce": 5,
    "balances": {
      "current": "85695696142360335537",
      "previous": "67183551741674101303"
    }
  },
  "blockNumber": "12239249",
  "created": "2021-04-14T16:22:01.251Z",
  "updated": "2021-04-14T16:22:01.337Z",
  "id": "607716a950c3ba0010570e0a"
}
```
* *stageAmount*: `85695696142360335537`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000100e8594039a3ba7a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000100e8594039a3ba7a000000000000000000000000000000000000000000000004a544459b313354b11f836c88684251683dc92bdaedb63dc385afd60131507ef3e90bedce5bb2ab475b5ae67b28936863891483ea08da9ae262c842bf26f3e419a9b26bb8c6bd71827915f759dfcbe6d3fa483e77fd5382c8de3da8750981414e57801c210629ccfe000000000000000000000000000000000000000000000000000000000000001b78689d33eba72301a8c4190f030c541670d5301b84696bebd6e7abd81e8f159939cbfa2402dfc3d1b983b8297eda39757f615f166341ab058521351076dadabe4530ab7df91a8c7886c89f774c1d487938299872099960e2ede9c529db9fe5fd000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bac19100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011505000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000024875ea89d2269f33ccf0000000000000000000000000000000000000000000024885fd2bb15229f93e300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000041c4b27f089c9a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000323036c42cb564e822e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e6a4e684d6d4d7a4e7930324e324d354c5455345a4441744f474d324e7930774d6a6c694f475a685a4463325a44596966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000f6d81f98521ad7a6f3dee1e52ffe79e43cc84d6e000000000000000000000000000000000000000000000004a544459b313354b1000000000000000000000000000000000000000000000003a45bec5af78f9a3700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1f836c88684251683dc92bdaedb63dc385afd60131507ef3e90bedce5bb2ab47",
      "signature": {
        "s": "0x7915f759dfcbe6d3fa483e77fd5382c8de3da8750981414e57801c210629ccfe",
        "r": "0x5b5ae67b28936863891483ea08da9ae262c842bf26f3e419a9b26bb8c6bd7182",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x78689d33eba72301a8c4190f030c541670d5301b84696bebd6e7abd81e8f1599",
      "signature": {
        "s": "0x4530ab7df91a8c7886c89f774c1d487938299872099960e2ede9c529db9fe5fd",
        "r": "0x39cbfa2402dfc3d1b983b8297eda39757f615f166341ab058521351076dadabe",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18512144400686234234",
    "total": "85695696142360335537"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18512144400686234234",
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
            "amount": "14812982136709462262318"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "18512144400686234"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNjNhMmMzNy02N2M5LTU4ZDAtOGM2Ny0wMjliOGZhZDc2ZDYifQ==",
    "nonce": 70917,
    "balances": {
      "current": "172502324707664801774799",
      "previous": "172520855364209888695267"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf6d81f98521ad7a6f3dee1e52ffe79e43cc84d6e",
    "nonce": 5,
    "balances": {
      "current": "85695696142360335537",
      "previous": "67183551741674101303"
    }
  },
  "blockNumber": "12239249",
  "created": "2021-04-14T16:22:01.251Z",
  "updated": "2021-04-14T16:22:01.337Z",
  "id": "607716a950c3ba0010570e0a"
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
0x0f200f9b000000000000000000000000000000000000000000000004a544459b313354b10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `85695696142360335537`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`