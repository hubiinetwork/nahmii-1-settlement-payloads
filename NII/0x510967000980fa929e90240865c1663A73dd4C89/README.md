# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x510967000980fa929e90240865c1663A73dd4C89`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000023bc21507aa17b856700000000000000000000000000000000000000000000000d478d3d080406a0a50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000d478d3d080406a0a5000000000000000000000000000000000000000000000023bc21507aa17b85670c01181d807418ed282a5e8a6b4f00b05a7be9dc895aeef3d5a988c6e935d602da18a86197e59110977d233b07cf41c03741000ced4d5101191616193c79235824b594f8c96e8b6121240d7fb2fffa563d73a38c0e0c5f6aea6b5961f055bb09000000000000000000000000000000000000000000000000000000000000001c531c6e35078aa4fddeeccd4349fccdfb167610ce9bedad7dc14773ff51b2b5a372268c25f12e449f2d741218b5af5fd8dc1e7fc586a7f8ff49900d0048c7a0b111470debac262eee048732207fc8ea189f1b79c92bfc22eee1c613b20b2073a7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7cf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000001c32235f877818622d55000000000000000000000000000000000000000000001c3f6e530d857eb7a8c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000003664905624edac80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e52bfebf77a3ec207f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d54417a4e3245795979316a4e7a51334c5455324d546b744f4749774d53316c595463774f54526c5a6a55774d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000510967000980fa929e90240865c1663a73dd4c89000000000000000000000000000000000000000000000023bc21507aa17b8567000000000000000000000000000000000000000000000016749413729d74e4c200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c01181d807418ed282a5e8a6b4f00b05a7be9dc895aeef3d5a988c6e935d602",
      "signature": {
        "s": "0x24b594f8c96e8b6121240d7fb2fffa563d73a38c0e0c5f6aea6b5961f055bb09",
        "r": "0xda18a86197e59110977d233b07cf41c03741000ced4d5101191616193c792358",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x531c6e35078aa4fddeeccd4349fccdfb167610ce9bedad7dc14773ff51b2b5a3",
      "signature": {
        "s": "0x11470debac262eee048732207fc8ea189f1b79c92bfc22eee1c613b20b2073a7",
        "r": "0x72268c25f12e449f2d741218b5af5fd8dc1e7fc586a7f8ff49900d0048c7a0b1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "244963517211269832869",
    "total": "659192247420821669223"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "244963517211269832869",
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
            "amount": "27839306988936000970879"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "244963517211269832"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMTAzN2EyYy1jNzQ3LTU2MTktOGIwMS1lYTcwOTRlZjUwMmMifQ==",
    "nonce": 112591,
    "balances": {
      "current": "133151147628899533466965",
      "previous": "133396356109628014569666"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x510967000980fa929e90240865c1663a73dd4c89",
    "nonce": 4,
    "balances": {
      "current": "659192247420821669223",
      "previous": "414228730209551836354"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:40.757Z",
  "updated": "2022-05-04T09:04:40.848Z",
  "id": "627241a8bbd75600116d081d"
}
```
* *stageAmount*: `659192247420821669223`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000d478d3d080406a0a50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000d478d3d080406a0a5000000000000000000000000000000000000000000000023bc21507aa17b85670c01181d807418ed282a5e8a6b4f00b05a7be9dc895aeef3d5a988c6e935d602da18a86197e59110977d233b07cf41c03741000ced4d5101191616193c79235824b594f8c96e8b6121240d7fb2fffa563d73a38c0e0c5f6aea6b5961f055bb09000000000000000000000000000000000000000000000000000000000000001c531c6e35078aa4fddeeccd4349fccdfb167610ce9bedad7dc14773ff51b2b5a372268c25f12e449f2d741218b5af5fd8dc1e7fc586a7f8ff49900d0048c7a0b111470debac262eee048732207fc8ea189f1b79c92bfc22eee1c613b20b2073a7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7cf000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000001c32235f877818622d55000000000000000000000000000000000000000000001c3f6e530d857eb7a8c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000003664905624edac80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e52bfebf77a3ec207f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d54417a4e3245795979316a4e7a51334c5455324d546b744f4749774d53316c595463774f54526c5a6a55774d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000510967000980fa929e90240865c1663a73dd4c89000000000000000000000000000000000000000000000023bc21507aa17b8567000000000000000000000000000000000000000000000016749413729d74e4c200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0c01181d807418ed282a5e8a6b4f00b05a7be9dc895aeef3d5a988c6e935d602",
      "signature": {
        "s": "0x24b594f8c96e8b6121240d7fb2fffa563d73a38c0e0c5f6aea6b5961f055bb09",
        "r": "0xda18a86197e59110977d233b07cf41c03741000ced4d5101191616193c792358",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x531c6e35078aa4fddeeccd4349fccdfb167610ce9bedad7dc14773ff51b2b5a3",
      "signature": {
        "s": "0x11470debac262eee048732207fc8ea189f1b79c92bfc22eee1c613b20b2073a7",
        "r": "0x72268c25f12e449f2d741218b5af5fd8dc1e7fc586a7f8ff49900d0048c7a0b1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "244963517211269832869",
    "total": "659192247420821669223"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "244963517211269832869",
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
            "amount": "27839306988936000970879"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "244963517211269832"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMTAzN2EyYy1jNzQ3LTU2MTktOGIwMS1lYTcwOTRlZjUwMmMifQ==",
    "nonce": 112591,
    "balances": {
      "current": "133151147628899533466965",
      "previous": "133396356109628014569666"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x510967000980fa929e90240865c1663a73dd4c89",
    "nonce": 4,
    "balances": {
      "current": "659192247420821669223",
      "previous": "414228730209551836354"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:40.757Z",
  "updated": "2022-05-04T09:04:40.848Z",
  "id": "627241a8bbd75600116d081d"
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
0x0f200f9b000000000000000000000000000000000000000000000023bc21507aa17b85670000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `659192247420821669223`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`