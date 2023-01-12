# nextcloud-manual

## Trabalhando na Versão 25

Em seguida (apenas no ambiente de desenvolvimento), mude as permissões dos arquivos

        sudo chmod 777 /var/www/html -R
        
Clonando apenas a branch stable25 dentro do diretório */var/www/html*

        git clone --branch stable25 https://github.com/nextcloud/server.git

e em seguida

        git submodule update --init

Modificando as permissões para o usuário e grupo do servidor

       sudo chown www-data:www-data config data apps apps-extra

Para evitar problemas ao executar comandos npm, composer, git, dentre outros, adicione o usuário ao grupo www-data

        usermod -a -G www-data <nome do usuário>

Após a instalação da versão, editar o arquivo config/config.php para habilitar o modo de depuração de erros

       <?php
       $CONFIG = array (
           'debug' => true,
           ... configuration goes here ...
       );

## Configurando o Banco de Dados

Esta parta fica a critério do seu SGBD de preferência

## Instalando a Mail App recomendada da NextCloud

Clonando a versão Stable2.2 da Mail App no diretório *apps/*

        git clone --branch stable2.2 https://github.com/nextcloud/mail.git

## Gerando a Estrutura do Plugin

        https://apps.nextcloud.com/developer/apps/generate

## Configuração Inicial do Plugin
