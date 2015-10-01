# salesforce-lds-seed

Sample project for SalesForce using [Lightning Design System](https://www.lightningdesignsystem.com) for kick-off purposes.

## Required

Generic:

* NodeJS

## Set-up

##### Salesforce access

0) Create file '.salesforce' with following content:

```shell
#!/bin/sh

export CLIENT_ID=YOUR-SALESFORCE-CLIENT-ID (3rd step)
export CLIENT_SECRET=YOUR-SALESFORCE-SECRET (3rd step)
export USERNAME=YOUR-SALESFORCE-USERNAME (2nd step)
export PASSWORD=YOUR-SALESFORCE-PASSWORD-AND-TOKEN (2nd step)
```

1) Enable REST API for your organization

REST API is enabled by default when you have one of the following editions:

a. Enterprise Edition

b. Unlimited Edition

c. Developer Edition

2) Generating token for your account

a) Go to 'My settings'->'Personal'->'Reset my security token'

b) Click 'Reset security token'

c) Based on instructions in e-mails paste your password and token into PASSWORD in .salesforce file

d) In .salesforce file set you USERNAME

3) Generating consumer key and secret for your account

a) Go to 'Setup'

b) Go to 'Build'->'Create'->'Apps' and create new CONNECTED app with:

* callback URL

* enabled OAuth settings

* proper OAuth scopes

c) paste generated consumer key and secret into .salesfoce file

4) Save .salesforce file

## Development

0) Set-up SalesForce

```shell
source .salesforce

```

1) Install needed dependencies

```shell
npm install
```

2) Run application locally

```shell
npm start
```

Then check your [browser](http://localhost:8088). Application will be run on port 8088


## Deployment

TODO

## Salesforce

[REST API](http://www.salesforce.com/us/developer/docs/api_rest/api_rest.pdf)