# [Polling Application - NOS]

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

Scripthash = 0xf3c691a512878f4c3823a3019eba04c33f6a6083

* Instructions for deploy it:  import contract /smart-contracts/nospollcontract.avm 0710 07 True False
* invoke 0xf3c691a512878f4c3823a3019eba04c33f6a6083 operation ["args"]

# SmartContract Operation Codes:
  
  * *Create*: invoke 0xf3c691a512878f4c3823a3019eba04c33f6a6083 create ["PollCreatorPublicAdd","PollID","Question"]

    The ID must he returned by the function GetStorage from NOS. `key = PollCreatorPublicAdd+"ID"`
    
  * *Access*: invoke 0xf3c691a512878f4c3823a3019eba04c33f6a6083 access ["PollCreatorPublicAdd","PollID"]

    The question must be returned using the function GetStorage from NOS `key = PollCreatorPublicAdd+ID`
    
  * *Vote*: invoke 0xf3c691a512878f4c3823a3019eba04c33f6a6083 vote ["PollOwnerPublickAdd","PollID","OptionVoted"]

    Will store the results and the data must be returned with the getStorage from NOS api `key = PollCreatorPublicAdd+ID+"V"` The string will got a format like:  `0ABAABBBAAA` 
      
  * *Results*: invoke 0xf3c691a512878f4c3823a3019eba04c33f6a6083 results ["PollOwnerPublickAdd","PollID"]

    The data must be returned with the getStorage from NOS api `key = PollCreatorPublicAdd+ID+"V"` The string will got a format like:  `0ABAABBBAAA`
    


