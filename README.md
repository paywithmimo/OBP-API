# README

The Open Bank Project API

## ABOUT

The Open Bank Project is an open source API for banks that enables account holders to interact with their bank using a wider range of applications and services.

The OBP API supports transparency options (enabling account holders to share configurable views of their transaction data with trusted individuals and even the public), data blurring (to preserve sensitive information) and data enrichment (enabling users to add tags, comments and images to transactions).

Thus, the OBP API abstracts away the peculiarities of each core banking system so that a wide range of apps can interact with  multiple banks on behalf of the account holder. We want to raise the bar of financial transparency and enable a rich ecosystem of innovative financial applications and services.

Our tag line is: Bank as a Platform. Transparency as an Asset.

The API uses OAuth 1.0 authentication.

The project roadmap is available [here.](https://trello.com/b/O9IjhPXB/open-bank-project-api) 

## DOCUMENTATION 

Please refer to the [wiki](https://github.com/OpenBankProject/OBP-API/wiki) to see the API specification. 

## STATUS

[V1.2] (https://github.com/OpenBankProject/OBP-API/wiki/REST-API-V1.2) is mostly implemented

## LICENSE

This project is dual licensed under the AGPL V3 (see NOTICE) and a commercial license from TESOBE
Some files (OAuth related) are licensed under the Apache 2 license.

## SETUP

Use Maven (or sbt) as build tool.

To compile and run jetty, install Maven 3 and execute:

mvn jetty:run

----

Alternatively, sbt can be used, but might need some tweaks.

$ sbt
...
> compile
> ~;container:start; container:reload /

(Note that you first have to start sbt and then on its console start jetty with the container:start task, otherwise it will exit immediately. More here: https://github.com/siasia/xsbt-web-plugin/wiki)

In OS X, sbt can be installed with $ sudo port install sbt

----

# Databases:

The default datastores used are MongoDB (metadata, transaction cache) and Postgres (user accounts).

