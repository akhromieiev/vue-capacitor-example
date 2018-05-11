# vue-capacitor-example

> A Vue.js project with Capacitor

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# init Capacitor
npx cap init vue-capacitor-example com.roma.vueCapacitorExample

# generate ios project and run it in Xcode
npm run build
npx cap add ios
npx cap sync
npx cap copy
npx cap open ios