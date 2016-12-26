<template>
  <div id="music">
    <div class="search">
      <span class="searchIcon">
        <img src="./images/icon-search.png" alt="搜索">
      </span>
      <input type="text" id="searchContent" placeholder="搜索 歌曲／专辑／歌手" @click="inputFocus">
      <span class="cancle" @click="cancleClick">取消</span>
      <div class="hotSearch">
        <ul>
          <li>
            <span class="num">1</span>
            <span class="singerName">陈奕迅</span>
            <span class="hotNum">88万</span>
          </li>
          <li>
            <span class="num">2</span>
            <span class="singerName">田馥甄</span>
            <span class="hotNum">88万</span>
          </li>
          <li>
            <span class="num">3</span>
            <span class="singerName">刘德华</span>
            <span class="hotNum">88万</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
  import $ from 'jquery'
  export default {
    methods: {
      inputFocus () {
        $('#searchContent').css('width', '90%')
        $('.cancle').css('width', '10%')
        $('.hotSearch').slideDown()
      },
      cancleClick () {
        $('#searchContent').css('width', '100%')
        $('.cancle').css('width', '0')
        $('.hotSearch').slideUp()
      }
    }
  }
</script>
<style>
  *{
    margin: 0;
    padding: 0;
  }
  body{
    background: #eeeeee;
  }
  li{
    list-style: none;
  }
  #music{
    width: 476px;
    margin: 0 auto;
  }
  #music .search{
    padding: 10px;
    width: 476px;
    height: 60px;
    background: #fff;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
    position: fixed;
  }
  #music #searchContent{
    width: 100%;
    border-radius: 5px;
    background: #eeeeee;
    height: 40px;
    border: 0;
    float: left;
    padding-left: 45px;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
    font-size: 16px;
    outline: none;
    transition: width 0.3s;
  }
  #music .cancle{
    float: left;
    width: 0;
    height: 40px;
    line-height: 40px;
    text-align: center;
    transition: width 0.3s;
    overflow: hidden;
    cursor: pointer;
  }
  #music .searchIcon{
    width: 40px;
    height: 40px;
    position: absolute;
    left: 10px;
    top: 10px;
  }
  #music .searchIcon img{
    width: 100%;
  }
  #music .hotSearch{
    position: absolute;
    width: 100%;
    top: 60px;
    left: 0;
    background: #fff;
    display: none;
  }
  #music .hotSearch ul li{
    height: 40px;
    padding: 0 10px;
    cursor: pointer;
    line-height: 40px;
  }
  #music .hotSearch ul li span.num{
    padding-right: 10px;
    float: left;
  }
  #music .hotSearch ul li span.singerName{
    display: block;
    width: 80%;
    float: left;
  }
  #music .hotSearch ul li span.hotNum{
    float: right;
    margin-right: 5px;
  }
</style>


