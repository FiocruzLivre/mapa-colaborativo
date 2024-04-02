# Mapa Colaborativo dos Movimentos Sociais em Saúde

## Instalação

```bash
git clone https://github.com/LibreCodeCoop/mediawiki-development/ mediakiwi
cd mediawiki
mkdir volumes
git clone git@github.com:LibreCodeCoop/mapa-colaborativo.git volumes/src
ln -s volumes/src/docker-compose.override.yml docker-compose.override.yml
docker compose up -d
docker compose exec mediawiki bash
composer i --no-dev
php maintenance/update.php --quick
```
