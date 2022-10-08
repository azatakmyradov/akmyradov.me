<script>
    export default {
        data() {
            return {
                javascript: true,
                css: false,
                testing: '71D4B7'
            }
        },
        methods: {
            switchTo(type) {
                if (type == 'javascript') {
                    this.css = false;
                    this.javascript = true;
                } else {
                    this.javascript = false;
                    this.css = true;
                }
            }
        }
    }
</script>

<template>
    <div class="w-[90vw] lg:w-[60vw]">
        <header class="bg-[#E8ECEF] py-2 pl-2 rounded-t-lg">
            azatakmyradov.js
        </header>
        <div class="bg-[#384a56] text-[#E8ECEF]">
            <ul class="flex">
                <li
                    :class="{
                        'py-2 px-2 cursor-pointer border-r': true,
                        'bg-[#233038]': javascript,
                        'hover:bg-[#233038]': ! javascript
                    }"
                    @click="switchTo('javascript')">
                    main.js
                </li>
                <li
                    :class="{
                        'py-2 px-2 cursor-pointer border-r': true,
                        'bg-[#233038]': css,
                        'hover:bg-[#233038]': !css
                    }"
                    @click="switchTo('css')">
                    main.css
                </li>
            </ul>
        </div>
        <main class="bg-[#4e606c] overflow-scroll">
            <pre class="pl-8 pr-8">
                <code v-if="javascript">
<span class="text-[#66d9ef]">let</span> <span class="text-[#f8f8f2]">me</span> <span class="text-[#EFB26E]">=</span> <span class="text-[#f8f8f2]">{</span>
  <span class="text-[#f8f8f2]">name:</span> <span class="text-[#FC659A]">'Azat Akmyradov'</span><span class="text-[#f8f8f2]">,</span>
  <span class="text-[#f8f8f2]">age:</span> <span class="text-[#ae81ff]">22</span><span class="text-[#f8f8f2]">,</span>
  <span class="text-[#f8f8f2]">occupation:</span> <span class="text-[#FC659A]">'Web Developer'</span><span class="text-[#f8f8f2]">,</span>
  <span class="text-[#f8f8f2]">find_me_at: {</span>
    <span class="text-[#f8f8f2]">github:</span> <a href="https://github.com/azatakmyradov" class="text-[#FC659A]">'https://github.com/azatakmyradov'</a><span class="text-[#f8f8f2]">,</span>
    <span class="text-[#f8f8f2]">twitter:</span> <a href="https://twitter.com/azat_akmyradov" class="text-[#FC659A]">'https://twitter.com/azat_akmyradov'</a><span class="text-[#f8f8f2]">,</span>
    <span class="text-[#f8f8f2]">instagram:</span> <a href="https://www.instagram.com/azat.akmyradov/" class="text-[#FC659A]">'https://instagram.com/azat.akmyradov/'</a><span class="text-[#f8f8f2]">,</span>
    <span class="text-[#f8f8f2]">Email:</span> <a href="mailto:azat@akmyradov.me" class="text-[#FC659A]">'azat@akmyradov.me'</a><span class="text-[#f8f8f2]">,</span>
  <span class="text-[#f8f8f2]">}</span>
<span class="text-[#f8f8f2]">}</span>
                </code><code v-if="css">
<span class="text-[#FC659A]">body</span> <span class="text-[#f8f8f2]">{</span>
  <span class="text-[#71D4B7]">background</span><span class="text-[#f8f8f2]">:</span> <span class="text-[#f8f8f2]">#71D4B7</span><span class="text-[#f8f8f2]">,</span>
<span class="text-[#f8f8f2]">}</span>
                </code>
            </pre>
        </main>
    </div>
</template>