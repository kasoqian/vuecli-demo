<template>
  <div>
    <div>
      当前执行的环境为：{{env.name}}
    </div>
    <div>
      调取参数呈现结果为：{{env.content}}
    </div>
    <br>
    <div>
      当前为公共环境，调取变量结果为：{{share}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      env:{
        name:"",
        content:""
      },
      share:""
    }
  },
  created(){
    this.env.name = process.env.NODE_ENV
    this.env.content = process.env.VUE_APP_TITLE

    this.share = process.env.VUE_APP_SHARE
  }
}
</script>

