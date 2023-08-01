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

![h26](https://github.com/C191068/Ali_Khatami_Hardhat2/assets/89090776/8f0cfe15-effe-4fab-beaa-68cf066a6d46)
Figure2: Instead of writing our deploy scripts to script folder shown with red arrow <br>
we create a new folder for that and that is ```akrkdeploy``` <br>

This ```akrkdeploy``` folder is where hardhat deploy module will be to deploy our solidity code <br>



