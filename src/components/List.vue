<template>
 
    <div id="list-container">
      <li class="list-item" v-for="item in items" :key="item.title">
        <p>{{ item.title }}</p>
        <img class = "list-image" src="https://picsum.photos/200/300"/>
        <p>{{item.content}}</p>
      </li>

  </div>
</template>

<script>

export default {
  name: 'List',
  data() {
    return {
      items: [
        { title: "Item 0", content: "Content item with description" },
        { title: "Item 1", content: "Content item with description" },
        { title: "Item 2", content: "Content item with description" },
        { title: "Item 1", content: "Content item with description" },

      ],
    };
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.list-container{
   display:flex;
  padding-left:20vw;
  padding-right: 20vw;
  overflow: scroll; 

}

.list-image{
  border-radius: 20px;
  
}

.list-item{
  background-color: black;
  color: white;
  min-height: 20vh;
  width: 20%;
    border-radius: 20px;
}
</style>
