# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2584AE708032961D307A0fAe613FD58124f65a4A`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001d05ab456afb113d70000000000000000000000000000000000000000000000000b026285779959740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b0262857799597400000000000000000000000000000000000000000000000134ee9e811a0b5304752ecafbdc482301d89e8289df1027432061b3ca5ded7db97455fe7436ab4a62d5624130287520cc77b8de65caebb0f6f5d20cae919107f4eafd4e9e77ffb9982c02d165bfc6f2cee288af8b71c33c5a4ee626b1d0cbfae9f8a80189f4589e15000000000000000000000000000000000000000000000000000000000000001cbc60121bcfc2a8ec639323d817526a56de7bd7f163d9752b689856817d7d22ff1ef61c144b5ac550bad21bd8b032b1be8e726a534aaf9432ed5d1673cf96702c6de10f47f9caea9a833a3cd955c0f423d766406f2a4c4818b244df52099dd5a5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b11f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004b3a484f8e75e21695a8000000000000000000000000000000000000000000004b3a5354c27d051222a700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002d181ab62338b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d924cc20632ed885f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d5456685a5746684e53316c4d44517a4c54566b4f546b74595445784e4330775a474d345a474a6b4f4455344e57596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000002584ae708032961d307a0fae613fd58124f65a4a000000000000000000000000000000000000000000000001d05ab456afb113d7000000000000000000000000000000000000000000000001c55851d13817ba6300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x752ecafbdc482301d89e8289df1027432061b3ca5ded7db97455fe7436ab4a62",
      "signature": {
        "s": "0x2c02d165bfc6f2cee288af8b71c33c5a4ee626b1d0cbfae9f8a80189f4589e15",
        "r": "0xd5624130287520cc77b8de65caebb0f6f5d20cae919107f4eafd4e9e77ffb998",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbc60121bcfc2a8ec639323d817526a56de7bd7f163d9752b689856817d7d22ff",
      "signature": {
        "s": "0x6de10f47f9caea9a833a3cd955c0f423d766406f2a4c4818b244df52099dd5a5",
        "r": "0x1ef61c144b5ac550bad21bd8b032b1be8e726a534aaf9432ed5d1673cf96702c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "793304809747339636",
    "total": "22260904285463859972"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "793304809747339636",
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
            "amount": "27617427408234172941811"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "793304809747339"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMTVhZWFhNS1lMDQzLTVkOTktYTExNC0wZGM4ZGJkODU4NWYifQ==",
    "nonce": 110879,
    "balances": {
      "current": "355252607911429391422888",
      "previous": "355253402009543948509863"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2584ae708032961d307a0fae613fd58124f65a4a",
    "nonce": 46,
    "balances": {
      "current": "33460254665910326231",
      "previous": "32666949856162986595"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:29.142Z",
  "updated": "2022-05-04T08:55:29.200Z",
  "id": "62723f813592fd001130b56b"
}
```
* *stageAmount*: `33460254665910326231`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000b026285779959740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000b0262857799597400000000000000000000000000000000000000000000000134ee9e811a0b5304752ecafbdc482301d89e8289df1027432061b3ca5ded7db97455fe7436ab4a62d5624130287520cc77b8de65caebb0f6f5d20cae919107f4eafd4e9e77ffb9982c02d165bfc6f2cee288af8b71c33c5a4ee626b1d0cbfae9f8a80189f4589e15000000000000000000000000000000000000000000000000000000000000001cbc60121bcfc2a8ec639323d817526a56de7bd7f163d9752b689856817d7d22ff1ef61c144b5ac550bad21bd8b032b1be8e726a534aaf9432ed5d1673cf96702c6de10f47f9caea9a833a3cd955c0f423d766406f2a4c4818b244df52099dd5a5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b11f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004b3a484f8e75e21695a8000000000000000000000000000000000000000000004b3a5354c27d051222a700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002d181ab62338b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d924cc20632ed885f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d5456685a5746684e53316c4d44517a4c54566b4f546b74595445784e4330775a474d345a474a6b4f4455344e57596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000002584ae708032961d307a0fae613fd58124f65a4a000000000000000000000000000000000000000000000001d05ab456afb113d7000000000000000000000000000000000000000000000001c55851d13817ba6300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x752ecafbdc482301d89e8289df1027432061b3ca5ded7db97455fe7436ab4a62",
      "signature": {
        "s": "0x2c02d165bfc6f2cee288af8b71c33c5a4ee626b1d0cbfae9f8a80189f4589e15",
        "r": "0xd5624130287520cc77b8de65caebb0f6f5d20cae919107f4eafd4e9e77ffb998",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbc60121bcfc2a8ec639323d817526a56de7bd7f163d9752b689856817d7d22ff",
      "signature": {
        "s": "0x6de10f47f9caea9a833a3cd955c0f423d766406f2a4c4818b244df52099dd5a5",
        "r": "0x1ef61c144b5ac550bad21bd8b032b1be8e726a534aaf9432ed5d1673cf96702c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "793304809747339636",
    "total": "22260904285463859972"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "793304809747339636",
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
            "amount": "27617427408234172941811"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "793304809747339"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMTVhZWFhNS1lMDQzLTVkOTktYTExNC0wZGM4ZGJkODU4NWYifQ==",
    "nonce": 110879,
    "balances": {
      "current": "355252607911429391422888",
      "previous": "355253402009543948509863"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2584ae708032961d307a0fae613fd58124f65a4a",
    "nonce": 46,
    "balances": {
      "current": "33460254665910326231",
      "previous": "32666949856162986595"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:29.142Z",
  "updated": "2022-05-04T08:55:29.200Z",
  "id": "62723f813592fd001130b56b"
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
0x0f200f9b000000000000000000000000000000000000000000000001d05ab456afb113d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `33460254665910326231`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`