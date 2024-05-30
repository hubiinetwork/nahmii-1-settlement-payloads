# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x68A6921AeB13351e1982b8199b403BB1b2BA1f55`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000035f000000000000000000000000000000000000000000000000000000000000035f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000035f000000000000000000000000000000000000000000000000000000000000035f0ad750bab98fc6247ef01338e733eaadf327ec5746adfd03b28d75754994db57be39b9ce73b53415bc63e2b9a234fa1faead70fa07236cfe3beccbe3d5062c015dcac0f221bb3a4112ec4f376a37f1b1cffd12081186a2ca7460ee90a28b7d23000000000000000000000000000000000000000000000000000000000000001cd4d5acfe6b69f64039d99de82db7611f9b40b8a6f15616cd405bd21ed59278af491eda9c2227e4fae56920acca81883fb3dac3c5ad50527ab1646eb34f78f5237d777d5dc04451738546268fbb332261e443817ff259fff44a53bf712bd05808000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005b100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6825341000000000000000000000000000000000000000000000000002386f2c68256a100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009954200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6d597959546b784d69307a4d54557a4c5455314e3245744f4755334e4330344f54686d595745784d6a51794e54496966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000068a6921aeb13351e1982b8199b403bb1b2ba1f55000000000000000000000000000000000000000000000000000000000000035f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0ad750bab98fc6247ef01338e733eaadf327ec5746adfd03b28d75754994db57",
      "signature": {
        "s": "0x5dcac0f221bb3a4112ec4f376a37f1b1cffd12081186a2ca7460ee90a28b7d23",
        "r": "0xbe39b9ce73b53415bc63e2b9a234fa1faead70fa07236cfe3beccbe3d5062c01",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd4d5acfe6b69f64039d99de82db7611f9b40b8a6f15616cd405bd21ed59278af",
      "signature": {
        "s": "0x7d777d5dc04451738546268fbb332261e443817ff259fff44a53bf712bd05808",
        "r": "0x491eda9c2227e4fae56920acca81883fb3dac3c5ad50527ab1646eb34f78f523",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "863",
    "total": "863"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "863",
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
            "amount": "628034"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZmYyYTkxMi0zMTUzLTU1N2EtOGU3NC04OThmYWExMjQyNTIifQ==",
    "nonce": 1457,
    "balances": {
      "current": "10000001455510337",
      "previous": "10000001455511201"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x68a6921aeb13351e1982b8199b403bb1b2ba1f55",
    "nonce": 20,
    "balances": {
      "current": "863",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:39.973Z",
  "updated": "2020-05-22T08:09:40.446Z",
  "id": "5ec788c3005df800101bc410"
}
```
* *stageAmount*: `863`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000035f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000035f000000000000000000000000000000000000000000000000000000000000035f0ad750bab98fc6247ef01338e733eaadf327ec5746adfd03b28d75754994db57be39b9ce73b53415bc63e2b9a234fa1faead70fa07236cfe3beccbe3d5062c015dcac0f221bb3a4112ec4f376a37f1b1cffd12081186a2ca7460ee90a28b7d23000000000000000000000000000000000000000000000000000000000000001cd4d5acfe6b69f64039d99de82db7611f9b40b8a6f15616cd405bd21ed59278af491eda9c2227e4fae56920acca81883fb3dac3c5ad50527ab1646eb34f78f5237d777d5dc04451738546268fbb332261e443817ff259fff44a53bf712bd05808000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005b100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6825341000000000000000000000000000000000000000000000000002386f2c68256a100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009954200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6d597959546b784d69307a4d54557a4c5455314e3245744f4755334e4330344f54686d595745784d6a51794e54496966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000068a6921aeb13351e1982b8199b403bb1b2ba1f55000000000000000000000000000000000000000000000000000000000000035f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0ad750bab98fc6247ef01338e733eaadf327ec5746adfd03b28d75754994db57",
      "signature": {
        "s": "0x5dcac0f221bb3a4112ec4f376a37f1b1cffd12081186a2ca7460ee90a28b7d23",
        "r": "0xbe39b9ce73b53415bc63e2b9a234fa1faead70fa07236cfe3beccbe3d5062c01",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd4d5acfe6b69f64039d99de82db7611f9b40b8a6f15616cd405bd21ed59278af",
      "signature": {
        "s": "0x7d777d5dc04451738546268fbb332261e443817ff259fff44a53bf712bd05808",
        "r": "0x491eda9c2227e4fae56920acca81883fb3dac3c5ad50527ab1646eb34f78f523",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "863",
    "total": "863"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "863",
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
            "amount": "628034"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZmYyYTkxMi0zMTUzLTU1N2EtOGU3NC04OThmYWExMjQyNTIifQ==",
    "nonce": 1457,
    "balances": {
      "current": "10000001455510337",
      "previous": "10000001455511201"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x68a6921aeb13351e1982b8199b403bb1b2ba1f55",
    "nonce": 20,
    "balances": {
      "current": "863",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:39.973Z",
  "updated": "2020-05-22T08:09:40.446Z",
  "id": "5ec788c3005df800101bc410"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000035f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `863`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``