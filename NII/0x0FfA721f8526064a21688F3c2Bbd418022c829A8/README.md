# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0FfA721f8526064a21688F3c2Bbd418022c829A8`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000007b43860132af9222c0000000000000000000000000000000000000000000000000000000175fc3cfe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000175fc3cfe00000000000000000000000000000000000000000000000412cba08e8c320aa6805acad40e1eedc3d2a51c64a2e970ace4944968b8dbb40c8cf75c634a6bd47434c04b795daa0e1bc6bde8815e0021f0f0db4c27dd6ec427f8e139d5cdc5b078493ddbae547d1bc60231121180080dd5bbad00a04d8283b10171f3cdedd6ded9000000000000000000000000000000000000000000000000000000000000001b06ced75cc9a06295ca864d089055d9b62b887c9bfc6093037e9978f7b41effe94ed1774c7eca2468c0398c6fe37c27919d372d14f3e2638fc351d872ba4853b71d9a8708f595fd47b4db87480ad17ad60f94d2cdec87eceeb736e51bf3d1fdd8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1ec000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049cb74a72714c51c84470000000000000000000000000000000000000000000049cb74a727163b787ec500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000005fbd800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9829c78777bda8fc20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68593259325a6a49354e533169596d466a4c5455354e444d744f5467335a4330335a5755334f5463314e3255325a54416966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000000ffa721f8526064a21688f3c2bbd418022c829a8000000000000000000000000000000000000000000000007b43860132af9222c000000000000000000000000000000000000000000000007b4386011b4fce52e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x805acad40e1eedc3d2a51c64a2e970ace4944968b8dbb40c8cf75c634a6bd474",
      "signature": {
        "s": "0x493ddbae547d1bc60231121180080dd5bbad00a04d8283b10171f3cdedd6ded9",
        "r": "0x34c04b795daa0e1bc6bde8815e0021f0f0db4c27dd6ec427f8e139d5cdc5b078",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x06ced75cc9a06295ca864d089055d9b62b887c9bfc6093037e9978f7b41effe9",
      "signature": {
        "s": "0x1d9a8708f595fd47b4db87480ad17ad60f94d2cdec87eceeb736e51bf3d1fdd8",
        "r": "0x4ed1774c7eca2468c0398c6fe37c27919d372d14f3e2638fc351d872ba4853b7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6274432254",
    "total": "75141328941891062438"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6274432254",
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
            "amount": "27624187408119070625730"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6274432"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhY2Y2ZjI5NS1iYmFjLTU5NDMtOTg3ZC03ZWU3OTc1N2U2ZTAifQ==",
    "nonce": 111084,
    "balances": {
      "current": "348485848026646809707591",
      "previous": "348485848026653090414277"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0ffa721f8526064a21688f3c2bbd418022c829a8",
    "nonce": 46,
    "balances": {
      "current": "142113443676931301932",
      "previous": "142113443670656869678"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:29.374Z",
  "updated": "2022-05-04T08:56:29.459Z",
  "id": "62723fbdbbd75600116d0642"
}
```
* *stageAmount*: `142113443676931301932`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000175fc3cfe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000175fc3cfe00000000000000000000000000000000000000000000000412cba08e8c320aa6805acad40e1eedc3d2a51c64a2e970ace4944968b8dbb40c8cf75c634a6bd47434c04b795daa0e1bc6bde8815e0021f0f0db4c27dd6ec427f8e139d5cdc5b078493ddbae547d1bc60231121180080dd5bbad00a04d8283b10171f3cdedd6ded9000000000000000000000000000000000000000000000000000000000000001b06ced75cc9a06295ca864d089055d9b62b887c9bfc6093037e9978f7b41effe94ed1774c7eca2468c0398c6fe37c27919d372d14f3e2638fc351d872ba4853b71d9a8708f595fd47b4db87480ad17ad60f94d2cdec87eceeb736e51bf3d1fdd8000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1ec000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049cb74a72714c51c84470000000000000000000000000000000000000000000049cb74a727163b787ec500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000005fbd800000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9829c78777bda8fc20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68593259325a6a49354e533169596d466a4c5455354e444d744f5467335a4330335a5755334f5463314e3255325a54416966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000000ffa721f8526064a21688f3c2bbd418022c829a8000000000000000000000000000000000000000000000007b43860132af9222c000000000000000000000000000000000000000000000007b4386011b4fce52e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x805acad40e1eedc3d2a51c64a2e970ace4944968b8dbb40c8cf75c634a6bd474",
      "signature": {
        "s": "0x493ddbae547d1bc60231121180080dd5bbad00a04d8283b10171f3cdedd6ded9",
        "r": "0x34c04b795daa0e1bc6bde8815e0021f0f0db4c27dd6ec427f8e139d5cdc5b078",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x06ced75cc9a06295ca864d089055d9b62b887c9bfc6093037e9978f7b41effe9",
      "signature": {
        "s": "0x1d9a8708f595fd47b4db87480ad17ad60f94d2cdec87eceeb736e51bf3d1fdd8",
        "r": "0x4ed1774c7eca2468c0398c6fe37c27919d372d14f3e2638fc351d872ba4853b7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6274432254",
    "total": "75141328941891062438"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6274432254",
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
            "amount": "27624187408119070625730"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6274432"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhY2Y2ZjI5NS1iYmFjLTU5NDMtOTg3ZC03ZWU3OTc1N2U2ZTAifQ==",
    "nonce": 111084,
    "balances": {
      "current": "348485848026646809707591",
      "previous": "348485848026653090414277"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0ffa721f8526064a21688f3c2bbd418022c829a8",
    "nonce": 46,
    "balances": {
      "current": "142113443676931301932",
      "previous": "142113443670656869678"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:29.374Z",
  "updated": "2022-05-04T08:56:29.459Z",
  "id": "62723fbdbbd75600116d0642"
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
0x0f200f9b000000000000000000000000000000000000000000000007b43860132af9222c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `142113443676931301932`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`