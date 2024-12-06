<script setup>
import { ref } from "vue";
let id = 0;
const attraction_list = ref([
  {id: id++, name: "勤美誠品綠園道", map_link: "https://g.co/kgs/oLC16wd", img: "https://cc.tvbs.com.tw/img/program/upload/2024/07/25/20240725221747-decb832e.jpg", desc: "勤美誠品綠園道，是一間位於臺灣臺中市西區的中型購物中心，商場樓板面積約為5,500坪，曾為閒置多年的大廣三百貨量販公益店舊址，後由勤美集團接手整修，並與誠品集團共同招商，於2008年5月開業。商場主力核心店為誠品書店、UNIQLO、UFC GYM、各式主題餐廳。", web: "https://travel.taichung.gov.tw/zh-tw/attractions/intro/83"},
  {id: id++, name: "路思義教堂", map_link: "https://g.co/kgs/C7X47nD", img: "https://travel.taichung.gov.tw/image/154/1024x768", desc: "路思義教堂是位於台灣台中市東海大學的基督新教禮拜堂，為著名台灣建築師陳其寬與美國華裔建築師貝聿銘之作。始建於1962年11月1日，並於1963年11月2日落成。被視為東海大學學校象徵與台灣最著名之現代建築之一。", web: "https://travel.taichung.gov.tw/zh-tw/attractions/intro/74"},
])
</script>

<template>

  <div>
    <div>
      <h2>景點</h2>
    </div>
    <div>
      <ul>
        <li v-for="attr in attraction_list" :key="attr.id">
          <img class="attr_img" :src="attr.img">
          <h3 class="attr_title">{{ attr.name }}</h3>
          <p class="attr_desc">{{ attr.desc }}</p>
          <a class="attr_map" :href="attr.map_link" target="_blank">地圖</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style>

h2 {
  font-weight: bold;
  font-family: monospace;
  font-size: 2rem;
}

h3 {
  font-weight: bold;
  font-family: monospace;
  font-size: 1.5rem;
}

.attr_map {
  /* float: right;  */
  padding: 4px;
  text-align: center;
  color: black;
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 4px;
}

.attr_desc {
  padding: 12px;
}

ul {
  list-style-type: none;
}

li {
  padding: 8px;
  border-radius: 12px;
}

@media (hover:hover){
  li:hover {
    background-color: rgba(255, 255, 255, 0.25);
  }
  .attr_map:hover {
    background-color: rgb(255, 255, 255);
  }
}

.attr_img {
  height: 64px;
  width: 64px;
  margin-left: 12px;
  float: right;
  border-radius: 12px;
}
</style>
