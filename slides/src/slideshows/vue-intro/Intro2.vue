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

    <slide enter="fadein" >
      <h1>Teil 1 &mdash; Recap</h1>
      <h3><img src="./assets/logo.png" alt="vue logo" style="vertical-align: middle; height: 100px;"> Vue</h3>
      
      <!-- Syntax highlighting funktioniert nicht, da v-pre den content bereits während des Parsens des .vue files 
      in einen einzelnen string umwandelt. hljs erwartet aber nodes. 
      ohne v-pre wird aber inhalt von vue interpretiert :-( -->
      <eg-code-block lang='html'>
        <div v-pre >
&lt;template>
  &lt;label>Wer bist Du?
    &lt;input v-model="text" />
  &lt;/label>
  &lt;p v-if="text">Hallo {{ text }}&lt;/p>
&lt;template>

&lt;script>
const app = new Vue({
        el: "#app",
        data: {
          text: ""
        }
});
&lt;/script>
        </div>
      </eg-code-block>
    </slide>

    <slide enter="fadein" >
      <h1>Teil 2</h1>
      <h3>Nuxt - Serverside Rendering und mehr</h3>
      <p>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 418.08 71.29" class="SVG-nuxtjs" data-v-d9640ef6=""><g id="Calque_2" data-name="Calque 2"><g id="Calque_1-2" data-name="Calque 1"><path d="M166.41 21.1a3.06 3.06 0 0 1 .85 2.22V66a3.43 3.43 0 0 1-.95 2.46 3.23 3.23 0 0 1-2.43 1 4.82 4.82 0 0 1-1.51-.24 2.59 2.59 0 0 1-1.16-.74l-27.65-36v33.89a3 3 0 0 1-3.09 3.09 2.87 2.87 0 0 1-2.18-.88 3.06 3.06 0 0 1-.84-2.21V23.6a3.25 3.25 0 0 1 1-2.42 3.15 3.15 0 0 1 2.35-.95 4.28 4.28 0 0 1 1.62.31 2.8 2.8 0 0 1 1.19.88l27.53 36.08V23.32a3 3 0 0 1 3.09-3.09 2.9 2.9 0 0 1 2.18.87zM223.21 21.1a3.44 3.44 0 0 1 .88 2.43v27a20.21 20.21 0 0 1-2.46 10 17.88 17.88 0 0 1-6.79 6.93A19.16 19.16 0 0 1 205.1 70a19.51 19.51 0 0 1-9.85-2.49 17.82 17.82 0 0 1-6.82-6.93 20.21 20.21 0 0 1-2.46-10v-27a3.23 3.23 0 0 1 1-2.43 3.51 3.51 0 0 1 2.53-1 3.29 3.29 0 0 1 2.36 1 3.2 3.2 0 0 1 1 2.39v27a12.87 12.87 0 0 0 1.69 6.58 12.14 12.14 0 0 0 10.55 6.15 12.56 12.56 0 0 0 6.26-1.62 12.22 12.22 0 0 0 4.64-4.53 12.7 12.7 0 0 0 1.72-6.58v-27a3.56 3.56 0 0 1 .84-2.43 3 3 0 0 1 2.33-1 3.05 3.05 0 0 1 2.32.99zM277.34 64.4a3.3 3.3 0 0 1 .63 2 3.06 3.06 0 0 1-1 2.39 3.33 3.33 0 0 1-2.29.91 3.15 3.15 0 0 1-2.74-1.4l-13.67-18.25-13.36 18.22a3.23 3.23 0 0 1-2.74 1.47 2.91 2.91 0 0 1-2.15-.88 2.73 2.73 0 0 1-.88-2 3.78 3.78 0 0 1 .85-2.32l14.42-19.63-14.49-19.48a3.27 3.27 0 0 1-.71-2 3.2 3.2 0 0 1 1-2.39 3.29 3.29 0 0 1 2.36-1 3.42 3.42 0 0 1 1.51.36 3.1 3.1 0 0 1 1.23 1.05l13.51 18.15 13.38-17.97a3.4 3.4 0 0 1 2.67-1.55 3 3 0 0 1 2.22 1 3 3 0 0 1 1 2.15 3.54 3.54 0 0 1-.7 2l-14.68 19.54zM328.09 21.1a3.07 3.07 0 0 1 1 2.36 3 3 0 0 1-1 2.32 3.56 3.56 0 0 1-2.43.84h-12.52v39.47a3.21 3.21 0 0 1-1 2.39 3.86 3.86 0 0 1-5.14 0 3.24 3.24 0 0 1-1-2.39V26.62h-12.49a3.44 3.44 0 0 1-2.42-.87 3.07 3.07 0 0 1-.95-2.36 3 3 0 0 1 .95-2.29 3.44 3.44 0 0 1 2.42-.87h32.15a3.48 3.48 0 0 1 2.43.87z" class="cls-1"></path> <path d="M343.49 68.2a14.8 14.8 0 0 1-5.49-5.42 3.56 3.56 0 0 1-.64-1.9 3 3 0 0 1 1.06-2.29 3.25 3.25 0 0 1 2.18-1 4.51 4.51 0 0 1 3.17 1.76 8.49 8.49 0 0 0 7.38 4.08 9 9 0 0 0 6.54-2.6 8.59 8.59 0 0 0 2.68-6.4V23.6a3.16 3.16 0 0 1 1.05-2.39 3.48 3.48 0 0 1 2.46-1 3.34 3.34 0 0 1 2.5.95 3.29 3.29 0 0 1 .95 2.42v30.9a15.23 15.23 0 0 1-2.11 7.88 15.53 15.53 0 0 1-5.8 5.69 16.34 16.34 0 0 1-8.27 2.12 15.25 15.25 0 0 1-7.66-1.97zM391.85 68.72a23.18 23.18 0 0 1-7.53-4.67 3.76 3.76 0 0 1-1.47-2.89 3.19 3.19 0 0 1 1-2.28 3.13 3.13 0 0 1 2.32-1 2.88 2.88 0 0 1 2 .77 19.56 19.56 0 0 0 5.8 3.83 17.56 17.56 0 0 0 6.79 1.24 13.19 13.19 0 0 0 7.49-2.05 6 6 0 0 0 3.06-5.13 6.58 6.58 0 0 0-3.06-5.66 27.19 27.19 0 0 0-9.1-3.34c-4.84-1-8.55-2.61-11.16-4.86s-3.9-5.37-3.9-9.35a12.44 12.44 0 0 1 2.2-7.33 14 14 0 0 1 6-4.82 21.53 21.53 0 0 1 8.72-1.69 23.84 23.84 0 0 1 8.23 1.41 17.31 17.31 0 0 1 6.26 3.73 4 4 0 0 1 1.62 3 3.14 3.14 0 0 1-.95 2.25 3 3 0 0 1-2.29 1 2.31 2.31 0 0 1-1.61-.57 14.51 14.51 0 0 0-5.07-3.09 16.83 16.83 0 0 0-6.14-1.22 12.89 12.89 0 0 0-7.49 1.94 6.22 6.22 0 0 0 0 10.37 26.21 26.21 0 0 0 8.27 3.1 43.61 43.61 0 0 1 9 2.81 12.68 12.68 0 0 1 5.38 4.5 13.53 13.53 0 0 1 1.89 7.53 12.06 12.06 0 0 1-2.28 7.24 15.08 15.08 0 0 1-6.23 4.93 21 21 0 0 1-8.65 1.76 26.07 26.07 0 0 1-9.1-1.46z" class="cls-2"></path> <path d="M6 65.67h22.69a7.57 7.57 0 0 1 .82-2.46l21.28-37.42L39.72 6.33zM79.44 65.67H90L62.28 16.94l-5 8.85 21.24 37.42a7.31 7.31 0 0 1 .92 2.46zM54.02 31.47l-19.45 34.2h38.89l-19.44-34.2z" class="cls-3"></path> <path d="M29.22 68.88a3.54 3.54 0 0 1-.19-.39 5 5 0 0 1-.34-2.82H6L39.72 6.33l11.07 19.46L54 20.11l-9.65-17C44.08 2.62 42.45 0 39.64 0c-1.27 0-3.09.55-4.57 3.15L.91 63.21c-.29.52-1.7 3.25-.3 5.67.64 1.1 2 2.41 5 2.41h28.61c-2.98 0-4.36-1.29-5-2.41z" fill="#00c58e"></path> <path d="M95 63.21L66.93 13.76c-.29-.52-1.91-3.15-4.73-3.15-1.27 0-3.09.54-4.57 3.14L54 20.11l3.23 5.68 5-8.85L90 65.67H79.44a4.73 4.73 0 0 1-.22 2.4 3.06 3.06 0 0 1-.22.49l-.09.18c-1.42 2.42-4.49 2.55-5.09 2.55h16.52c.61 0 3.67-.13 5.09-2.55.63-1.1 1.08-2.95-.43-5.53zM95.04 63.21z" class="cls-5"></path> <path d="M78.91 68.74l.09-.18a3.06 3.06 0 0 0 .22-.49 4.73 4.73 0 0 0 .22-2.4 7.31 7.31 0 0 0-.92-2.46L57.25 25.79 54 20.11l-3.23 5.68-21.26 37.42a7.57 7.57 0 0 0-.82 2.46 5 5 0 0 0 .31 2.82 3.54 3.54 0 0 0 .19.39c.64 1.1 2 2.41 5 2.41h39.6c.63 0 3.7-.13 5.12-2.55zM54 31.47l19.44 34.2H34.57z" fill="#2f495e"></path></g></g></svg>
      <p>
      <h3>Vuex - Statehandling alà Redux</h3>
    </slide>


    <slide enter="fadein" steps="7">
      <h1>Nuxt</h1>
      <h3>Warum Nuxt?</h3>
      <ul>
        <li class="server" v-if='step >= 2'>Server Side Rendering</li>
        <li class="traffic" v-if='step >= 3'>Router Config via Pages Directory</li>
        <li class="movie" v-if='step >= 4'>Page Transitions</li>
        <li class="page" v-if='step >= 5'>Layouts</li>
        <li class="data" v-if='step >= 6'>AsyncData</li>
        <li class="store" v-if='step >= 7'>Store / VueX</li>
      </ul>
    </slide>

    <slide enter="fadein">
      <h3>Nuxt &mdash; 💻 Server Side Rendering</h3>
      <p>
        Warum rendern auf dem Server?
      </p>
      <ul>
          <li class="racer">Performance</li>
          <li class="seo">SEO</li>
          <li class="money">Hosting</li>
        </ul>
      <p>Aber geht dann noch dynamisches Verhalten? <em>(Spoiler: Ja)</em></p>
    </slide>  

    <slide enter="fadein" steps="3">
      <h3>Nuxt &mdash; 🚧 Router Config via Pages Directory</h3>
      <div class="compare">
        <div class="vue">
      <p>Standard Vue</p>
      <eg-code-block v-if='step === 1 || step === 3' lang='html'>
              <div v-pre >
&lt;div id="app">
  &lt;h1>Hello App!&lt;/h1>
  &lt;p>
    &lt;router-link to="/foo">Go to Foo&lt;/router-link>
    &lt;router-link to="/bar">Go to Bar&lt;/router-link>
  &lt;/p>
  &lt;router-view>&lt;/router-view>
&lt;/div>
            </div>
          </eg-code-block>

      <eg-code-block v-if='step === 1 || step === 3' lang='js'>
              <div v-pre >
const router = new VueRouter({
  { path: '/foo', component: Foo },
  { path: '/bar:id', component: Bar }
})
const app = new Vue({ router }).$mount('#app')

            </div>
          </eg-code-block>
</div>
<div class="nuxt">
  <p>Nuxt</p>
  <eg-code-block v-if='step >= 2' lang='js'>
    <div v-pre >
&lt;div id="app">
  &lt;h1>Hello App!&lt;/h1>
  &lt;p>
    &lt;nuxt-link to="/foo">Go to Foo&lt;/nuxt-link>
    &lt;nuxt-link to="/bar">Go to Bar&lt;/nuxt-link>
  &lt;/p>
&lt;/div>
      </div>
    </eg-code-block>

    <div v-if='step >= 2'>
      <img src="./assets/pages-dir.png" alt="Directory structure pages. Directory or file per route." class="center"/>
    </div>
  </div>
</div>
  </slide> 

    <slide enter="fadein">
      <h3>Nuxt &mdash; 🎬 Page Transitions</h3>
<p>Standard Transition Name: Page</p>
      <eg-code-block lang='js'>
        <div v-pre >
.page-enter-active, .page-leave-active {
  transition: opacity .5s;
}
.page-enter, .page-leave-to {
  opacity: 0;
}
      </div>
    </eg-code-block>
    <p>Name der Transition im Css kann mit dem Key <code>transition</code> im Root oder in jeder Seite überschrieben werden. z.B.</p> 
      <eg-code-block lang='js'>
              <div v-pre >
export default {
  transition: 'bounce' // Nutze .bounce-enter-active usw. aus css
}
      </div>
    </eg-code-block>
    </slide> 
    <slide enter="fadein">
      <h3>Nuxt &mdash; 📃Layouts</h3>
      <p><code>layouts/default.vue</code> ist das Standard Layout für alle Seiten</p>
      <p>Jede Seite kann mit dem Key <code>layout</code> ein spezifisches Layout nutzen</p>
      <eg-code-block lang='js'>
              <div v-pre >
export default {
  layout: 'no-ads' // Nutze layout/no-ads.vue als layout
}
      </div>
    </eg-code-block>
    <p>Die Komponente <code>nuxt</code> wird durch den aktuellen Inhalt ersetzt</p>
      <eg-code-block lang='html'>
              <div v-pre >
&lt;template>
  &lt;sidebar>&lt;nav />&lt;/sidebar>
  &lt;article>
  &lt;nuxt />
  &lt;/article>
&lt;/template>
      </div>
    </eg-code-block>

    </slide>

    <slide enter="fadein">
      <h3>Nuxt &mdash; ✨ AsyncData</h3>
      <p>Lifecycle hook vor dem ersten Rendern</p>
      <p>Daten asynchron holen in Promise</p>
      <p>Result wird automatisch mit data gemischt</p>
      <p>Bei Nutzung von VueX stattdessen fetch benutzen</p>
    </slide> 
<!--     
    <slide enter="fadein">
      <h3>Nuxt &mdash; 🛒 Store / VueX</h3>
    </slide>  -->

    <slide enter="fadein"> 
      <h3>VueX &mdash; 🛒 Store</h3>
      <p>Wann VueX &mdash; und wann nicht</p>
    </slide> 

    <slide enter="fadein">
      <h3>VueX &mdash; State, Mutations, Actions</h3>
      <p>
      <img src="./assets/vuex.png" 
        alt="Bestandteildiagramm von VueX" 
        class="center"
        style="height:70vh"/>
      </p>
    </slide> 

    <slide enter="fadein">
      <h3>VueX &mdash; Spielregeln</h3>
      <ul>
        <li class="global">Application(!) State existiert nur im Store</li>
        <li class="mutate">Der State wird nur über Mutations verändert</li>
        <li class="async">Asynchrone Logik benutzt immer Actions via dispatch, keine Mutations</li>
      </ul>
    </slide> 

    <slide enter="fadein">
      <h3>VueX &mdash; Demo (Nuxt Version)</h3>
      <div class="compare">
        <div class="left">
          <p>stars.vue</p>
          <eg-code-block lang='js'>
            <div v-pre >
&lt;template>
  &lt;h1>Stars: {{ $store.state.stars }}&lt;/h1>
&lt;/template>

&lt;script>
export default {
  async fetch ({ store, params }) {
    await store.dispatch('GET_STARS');
  }
}
&lt;/script>
            </div>
          </eg-code-block>
        </div>
        <div class="right">
          <p>store/index.js</p>
          <eg-code-block lang='js'>
            <div v-pre >
export const state = () => ({
  stars: 0.0
})

export const mutations = {
  SET_STARS (state, stars) {
    state.stars = stars
  }
}

export const actions = {
  async GET_STARS ({ commit }) {
    const { data } = await axios.get('http://my-api/stars')
    commit('SET_STARS', data)
  }
}
            </div>
          </eg-code-block>
        </div>      </div>
    </slide> 

    <slide enter="fadein" class="demo">
      <h1>
        Fragen?
      </h1>

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
    title: "Einführung in Vue.js - Teil 2",
    description: "Vortrag für den Webmontag Bonn",
    path: "vue-intro2"
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

    .eg-code-block.box {
      background: goldenrod;
    }

    .twocolumn {
      columns: 2;
    }

    img.center {
      margin: 0 auto;
    }

    .SVG-nuxtjs {
      max-height: 3em;
      .cls-3 {
        fill: white;
      }
    }

    .compare {
      display: grid;
      grid-template-columns: [vue] 1fr [nuxt] 1fr;
      grid-gap: 2em;

      .vue {
        grid-column-start: vue;
      }
      .nuxt {
        grid-column-start: nuxt;
      }
    }

    p code {
      font-size: 1em;
    }

    ul,
    li {
      list-style: none;
      margin: 0;
      padding: 0;
    }

    li {
      position: relative;
      padding-left: 1.2em;
      margin-bottom: 20px;

      &:before {
        display: block;
        position: absolute;
        top: 0;
        left: 0;
        content: "";
        font-size: 0.75em;
      }
    }

    li.box:before {
      content: "❑";
    }
    li.hand:before {
      content: "☞";
    }
    li.star:before {
      content: "✭";
    }
    li.triangle:before {
      content: "►";
    }
    li.dot:before {
      content: "◉";
    }
    li.quote:before {
      content: "»";
      font-size: 1.2em;
    }
    li.arrow:before {
      content: "→";
    }
    li.sun:before {
      content: "☀️";
    }
    li.checkmark:before {
      content: "✓";
    }
    li.smiley:before {
      content: "😀";
    }
    li.server:before {
      content: "💻";
    }
    li.traffic:before {
      content: "🚧";
    }
    li.movie:before {
      content: "🎬";
    }
    li.page:before {
      content: "📃";
    }
    li.data:before {
      content: "✨";
    }
    li.store:before {
      content: "🛒";
    }
    li.racer:before {
      content: "🚀";
    }
    li.seo:before {
      content: "🔍";
    }
    li.money:before {
      content: "💰";
    }
    li.global:before {
      content: "🌍";
    }
    li.mutate:before {
      content: "🧬";
    }
    li.async:before {
      content: "⏱";
    }
  }
}
</style>
