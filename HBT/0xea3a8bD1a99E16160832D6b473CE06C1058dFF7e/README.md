# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xea3a8bD1a99E16160832D6b473CE06C1058dFF7e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000d3e7730000000000000000000000000000000000000000000000000000000000d3e773000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000d3e7730000000000000000000000000000000000000000000000000000000000d3e7738bcd0882814144ebf053543f3dadcbe3f36fd4ec277f6dd83319a41657bade28e72211c32aa1868117fc257838a152f5b42a02ee7b9502aad89cb6707ce990684cec1d40a311fa8437c080642bfbd2a73ae84dff96ad4bc27e4f762a012461f6000000000000000000000000000000000000000000000000000000000000001ce36d30d587cf0189ca73b06e2224f8fff18d5ab8937608a0031fe8090ac508a41a381c943aa1dfaba07c210f28a3f7c4b25a0b77bc42e483a29acd196fae14c6571808b869508c61707d28fe8512e3ec7502f500709910af6bc166a583a40215000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56aa00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bab00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e150cca972ffc000000000000000000000000000000000000000000000000002e150ccb6b4dae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000363f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ade460365000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a4745335a6a4d324d5330315a474e6b4c545578595759744f5441324e5330794e574530596a466a4f44646c596a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000ea3a8bd1a99e16160832d6b473ce06c1058dff7e0000000000000000000000000000000000000000000000000000000000d3e773000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8bcd0882814144ebf053543f3dadcbe3f36fd4ec277f6dd83319a41657bade28",
      "signature": {
        "s": "0x4cec1d40a311fa8437c080642bfbd2a73ae84dff96ad4bc27e4f762a012461f6",
        "r": "0xe72211c32aa1868117fc257838a152f5b42a02ee7b9502aad89cb6707ce99068",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe36d30d587cf0189ca73b06e2224f8fff18d5ab8937608a0031fe8090ac508a4",
      "signature": {
        "s": "0x571808b869508c61707d28fe8512e3ec7502f500709910af6bc166a583a40215",
        "r": "0x1a381c943aa1dfaba07c210f28a3f7c4b25a0b77bc42e483a29acd196fae14c6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "13887347",
    "total": "13887347"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13887347",
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
            "amount": "46678803301"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13887"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZGE3ZjM2MS01ZGNkLTUxYWYtOTA2NS0yNWE0YjFjODdlYjgifQ==",
    "nonce": 7083,
    "balances": {
      "current": "12970993611386876",
      "previous": "12970993625288110"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xea3a8bd1a99e16160832d6b473ce06c1058dff7e",
    "nonce": 22,
    "balances": {
      "current": "13887347",
      "previous": "0"
    }
  },
  "blockNumber": "10114730",
  "created": "2020-05-22T08:54:10.540Z",
  "updated": "2020-05-22T08:54:10.611Z",
  "id": "5ec79332b0c6090011d5b20f"
}
```
* *stageAmount*: `13887347`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000d3e773000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000d3e7730000000000000000000000000000000000000000000000000000000000d3e7738bcd0882814144ebf053543f3dadcbe3f36fd4ec277f6dd83319a41657bade28e72211c32aa1868117fc257838a152f5b42a02ee7b9502aad89cb6707ce990684cec1d40a311fa8437c080642bfbd2a73ae84dff96ad4bc27e4f762a012461f6000000000000000000000000000000000000000000000000000000000000001ce36d30d587cf0189ca73b06e2224f8fff18d5ab8937608a0031fe8090ac508a41a381c943aa1dfaba07c210f28a3f7c4b25a0b77bc42e483a29acd196fae14c6571808b869508c61707d28fe8512e3ec7502f500709910af6bc166a583a40215000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56aa00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bab00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e150cca972ffc000000000000000000000000000000000000000000000000002e150ccb6b4dae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000363f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ade460365000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a4745335a6a4d324d5330315a474e6b4c545578595759744f5441324e5330794e574530596a466a4f44646c596a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000ea3a8bd1a99e16160832d6b473ce06c1058dff7e0000000000000000000000000000000000000000000000000000000000d3e773000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8bcd0882814144ebf053543f3dadcbe3f36fd4ec277f6dd83319a41657bade28",
      "signature": {
        "s": "0x4cec1d40a311fa8437c080642bfbd2a73ae84dff96ad4bc27e4f762a012461f6",
        "r": "0xe72211c32aa1868117fc257838a152f5b42a02ee7b9502aad89cb6707ce99068",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe36d30d587cf0189ca73b06e2224f8fff18d5ab8937608a0031fe8090ac508a4",
      "signature": {
        "s": "0x571808b869508c61707d28fe8512e3ec7502f500709910af6bc166a583a40215",
        "r": "0x1a381c943aa1dfaba07c210f28a3f7c4b25a0b77bc42e483a29acd196fae14c6",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "13887347",
    "total": "13887347"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13887347",
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
            "amount": "46678803301"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13887"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZGE3ZjM2MS01ZGNkLTUxYWYtOTA2NS0yNWE0YjFjODdlYjgifQ==",
    "nonce": 7083,
    "balances": {
      "current": "12970993611386876",
      "previous": "12970993625288110"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xea3a8bd1a99e16160832d6b473ce06c1058dff7e",
    "nonce": 22,
    "balances": {
      "current": "13887347",
      "previous": "0"
    }
  },
  "blockNumber": "10114730",
  "created": "2020-05-22T08:54:10.540Z",
  "updated": "2020-05-22T08:54:10.611Z",
  "id": "5ec79332b0c6090011d5b20f"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000d3e773000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13887347`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`