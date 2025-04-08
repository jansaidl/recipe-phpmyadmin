# Zerops x PhpMyAdmin
The concept of a utility tool illustrates how to set up and use the technologies supported by [Zerops](https://zerops.io).

<br />

![phpmyadmin](https://github.com/zeropsio/recipe-shared-assets/blob/main/covers/svg/cover-phpmyadmin.svg)

## Deploy on Zerops
You can add the latest version of PhpMyAdmin to your project by clicking the ```Import Services``` button in the project details and then copying the provided code.


```yaml
services:
  - hostname: phpmyadmin
    type: php-nginx@8.4
    enableSubdomainAccess: true
    buildFromGit: https://github.com/zeropsio/recipe-phpmyadmin
```
See the [Zerops documentation](https://docs.zerops.io/references/import) and [zerops.yaml](https://github.com/zeropsio/recipe-adminer/blob/main/zerops.yml) to understand how to use it.



<br/>
<br/>

## PhpMyAdmin

[PhpMyAdmin](https://www.phpmyadmin.net/) is a full-featured database management tool written in PHP. 


## Production vs. development

- For production environments, it is not advisable to make PhpMyAdmin publicly accessible. Consider either disabling ```Public Access through the Zerops.io subdomain```  after deployment in GUI  or directly setting `enableSubdomainAccess` to `false` in import file.
- To access PhpMyAdmin in production environment you can use a  [VPN](https://docs.zerops.io/references/vpn) through [ZCLI](https://docs.zerops.io/references/cli). Once connected, PhpMyAdmin will be available at the address `phpmyadmin.zerops` (or whatever hostname you set).

<br/>
<br/>

Need help setting your project up? Join [Zerops Discord community](https://discord.com/invite/WDvCZ54).