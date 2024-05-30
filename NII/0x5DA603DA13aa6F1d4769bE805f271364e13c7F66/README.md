# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5DA603DA13aa6F1d4769bE805f271364e13c7F66`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000004fcf96fe5c88e9979a000000000000000000000000000000000000000000000001e468eef08e5a93940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001e468eef08e5a939400000000000000000000000000000000000000000000003519033e3079d4fbac704d5b6e2ad740a2d9590735818c6f8046bd350895b0bb15c22b868017a31874651e54be12cc9a81c2a1bf8f1a32a2e4641a89a29cd48e68494d09c7b635346456de3421fd0096629ff6cc6ca203570f639839f1197041ecf087b6ea8cceeb0c000000000000000000000000000000000000000000000000000000000000001c8cd1485da23b00e0144f530f127968b53551adbf12bf0fe01111f237dc5718e768748a07ca75c1536dae8c562bbd31e4f6af23fe6ffb6d4dd4b0bf1f1668ff5835123016c94dc3b023ebe5d3df373ff8e5a61168ce931d99a4c75ddc6f165df9000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b139000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004afdcc73bc892f62874d000000000000000000000000000000000000000000004affb158adc3329df6ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000007c024974e0dbcb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9344408d01c5ae06f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a4455344e4745304d53316b4e7a457a4c5455334e6a67744f444d304e79307859544d784e444e6b4f4749304f44516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005da603da13aa6f1d4769be805f271364e13c7f6600000000000000000000000000000000000000000000004fcf96fe5c88e9979a00000000000000000000000000000000000000000000004deb2e0f6bfa8f040600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x704d5b6e2ad740a2d9590735818c6f8046bd350895b0bb15c22b868017a31874",
      "signature": {
        "s": "0x56de3421fd0096629ff6cc6ca203570f639839f1197041ecf087b6ea8cceeb0c",
        "r": "0x651e54be12cc9a81c2a1bf8f1a32a2e4641a89a29cd48e68494d09c7b6353464",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8cd1485da23b00e0144f530f127968b53551adbf12bf0fe01111f237dc5718e7",
      "signature": {
        "s": "0x35123016c94dc3b023ebe5d3df373ff8e5a61168ce931d99a4c75ddc6f165df9",
        "r": "0x68748a07ca75c1536dae8c562bbd31e4f6af23fe6ffb6d4dd4b0bf1f1668ff58",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "34905411628882891668",
    "total": "979479788560407919532"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "34905411628882891668",
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
            "amount": "27618542023221509283951"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "34905411628882891"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZDU4NGE0MS1kNzEzLTU3NjgtODM0Ny0xYTMxNDNkOGI0ODQifQ==",
    "nonce": 110905,
    "balances": {
      "current": "354136878309105712924493",
      "previous": "354171818626146224699052"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5da603da13aa6f1d4769be805f271364e13c7f66",
    "nonce": 46,
    "balances": {
      "current": "1472251204708799715226",
      "previous": "1437345793079916823558"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:36.514Z",
  "updated": "2022-05-04T08:55:36.624Z",
  "id": "62723f883592fd001130b575"
}
```
* *stageAmount*: `1472251204708799715226`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001e468eef08e5a93940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001e468eef08e5a939400000000000000000000000000000000000000000000003519033e3079d4fbac704d5b6e2ad740a2d9590735818c6f8046bd350895b0bb15c22b868017a31874651e54be12cc9a81c2a1bf8f1a32a2e4641a89a29cd48e68494d09c7b635346456de3421fd0096629ff6cc6ca203570f639839f1197041ecf087b6ea8cceeb0c000000000000000000000000000000000000000000000000000000000000001c8cd1485da23b00e0144f530f127968b53551adbf12bf0fe01111f237dc5718e768748a07ca75c1536dae8c562bbd31e4f6af23fe6ffb6d4dd4b0bf1f1668ff5835123016c94dc3b023ebe5d3df373ff8e5a61168ce931d99a4c75ddc6f165df9000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b139000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004afdcc73bc892f62874d000000000000000000000000000000000000000000004affb158adc3329df6ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000007c024974e0dbcb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9344408d01c5ae06f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a4455344e4745304d53316b4e7a457a4c5455334e6a67744f444d304e79307859544d784e444e6b4f4749304f44516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000005da603da13aa6f1d4769be805f271364e13c7f6600000000000000000000000000000000000000000000004fcf96fe5c88e9979a00000000000000000000000000000000000000000000004deb2e0f6bfa8f040600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x704d5b6e2ad740a2d9590735818c6f8046bd350895b0bb15c22b868017a31874",
      "signature": {
        "s": "0x56de3421fd0096629ff6cc6ca203570f639839f1197041ecf087b6ea8cceeb0c",
        "r": "0x651e54be12cc9a81c2a1bf8f1a32a2e4641a89a29cd48e68494d09c7b6353464",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8cd1485da23b00e0144f530f127968b53551adbf12bf0fe01111f237dc5718e7",
      "signature": {
        "s": "0x35123016c94dc3b023ebe5d3df373ff8e5a61168ce931d99a4c75ddc6f165df9",
        "r": "0x68748a07ca75c1536dae8c562bbd31e4f6af23fe6ffb6d4dd4b0bf1f1668ff58",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "34905411628882891668",
    "total": "979479788560407919532"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "34905411628882891668",
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
            "amount": "27618542023221509283951"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "34905411628882891"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZDU4NGE0MS1kNzEzLTU3NjgtODM0Ny0xYTMxNDNkOGI0ODQifQ==",
    "nonce": 110905,
    "balances": {
      "current": "354136878309105712924493",
      "previous": "354171818626146224699052"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5da603da13aa6f1d4769be805f271364e13c7f66",
    "nonce": 46,
    "balances": {
      "current": "1472251204708799715226",
      "previous": "1437345793079916823558"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:36.514Z",
  "updated": "2022-05-04T08:55:36.624Z",
  "id": "62723f883592fd001130b575"
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
0x0f200f9b00000000000000000000000000000000000000000000004fcf96fe5c88e9979a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1472251204708799715226`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`