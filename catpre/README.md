# catpre

> A Vue.js project

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

## Note
``` bash
main.js 主要是要多放router
index.js 主要是放path也就是自定義所需要的介面UI也就是 component
App.vue 主要負責表現畫面及資料，不同的path需要不同的vue來做呈現

v-model是一個常用的指令，通常會用來做表單資料的雙向綁定(Two-way Binding)，意思就是說將View與資料綁在一起，當使用者輸入資料到輸入框後，會自動將資料存在一個變數中，並即時更新資料到綁定的View當中，輸入框/按鈕/選單。
v-model.lazy 讓數值不會即時反應要移出對應input外才會更新

讓HTML元素中的屬性和vue instance做綁定，Vue有提供一個指令v-bind，就可以做到這樣的功能。


第一種：data改變，UI內容跟著更新。
第二種：使用者在UI輸入內容，data跟著更新。
v-model：雙向綁定資料(第一種&第二種)，只能在HTML表單元素和自訂元件上使用。
v-bind：單向綁定(第一種)HTML元素的屬性。

![123](https://github.com/Terry-Hsieh/mycatweb/blob/master/catpre/1.jpg)
#HTML TAG#
<ul>
    <a href="url" :style="color and fontsize"> #寫成object的集合 
</ul>


```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
