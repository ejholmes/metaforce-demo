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
To deploy the files under `src` to an organization, run:

```bash
$ rake metaforce:deploy
```


## Retrieving
To retrieve the content you just deployed to the 'retrieved' directory, run:

```bash
$ rake metaforce:retrieve
```

## More Complex Tasks
If you require more complex deployment and retrieval tasks, take a look at the
[rake tasklib tasks](https://github.com/ejholmes/metaforce/blob/develop/lib/metaforce/rake)
and the [metaforce documentation](http://rubydoc.info/gems/metaforce/frames).
