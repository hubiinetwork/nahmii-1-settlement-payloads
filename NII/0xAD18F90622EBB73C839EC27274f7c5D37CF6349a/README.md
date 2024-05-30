# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAD18F90622EBB73C839EC27274f7c5D37CF6349a`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de12691d2b2b0000000000000000000000000000000000000000000000000f349ce01b565c080000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000f349ce01b565c080000000000000000000000000000000000000000000000000f349ce01b565c080004227b08179afbf694f05eb268893016180ee593a78e117c459e4fa03c7e40de55f4920fe2e60b156bf53e0da3428f6c72d71c7d3a6ad0ddc919b4a2bde72ea210987141a5895e90b27470ab146024780fa7004573e9622ce385c42205f2cc68a000000000000000000000000000000000000000000000000000000000000001c1d05318ccfd9c998c1184f99ef7d048af665e5406c138510bd84dad85e31936aee1d5714eefeb54ce431ecdc2c1c4d109511e54dc5bfc202fd61ab8f70b6226a4dfd697103ba81b62ba06a098d5201aaa91437537b95f8ec7fe63effcb783a2e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1bf7c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000004000000000000000000000000ad18f90622ebb73c839ec27274f7c5d37cf6349a0000000000000000000000000000000000000000000000000de12691d2b2b0000000000000000000000000000000000000000000000000f395f74ca1c518800000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000003e48245a8ca550000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003e48245a8ca550000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e7a67344e7a4a6c4e5331685a6a6b794c54526b4e5455744f57457a4e5330774e7a4a6b4e5749325a57566a5954636966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001a3ddbfab3af26a6e24700000000000000000000000000000000000000000000194a922cb1f9c0e6624700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4227b08179afbf694f05eb268893016180ee593a78e117c459e4fa03c7e40de5",
      "signature": {
        "s": "0x0987141a5895e90b27470ab146024780fa7004573e9622ce385c42205f2cc68a",
        "r": "0x5f4920fe2e60b156bf53e0da3428f6c72d71c7d3a6ad0ddc919b4a2bde72ea21",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1d05318ccfd9c998c1184f99ef7d048af665e5406c138510bd84dad85e31936a",
      "signature": {
        "s": "0x4dfd697103ba81b62ba06a098d5201aaa91437537b95f8ec7fe63effcb783a2e",
        "r": "0xee1d5714eefeb54ce431ecdc2c1c4d109511e54dc5bfc202fd61ab8f70b6226a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4487877000000000000000",
    "total": "4487877000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4487877000000000000000",
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
            "amount": "4487877000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4487877000000000000"
      }
    },
    "wallet": "0xad18f90622ebb73c839ec27274f7c5d37cf6349a",
    "data": "eyJyZWYiOiI1Nzg4NzJlNS1hZjkyLTRkNTUtOWEzNS0wNzJkNWI2ZWVjYTcifQ==",
    "nonce": 4,
    "balances": {
      "current": "1000123000000000000",
      "previous": "4493365000000000000000"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 21,
    "balances": {
      "current": "123922631122510391206471",
      "previous": "119434754122510391206471"
    }
  },
  "blockNumber": "14794620",
  "created": "2022-05-17T20:28:02.961Z",
  "updated": "2022-05-17T20:28:03.044Z",
  "id": "628405527832e20011830ef3"
}
```
* *stageAmount*: `1000123000000000000`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000f349ce01b565c080000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000f349ce01b565c080000000000000000000000000000000000000000000000000f349ce01b565c080004227b08179afbf694f05eb268893016180ee593a78e117c459e4fa03c7e40de55f4920fe2e60b156bf53e0da3428f6c72d71c7d3a6ad0ddc919b4a2bde72ea210987141a5895e90b27470ab146024780fa7004573e9622ce385c42205f2cc68a000000000000000000000000000000000000000000000000000000000000001c1d05318ccfd9c998c1184f99ef7d048af665e5406c138510bd84dad85e31936aee1d5714eefeb54ce431ecdc2c1c4d109511e54dc5bfc202fd61ab8f70b6226a4dfd697103ba81b62ba06a098d5201aaa91437537b95f8ec7fe63effcb783a2e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1bf7c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000004000000000000000000000000ad18f90622ebb73c839ec27274f7c5d37cf6349a0000000000000000000000000000000000000000000000000de12691d2b2b0000000000000000000000000000000000000000000000000f395f74ca1c518800000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000003e48245a8ca550000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003e48245a8ca550000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e7a67344e7a4a6c4e5331685a6a6b794c54526b4e5455744f57457a4e5330774e7a4a6b4e5749325a57566a5954636966513d3d0000000000000000000000000000000000000000000000000000000000000015000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001a3ddbfab3af26a6e24700000000000000000000000000000000000000000000194a922cb1f9c0e6624700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4227b08179afbf694f05eb268893016180ee593a78e117c459e4fa03c7e40de5",
      "signature": {
        "s": "0x0987141a5895e90b27470ab146024780fa7004573e9622ce385c42205f2cc68a",
        "r": "0x5f4920fe2e60b156bf53e0da3428f6c72d71c7d3a6ad0ddc919b4a2bde72ea21",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1d05318ccfd9c998c1184f99ef7d048af665e5406c138510bd84dad85e31936a",
      "signature": {
        "s": "0x4dfd697103ba81b62ba06a098d5201aaa91437537b95f8ec7fe63effcb783a2e",
        "r": "0xee1d5714eefeb54ce431ecdc2c1c4d109511e54dc5bfc202fd61ab8f70b6226a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4487877000000000000000",
    "total": "4487877000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4487877000000000000000",
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
            "amount": "4487877000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4487877000000000000"
      }
    },
    "wallet": "0xad18f90622ebb73c839ec27274f7c5d37cf6349a",
    "data": "eyJyZWYiOiI1Nzg4NzJlNS1hZjkyLTRkNTUtOWEzNS0wNzJkNWI2ZWVjYTcifQ==",
    "nonce": 4,
    "balances": {
      "current": "1000123000000000000",
      "previous": "4493365000000000000000"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 21,
    "balances": {
      "current": "123922631122510391206471",
      "previous": "119434754122510391206471"
    }
  },
  "blockNumber": "14794620",
  "created": "2022-05-17T20:28:02.961Z",
  "updated": "2022-05-17T20:28:03.044Z",
  "id": "628405527832e20011830ef3"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de12691d2b2b0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000123000000000000`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`