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


![h26](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/8f0cfe15-effe-4fab-beaa-68cf066a6d46)
Figure2: Instead of writing our deploy scripts to script folder shown with red arrow <br>
we create a new folder for that and that is ```akrkdeploy``` <br>

This ```akrkdeploy``` folder is where hardhat deploy module will be to deploy our solidity code <br>

To write our scripts we have to add one more thing and that hardhat-deploy-ethers to our package here <br>

![h27](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/b7370021-0d7e-4758-8e95-e9bdfebc7545)

Figure3: here when we give the command 

```
npm install --save-dev  @nomiclabs/hardhat-ethers@npm:hardhat-deploy-ethers ethers

```

then we can see that at package.json file that hardhat ethers package is overriden by hardhat deploy ethers package <br>


![h28](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/96f3ec65-c328-4377-a4df-8bfeae4e0c9c)
Figure4: inside the akrkdeploy folder it is better to give scripts number so that we can run them <br>
in orders <br>

Hardhat deploy is different from normal deploy here we don't need to have main functions <br>
nor we have to call main function <br>
It gonna run a specific function that we define inside the script <br>




