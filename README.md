# Ali_Khatami_Hardhat2

### Hardhat Deploy

If we use only javascript to deploy our smart contract it is not saving our deployment to any file <br>

having everything inside deploy script for deploying can make test and deploy script not working together<br>

Here we gonna talk about hardhat deploy package <br>

It is the link of the package https://github.com/wighawag/hardhat-deploy <br>

It is Replicable Deployments And Easy Testing 

![h25](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/6990409b-f8cf-4c69-ba6a-0a0ad9ee706f)
Figure1: To add hardhat deploy we add the above command 

```
yarn add --dev hardhat-deploy

````
Then from this link https://github.com/wighawag/hardhat-deploy

we paste the code below : <br>



```
require('hardhat-deploy');

```

<br><br>

![d7](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/9c4c5dbc-5949-44ce-9273-1ddb908cb7ba)

We have to run the commmand given below <br>

```

yarn add --dev "@nomicfoundation/hardhat-network-helpers@^1.0.0" "@nomicfoundation/hardhat-verify@^1.0.0" "@types/mocha@>=9.1.0" "@typechain/ethers-v6@^0.4.0" "@typechain/hardhat@^8.0.0" "hardhat-gas-reporter@^1.0.8" "solidity-coverage@^0.8.1" "ts-node@>=8.0.0" "typechain@^8.2.0" "typescript@>=4.5.0"

```

<br>

Then I will give the command below: <br>

```
yarn hardhat

```

<br>

![d8](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/58aec6ec-dd59-460c-9219-e44afca648ab)

We can see a bunch of new task in here with one of them being deployed <br>

This deploy task gonna be the main task we use to deploy our contract <br>














![h26](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/8f0cfe15-effe-4fab-beaa-68cf066a6d46)
Figure2: Instead of writing our deploy scripts to script folder shown with red arrow <br>
we create a new folder for that and that is ```akrkdeploy``` <br>

This ```akrkdeploy``` folder is where hardhat deploy module will be to deploy our solidity code <br>

To write our scripts we have to add one more thing and that hardhat-deploy-ethers to our package here <br>

![d9](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/46f70c39-ed17-4f9d-b48f-7a4adf60d7db)


Figure3: here when we give the command 

```
yarn add -D @nomiclabs/hardhat-ethers@npm:hardhat-deploy-ethers@*
```

then we can see that at package.json file that hardhat ethers package is overriden by hardhat deploy ethers package <br>


Ok now we have setup we can run our deploy script <br>

the way that hardhat deploy works is the scripts get added to our akrkdeploy folder <br>

will get run when we run yarn hardhat deploy <br>

So a good way is to number them so that they run in order <br>
you want them to run <br>

Since we have one contract to deploy <br>




![h28](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/96f3ec65-c328-4377-a4df-8bfeae4e0c9c)
Figure4: inside the akrkdeploy folder it is better to give scripts number so that we can run them <br>
in orders <br>

Hardhat deploy is different from normal deploy here we don't need to have main functions <br>
nor we have to call main function <br>
It gonna run a specific function that we define inside the script <br>




![d10](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/115a7a85-5723-4bdb-998f-7aa9dbd3ce6a)


We gonna export this function as a default function for our hardhat deploy to look for  <br>


![d11](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/fb2ec79a-e99f-40f5-8c88-ae6da3f6b03e)

For that we write the above line of code <br>


![d12](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/3189f454-c276-45ec-b9c5-4b6eb548c74f)

here hre is hardhat runtime environment <br>

Whenever we run a deploy script , hardhat deploy automatically calls this function <br>

and just passes hardhat object into it <br>











