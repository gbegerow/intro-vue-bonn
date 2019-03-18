<template lang="html">
  <div id="vue-intro">
    <div class="eg-slideshow eg-theme-agrume">
      <slide leave="fadeOut" >
        <h1><img class="logo" src="./assets/logo.png" height="128px">Vue.js</h1>
        <h3>Einführung in Vue.js</h3>
        
        <p>
          Vue (gesprochen [vju:], wie View] ist ein progessives Framework
          um User Interfaces zu bauen.
        </p>
        <p>
          Der Einsatz reicht vom einfachen jQuery Ersatz
          zur mehr als vollwertigen Alternative zu
          Single Page Frameworks wie Angular, Aurelia oder React.
        </p>
        <p>Ein Vortrag für den Webmontag Bonn von Georg Begerow Twitter: @gbegerow Mail: gbegerow@gmail.com</p>
      </slide>

      <slide leave="fadeOut" steps="2">
        <h3>Hello World</h3>
        
            <eg-code-block lang='html'>
              <div v-pre>&lt;script src="https://cdn.jsdelivr.net/npm/vue@2.5.21/dist/vue.js">&lt;/script>
&lt;div id="app">Hallo {{ text }}, lern Vue.js kennen.&lt;/div>
&lt;script>new Vue({
  el: '#app',
  data: {
    text: 'Webmontag Bonn'
  }
});
&lt;/script></div></eg-code-block>
        <p id="demo-Hello-World" class="result" v-if="step === 2">Hallo {{ text }}, lern Vue.js kennen.</p>
      </slide>

      <slide leave="fadeOut">
        <h3>Direktiven</h3>
        <ul class="twocolumn">
          <li>v-for</li>
          <li>v-if</li>
          <li>v-else</li>
          <li>v-else-if</li>
          <li>v-show</li>

          <li>
            v-bind
            <abbr>:</abbr></li>
          <li>
            v-on
            <abbr>@</abbr></li>
          <li>v-model</li>


          <li>v-text</li>
          <li>v-html</li>

          <li>v-pre</li>
          <li>v-cloak</li>
          <li>v-once</li>
          <li>eigene direktiven...</li>
        </ul>
      </slide>


      <slide leave="fadeOut" steps="3">
        <h3>Direktiven</h3>
        <!-- <div>Step: {{ step }}</div> -->
        <ul>
          <li>v-for
            <eg-code-block v-if='step === 1' lang='html'>
              <div v-pre >
&lt;ul>
  &lt;li v-for="u in user" bind:key="u.id">
    {{u.Name}}
  &lt;/li>
&lt;/ul>
                </div>
            </eg-code-block>
          </li>
          <li>v-if</li>
          <li>v-else</li>
          <li>v-else-if
            <eg-code-block v-if='step === 2' lang='html'>
              <div v-pre>&lt;p v-if="cart.length === 0">Ihr Warenkorb ist leer&lt;/p>
&lt;p v-else-if="cart.length >= 100">Ihr Warenkorb ist voll&lt;/p>
&lt;p v-else>Ihr Warenkorb enthält {{cart.length}} Artikel&lt;/p></div>
            </eg-code-block>
          </li>
          <li>v-show
          <eg-code-block v-if='step === 3' lang='html'>
              <div v-pre >
&lt;p v-show="sales">Angebotszeit!&lt;/p>
              </div>
            </eg-code-block>
          </li>
        </ul>
      </slide>

      <slide leave="fadeOut" steps="4">
        <h3>Direktiven</h3>
        <ul>
          <li>
            v-bind
            <abbr>:</abbr>
            <eg-code-block v-if='step === 1' lang='html'>
              <div v-pre >
&lt;p v-text="simpleText">&lt;/p>
&lt;p>{{ simpleText }}&lt;/p>
               </div>
            </eg-code-block>          
          </li>
          <li>
            v-on
            <abbr>@</abbr>
            <eg-code-block v-if='step === 2' lang='html'>
              <div v-pre >
&lt;button v-on:click="alert('Catchya!!')">Click mich&lt;/button>
              </div>
            </eg-code-block> 
            <div class="result" v-if='step === 2'>
              <button v-on:click.stop="alert('Catchya!!')">Click mich</button>
            </div>
          </li>
          <li>v-model            
            <eg-code-block v-if='step === 3' lang='html'>
              <div v-pre >
&lt;input v-model="text">&lt;span>{{ text }}&lt;/span>
              </div>
            </eg-code-block> 
            <div class="result" v-if='step === 3'>
              <input v-model="text"/>
              <span>{{ text }}</span>
            </div>
          </li>


          <li>v-text
            <eg-code-block v-if='step === 4' lang='html'>
              <div v-pre >
&lt;p v-text="simpleText">&lt;/p>
&lt;p>{{ simpleText }}&lt;/p>
            </div>
          </eg-code-block>
          </li>
          <li>v-html           
            <eg-code-block v-if='step === 4' lang='html'>
              <div v-pre >
