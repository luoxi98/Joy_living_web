<template>
  <div class="search">
    <input class="search_input" type="text" placeholder="在这里搜索..." v-model="search" />
    <button class="search_btn"><i class="iconfont icon-sousuo" @click.enter="search_btn" ></i></button>
  </div>
</template>

<script>

export default {
  data() {
    return {
      search:""
    }
  },
  methods: {
    search_btn(){
        this.$router.push({path:"/home/search",query:{keyword:this.search}})
    }
  },
};
</script>

<style>
.search {
  display: flex;
  height: 48px;

}
.search_input {
  width: 605px;
  height: 48px;
  font-size: 18px;
  outline: none;
  color: #000;
  padding: 0 30px;
  /* color: #ddd; */
  border: 1px #f4f4f4 solid;
  background-color: #f4f4f4;
  border-top-left-radius: 30px;
  border-bottom-left-radius: 30px;
}
.search_btn {
  cursor: pointer;
  padding-right:20px ;
  width: 50px;
  background-color: #f4f4f4;
  border-top-right-radius: 30px;
  border-bottom-right-radius: 30px;
}
.search_btn>.icon-sousuo{
  font-size: 20px;
}
</style>