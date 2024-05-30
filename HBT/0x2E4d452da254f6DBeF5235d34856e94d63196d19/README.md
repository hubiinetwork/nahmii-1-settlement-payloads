# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2E4d452da254f6DBeF5235d34856e94d63196d19`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004238c57a000000000000000000000000000000000000000000000000000000004238c57a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004238c57a000000000000000000000000000000000000000000000000000000004238c57a6c05770239c91e5f5254d113cec1607e78038a3409a1fca8cdc93da1f9835784d7d1c6f0938893e835396b16d2d6d6413a3fd2721aef20d9b4b05a482c855ee0621759d0fe44d2ad0f10f1af6e74ac36e480701746f652201cc71ffd4bd3ce3f000000000000000000000000000000000000000000000000000000000000001bb53a06ee4f93027b2726ffa2b0b5ad7db3a8530c226274020b2cde647bddae1b8aec32d439a9bfe3ace44d8df6501ceadbd7a68aed51aa7b835d8291dfa21ef80dab9e0aa11cc234641bd42d66a1687ef63811a703bf7249f7ef7fc31b3787bc000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e181a0c300f9f000000000000000000000000000000000000000000000000002e181a4e79c90100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000010f3e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1678c20a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596a637a59545a684e7930344d4445774c5455354d44677459574e6d4d4330314d574d7a596a4d304d5446685957516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000002e4d452da254f6dbef5235d34856e94d63196d19000000000000000000000000000000000000000000000000000000004238c57a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6c05770239c91e5f5254d113cec1607e78038a3409a1fca8cdc93da1f9835784",
      "signature": {
        "s": "0x621759d0fe44d2ad0f10f1af6e74ac36e480701746f652201cc71ffd4bd3ce3f",
        "r": "0xd7d1c6f0938893e835396b16d2d6d6413a3fd2721aef20d9b4b05a482c855ee0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb53a06ee4f93027b2726ffa2b0b5ad7db3a8530c226274020b2cde647bddae1b",
      "signature": {
        "s": "0x0dab9e0aa11cc234641bd42d66a1687ef63811a703bf7249f7ef7fc31b3787bc",
        "r": "0x8aec32d439a9bfe3ace44d8df6501ceadbd7a68aed51aa7b835d8291dfa21ef8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1111016826",
    "total": "1111016826"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1111016826",
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
            "amount": "43326685706"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1111016"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYjczYTZhNy04MDEwLTU5MDgtYWNmMC01MWMzYjM0MTFhYWQifQ==",
    "nonce": 6435,
    "balances": {
      "current": "12974349081382815",
      "previous": "12974350193510657"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2e4d452da254f6dbef5235d34856e94d63196d19",
    "nonce": 22,
    "balances": {
      "current": "1111016826",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:09.944Z",
  "updated": "2020-05-22T08:49:10.044Z",
  "id": "5ec79205005df800101bcaa0"
}
```
* *stageAmount*: `1111016826`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004238c57a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004238c57a000000000000000000000000000000000000000000000000000000004238c57a6c05770239c91e5f5254d113cec1607e78038a3409a1fca8cdc93da1f9835784d7d1c6f0938893e835396b16d2d6d6413a3fd2721aef20d9b4b05a482c855ee0621759d0fe44d2ad0f10f1af6e74ac36e480701746f652201cc71ffd4bd3ce3f000000000000000000000000000000000000000000000000000000000000001bb53a06ee4f93027b2726ffa2b0b5ad7db3a8530c226274020b2cde647bddae1b8aec32d439a9bfe3ace44d8df6501ceadbd7a68aed51aa7b835d8291dfa21ef80dab9e0aa11cc234641bd42d66a1687ef63811a703bf7249f7ef7fc31b3787bc000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e181a0c300f9f000000000000000000000000000000000000000000000000002e181a4e79c90100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000010f3e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1678c20a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596a637a59545a684e7930344d4445774c5455354d44677459574e6d4d4330314d574d7a596a4d304d5446685957516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000002e4d452da254f6dbef5235d34856e94d63196d19000000000000000000000000000000000000000000000000000000004238c57a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6c05770239c91e5f5254d113cec1607e78038a3409a1fca8cdc93da1f9835784",
      "signature": {
        "s": "0x621759d0fe44d2ad0f10f1af6e74ac36e480701746f652201cc71ffd4bd3ce3f",
        "r": "0xd7d1c6f0938893e835396b16d2d6d6413a3fd2721aef20d9b4b05a482c855ee0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb53a06ee4f93027b2726ffa2b0b5ad7db3a8530c226274020b2cde647bddae1b",
      "signature": {
        "s": "0x0dab9e0aa11cc234641bd42d66a1687ef63811a703bf7249f7ef7fc31b3787bc",
        "r": "0x8aec32d439a9bfe3ace44d8df6501ceadbd7a68aed51aa7b835d8291dfa21ef8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1111016826",
    "total": "1111016826"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1111016826",
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
            "amount": "43326685706"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1111016"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYjczYTZhNy04MDEwLTU5MDgtYWNmMC01MWMzYjM0MTFhYWQifQ==",
    "nonce": 6435,
    "balances": {
      "current": "12974349081382815",
      "previous": "12974350193510657"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2e4d452da254f6dbef5235d34856e94d63196d19",
    "nonce": 22,
    "balances": {
      "current": "1111016826",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:09.944Z",
  "updated": "2020-05-22T08:49:10.044Z",
  "id": "5ec79205005df800101bcaa0"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004238c57a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1111016826`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`