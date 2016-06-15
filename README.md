# inventaire-deploy

Tools and scripts to install self-hosted [inventaire](https://github.com/inventaire/inventaire) instance

![deploy](https://qzprod.files.wordpress.com/2014/06/matrix-computers.jpg?quality=80&strip=all&w=500)

## Installation
### Ubuntu
On your server:
```sh
# cloning the deployment tools in the local directory
git clone https://github.com/inventaire/inventaire-deploy .
# start the magic
./install
```

### Other environments
one environment -> one branch

Want to install it in a different environment? Request a new (orphan) branch and send your pull request!

## Other services

By default, this setup uses the same services as [inventaire.io](https://inventaire.io), but you can start your own instance of those too:

### Prerender
* repo: [inventaire/prerender](https://github.com/inventaire/prerender)
* live: [http://136.243.86.191:3000](http://136.243.86.191:3000)
* setup: once you installed your instance, replace `http://136.243.86.191:3000` by your own instance url in [inventaire.original.nginx](https://github.com/inventaire/inventaire-deploy/blob/master/nginx/inventaire.original.nginx) (or directly in `/etc/nginx/sites-available/default` if you already run the installation process)

### Wikidata Subset Search Engine
* repo: [inventaire/wikidata-subset-search-engine](https://github.com/inventaire/wikidata-subset-search-engine)
* live: [https://data.inventaire.io/](https://data.inventaire.io/)
* setup: integration is very much in progress and might change a few times in the coming weeks after this writing so the most future-proof advice there is to make a global search in the [client's code](http://github.com/inventaire/inventaire-client) and to replace every instance of `data.inventaire.io` by your own url
