## Settlement of NII
The steps outlined below are recommended in order to settle the Nahmii 1 balance of NII of account `0xC4EE132Ec2Ca460cC7998838aEf527dEd72DF457`. The contract function invocation payloads required are included in directories named according to the execution order of the steps.
### Ordered set of steps:
0. [DriipSettlementChallengeByPayment.stopChallenge](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#writeContract)
1. [DriipSettlementChallengeByPayment.startChallengeFromPayment](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#writeContract)
2. [DriipSettlementByPayment.settlePayment](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#writeContract)
3. [ClientFund.withdraw](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#writeContract)
