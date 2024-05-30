# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9C0BCA4c95Ecf9507c05eD9Ae34123fB381387Eb`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000002afe2300000000000000000000000000000000000000000000000000000000002afe23000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002afe2300000000000000000000000000000000000000000000000000000000002afe23315b4e62887b38dcf72368bfa3e535d7b7ac1240ee2a1a167fefd9a5c3dace56b65569493ef62422581d9ad7c7437d7cb3a110284d8028d50acaea02f311d8444b973821a3f09530d2f06cf63499d673f1cef6c88094a6db4db602c8b16d107f000000000000000000000000000000000000000000000000000000000000001c47e46588a56cfe821f6cb68d0636863b18a3ab7e9347129ed543dfa223bfabded61c579580b709eacd9bfd2641a1e0d3c0f9a6eee679efc47c8eae8eeb9f7443508795d5c028e4942ba7177522c9de337679161df8faa4d15b06b2b03d6a92a2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a9800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e163985321ffd000000000000000000000000000000000000000000000000002e1639855d292100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000b01000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a915d2216000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493159325178596a6378597930304f54426b4c54566c596a6b7459574e694e53316a4e6a4e6b4f446c68597a597a5957596966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000009c0bca4c95ecf9507c05ed9ae34123fb381387eb00000000000000000000000000000000000000000000000000000000002afe23000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x315b4e62887b38dcf72368bfa3e535d7b7ac1240ee2a1a167fefd9a5c3dace56",
      "signature": {
        "s": "0x4b973821a3f09530d2f06cf63499d673f1cef6c88094a6db4db602c8b16d107f",
        "r": "0xb65569493ef62422581d9ad7c7437d7cb3a110284d8028d50acaea02f311d844",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x47e46588a56cfe821f6cb68d0636863b18a3ab7e9347129ed543dfa223bfabde",
      "signature": {
        "s": "0x508795d5c028e4942ba7177522c9de337679161df8faa4d15b06b2b03d6a92a2",
        "r": "0xd61c579580b709eacd9bfd2641a1e0d3c0f9a6eee679efc47c8eae8eeb9f7443",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2817571",
    "total": "2817571"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2817571",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "45388472854"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2817"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1Y2QxYjcxYy00OTBkLTVlYjktYWNiNS1jNjNkODlhYzYzYWYifQ==",
    "nonce": 6808,
    "balances": {
      "current": "12972285232291837",
      "previous": "12972285235112225"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c0bca4c95ecf9507c05ed9ae34123fb381387eb",
    "nonce": 6,
    "balances": {
      "current": "2817571",
      "previous": "0"
    }
  },
  "blockNumber": "10114715",
  "created": "2020-05-22T08:51:48.602Z",
  "updated": "2020-05-22T08:51:48.670Z",
  "id": "5ec792a4b0c6090011d5b1aa"
}
```
* *stageAmount*: `2817571`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000002afe23000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002afe2300000000000000000000000000000000000000000000000000000000002afe23315b4e62887b38dcf72368bfa3e535d7b7ac1240ee2a1a167fefd9a5c3dace56b65569493ef62422581d9ad7c7437d7cb3a110284d8028d50acaea02f311d8444b973821a3f09530d2f06cf63499d673f1cef6c88094a6db4db602c8b16d107f000000000000000000000000000000000000000000000000000000000000001c47e46588a56cfe821f6cb68d0636863b18a3ab7e9347129ed543dfa223bfabded61c579580b709eacd9bfd2641a1e0d3c0f9a6eee679efc47c8eae8eeb9f7443508795d5c028e4942ba7177522c9de337679161df8faa4d15b06b2b03d6a92a2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a9800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e163985321ffd000000000000000000000000000000000000000000000000002e1639855d292100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000b01000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a915d2216000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493159325178596a6378597930304f54426b4c54566c596a6b7459574e694e53316a4e6a4e6b4f446c68597a597a5957596966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000009c0bca4c95ecf9507c05ed9ae34123fb381387eb00000000000000000000000000000000000000000000000000000000002afe23000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x315b4e62887b38dcf72368bfa3e535d7b7ac1240ee2a1a167fefd9a5c3dace56",
      "signature": {
        "s": "0x4b973821a3f09530d2f06cf63499d673f1cef6c88094a6db4db602c8b16d107f",
        "r": "0xb65569493ef62422581d9ad7c7437d7cb3a110284d8028d50acaea02f311d844",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x47e46588a56cfe821f6cb68d0636863b18a3ab7e9347129ed543dfa223bfabde",
      "signature": {
        "s": "0x508795d5c028e4942ba7177522c9de337679161df8faa4d15b06b2b03d6a92a2",
        "r": "0xd61c579580b709eacd9bfd2641a1e0d3c0f9a6eee679efc47c8eae8eeb9f7443",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2817571",
    "total": "2817571"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2817571",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "45388472854"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2817"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1Y2QxYjcxYy00OTBkLTVlYjktYWNiNS1jNjNkODlhYzYzYWYifQ==",
    "nonce": 6808,
    "balances": {
      "current": "12972285232291837",
      "previous": "12972285235112225"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c0bca4c95ecf9507c05ed9ae34123fb381387eb",
    "nonce": 6,
    "balances": {
      "current": "2817571",
      "previous": "0"
    }
  },
  "blockNumber": "10114715",
  "created": "2020-05-22T08:51:48.602Z",
  "updated": "2020-05-22T08:51:48.670Z",
  "id": "5ec792a4b0c6090011d5b1aa"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000002afe23000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2817571`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`