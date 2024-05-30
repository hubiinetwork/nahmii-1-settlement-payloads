# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd09B72527f8DA186750FB7F8d32eD76cde623948`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000008add578d8b99a2e60000000000000000000000000000000000000000000000000000000021084ec90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000021084ec90000000000000000000000000000000000000000000000000000000302ec7375cb17a7005e58d1e3dc819690fa80bdf72611b48f378570e248975de8e572e8429b940e67dc9441ac99fcfba3ede4e78cf665aced31530e873f91984147133f7e78e749e88a82137519aa651579fe8ffc3aae25d2678ce576d0b2fb0198e2cfa3000000000000000000000000000000000000000000000000000000000000001b9dadcc50ccc965a4b8a9f15ac9ef4864ebe21bee93a90d12a38dfc39381c3a00530eb7423b382130cc3feb8230fee5faca7623573b743868988611ead1e6bbbd3acbe0064951a3b0dfd6d6321f30819b6838f511bf79ea5efabae4e853c29678000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b74b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002dae08f047ec773d8231000000000000000000000000000000000000000000002dae08f047ec984e45ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000874d00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b34f6b229df20bf10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e3245314e4463334e6930334d3249314c5456695a5751744f54497a4f5330784f545534595441355a6d466d4f44456966513d3d000000000000000000000000000000000000000000000000000000000000001d000000000000000000000000d09b72527f8da186750fb7f8d32ed76cde6239480000000000000000000000000000000000000000000000008add578d8b99a2e60000000000000000000000000000000000000000000000008add578d6a91541d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcb17a7005e58d1e3dc819690fa80bdf72611b48f378570e248975de8e572e842",
      "signature": {
        "s": "0x78e749e88a82137519aa651579fe8ffc3aae25d2678ce576d0b2fb0198e2cfa3",
        "r": "0x9b940e67dc9441ac99fcfba3ede4e78cf665aced31530e873f91984147133f7e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9dadcc50ccc965a4b8a9f15ac9ef4864ebe21bee93a90d12a38dfc39381c3a00",
      "signature": {
        "s": "0x3acbe0064951a3b0dfd6d6321f30819b6838f511bf79ea5efabae4e853c29678",
        "r": "0x530eb7423b382130cc3feb8230fee5faca7623573b743868988611ead1e6bbbd",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "554192585",
    "total": "12933952373"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "554192585",
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
            "amount": "27756823750511537818609"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "554192"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyN2E1NDc3Ni03M2I1LTViZWQtOTIzOS0xOTU4YTA5ZmFmODEifQ==",
    "nonce": 112459,
    "balances": {
      "current": "215716869291787148952113",
      "previous": "215716869291787703698890"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd09b72527f8da186750fb7f8d32ed76cde623948",
    "nonce": 29,
    "balances": {
      "current": "10006250212531217126",
      "previous": "10006250211977024541"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:54.174Z",
  "updated": "2022-05-04T09:03:54.291Z",
  "id": "6272417a3592fd001130b791"
}
```
* *stageAmount*: `10006250212531217126`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000021084ec90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000021084ec90000000000000000000000000000000000000000000000000000000302ec7375cb17a7005e58d1e3dc819690fa80bdf72611b48f378570e248975de8e572e8429b940e67dc9441ac99fcfba3ede4e78cf665aced31530e873f91984147133f7e78e749e88a82137519aa651579fe8ffc3aae25d2678ce576d0b2fb0198e2cfa3000000000000000000000000000000000000000000000000000000000000001b9dadcc50ccc965a4b8a9f15ac9ef4864ebe21bee93a90d12a38dfc39381c3a00530eb7423b382130cc3feb8230fee5faca7623573b743868988611ead1e6bbbd3acbe0064951a3b0dfd6d6321f30819b6838f511bf79ea5efabae4e853c29678000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b74b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002dae08f047ec773d8231000000000000000000000000000000000000000000002dae08f047ec984e45ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000874d00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b34f6b229df20bf10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e3245314e4463334e6930334d3249314c5456695a5751744f54497a4f5330784f545534595441355a6d466d4f44456966513d3d000000000000000000000000000000000000000000000000000000000000001d000000000000000000000000d09b72527f8da186750fb7f8d32ed76cde6239480000000000000000000000000000000000000000000000008add578d8b99a2e60000000000000000000000000000000000000000000000008add578d6a91541d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcb17a7005e58d1e3dc819690fa80bdf72611b48f378570e248975de8e572e842",
      "signature": {
        "s": "0x78e749e88a82137519aa651579fe8ffc3aae25d2678ce576d0b2fb0198e2cfa3",
        "r": "0x9b940e67dc9441ac99fcfba3ede4e78cf665aced31530e873f91984147133f7e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9dadcc50ccc965a4b8a9f15ac9ef4864ebe21bee93a90d12a38dfc39381c3a00",
      "signature": {
        "s": "0x3acbe0064951a3b0dfd6d6321f30819b6838f511bf79ea5efabae4e853c29678",
        "r": "0x530eb7423b382130cc3feb8230fee5faca7623573b743868988611ead1e6bbbd",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "554192585",
    "total": "12933952373"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "554192585",
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
            "amount": "27756823750511537818609"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "554192"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyN2E1NDc3Ni03M2I1LTViZWQtOTIzOS0xOTU4YTA5ZmFmODEifQ==",
    "nonce": 112459,
    "balances": {
      "current": "215716869291787148952113",
      "previous": "215716869291787703698890"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd09b72527f8da186750fb7f8d32ed76cde623948",
    "nonce": 29,
    "balances": {
      "current": "10006250212531217126",
      "previous": "10006250211977024541"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:54.174Z",
  "updated": "2022-05-04T09:03:54.291Z",
  "id": "6272417a3592fd001130b791"
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
0x0f200f9b0000000000000000000000000000000000000000000000008add578d8b99a2e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10006250212531217126`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`