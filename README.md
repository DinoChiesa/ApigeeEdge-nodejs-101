# ouT OF DaTe

As of January 2022, this repo is out of date. It shows how to use hosted targets within Apigee, a feature which is now deprecated. If you want to run nodejs apps or services, consider using AppEngine or Cloud Run.

# Example Nodejs API Proxy

This is an example API Proxy for Apigee Edge that uses nodejs.

## Deploying

You can deploy the API Proxy with any tool that uses the Apigee Edge management API.

[One command-line tool](./tools/importAndDeploy.js) is available in the tools directory.

An example of usage:

```
ORG=myorg
ENV=test
cd tools
npm install
cd ..
node tools/importAndDeploy.js -v -o $ORG -e $ENV -d .
```

## Invoking the Proxy

```
curl -i https://$ORG-$ENV.apigee.net/nodejs-101/servicex
```


```
curl -i -X POST -d '' https://$ORG-$ENV.apigee.net/nodejs-101/servicex
```



