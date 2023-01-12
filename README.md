# nextcloud-manual

## Trabalhando na Versão 25

Clonando apenas a branch stable25 dentro do diretório */var/www/html*

        git clone --branch stable25 https://github.com/nextcloud/server.git

Modificando as permissões para o usuário e grupo do servidor

       sudo chown www-data:www-data /var/www/html

Para evitar problemas ao executar comandos npm, composer, git, dentre outros, adicione o usuário ao grupo www-data

        usermod -a -G www-data <nome do usuário>

Em seguida (apenas no ambiente de desenvolvimento), mude as permissões dos arquivos

        sudo chmod 777 /var/www/html -R

## Configurando o Banco de Dados
