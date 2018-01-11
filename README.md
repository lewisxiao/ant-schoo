# Ant Schoo App
## Getting Started

### Prerequisites

Support for Node.js > 5

### Installation

```sh
$ git clone https://github.com/lewisxiao/ant-schoo-app.git ant-schoo
$ cd ant-schoo
$ npm install
```

## Development

There are two ways in which you can build and run the web app:

* Build once for (ready for ***Production***):
  * `$ npm run build`
  * `$ npm run build:serve`

  The last command will boot up HTTP server on `3003` port and serve `build/client` directory in a default browser

* Hot reloading via webpack middlewares:
  * `$ npm start`
  * Point your browser to http://localhost:3000/, page hot reloads automatically when there are changes

## Expose App on Your Local Dev Machine

Assign yourself a unique publicly accessible url that will proxy all requests to your locally running webserver.

```sh
$ npm install -g localtunnel
$ npm start
$ npm run tunnel # run in a new tab
```

You will receive a url, for example `https://tbst.localtunnel.me`, that you can share with anyone for as long as your local instance of `lt` remains active. Any requests will be routed to your local service at the specified port.

## Error Tracking and Insights with Sentry

In order to get info on errors that happened in production, we integrate [Sentry](https://sentry.io/for/javascript/) into our application to track errors and get context on what happened.

To use it on your side, configure it first:

* Create account at [https://sentry.io/signup/](https://sentry.io/signup/)
* Add new project for your app on Sentry website
* In `/src/client/assets/javascripts/app/config.js` file assign `SENTRY_KEY` and `SENTRY_APP` constants values that you got after adding a new project
* Don't forget to define `Allowed Domains` section under your `Project Settings` on Sentry website to track errors from required domains

## Debugging

For debugging purposes please use:
- [Redux DevTools
](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd) plugin for Chrome to simplify debugging React apps.
- [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)