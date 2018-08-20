# [Polling Application - NOS]

For code review: https://github.com/blascokoa/nospollsystem

original REPO: https://github.com/blascokoa/nOSpoll
See contributors there.

# What is nOSpoll?
nOSpoll is a DApp created to utilize the NEO blockchain as a decision making tool for organizations, using a blockchain for public polls would be most desirable as these decision-making requires trust and a publicly verifiable and transparent system. 


# Prerequisites
You should have node and npm installed in your system.


# Download and Installation

To begin using this app, follow steps to get started:
* Clone the repo
* Run `npm install`
* After this run `npm start` which will launch the application in your local

# SmartContract Deploy

Scripthash = 0x0dfbdd64e96689d5f4cfe5d289bf96bd5b270a1b

* Instructions for deploy it:  import contract /smart-contracts/contract.avm 0710 05 True False
* invoke 0x0dfbdd64e96689d5f4cfe5d289bf96bd5b270a1b operation ["args"]

# SmartContract Operation Codes:
  
  * *Create*: invoke 0x0dfbdd64e96689d5f4cfe5d289bf96bd5b270a1b create ["PollCreatorPublicAdd","PollID","Question"]

    Allow to create a poll.
    
  * *Access*: invoke 0x0dfbdd64e96689d5f4cfe5d289bf96bd5b270a1b access ["PollCreatorPublicAdd","PollID"]

    With Owner Address and Poll Id generated during the create phase, an user can access the poll.
    
  * *Vote*: invoke 0x0dfbdd64e96689d5f4cfe5d289bf96bd5b270a1b vote ["PollOwnerPublickAdd","PollID","OptionVoted"]

    With Owner Address and Poll Id generated during the create phase, an user can vote. 
      
  * *Results*: invoke 0x0dfbdd64e96689d5f4cfe5d289bf96bd5b270a1b results ["PollOwnerPublickAdd","PollID"]

    With Owner Address and Poll Id generated during the create phase, it is possible to get the results.
    


