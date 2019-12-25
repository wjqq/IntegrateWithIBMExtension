# IntegrateWithIBMExtension

This is hello world work with IBM Blockchain Platform VS Code extension

1 - Install the IBM Blockchain Platform VS Code extension 

https://cloud.ibm.com/docs/services/blockchain/howto?topic=blockchain-develop-vscode


2 - Based on the sample chaincode, add one more method history to query the history of user's balance.

func (cc *Chaincode) history(stub shim.ChaincodeStubInterface, args []string) sc.Response..

2.0 First intializate the balance user a and b with 100, 200 seprately.

2.1 invoke method "invoke", transfer 54 from a to b.
[12/25/2019 5:38:38 PM] [INFO] submitting transaction invoke with args a,b,54 on channel mychannel

2.2 Query user a's balance changes like below.
[12/25/2019 5:39:01 PM] [SUCCESS] Returned value from history: [{"TxId":"4ce8716a0b851647c42b7aec23fa0e23d3c748be3f9694965900091ba72cc0c9", "Value":100},{"TxId":"9e61e302ecc63646e810c3fa11c95e484877410873780a4226266dae55c129e9", "Value":46}]

2.3 Query user b's balance changes like below.
[12/25/2019 5:39:19 PM] [SUCCESS] Returned value from history: [{"TxId":"4ce8716a0b851647c42b7aec23fa0e23d3c748be3f9694965900091ba72cc0c9", "Value":200},{"TxId":"9e61e302ecc63646e810c3fa11c95e484877410873780a4226266dae55c129e9", "Value":254}]


***If you want to interact with the Network built with the Plugin, please refer to the https://github.com/wjqq/hfclient project, see file query_plugin.js how to connect it. ***

