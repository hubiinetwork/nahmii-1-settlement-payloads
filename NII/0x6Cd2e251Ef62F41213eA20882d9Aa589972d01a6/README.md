# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6Cd2e251Ef62F41213eA20882d9Aa589972d01a6`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000007a875ab5d81a9970000000000000000000000000000000000000000000000000000000004d4fccf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000004d4fccf0000000000000000000000000000000000000000000000000000000070c4ee71e953d6ac4f5f4b69545a7192438838d130ed92d4cf0d7d756348b1209e4788a14b08593e817378e6cf6b5bbf5212c24ad4e980b2ba769e7e70fbe09d753407113c93581180cb2bc2487ec2644091841feb83600cb72832a211824d13b1a0a28c000000000000000000000000000000000000000000000000000000000000001c11887a8282e68c3b888391417ea3f4f5b512a9f659dc248f7357c292c912bdbce9270573be37cebbb5140db8b45249248bcdb5fa3d07fa59c406c1f39695f4b0496ca6ac07521c051cbed545848f999abdee666c12a07d16fb51abbfd89e94b7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0cd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bb83f9eb41b4b674308000000000000000000000000000000000000000000004bb83f9eb41b503d7c8200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000013cab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d904950ffb70fa750d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d4441314d6d46684e7930335a6d4d354c5455304e446374596a59334d4331694d444a6c59544e6d4f475a68596a516966513d3d000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000006cd2e251ef62f41213ea20882d9aa589972d01a600000000000000000000000000000000000000000000000007a875ab5d81a99700000000000000000000000000000000000000000000000007a875ab58acacc800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe953d6ac4f5f4b69545a7192438838d130ed92d4cf0d7d756348b1209e4788a1",
      "signature": {
        "s": "0x3c93581180cb2bc2487ec2644091841feb83600cb72832a211824d13b1a0a28c",
        "r": "0x4b08593e817378e6cf6b5bbf5212c24ad4e980b2ba769e7e70fbe09d75340711",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x11887a8282e68c3b888391417ea3f4f5b512a9f659dc248f7357c292c912bdbc",
      "signature": {
        "s": "0x496ca6ac07521c051cbed545848f999abdee666c12a07d16fb51abbfd89e94b7",
        "r": "0xe9270573be37cebbb5140db8b45249248bcdb5fa3d07fa59c406c1f39695f4b0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "81067215",
    "total": "1891954289"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "81067215",
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
            "amount": "27615106066063487038733"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "81067"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMDA1MmFhNy03ZmM5LTU0NDctYjY3MC1iMDJlYTNmOGZhYjQifQ==",
    "nonce": 110797,
    "balances": {
      "current": "357576271424285980443400",
      "previous": "357576271424286061591682"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6cd2e251ef62f41213ea20882d9aa589972d01a6",
    "nonce": 30,
    "balances": {
      "current": "551820333221521815",
      "previous": "551820333140454600"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:05.083Z",
  "updated": "2022-05-04T08:55:05.190Z",
  "id": "62723f693592fd001130b54e"
}
```
* *stageAmount*: `551820333221521815`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000004d4fccf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000004d4fccf0000000000000000000000000000000000000000000000000000000070c4ee71e953d6ac4f5f4b69545a7192438838d130ed92d4cf0d7d756348b1209e4788a14b08593e817378e6cf6b5bbf5212c24ad4e980b2ba769e7e70fbe09d753407113c93581180cb2bc2487ec2644091841feb83600cb72832a211824d13b1a0a28c000000000000000000000000000000000000000000000000000000000000001c11887a8282e68c3b888391417ea3f4f5b512a9f659dc248f7357c292c912bdbce9270573be37cebbb5140db8b45249248bcdb5fa3d07fa59c406c1f39695f4b0496ca6ac07521c051cbed545848f999abdee666c12a07d16fb51abbfd89e94b7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0cd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bb83f9eb41b4b674308000000000000000000000000000000000000000000004bb83f9eb41b503d7c8200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000013cab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d904950ffb70fa750d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d4441314d6d46684e7930335a6d4d354c5455304e446374596a59334d4331694d444a6c59544e6d4f475a68596a516966513d3d000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000006cd2e251ef62f41213ea20882d9aa589972d01a600000000000000000000000000000000000000000000000007a875ab5d81a99700000000000000000000000000000000000000000000000007a875ab58acacc800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe953d6ac4f5f4b69545a7192438838d130ed92d4cf0d7d756348b1209e4788a1",
      "signature": {
        "s": "0x3c93581180cb2bc2487ec2644091841feb83600cb72832a211824d13b1a0a28c",
        "r": "0x4b08593e817378e6cf6b5bbf5212c24ad4e980b2ba769e7e70fbe09d75340711",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x11887a8282e68c3b888391417ea3f4f5b512a9f659dc248f7357c292c912bdbc",
      "signature": {
        "s": "0x496ca6ac07521c051cbed545848f999abdee666c12a07d16fb51abbfd89e94b7",
        "r": "0xe9270573be37cebbb5140db8b45249248bcdb5fa3d07fa59c406c1f39695f4b0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "81067215",
    "total": "1891954289"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "81067215",
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
            "amount": "27615106066063487038733"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "81067"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMDA1MmFhNy03ZmM5LTU0NDctYjY3MC1iMDJlYTNmOGZhYjQifQ==",
    "nonce": 110797,
    "balances": {
      "current": "357576271424285980443400",
      "previous": "357576271424286061591682"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6cd2e251ef62f41213ea20882d9aa589972d01a6",
    "nonce": 30,
    "balances": {
      "current": "551820333221521815",
      "previous": "551820333140454600"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:05.083Z",
  "updated": "2022-05-04T08:55:05.190Z",
  "id": "62723f693592fd001130b54e"
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
0x0f200f9b00000000000000000000000000000000000000000000000007a875ab5d81a9970000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `551820333221521815`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`