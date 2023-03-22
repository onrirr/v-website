<script setup lang="ts">
import navbar from '@/components/navbar.vue';
</script>

<template>
  <navbar />
  <main>
    <div>
      <h1 class="title">The <img src="https://vlang.io/img/v-logo.png" width="48" height="48"> Programming Language <a
          class="button">BETA</a> </h1>
      <p class="subtitle">A simple, fast, safe, compiled language for developing maintainable software.</p>
    </div>
    <div class="buttonss">
      <div class="dropdown">
        <a class="btn" style="padding: 12px 34px;"> Download </a>
        <div class="dropdown-content">
          <a href="#" class="name">Windows <img
              src="https://icongr.am/simple/windows.svg?size=16&color=ffffff&colored=false"></a>
          <a href="#" class="name">Mac <img
              src="https://icongr.am/simple/apple.svg?size=16&color=ffffff&colored=false"></a>
          <a href="#" class="name">Linux <img
              src="https://icongr.am/simple/linux.svg?size=16&color=ffffff&colored=false"></a>
        </div>
      </div>
      <div class="dropdown">
        <a class="btn" style="padding: 12px 36px;">Support </a>
        <div class="dropdown-content">
          <a href="#" class="name">Patreon <img
              src="https://icongr.am/simple/patreon.svg?size=16&color=ffffff&colored=false"></a>
          <a href="#" class="name">PayPal <img
              src="https://icongr.am/simple/paypal.svg?size=16&color=ffffff&colored=false"></a>
          <a href="#" class="name">GitHub <img
              src="https://icongr.am/simple/github.svg?size=16&color=ffffff&colored=false"></a>
        </div>
      </div>
    </div>


    <div class="submain">

      <div class="explanation">
        <h1 class="semi-title-X"><img src="https://vlang.io/img/v-logo.png" width="56" height="56"> is </h1>
        <h1 class="semi-title">&#x2022 Simple</h1>
        <p> V is a simple language with a clean syntax and a focus on readability. It is designed to be easy to learn and
          easy to use.</p>
        <ul>
          <li>&#x2022 Simple syntax</li>
          <li>&#x2022 Easy to learn</li>
          <li>&#x2022 Easy to use</li>
          <li>&#x2022 Easy to read</li>
          <li>&#x2022 Easy to maintain</li>
        </ul>
        <br>
        <h1 class="semi-title">&#x2022 Fast</h1>
        <p> Lorem Ipsum Dolor Sit Amet </p>

        <ul>&#x2022 Fast compilation</ul>
        <ul>&#x2022 Fast execution</ul>
        <ul>&#x2022 Fast development</ul>


      </div>
      <pre class="code-snippet"><code>fn foo(i int, k int) {
    println('${i}: ${k}')
  }

  fn bar(i f64, k f64, j f64) {
    println('${i}: ${k} : ${j}')
  }

  fn baz(s string) {
    println(s)
  }

  fn call[T](func_name string, args ...T) {
    match func_name {
      'foo' { foo(...args) }
      'bar' { bar(...args) }
      'baz' { baz(...args) }
      else {}
    }
  }

  fn main() {
    call('foo', 10, 100)
    call('bar', 1.2, 1.3, 1.4)
    call('baz', 'test')
  }
  </code>
  </pre>
    </div>
  </main>
</template>
