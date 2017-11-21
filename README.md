# Storyblok Vue.js/Bootstrap 4 Starter Template
> A Vue.js/Bootstrap 4 SPA boilerplate for Storyblok's headless CMS

## An experiment by Team SI's developers
This project is a work in progress, created for evaluating the feasibility of using a decoupled, headless / API-first architecture at Team SI. The goal is for the content store (CMS) to declare all the layouts/components rendered by the SPA, making a headless CMS a real possibility for marketing websites where quick content and layout changes are often needed.

Vue.js makes this possible by binding the data source to dynamic components such as grid elements, carousels, call-to-actions and other reusable "blocks".

[Demo Site](https://teamsi-vuejs-starter.netlify.com/)

## Concepts
- Simply create your schemas and data in the CMS, then code reusable Vue.js components in this project with props to match the schema.
- To use components this project already includes, just create your content schemas to match the props.
- `dist` folder can be deployed directly to a CDN - no need for a full web server.
- Site can be pre-rendered with [Netlify's pre-rendering service](https://www.netlify.com/docs/prerendering/) to allow search engines to pick up content generated by Javascript (we plan to look into [server-side rendering](https://vuejs.org/v2/guide/ssr.html) later).

## Features (so far)
- CI/CD support: we add the `DEPLOY_PRIME_URL` environment variable value to API requests as the `env` parameter to eliminate CORS issues that could arise from accessing the API from multiple environments. Works great with [Netlify Deploy Previews](https://www.netlify.com/docs/continuous-deployment/)!
- Multi-site ready: just add each space's token to an `API_TOKEN` environment variable.
- Dynamic navigation support, allowing the data store to define a custom navbar - or even a mega menu.
- Several reusable content blocks. So far we have support for grid rows and columns, hero components, call-to-actions, markdown, images, and Youtube videos.
- Reusable page templates.
- Automatic lazy loading and in-place image optimization on image components via StoryBlok's [Image Service](https://www.storyblok.com/docs/image-service) (just specify the width and/or height on each component instance).

## Build Setup
``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


## Copyright and license
Code and documentation copyright 2017 by [the authors](https://github.com/teamsidev/storyblok-vue.js-bootstrap4-starter/graphs/contributors) and Team SI. Code released under the [MIT License](https://github.com/teamsidev/storyblok-vue.js-bootstrap4-starter/blob/master/LICENSE).
