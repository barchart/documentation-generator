## Setup

This CLI has been published to the Node Package Manager (NPM). The package is named `@barchart/barchart-documentation`; install as follows:

```shell script
npm install @barchart/barchart-documentation -S
```

## How to use

!> WARNING: The CLI is **context sensitive**. All commands will be executed for the **current path**. 

To show help, use the `--help` flag.

```shell script
barchart-documentation --help
```

### Initializing

To initialize documentation folder run the following command:

```shell script
barchart-documentation init
```

> The `init` command is a part of the `barchart-documentation generate` command.

Learn more about the documentation folder structure [here](/content/product_overview#release-notes).

### Creating documentation

The CLI support `JSDoc` and `OpenAPI` v3 specification. 

To generate documentation run the following command:

```shell script
barchart-documentation generate
```

The `generate` command generates documentation from `JSDoc`, `OpenAPI`, and updates sidebars and compile release notes. 

During the generation process, the CLI will ask from which sources to create documentation, and ask paths to these sources. All paths will be cached for each package so CLI will ask for them only once.

!> The CLI supports generating documentation for `OpenAPI` only from `.yaml` files.

### Run documentation locally

The CLI allows you to run a local web server to host documentation. By default, the web server will use port `3000`, if the port is busy, any free port will be used. 

To run the documentation locally, use the following command:

```shell script
barchart-documentation serve
```

### Cache

The CLI caches paths to source code, and an OpenAPI file of each project. To clear cache use the following commands:

* `barchart-documentation clear-cache` — clears cache for all packages.
* `barchart-documentation clear-package-cache` — clears cache for current package.


### Deploy

The CLI uses Docsify which allows to deploy the documentation to the **GitHub Pages**. Learn more about how to deploy documentation to the **GitHub Pages** [here](https://docsify.js.org/#/deploy?id=github-pages). 