# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4E7F3F577963265617541bf1661C6389FE133574`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001176a6fee4992464950000000000000000000000000000000000000000000000000000000433b0c7410000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000433b0c74100000000000000000000000000000000000000000000000705643a755f3dfadf62f8917f4def850d1448a6e87e7f54b231248402f77013a4d2c15e016e70cb29de8002847e3a86f437ac7e6b02688904ce45beb07f7a299f2da091683b077d9426609c8358e0627dc93c2914d3a34002459c91a949ccaaabbea0b028c828eea3000000000000000000000000000000000000000000000000000000000000001c17746944d9ad14eae12855875e21ad0dc6cf49115ce804e083d5ba22bafe034cdebd8840990fcb2153b5b9648121f7cd2f869b0fb5a229b7167435e3ee0b5e94759083546c2f541b20c7f4cd8c6cc2b86c69111f27c6cc551ca15d55ae583f2c000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b06d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004eeec5b0dda4fb276a13000000000000000000000000000000000000000000004eeec5b0dda92feb91c800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000011360740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d83239ffd42cc659930000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c597a42684e47513159793034596a566b4c5455784e3255744f544579595330344d544d30596d5a6c59574a69596d4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004e7f3f577963265617541bf1661c6389fe13357400000000000000000000000000000000000000000000001176a6fee49924649500000000000000000000000000000000000000000000001176a6fee065739d5400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x62f8917f4def850d1448a6e87e7f54b231248402f77013a4d2c15e016e70cb29",
      "signature": {
        "s": "0x26609c8358e0627dc93c2914d3a34002459c91a949ccaaabbea0b028c828eea3",
        "r": "0xde8002847e3a86f437ac7e6b02688904ce45beb07f7a299f2da091683b077d94",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x17746944d9ad14eae12855875e21ad0dc6cf49115ce804e083d5ba22bafe034c",
      "signature": {
        "s": "0x759083546c2f541b20c7f4cd8c6cc2b86c69111f27c6cc551ca15d55ae583f2c",
        "r": "0xdebd8840990fcb2153b5b9648121f7cd2f869b0fb5a229b7167435e3ee0b5e94",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18047092545",
    "total": "129515708259611048671"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18047092545",
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
            "amount": "27599948339331807467923"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "18047092"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlYzBhNGQ1Yy04YjVkLTUxN2UtOTEyYS04MTM0YmZlYWJiYmMifQ==",
    "nonce": 110701,
    "balances": {
      "current": "372749155882697230871059",
      "previous": "372749155882715296010696"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4e7f3f577963265617541bf1661c6389fe133574",
    "nonce": 46,
    "balances": {
      "current": "322144450453447140501",
      "previous": "322144450435400047956"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:35.603Z",
  "updated": "2022-05-04T08:54:35.799Z",
  "id": "62723f4b3592fd001130b531"
}
```
* *stageAmount*: `322144450453447140501`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000433b0c7410000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000433b0c74100000000000000000000000000000000000000000000000705643a755f3dfadf62f8917f4def850d1448a6e87e7f54b231248402f77013a4d2c15e016e70cb29de8002847e3a86f437ac7e6b02688904ce45beb07f7a299f2da091683b077d9426609c8358e0627dc93c2914d3a34002459c91a949ccaaabbea0b028c828eea3000000000000000000000000000000000000000000000000000000000000001c17746944d9ad14eae12855875e21ad0dc6cf49115ce804e083d5ba22bafe034cdebd8840990fcb2153b5b9648121f7cd2f869b0fb5a229b7167435e3ee0b5e94759083546c2f541b20c7f4cd8c6cc2b86c69111f27c6cc551ca15d55ae583f2c000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b06d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004eeec5b0dda4fb276a13000000000000000000000000000000000000000000004eeec5b0dda92feb91c800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000011360740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d83239ffd42cc659930000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c597a42684e47513159793034596a566b4c5455784e3255744f544579595330344d544d30596d5a6c59574a69596d4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004e7f3f577963265617541bf1661c6389fe13357400000000000000000000000000000000000000000000001176a6fee49924649500000000000000000000000000000000000000000000001176a6fee065739d5400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x62f8917f4def850d1448a6e87e7f54b231248402f77013a4d2c15e016e70cb29",
      "signature": {
        "s": "0x26609c8358e0627dc93c2914d3a34002459c91a949ccaaabbea0b028c828eea3",
        "r": "0xde8002847e3a86f437ac7e6b02688904ce45beb07f7a299f2da091683b077d94",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x17746944d9ad14eae12855875e21ad0dc6cf49115ce804e083d5ba22bafe034c",
      "signature": {
        "s": "0x759083546c2f541b20c7f4cd8c6cc2b86c69111f27c6cc551ca15d55ae583f2c",
        "r": "0xdebd8840990fcb2153b5b9648121f7cd2f869b0fb5a229b7167435e3ee0b5e94",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18047092545",
    "total": "129515708259611048671"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18047092545",
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
            "amount": "27599948339331807467923"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "18047092"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlYzBhNGQ1Yy04YjVkLTUxN2UtOTEyYS04MTM0YmZlYWJiYmMifQ==",
    "nonce": 110701,
    "balances": {
      "current": "372749155882697230871059",
      "previous": "372749155882715296010696"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4e7f3f577963265617541bf1661c6389fe133574",
    "nonce": 46,
    "balances": {
      "current": "322144450453447140501",
      "previous": "322144450435400047956"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:35.603Z",
  "updated": "2022-05-04T08:54:35.799Z",
  "id": "62723f4b3592fd001130b531"
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
0x0f200f9b00000000000000000000000000000000000000000000001176a6fee4992464950000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `322144450453447140501`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`