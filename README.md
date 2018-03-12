# Compose-Mediawiki 

## Quickstart for using Mediawiki

Download MediaWiki 1.30

    git clone https://gerrit.wikimedia.org/r/p/mediawiki/core.git --branch REL1_30 mediawiki

Install dependencies

    docker run --rm --interactive --tty --volume $PWD/mediawiki:/app composer install --no-dev

Start

    docker-compose up --build -d


## Extra

Install Semantic Mediawiki

    docker run --rm --interactive --tty --volume $PWD/mediawiki:/app composer require mediawiki/semantic-media-wiki "~2.5" --update-no-dev

Run maintenance script

    docker exec composemediawiki_phpfpm_1 maintenance/update.php --skip-external-dependencies