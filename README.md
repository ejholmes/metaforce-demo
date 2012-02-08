# Metaforce Demo
This is a sample project showing how to deploy and retrieve code from a
Salesforce organization using
[metaforce](https://github.com/ejholmes/metaforce) and Rake.

## Running
First, clone the project:

```bash
$ git clone git://github.com/ejholmes/metaforce-demo.git
```

Then run bundler to install the necessary gems:

```bash
$ bundle install
```

## Deploying
To deploy the files under `codepkg` to an organization, run:

```bash
$ rake deploy
```


## Retrieve
To retrieve the content you just deployed to the 'retrieve' directory, run:

```bash
$ rake retrieve
```
