# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x90cd1023B6Af7716453925BB3c219DdF8E6C5F94`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000c45a4c9f8eca21cd0000000000000000000000000000000000000000000000000f69bd20e97b9d940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000f69bd20e97b9d94000000000000000000000000000000000000000000000000c45a4c9f8eca21cd7aaf152750177945cee82d566e12fd0b23494cc0512b761caad3fded893430792617ef0b9f455151e36026079b7a0d0380cb35065ee30634fb9f3bfd5e6de6d431ceffe295c5a691b5179dde48f5201a3005cf9a5f944b540aa1e3251d433d7b000000000000000000000000000000000000000000000000000000000000001bcabaa7fde78d84b370782028a40da42fd4d2ae391bbac12ceff3b21872c08094aa395cfff21f70c59d3d756b85e791fa1771c02b41cedd6e598573e03dd68df94fa109bc2b0e5c7271df70dc7200123a2efe5cab90329fd679faf5fad7d5eafa000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b56b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003415a192be2d7973e351000000000000000000000000000000000000000000003415b1006d6a52c8f89a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000003f21befd977b50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df0ffe2f6dbda7d4810000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a596a466c4d6d59334d7930345a6a46684c5455344e5759744f546c6d4e6930304e575577596d4e6d4d4467794e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000090cd1023b6af7716453925bb3c219ddf8e6c5f94000000000000000000000000000000000000000000000000c45a4c9f8eca21cd000000000000000000000000000000000000000000000000b4f08f7ea54e843900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7aaf152750177945cee82d566e12fd0b23494cc0512b761caad3fded89343079",
      "signature": {
        "s": "0x31ceffe295c5a691b5179dde48f5201a3005cf9a5f944b540aa1e3251d433d7b",
        "r": "0x2617ef0b9f455151e36026079b7a0d0380cb35065ee30634fb9f3bfd5e6de6d4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcabaa7fde78d84b370782028a40da42fd4d2ae391bbac12ceff3b21872c08094",
      "signature": {
        "s": "0x4fa109bc2b0e5c7271df70dc7200123a2efe5cab90329fd679faf5fad7d5eafa",
        "r": "0xaa395cfff21f70c59d3d756b85e791fa1771c02b41cedd6e598573e03dd68df9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1110626732177333652",
    "total": "14148705427516957133"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1110626732177333652",
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
            "amount": "27726608753488489337985"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1110626732177333"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYjFlMmY3My04ZjFhLTU4NWYtOTlmNi00NWUwYmNmMDgyNzkifQ==",
    "nonce": 111979,
    "balances": {
      "current": "245962081311858678293329",
      "previous": "245963193049217587804314"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x90cd1023b6af7716453925bb3c219ddf8e6c5f94",
    "nonce": 13,
    "balances": {
      "current": "14148705427516957133",
      "previous": "13038078695339623481"
    }
  },
  "blockNumber": "14709986",
  "created": "2022-05-04T09:01:21.929Z",
  "updated": "2022-05-04T09:01:22.022Z",
  "id": "627240e17832e20011830dbb"
}
```
* *stageAmount*: `14148705427516957133`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000f69bd20e97b9d940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000f69bd20e97b9d94000000000000000000000000000000000000000000000000c45a4c9f8eca21cd7aaf152750177945cee82d566e12fd0b23494cc0512b761caad3fded893430792617ef0b9f455151e36026079b7a0d0380cb35065ee30634fb9f3bfd5e6de6d431ceffe295c5a691b5179dde48f5201a3005cf9a5f944b540aa1e3251d433d7b000000000000000000000000000000000000000000000000000000000000001bcabaa7fde78d84b370782028a40da42fd4d2ae391bbac12ceff3b21872c08094aa395cfff21f70c59d3d756b85e791fa1771c02b41cedd6e598573e03dd68df94fa109bc2b0e5c7271df70dc7200123a2efe5cab90329fd679faf5fad7d5eafa000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b56b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003415a192be2d7973e351000000000000000000000000000000000000000000003415b1006d6a52c8f89a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000003f21befd977b50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df0ffe2f6dbda7d4810000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a596a466c4d6d59334d7930345a6a46684c5455344e5759744f546c6d4e6930304e575577596d4e6d4d4467794e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000090cd1023b6af7716453925bb3c219ddf8e6c5f94000000000000000000000000000000000000000000000000c45a4c9f8eca21cd000000000000000000000000000000000000000000000000b4f08f7ea54e843900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7aaf152750177945cee82d566e12fd0b23494cc0512b761caad3fded89343079",
      "signature": {
        "s": "0x31ceffe295c5a691b5179dde48f5201a3005cf9a5f944b540aa1e3251d433d7b",
        "r": "0x2617ef0b9f455151e36026079b7a0d0380cb35065ee30634fb9f3bfd5e6de6d4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcabaa7fde78d84b370782028a40da42fd4d2ae391bbac12ceff3b21872c08094",
      "signature": {
        "s": "0x4fa109bc2b0e5c7271df70dc7200123a2efe5cab90329fd679faf5fad7d5eafa",
        "r": "0xaa395cfff21f70c59d3d756b85e791fa1771c02b41cedd6e598573e03dd68df9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1110626732177333652",
    "total": "14148705427516957133"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1110626732177333652",
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
            "amount": "27726608753488489337985"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1110626732177333"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYjFlMmY3My04ZjFhLTU4NWYtOTlmNi00NWUwYmNmMDgyNzkifQ==",
    "nonce": 111979,
    "balances": {
      "current": "245962081311858678293329",
      "previous": "245963193049217587804314"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x90cd1023b6af7716453925bb3c219ddf8e6c5f94",
    "nonce": 13,
    "balances": {
      "current": "14148705427516957133",
      "previous": "13038078695339623481"
    }
  },
  "blockNumber": "14709986",
  "created": "2022-05-04T09:01:21.929Z",
  "updated": "2022-05-04T09:01:22.022Z",
  "id": "627240e17832e20011830dbb"
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
0x0f200f9b000000000000000000000000000000000000000000000000c45a4c9f8eca21cd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14148705427516957133`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`