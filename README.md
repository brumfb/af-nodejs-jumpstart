# AppFog Node.js Jumpstart

## Introduction

The AppFog Node.js Jumpstart is a sample application that can be used to get started quickly with a new Node.js web application on AppFog.

## Getting Started
### Building the app and pushing to AppFog

To get started, copy the contents of this repo to a new source code repository that you have edit privileges to. Clone that repository and [login to AppFog](https://www.centurylinkcloud.com/knowledge-base/appfog/login-using-cf-cli/). To deploy the application, run the following from the top-level project directory:

```
$ cf push
```

Since the manifest.yml file sets the name of the application to `${random-word}`, the name of the application will be generated during the deployment process. Here is example output of the application deployment using `cf push`:

```
cf push
Using manifest file /Users/demo/node/manifest.yml

Creating app ascitic-flavopurpurin in org DEMO / space Dev as Demouser...
OK

Creating route ascitic-flavopurpurin.useast.appfog.ctl.io...
OK

Binding ascitic-flavopurpurin.useast.appfog.ctl.io to ascitic-flavopurpurin...
OK

Uploading ascitic-flavopurpurin...
Uploading app files from: /Users/demo/node
Uploading 27.8K, 7 files
Done uploading               
OK

Starting app ascitic-flavopurpurin in org DEMO / space Dev as Demouser...
-----> Downloaded app package (12K)
-------> Buildpack version 1.3.1
       Node.js Buildpack v64
-----> Reading application state
       package.json...
       build directory...
       cache directory...
       environment variables...
       Node engine range:   0.10.25
       Npm engine:          2.11.1
       Start mechanism:     server.js
       node_modules source: package.json
       node_modules cached: false
       NPM_CONFIG_PRODUCTION=true
       NODE_MODULES_CACHE=true
       Downloading and installing node 0.10.25...
       Downloading and installing npm 2.11.1 (replacing version 1.3.24)...
-----> Building dependencies
       Installing node modules
       npm WARN package.json af-nodejs-jumpstart@0.0.1 No repository field.
       express@4.12.4 node_modules/express
       ├── merge-descriptors@1.0.0
       ├── utils-merge@1.0.0
       ├── cookie-signature@1.0.6
       ├── methods@1.1.1
       ├── cookie@0.1.2
       ├── fresh@0.2.4
       ├── escape-html@1.0.1
       ├── range-parser@1.0.2
       ├── content-type@1.0.1
       ├── finalhandler@0.3.6
       ├── vary@1.0.0
       ├── parseurl@1.3.0
       ├── serve-static@1.9.3
       ├── content-disposition@0.5.0
       ├── path-to-regexp@0.1.3
       ├── depd@1.0.1
       ├── qs@2.4.2
       ├── on-finished@2.2.1 (ee-first@1.1.0)
       ├── debug@2.2.0 (ms@0.7.1)
       ├── etag@1.6.0 (crc@3.2.1)
       ├── proxy-addr@1.0.8 (forwarded@0.1.0, ipaddr.js@1.0.1)
       ├── send@0.12.3 (destroy@1.0.3, ms@0.7.1, mime@1.3.4)
       ├── accepts@1.2.9 (negotiator@0.5.3, mime-types@2.1.1)
       └── type-is@1.6.3 (media-typer@0.3.0, mime-types@2.1.1)
-----> Checking startup method
       No Procfile; Adding 'web: node server.js' to new Procfile
web: node server.js
-----> Finalizing build
       Creating runtime environment
       Cleaning previous cache
       Caching results for future builds
-----> Build succeeded!
       af-nodejs-jumpstart@0.0.1 /tmp/staged/app
       └── express@4.12.4

-----> Uploading droplet (6.9M)

1 of 1 instances running

App started


OK

App ascitic-flavopurpurin was started using this command `node server.js`

Showing health and status for app ascitic-flavopurpurin in org DEMO / space Dev as Demouser...
OK

requested state: started
instances: 1/1
usage: 256M x 1 instances
urls: ascitic-flavopurpurin.useast.appfog.ctl.io
last uploaded: Thu Jun 11 17:24:09 UTC 2015
stack: cflinuxfs2

     state     since                    cpu    memory          disk        details   
#0   running   2015-06-11 02:24:45 PM   0.0%   22.4M of 256M   32M of 1G     
```

Once the application is running, copy the value for `urls:`, in the case above `ascitic-flavopurpurin.useast.appfog.ctl.io`, and go to that URL in a browser. You should see a page that looks like:

<img src="https://raw.githubusercontent.com/CenturyLinkCloud/af-static-jumpstart/master/images/welcome-to-appfog-screenshot.png"/>

## Customizing the app

### Knowing where the code is

* Web page: `public/index.html`.
* Application Controller: `server.js`.

### Deploying Node.js apps to AppFog

A very useful read is [here](https://www.centurylinkcloud.com/knowledge-base/appfog/deploy-nodejs-application/). This will give you an overview of the general process used to deploy Node.js applications to AppFog.

### Moving forward

As a start point, you can modify the file `server.js` as needed.

A very good place to start with Nodejs is [here](http://nodeschool.io/).

If you are more experienced, [this](https://nodejs.org/api/) can be useful for you.
