# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd668337cB6b623216a93e55b76F8AF19aF10Abf5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000012bff771e7d5b0000000000000000000000000000000000000000000000000000071cd417e50b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000071cd417e50b0000000000000000000000000000000000000000000000000000c79637c16fc4ffcfd0356172bbe0457006f0302df504eaab85cf56858dd814e06d98c9415dc25ca4fb42201bacebc75bb213bf6ca371194e678bc86efbfad64e060c0f96688e4b46d6b4388b26e394e3890665a0f0f03dbee8b671e37937b1dc1ba5be8057ec000000000000000000000000000000000000000000000000000000000000001b879d536ae8d07af2de1841b0695f866dc89612a79a98560f613b2e8fdac2d0e8ee7d10051829b85e090b5901c601d480bca0ee06ee5f356a0467534d1126880f6e5228170c8e6a61640ed8b05bfa05bdb6107015fb42fa521e93393e4f1b6716000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afd4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052af2a07d4780d687b8f0000000000000000000000000000000000000000000052af2a07db96b3a2317800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001d221d0de0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d73c9ca1366cf2c9220000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b596a4a6d597a63785a5331694f574a6b4c545669597a49744f544d335a43316a5a54646c4e3251335a545978597a676966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000d668337cb6b623216a93e55b76f8af19af10abf500000000000000000000000000000000000000000000000000012bff771e7d5b000000000000000000000000000000000000000000000000000124e2a306985000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xffcfd0356172bbe0457006f0302df504eaab85cf56858dd814e06d98c9415dc2",
      "signature": {
        "s": "0x4b46d6b4388b26e394e3890665a0f0f03dbee8b671e37937b1dc1ba5be8057ec",
        "r": "0x5ca4fb42201bacebc75bb213bf6ca371194e678bc86efbfad64e060c0f96688e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x879d536ae8d07af2de1841b0695f866dc89612a79a98560f613b2e8fdac2d0e8",
      "signature": {
        "s": "0x6e5228170c8e6a61640ed8b05bfa05bdb6107015fb42fa521e93393e4f1b6716",
        "r": "0xee7d10051829b85e090b5901c601d480bca0ee06ee5f356a0467534d1126880f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7820398814475",
    "total": "219447994445764"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7820398814475",
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
            "amount": "27582249933189550360866"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7820398814"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkYjJmYzcxZS1iOWJkLTViYzItOTM3ZC1jZTdlN2Q3ZTYxYzgifQ==",
    "nonce": 110548,
    "balances": {
      "current": "390465260431096595118991",
      "previous": "390465260438924814332280"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd668337cb6b623216a93e55b76f8af19af10abf5",
    "nonce": 45,
    "balances": {
      "current": "329851191852379",
      "previous": "322030793037904"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:50.541Z",
  "updated": "2022-05-04T08:53:50.650Z",
  "id": "62723f1e7832e20011830bdb"
}
```
* *stageAmount*: `329851191852379`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000071cd417e50b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000071cd417e50b0000000000000000000000000000000000000000000000000000c79637c16fc4ffcfd0356172bbe0457006f0302df504eaab85cf56858dd814e06d98c9415dc25ca4fb42201bacebc75bb213bf6ca371194e678bc86efbfad64e060c0f96688e4b46d6b4388b26e394e3890665a0f0f03dbee8b671e37937b1dc1ba5be8057ec000000000000000000000000000000000000000000000000000000000000001b879d536ae8d07af2de1841b0695f866dc89612a79a98560f613b2e8fdac2d0e8ee7d10051829b85e090b5901c601d480bca0ee06ee5f356a0467534d1126880f6e5228170c8e6a61640ed8b05bfa05bdb6107015fb42fa521e93393e4f1b6716000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afd4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052af2a07d4780d687b8f0000000000000000000000000000000000000000000052af2a07db96b3a2317800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001d221d0de0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d73c9ca1366cf2c9220000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b596a4a6d597a63785a5331694f574a6b4c545669597a49744f544d335a43316a5a54646c4e3251335a545978597a676966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000d668337cb6b623216a93e55b76f8af19af10abf500000000000000000000000000000000000000000000000000012bff771e7d5b000000000000000000000000000000000000000000000000000124e2a306985000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xffcfd0356172bbe0457006f0302df504eaab85cf56858dd814e06d98c9415dc2",
      "signature": {
        "s": "0x4b46d6b4388b26e394e3890665a0f0f03dbee8b671e37937b1dc1ba5be8057ec",
        "r": "0x5ca4fb42201bacebc75bb213bf6ca371194e678bc86efbfad64e060c0f96688e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x879d536ae8d07af2de1841b0695f866dc89612a79a98560f613b2e8fdac2d0e8",
      "signature": {
        "s": "0x6e5228170c8e6a61640ed8b05bfa05bdb6107015fb42fa521e93393e4f1b6716",
        "r": "0xee7d10051829b85e090b5901c601d480bca0ee06ee5f356a0467534d1126880f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7820398814475",
    "total": "219447994445764"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7820398814475",
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
            "amount": "27582249933189550360866"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7820398814"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkYjJmYzcxZS1iOWJkLTViYzItOTM3ZC1jZTdlN2Q3ZTYxYzgifQ==",
    "nonce": 110548,
    "balances": {
      "current": "390465260431096595118991",
      "previous": "390465260438924814332280"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd668337cb6b623216a93e55b76f8af19af10abf5",
    "nonce": 45,
    "balances": {
      "current": "329851191852379",
      "previous": "322030793037904"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:50.541Z",
  "updated": "2022-05-04T08:53:50.650Z",
  "id": "62723f1e7832e20011830bdb"
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
0x0f200f9b00000000000000000000000000000000000000000000000000012bff771e7d5b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `329851191852379`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`