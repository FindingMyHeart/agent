<template>
  <div class="index">
    <mt-header fixed title="index"></mt-header>
    <div class="page-content">
      <!--<i-icon name="icon-search"></i-icon>-->
      <!--<i-icon name="icon-Artboard26" symbol></i-icon>-->
      <!--<p v-for="i in 20" :key="i" @click="toDetail">{{i}}index</p>-->

      <!--<mt-cell-->
        <!--title="充值-今日"-->
        <!--to="/Order"-->
        <!--is-link-->
        <!--label="描述信息"-->
        <!--value="fff">-->
        <!--<span style="color: green;font-size:20px;align:left">{{this.money}}</span>-->
      <!--</mt-cell>-->
      <!--<div class="page-cell">-->
      <!--<div class="page-title">Cell</div>-->
      <mt-cell
        title="充值-今日"
        to="/Order"
        is-link
        label="描述信息"
        value="fff">
        <span style="color: green;font-size:20px;align:left">{{this.money}}</span>
      </mt-cell>


      <mt-cell
        title="可结算"
        to="/Order"
        is-link
        value="fff">
        <span style="color: green;font-size:20px;align:left">{{this.money}}</span>
        <span style="color: green;font-size:20px;align:left">{{this.money}}</span>
      </mt-cell>

      <mt-cell
        title="推荐代理"
        to="/Order"
        is-link>
        <span style="color: green;font-size:20px;align:left">{{this.money}}</span>
        <!--<span style="color: green;font-size:20px;align:left">{{this.money}}</span>-->
      </mt-cell>

      <mt-cell
        title="成为代理"
        to="/Order"
        is-link>
        <!--<span style="color: green;font-size:20px;align:left">{{this.money}}</span>-->
      </mt-cell>

      <mt-cell
        title="关系查询"
        to="/Order"
        is-link>
        <!--<span style="color: green;font-size:20px;align:left">{{this.money}}</span>-->
      </mt-cell>

      <mt-cell
        title="用户协议"
        to="/Order"
        is-link>
        <!--<span style="color: green;font-size:20px;align:left">{{this.money}}</span>-->
      </mt-cell>

      <!--<mt-cell title="标题" label="描述信息" is-link></mt-cell>-->

      <!--<mt-cell title="标题文字" is-link>-->
        <!--<span style="color: green">这里是元素</span>-->
      <!--</mt-cell>-->
    </div>

<!--</div>-->
  </div>


</template>

<script>
  import {getAgentInfo } from '@/api/api'
  export default {
    name: 'index',
    data() {
      return {
          agentId:1000,
          money:0
      }
    },
    created() {
      //获得信息

      getAgentInfo().then(response=>{
          this.money = response.money
        console.log("--------------------------------")
          console.log(response.money)
      })
      console.log("00000000000000000000")
    },
    methods: {
      toDetail() {
        this.$router.push('/detail')
      }
    }
  }
</script>
