# Open-Source Services

***TheBettermint*** backend was built using a series of typescript packages, a nodejs backend framework, and Docker containers for deployment. 
 
***registry*** ( [github](https://github.com/thebettermint/registry) | [npm](https://github.com/thebettermint/registry/packages/1491220) )
<br>A package was created to store all nonprofit information including wallet address, ein, initiatives, etc. See [here](https://github.com/thebettermint/registry) for more information.
<br>*Technologies used: typescript, npm, xrpl.js, jest*
 
***xrpl-tx-parser***  ( [github](https://github.com/thebettermint/xrpl-tx-parser) | [npm](https://github.com/thebettermint/xrpl-tx-parser/packages/1505301) )
<br>A package was created to listen for incoming payments made to our registered organizations on the XLS20 devnet. These transactions are then parsed and passed back. See [here](https://github.com/thebettermint/xrpl-tx-parser) for more information.
<br>*Technologies used: typescript, npm, xrpl.js, jest*
 
***xrpl-xaddress-manager*** ( [github](https://github.com/thebettermint/xrpl-xaddress-manager) ) 
<br>A package was created to track XRPL account balances that are using destination tags. This package comes in handy for nonprofit organizations that would like to manage multiple donation initiatives using the same XRPL address. See [here](https://github.com/thebettermint/xrpl-xaddress-manager) for more information.
<br>*Technologies used: typescript, npm, xrpl, jest, mongdb, xrpl-tx-parser*
 
***xrpl-pay-bot*** ( [github](https://github.com/thebettermint/xrpl-pay-bot) )
<br>A package was created to send payments to our registry walls as a means of testing the mint-bot. See [here](https://github.com/thebettermint/xrpl-pay-bot) for more information.
<br>*Technologies used: typescript, npm, xrpl.js, jest, xrpl-accountlib*
 
***xrpl-auto-funder***  ( [github](https://github.com/thebettermint/xrpl-auto-funder) | [npm](https://github.com/thebettermint/xrpl-auto-funder/packages/1507700) )
<br>A package was created to auto-fund all wallets within the registry. The package uses the publicly provided faucets to programmatically create a new funded account and then send the fund to our wallets. The package supports the following faucets: testnet, devnet, xls20 devnet, hooksv2. See [here](https://github.com/thebettermint/xrpl-auto-funder) for more information.
<br>*Technologies used: typescript, npm, xrpl.js, jest*
 
***xrpl-mint-bot*** ( [github](https://github.com/thebettermint/xrpl-mint-bot) )
<br>A package was created to auto-mint NFT receipts for payments sent to the wallets within the registry. The package will only mint an NFT if the destination tag matches our registry. Payments are categorized by their amount and tiered ( bronze, silver, gold) NFT is automatically minted and offered to the donor's account. See [here](https://github.com/thebettermint/xrpl-mint-bot) for more information.
<br>*Technologies used: typescript, npm, xrpl.js, jest, mongodb, express, ipfs, docker, xrpl-tx-parser*