&lt;p v-html="formatedDescription">&lt;/p>
              </div>
            </eg-code-block>
          </li>

        </ul>
      </slide>

      <slide leave="fadeOut">
        <h3>Direktiven</h3>
        <ul class="twocolumn">
          <li>v-for</li>
          <li>v-if</li>
          <li>v-else</li>
          <li>v-else-if</li>
          <li>v-show</li>

          <li>
            v-bind
            <abbr>:</abbr></li>
          <li>
            v-on
            <abbr>@</abbr></li>
          <li>v-model</li>


          <li>v-text</li>
          <li>v-html</li>

          <li>v-pre</li>
          <li>v-cloak</li>
          <li>v-once</li>
          <li>eigene direktiven...</li>
        </ul>
      </slide>

    <slide enter="fadein" >
      <h3>Vue Lifecycle</h3>
      <img src="./assets/Vue-instance-lifecycle-codingexplained.png" alt="" class="center"/>
      <p>Image von <a href="https://codingexplained.com/coding/front-end/vue-js/vue-instance-lifecycle-hooks">CodingExplained</a></p>
    </slide>


    <slide enter="fadein" class="demo" >
      <h1>Demo</h1>
      <h3>Progressive Clock</h3>
    </slide>

    <slide enter="fadein" >
      <h3>Clock als Component</h3>
      <eg-code-block lang='javascript'>
              <div v-pre >
     const Clock = Vue.component('clock',{
        template: '&lt;div class="clocks">{{ time }} Uhr&lt;/div>',
        //style: No scoped style without CSS loader
        data() {
            return {
              time: ""
            };
          },
          methods: {
            setClock: function(params) {
              this.time = new Date().toLocaleTimeString("de");
            }
          },
          mounted: function() {
            this.setClock();
            window.setInterval(() => {
              this.setClock();
            }, 1000);
          }
        });
                      </div>
            </eg-code-block>
    </slide>


    <slide enter="fadein" class="demo" >
      <h3>Components nutzen</h3>
      <eg-code-block lang='javascript'>
              <div v-pre >
import Clock from "./clock.vue"; // vue file erfordert loader
      
const app = new Vue({
        el: "#app",
        template: "&lt;Clock />",
        data: {
          time: ""
        },
        components: [
          Clock
        ]
});
              </div>
            </eg-code-block>
    </slide>
    

    <slide enter="fadein" class="demo" >
      <h3>Single File Component</h3>
      <eg-code-block lang='javascript'>
              <div v-pre >
&lt;template>
  &lt;div class="clock">{{ time }}&lt;/div>
&lt;/template>

&lt;script>
export default {
  data() {
    return { time: "" };
  },
  methods: {
    setClock: function(params) {
      this.time = new Date().toLocaleTimeString("de");
    }
  },
  mounted: function() {
    this.setClock();
    window.setInterval(() => { this.setClock(); }, 1000);
  }
};
&lt;/script>

&lt;style scoped>
.clock {
  font-family: fantasy;
  font-size: 300%;
}
&lt;/style>
              </div>
            </eg-code-block>
    </slide>


    <slide enter="fadein" >
      <h1>Im März geht es weiter...</h1>
      <h3>Nuxt - Serverside Rendering und mehr</h3>
      <h3>Vuex - Statehandling alà Redux</h3>
    </slide>



    </div>
  </div>
</template>

<script>
import eagle from "eagle.js";
export default {
  mixins: [eagle.slideshow],
  infos: {
    // These infos appear on the home page, below the slideshow's thumbnail
    title: "Einführung in Vue.js",
    description: "Vortrag für den Webmontag Bonn",
    path: "vue-intro"
  },
  data() {
    return {
      text: "Webmontag Bonn",
      time: ""
    };
  },
  methods: {
    setClock() {
      this.time = new Date().toLocaleTimeString();
    }
  }
};
</script>

<style lang='scss'>
@import url(https://fonts.googleapis.com/css?family=Raleway);
#vue-intro {
  .eg-slideshow {
    font-family: "Raleway";
    background-color: #eef;
    .eg-slide {
      .eg-slide-content {
        width: 80%;
        max-width: 80%;
        margin: 0 auto;
      }

      .eg-code-block,
      code {
        font-family: "Fira Code", Consolas, "Courier New", Courier, monospace;
        font-size: 24px;
        line-height: 110%;
        padding: 0;
      }

      .logo {
        float: left;
        height: auto;
      }

      .result {
        padding: 1em;
        border: maroon 1px solid;
        background-color: lightgoldenrodyellow;
        justify-self: center;
        align-self: center;
      }
    }
  }

  .eg-code-block.box {
    background: goldenrod;
  }

  .twocolumn {
    columns: 2;
  }

  img.center {
    margin: 0 auto;
  }
}
</style>
