<script setup>
import Navbar from '../components/Navbar.vue'
import Footer from '../components/Footer.vue'

import { onMounted, ref } from 'vue';

const quotes = [
  {
    author: "Swastik Baranwal",
    quote: "In my opinion V does have a lot of potential and has rapid development which can keep up with its promises and rock when it comes out.",
    platform: "dev.to"
  },
  {
    author: "Unknown",
    quote: "If Rust and Golang had children, then it would be V",
    platform: "Unknown"
  }
]
// get random quote
const quot = quotes[Math.floor(Math.random() * quotes.length)];
let author = ref(quot.author);
let quote = ref(quot.quote);
let platform = ref(quot.platform);

const text = ref("Faster");

onMounted(() => {
  const words = ["Simpler", "Better", "Easier", "More Maintainable", "Faster"];
  let i = 0;
  const animate = ref(false);

  setInterval(() => {
    animate.value = true;
    setTimeout(() => {
      text.value = words[i];
      i = (i + 1) % words.length;
      animate.value = false;
    }, 500); // Adjust the duration of the animation (in milliseconds) as per your preference
  }, 10000);

  return {
    text,
    animate
  };
});


</script>

<template>
  <Navbar />

  <nmain>
    <!-- Hero -->
    <div
      class="relative overflow-hidden before:absolute before:top-0 before:left-1/2 before:bg-[url('../svg/component/polygon.svg')] before:bg-no-repeat before:bg-top before:bg-cover before:w-full before:h-full before:-z-[1] before:transform before:-translate-x-1/2 dark:before:bg-[url('../svg/component/polygon-dark.svg')]">
      <div class="max-w-[85rem] mx-auto px-4 sm:px-6 lg:px-8 ">
        <!-- Title -->
        <div class="mt-5 max-w-2xl text-center mx-auto">
          <h1 class="block font-bold text-gray-800 text-4xl md:text-5xl lg:text-6xl dark:text-gray-200">
            Build
            <span id="text" class="bg-clip-text bg-gradient-to-tl from-blue-600 to-violet-600 text-transparent word-transition" :class="{ 'word-animation-active': animate }" :key="text">{{ text
            }}</span>
            Software
          </h1>
        </div>
        <!-- End Title -->

        <div class="mt-5 max-w-3xl text-center mx-auto">
          <p class="text-lg text-gray-600 dark:text-gray-400">Simple, fast, safe, compiled. For developing maintainable
            software. </p>
        </div>

        <!-- Buttons -->
        <div class="mt-8 grid gap-3 w-full sm:inline-flex sm:justify-center">
          <a class="inline-flex justify-center items-center gap-x-3 text-center bg-gradient-to-tl from-blue-600 to-violet-600 hover:from-violet-600 hover:to-blue-600 border border-transparent text-white text-sm font-medium rounded-md focus:outline-none focus:ring-2 focus:ring-blue-600 focus:ring-offset-2 focus:ring-offset-white py-3 px-4 dark:focus:ring-offset-gray-800"
            href="#">
            Get started
            <svg class="w-3 h-3" width="16" height="16" viewBox="0 0 16 16" fill="none">
              <path d="M5.27921 2L10.9257 7.64645C11.1209 7.84171 11.1209 8.15829 10.9257 8.35355L5.27921 14"
                stroke="currentColor" stroke-width="2" stroke-linecap="round" />
            </svg>
          </a>
          <a class="relative group inline-flex justify-center items-center gap-x-3.5 text-center bg-white border hover:border-gray-300 shadow-sm font-mono text-sm font-medium rounded-md focus:outline-none focus:ring-2 focus:ring-gray-400 focus:ring-offset-2 focus:ring-offset-white transition p-2 pl-4 dark:bg-slate-900 dark:border-gray-800 dark:hover:border-gray-600 dark:shadow-slate-700/[.7] dark:text-white dark:focus:ring-gray-700 dark:focus:ring-offset-gray-800"
            href="javascript:;">
            $ lorem ipsum install sccript
            <span
              class="flex justify-center items-center bg-gray-200 rounded-md w-7 h-7 dark:bg-gray-700 dark:text-gray-400">
              <svg class="w-3.5 h-3.5 group-hover:rotate-6 transition" width="16" height="16" fill="currentColor"
                viewBox="0 0 16 16">
                <path
                  d="M4 1.5H3a2 2 0 0 0-2 2V14a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2V3.5a2 2 0 0 0-2-2h-1v1h1a1 1 0 0 1 1 1V14a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V3.5a1 1 0 0 1 1-1h1v-1z" />
                <path
                  d="M9.5 1a.5.5 0 0 1 .5.5v1a.5.5 0 0 1-.5.5h-3a.5.5 0 0 1-.5-.5v-1a.5.5 0 0 1 .5-.5h3zm-3-1A1.5 1.5 0 0 0 5 1.5v1A1.5 1.5 0 0 0 6.5 4h3A1.5 1.5 0 0 0 11 2.5v-1A1.5 1.5 0 0 0 9.5 0h-3z" />
              </svg>
            </span>
          </a>
        </div>
        <!-- End Buttons -->

      </div>
    </div>
    <!-- End Hero -->
  </nmain>
  <div class="relative max-w-[85rem] px-4 py-10 sm:px-6 lg:px-8 lg:py-14 mx-auto">
    <!-- Blockquote -->
    <blockquote class="text-center lg:mx-auto lg:w-3/5">

      <div class="mt-6 lg:mt-10">
        <p class="relative text-xl sm:text-2xl md:text-3xl md:leading-normal font-medium text-gray-800">
          <svg
            class="absolute top-0 left-0 transform -translate-x-8 -translate-y-8 h-16 w-16 text-gray-200 sm:h-24 sm:w-24 dark:text-gray-700"
            width="16" height="13" viewBox="0 0 16 13" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <path
              d="M7.18079 9.25611C7.18079 10.0101 6.93759 10.6211 6.45119 11.0891C5.96479 11.5311 5.35039 11.7521 4.60799 11.7521C3.71199 11.7521 2.96958 11.4531 2.38078 10.8551C1.81758 10.2571 1.53598 9.39911 1.53598 8.28111C1.53598 7.08511 1.86878 5.91511 2.53438 4.77111C3.22559 3.60111 4.18559 2.67811 5.41439 2.00211L6.29759 3.36711C5.63199 3.83511 5.09439 4.35511 4.68479 4.92711C4.30079 5.49911 4.04479 6.16211 3.91679 6.91611C4.14719 6.81211 4.41599 6.76011 4.72319 6.76011C5.43999 6.76011 6.02879 6.99411 6.48959 7.46211C6.95039 7.93011 7.18079 8.52811 7.18079 9.25611ZM14.2464 9.25611C14.2464 10.0101 14.0032 10.6211 13.5168 11.0891C13.0304 11.5311 12.416 11.7521 11.6736 11.7521C10.7776 11.7521 10.0352 11.4531 9.44639 10.8551C8.88319 10.2571 8.60159 9.39911 8.60159 8.28111C8.60159 7.08511 8.93439 5.91511 9.59999 4.77111C10.2912 3.60111 11.2512 2.67811 12.48 2.00211L13.3632 3.36711C12.6976 3.83511 12.16 4.35511 11.7504 4.92711C11.3664 5.49911 11.1104 6.16211 10.9824 6.91611C11.2128 6.81211 11.4816 6.76011 11.7888 6.76011C12.5056 6.76011 13.0944 6.99411 13.5552 7.46211C14.016 7.93011 14.2464 8.52811 14.2464 9.25611Z"
              fill="currentColor" />
          </svg>
          <span class="relative z-10 italic text-gray-800 dark:text-gray-200">{{ quote }}</span>
        </p>
      </div>

      <footer class="mt-6">
        <div class="font-semibold text-gray-800 dark:text-gray-200">{{ author }}</div>
        <div class="text-sm text-gray-500"> {{ platform }} </div>
      </footer>
    </blockquote>
    <!-- End Blockquote -->
  </div>
  <main>
    <!-- Hero -->
    <div class="max-w-[85rem] mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Grid -->
      <div class="grid md:grid-cols-2 gap-4 md:gap-8 xl:gap-20 md:items-center">
        <div>
          <h1 class="block text-3xl font-bold text-gray-800 sm:text-4xl lg:text-6xl lg:leading-tight dark:text-white">
            The <img src="../assets/logo.svg" class="inline-block h-16 align-middle" /> Programming
            Language
          </h1>
          <p class="mt-3 text-lg text-gray-800 dark:text-gray-400 mb-5">
            Simple, fast, safe, compiled. For developing maintainable software.
          </p>

          <!-- Buttons -->
          <div class="mt-5 grid gap-3 w-full sm:inline">
            <button type="button" style="background-color: #121212" data-hs-overlay="#hs-sign-out-alert"
              class="py-3 mr-2 px-4 inline-flex justify-center items-center gap-2 rounded-md border font-semibold text-gray-400 hover:bg-gray-900 focus:outline-none focus:ring-2 focus:ring-gray-800 focus:ring-offset-2 transition-all text-sm dark:focus:ring-gray-900 dark:border-gray-700 dark:focus:ring-offset-gray-800">
              Support Us
            </button>
            <div class="inline-flex">
              <button type="button" style="background-color: #121212"
                class="relative py-3 px-4 inline-flex justify-center items-center gap-2 rounded-l-md border font-medium text-gray-700 shadow-sm align-middle hover:bg-gray-50 focus:z-10 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-white focus:ring-blue-600 transition-all text-sm dark:hover:bg-slate-800 dark:border-gray-700 dark:hover:text-white dark:text-gray-400 dark:focus:ring-offset-gray-800">
                Download for Windows
              </button>
              <div class="mr-5 hs-dropdown relative inline-flex [--placement:bottom-right]">
                <button id="hs-split-dropdown" type="button" style="background-color: #121212"
                  class="hs-dropdown-toggle relative -ml-[.3125rem] py-3 px-4 inline-flex justify-center items-center gap-2 h-[2.875rem] w-[2.875rem] rounded-r-md border font-medium text-gray-700 shadow-sm align-middle hover:bg-gray-50 focus:z-10 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-white focus:ring-blue-600 transition-all text-sm dark:hover:bg-slate-800 dark:border-gray-700 dark:text-gray-400 dark:hover:text-white dark:focus:ring-offset-gray-800">
                  <span class="sr-only">Toggle Dropdown</span>
                  <svg class="hs-dropdown-open:rotate-180 w-2.5 h-2.5 text-gray-600" width="16" height="16"
                    viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M2 5L8.16086 10.6869C8.35239 10.8637 8.64761 10.8637 8.83914 10.6869L15 5"
                      stroke="currentColor" stroke-width="2" stroke-linecap="round" />
                  </svg>
                </button>

                <div style="background-color: #121212"
                  class="hs-dropdown-menu w-72 transition-[opacity,margin] duration hs-dropdown-open:opacity-100 opacity-0 hidden z-10 bg-white shadow-md rounded-lg p-2 mt-2 dark:bg-gray-800 dark:border dark:border-gray-700 dark:divide-gray-700"
                  aria-labelledby="hs-split-dropdown">
                  <a class="flex items-center gap-x-3.5 py-2 px-3 rounded-md text-sm text-gray-800 hover:bg-gray-100 focus:ring-2 focus:ring-blue-500 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-gray-300"
                    href="#">
                    Windows
                  </a>
                  <a class="flex items-center gap-x-3.5 py-2 px-3 rounded-md text-sm text-gray-800 hover:bg-gray-100 focus:ring-2 focus:ring-blue-500 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-gray-300"
                    href="#">
                    Macos
                  </a>
                  <a class="flex items-center gap-x-3.5 py-2 px-3 rounded-md text-sm text-gray-800 hover:bg-gray-100 focus:ring-2 focus:ring-blue-500 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-gray-300"
                    href="#">
                    Linux
                  </a>
                </div>
              </div>
            </div>
          </div>
          <!-- End Buttons -->
          <!-- End Review -->
        </div>
        <!-- End Col -->

        <div class="relative">
          <code style="background: #fffcfc05"
            class="text-xl sm:text-xl inline-flex text-left items-center space-x-4 text-white rounded-lg p-10">
                        <span>
                          <span class="text-blue-500">areas</span> := [
                          <span class="text-green-500">'game'</span>, <span class="text-green-500">'web'</span>,
                          <span class="text-green-500">'tools'</span>,
                          <span class="text-green-500">'science'</span>,
                          <span class="text-green-500">'systems'</span>,
                          <span class="text-green-500">'embedded'</span>,
                          <span class="text-green-500">'drivers'</span>,
                          <span class="text-green-500">'GUI'</span> ] <br /><br /><span class="text-blue-500"
                            >for</span
                          >
                          area <span class="text-blue-500">in</span> areas { <br /><span class="ml-5"
                            ><span class="text-blue-500">if</span> area <span class="text-white">==</span>
                            <span class="text-green-500">'game'</span> {</span
                          >
                          <br /><span class="ml-10"
                            ><span class="text-blue-200">println</span>("What is your favorite game?")</span
                          >
                          <br /><span class="ml-5"
                            ><span class="text-green-500"><span class="text-white">}</span> else</span> {</span
                          >
                          <br /><span class="ml-10"
                            ><span class="text-blue-200">println</span>('Hello,
                            <span class="text-yellow-500">${area}</span> developers!')</span
                          >
                          <br /><span class="ml-5">}</span> <br /><span>}</span>
                        </span>
                      </code>

          <!-- End SVG-->
        </div>
        <!-- End Col -->
      </div>
      <!-- End Grid -->
    </div>
    <!-- End Hero -->
  </main>
  <sub class="mt-10">
    <!-- grid of 6 images -->
    <!-- Testimonials -->
    <div id="test" class="max-w-[85rem] px-4 py-10 sm:px-6 lg:px-8 lg:py-14 mx-auto">
      <center>
        <h1
          class="mb-4 text-4xl font-extrabold leading-none tracking-tight text-gray-900 md:text-5xl lg:text-4xl dark:text-white">
          Partners & Sponsors
        </h1>
      </center>
      <div class="grid grid-cols-1 gap-12 sm:grid-cols-2 md:gap-20 md:grid-cols-3 lg:grid-cols-5 lg:gap-8">
        <div class="text-center">
          <img src="../assets/chipnetics.svg" class="w-auto h-32 mx-auto text-gray-800 dark:text-gray-200" height="512" />
        </div>
        <div class="text-center">
          <img src="../assets/whatlab.png" class="w-auto h-28 mx-auto text-gray-800 dark:text-gray-200" height="512" />
        </div>
        <div class="text-center">
          <img src="../assets/sponsor_mx.png" class="w-auto h-32 mx-auto text-gray-800 dark:text-gray-200" height="512" />
        </div>
        <div class="text-center image-center self-center bg-center">
          <img src="../assets/syndica.png" class="w-auto h-14 mx-auto text-gray-800 dark:text-gray-200" height="512" />
        </div>
        <div class="text-center image-center self-center bg-center">
          <img src="../assets/threefold.png" class="w-auto h-32 mx-auto text-gray-800 dark:text-gray-200" height="512" />
        </div>
      </div>
    </div>
  </sub>
  <remain>
    <div class="max-w-[85rem] px-4 py-10 sm:px-6 lg:px-8 lg:py-14 mx-auto">
      <div class="max-w-4xl mx-auto">
        <!-- Grid -->
        <div class="grid md:grid-cols-2 gap-6 lg:gap-12">
          <div class="space-y-6 lg:space-y-10">
            <!-- Icon Block -->
            <div class="flex">
              <box-icon size="48px" name="run" color="#ffffff"></box-icon>
              <div class="ml-5 sm:ml-8">
                <h3 class="text-base sm:text-lg font-semibold text-gray-800 dark:text-gray-200">
                  Performance
                </h3>
                <p class="mt-1 text-gray-600 dark:text-gray-400">
                  V is designed to be as performant as possible and it is as fast as C (V's main
                  backend compiles to human readable C), with equivalent code.
                </p>
              </div>
            </div>
            <!-- End Icon Block -->

            <!-- Icon Block -->
            <div class="flex">
              <box-icon size="48px" name="package" color="#ffffff"></box-icon>

              <div class="ml-5 sm:ml-8">
                <h3 class="text-base sm:text-lg font-semibold text-gray-800 dark:text-gray-200">
                  Fast compilation
                </h3>
                <p class="mt-1 text-gray-600 dark:text-gray-400">
                  V is written in V and compiles itself in under a second. V compiles ≈110k/≈500k
                  lines of code per second.
                </p>
              </div>
            </div>
            <!-- End Icon Block -->

            <!-- Icon Block -->
            <div class="flex">
              <box-icon size="48px" name="intersect" color="#ffffff"></box-icon>

              <div class="ml-5 sm:ml-8">
                <h3 class="text-base sm:text-lg font-semibold text-gray-800 dark:text-gray-200">
                  C interop
                </h3>
                <p class="mt-1 text-gray-600 dark:text-gray-400">
                  V can interop with C without any performance bottlenecks. But these features can
                  be disabled/bypassed when performance is more important).
                </p>
              </div>
            </div>
            <!-- End Icon Block -->
          </div>
          <!-- End Col -->

          <div class="space-y-6 lg:space-y-10">
            <!-- Icon Block -->
            <div class="flex">
              <box-icon size="48px" name="memory-card" color="#ffffff"></box-icon>

              <div class="ml-5 sm:ml-8">
                <h3 class="text-base sm:text-lg font-semibold text-gray-800 dark:text-gray-200">
                  Flexible memory management
                </h3>
                <p class="mt-1 text-gray-600 dark:text-gray-400">
                  V avoids doing unnecessary allocations by using value types, string buffers,
                  promoting a simple abstraction-free code style. V also has 4 ways of managing
                  memory.
                </p>
              </div>
            </div>
            <!-- End Icon Block -->

            <!-- Icon Block -->
            <div class="flex">
              <box-icon size="48px" name="hot" type="solid" color="#ffffff"></box-icon>

              <div class="ml-5 sm:ml-8">
                <h3 class="text-base sm:text-lg font-semibold text-gray-800 dark:text-gray-200">
                  Hot code reloading
                </h3>
                <p class="mt-1 text-gray-600 dark:text-gray-400">
                  Get your changes instantly without recompiling, saving time during development.
                </p>
              </div>
            </div>
            <!-- End Icon Block -->

            <!-- Icon Block -->
            <div class="flex">
              <box-icon size="48px" name="landscape" color="#ffffff"></box-icon>

              <div class="ml-5 sm:ml-8">
                <h3 class="text-base sm:text-lg font-semibold text-gray-800 dark:text-gray-200">
                  A powerful graphics library
                </h3>
                <p class="mt-1 text-gray-600 dark:text-gray-400">
                  Cross-platform drawing library, using OpenGL/Metal/DirectX 11 for rendering 2D/3D
                  applications.
                </p>
              </div>
            </div>
            <!-- End Icon Block -->
          </div>
          <!-- End Col -->
        </div>
        <!-- End Grid -->
      </div>
    </div>
  </remain>
  <center>
    <div class="flex flex-col" style="width: 70%" id="hide">
      <div class="-m-1.5 overflow-x-auto">
        <div class="p-1.5 min-w-full inline-block align-middle">
          <div class="overflow-hidden">
            <table class="min-w-full divide-y divide-gray-200 dark:divide-gray-700">
              <thead>
              </thead>
              <tbody class="divide-y divide-gray-200 dark:divide-gray-700">
                <tr>
                  <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-800 dark:text-gray-200">Fast
                    compilation: </td>
                  <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-800 dark:text-gray-200">V, D, Go, Delphi</td>
                </tr>
                <tr>
                  <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-800 dark:text-gray-200">Simplicity
                    & maintainability: </td>
                  <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-800 dark:text-gray-200">V, Go</td>
                </tr>
                <tr>
                  <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-800 dark:text-gray-200">Great
                    performance on par with C and zero cost C interop:</td>
                  <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-800 dark:text-gray-200">V, C, C++, D, Delphi,
                    Rust</td>
                </tr>
                <tr>
                  <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-800 dark:text-gray-200">Safety
                    (immutability, no null, option types, free from data races) </td>
                  <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-800 dark:text-gray-200">V, Rust</td>
                </tr>
                <tr>
                  <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-800 dark:text-gray-200">Easy
                    concurrency: </td>
                  <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-800 dark:text-gray-200">V, Go</td>
                </tr>
                <tr>
                  <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-800 dark:text-gray-200">Easy cross
                    compilation: </td>
                  <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-800 dark:text-gray-200">V, Go</td>
                </tr>
                <tr>
                  <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-800 dark:text-gray-200">Small
                    compiler with zero dependencies: </td>
                  <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-800 dark:text-gray-200">V</td>
                </tr>
                <tr>
                  <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-800 dark:text-gray-200">No global
                    state: </td>
                  <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-800 dark:text-gray-200">V</td>
                </tr>
                <tr>
                  <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-800 dark:text-gray-200">Hot code
                    reloading: </td>
                  <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-800 dark:text-gray-200">V, C# (.NET 6+), Dart
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
  </div>
  </center>
<Footer /></template>