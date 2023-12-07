
Overview: This docs is written as a quick actionable guide to lock UA-config, you can complement this guide with our docs

  

[https://layerzero.gitbook.io/docs/evm-guides/ua-custom-configuration](https://layerzero.gitbook.io/docs/evm-guides/ua-custom-configuration)

  

[https://layerzero.gitbook.io/docs/evm-guides/ua-custom-configuration/ua-utils-tooling](https://layerzero.gitbook.io/docs/evm-guides/ua-custom-configuration/ua-utils-tooling)

  

[https://layerzero.gitbook.io/docs/evm-guides/ua-custom-configuration/ua-configuration-lock](https://layerzero.gitbook.io/docs/evm-guides/ua-custom-configuration/ua-configuration-lock)

  
  
  
  
  
  

**1.  First fork this repo**  [https://github.com/LayerZero-Labs/boilerplate](https://github.com/LayerZero-Labs/boilerplate)
    
```
Git clone https://github.com/jasonfonglz/LzUALockConfig.git
```

  

**2. Yarn or npm install**
    
**3.  Enter seed phrase in .env file**
    
  

**4. Generate the config file based on your current configuration**
    

  

The arguments:

**Networks**: a comma separated list of each network and their respective UA address. In our example, it’s fantom-testnet:0xFd7e266AF7CC7ef8645D6bF43C800b7f82ca1042

,bsc-testnet:0xFd7e266AF7CC7ef8645D6bF43C800b7f82ca1042

  

**Name**: The name of your contract, used in a hardhat-deploy situation. you can just put “” to signal you’re not using hardhat-deploy, instead the address field would be present.

  
```
npx hardhat generateAppConfig --networks fantom-testnet:0xFd7e266AF7CC7ef8645D6bF43C800b7f82ca1042

,bsc-testnet:0xFd7e266AF7CC7ef8645D6bF43C800b7f82ca1042 --name “”
```
  

The config json would then be generated here:

**constants/defaultConfig.json**

  
  

7.  Lock the config with this command
    
```
npx hardhat setConfig --config-path "./constants/defaultConfig.json"
```
  

Type yes when it asks this.

![](https://lh7-us.googleusercontent.com/A1zsORZMczn7fx6pSANjuJhphvzpByoZe8aHE-Jf7xp6yH8Kz1S1eN_DUMQhCQm_94q2z0wZWiYygtuDxtJBPV9xhbeqTCJ_TQ2f4i1_dzCsKuvreYBWhGRolGju9xsIri4wCSdpG8WC31VNLPmWEUs)

  

It’d then show the progress of config setting.

![](https://lh7-us.googleusercontent.com/b5fYLS8rU-e9Xm8NYdwDSdFD2XOrKVVAqLFHZzgthMah597H_ZDJWc8GZ-yZDMRtB2Rvq1laFKwyBgoAbO_7OaG5fy2pg5JKrbKgUlsb4RZHMu_3sfSe02np82b1bMxsJ-XuKs82CdVBrApeCYw5DNY)