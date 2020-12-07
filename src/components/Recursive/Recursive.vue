<template>
  <div id="app">
      <div>
          <h1> 재귀 컴포넌트 </h1>
          <tree :subs="orgcharts" />
      </div>
  </div>
</template>

<script>
import Tree from './Tree';

export default {
  name: 'Recursive',
  data() {
    return {
        orgcharts: [
            {name: "a", subs: [
                {name: "a2", subs: [
                    {name: "a3", subs: [
                        {name: "a4"},
                        {name: "b4"},
                        {name: "c4"},
                    ]}
                ]},
                {name: "b2", subs: [
                    {name: "b3"},
                    {name: "c3"},
                    {name: "d3"}
                ]}
            ]}
        ]
    }
  },
  components: {
      Tree
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
