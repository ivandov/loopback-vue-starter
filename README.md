# LoopBack Vue Starter
The LoopBack Vue Starter template has a very minimal set of features pre-enabled. The starter template uses [LoopBack v3.x](http://loopback.io/doc/en/lb3/) for API serving & management and [Vue.JS v2.0](https://vuejs.org/) as an embedded frontend client.

This project was built with [vue-cli 3](https://cli.vuejs.org/) and therefore can use the `vue ui` command to manage Vue plugins.

For a detailed walkthrough of building this yourself, please reference this [Strongblog post](https://strongloop.com/strongblog/embeddding-frontend-frameworks-into-loopback).

## Getting Started
Just clone the project and install the `npm` dependencies.

```
git clone https://github.com/ivandov/loopback-vue-starter.git
cd loopback-vue-starter
npm install
```

## Run in Development Mode
The Development mode runs the LoopBack server through [nodemon](https://www.npmjs.com/package/nodemon) to auto-reload any changes. The UI frontend is started as a separate task on a different port. This allows for the ability to manually start the server and the UI separately if needed. 

To run the LoopBack server and Vue frontend in development mode (with active reload) run:
```
npm run dev
```
- The LoopBack Explorer will be starter on [localhost:3000/explorer](http://localhost:3000/explorer/)
- The Vue application will be started on [localhost:8080/#](http://localhost:8080/#/)

**Note** If production mode has been run previously, the `client/dist` folder will exist and you may see an outdated version of your application loaded on [localhost:3000/#](http://localhost:3000/)

## Run in Production Mode
This mode will pack the Vue.JS frontend into a `dist` folder located under `client`. The LoopBack server will automatically serve the application from this folder as it is preconfigured to serve static assets from `client/dist`.

To build the application for distribution and run the LoopBack server in production mode, run: 
```
npm run prod
```
- The LoopBack Explorer will be starter on [localhost:3000/explorer](http://localhost:3000/explorer/)
- The Vue application will be started on [localhost:3000/#](http://localhost:3000/#/)


## Enabling Additional Vue Plugins
Additional Vue plugins can be managed via the [vue-cli](https://cli.vuejs.org/) or using [vue ui](https://cli.vuejs.org/guide/creating-a-project.html#using-the-gui). Just import the root directory as an existing project and manage plugins as necessary.

The vue-router plugin is auto-enabled since it is not easy to add it as a plugin through the UI / cli, and quite easy to remove/ignore if not used. 

![Vue Plugins](client/public/vue_plugins.png)
