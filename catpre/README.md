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
v-model：雙向綁定資料(第一種&第二種)，只能在HTML表單元素和自訂元件上使用。無縮寫
v-bind：單向綁定(第一種)HTML元素的屬性，縮寫為 : 像是<a :href="url"></a>中href前的":"
若使用v-bind,在編譯時會得到"number"的資料型態
沒使用會得到一般字串"string"的資料型態

寫function的方法是methosd:{
    'function name()'{
        功能
    }
}
多個function記得逗號


在HTML中，屬性是不區分大小寫的，也就是說如果你在HTML中寫myattribute跟寫myAttribute，HTML會看成是一樣的東西，所以如果我們在元件中使用props去接收屬性的資料時，寫的是camelCase(駝峰式命名法)的屬性名稱，在HTML中就要自動轉換為kebab-case(用dash間隔的命名法)。

html
<div id="app">
    <child my-message="HelloWorld"></child>
</div>
元件
Vue.component('child', {
    props: ['myMessage'],
    template: '<p>{{ myMessage }}</p>'
})

var vm = new Vue ({
    el: '#app'
})
```

![](https://raw.githubusercontent.com/Terry-Hsieh/mycatweb/master/catpre/imgstore/1.jpg "function")
![](https://raw.githubusercontent.com/Terry-Hsieh/mycatweb/master/catpre/imgstore/2.jpg "v-on")
![](https://raw.githubusercontent.com/Terry-Hsieh/mycatweb/master/catpre/imgstore/3.jpg "event")
![](https://raw.githubusercontent.com/Terry-Hsieh/mycatweb/master/catpre/imgstore/4.jpg "mouse/keyboard")

``` bash
#HTML TAG#
<ul>
    <a href="url" :style="color and fontsize"> #寫成object的集合 
</ul>


```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
