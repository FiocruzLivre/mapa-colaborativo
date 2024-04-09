# Mapa Colaborativo dos Movimentos Sociais em Saúde

## Instalação

1. Tenha em mãos o dump do projeto e coloque na pasta `volumes/mysql/dump`
2. Caso necessário, crie o arquivo `.env` ou utilize um existente.
3. Execute os comandos que seguem:
    ```bash
    mkdir volumes
    git clone https://github.com/LibreCodeCoop/mediawiki-development/ volumes/mediawiki
    git clone https://github.com/LibreCodeCoop/mapa-colaborativo.git volumes/src
    git -C volumes/mediawiki submodule update --init --recursive
    docker compose up -d
    docker compose exec chown -R www-data:www-data /var/www/mediawiki
    docker compose exec -u www-data mediawiki bash
    composer update --no-dev -o
    php maintenance/update.php --quick
    ```
