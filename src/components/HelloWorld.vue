<template>
  <div id="HelloWorld">
    {{message}}
    <button v-on:click="reverseMessage('123',$event)">Reverse Message</button>
    <li
      v-for="item in items"
      v-bind:key="item.id"
    >
      {{item.mes}}
    </li>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      message: "hello vue.js",
      items: [{ mes: 123 }, { mes: 456 }]
    };
  },
  methods: {
    reverseMessage: function (demo,event) {
      console.log(demo,event);
      this.message = this.message
        .split("")
        .reverse()
        .join("");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
