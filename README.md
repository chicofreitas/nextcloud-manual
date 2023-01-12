# nextcloud-manual

## Trabalhando na Versão 25

Modificando as permissões para o usuário e grupo do servidor

       sudo chown www-data:www-data /var/www/html

Para evitar problemas ao executar comandos npm, composer, git, dentre outros, adicione o usuário ao grupo www-data

        usermod -a -G www-data <nome do usuário>

Em seguida (apenas no ambiente de desenvolvimento), mude as permissões dos arquivos

        sudo chmod 777 /var/www/html -R
        
Clonando apenas a branch stable25 dentro do diretório */var/www/html*

        git clone --branch stable25 https://github.com/nextcloud/server.git

e em seguida

        git submodule update --init

Após a instalação da versão, editar o arquivo config/config.php para habilitar o modo de depuração de erros

       <?php
       $CONFIG = array (
           'debug' => true,
           ... configuration goes here ...
       );

## Configurando o Banco de Dados


## 
