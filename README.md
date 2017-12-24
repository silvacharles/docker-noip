#### No-IP

##### OBS: Só funciona em arquitetura arm com a tag  charlessilva/noip:latest ou charlessilva/noip:arm32v7
##### Versão para arquitetura x64 utilizar a tag  charlessilva/noip:amd64

charlessilva/noip é uma imagem docker do cliente oficial de atualização de DNS dinâmico [no-ip](http://www.noip.com)

* Configure uma conta em www.noip.com

* Execute ```docker run -ti -v "/opt/noip:/usr/local/etc/" charlessilva/noip:latest noip2 -C```

Esta etapa pedirá suas credenciais noip e gerará a configuração necessária para o seu contêiner ser executado

* Execute ```docker run -it -v "/opt/noip:/usr/local/etc/" --restart=always -d charlessilva/noip:latest```

Isso iniciará seu daemon de contêiner noip e ele irá reiniciá-lo, mesmo se você reiniciar o seu pi, agora você pode acessar seu dispositivo em qualquer lugar do mundo, pois atualizará o DNS automaticamente
