# Mapa Colaborativo dos Movimentos Sociais em Saúde

## Instalação

```bash
mkdir volumes
git clone https://github.com/LibreCodeCoop/mediawiki-development/ volumes/mediakiwi
git clone git@github.com:LibreCodeCoop/mapa-colaborativo.git volumes/src
git -C volumes/mediawiki submodule update --init --recursive
docker compose up -d
docker compose exec chown -R www-data:www-data /var/www/mediawiki
docker compose exec -u www-data mediawiki bash
composer update --no-dev -o
php maintenance/update.php --quick
```
