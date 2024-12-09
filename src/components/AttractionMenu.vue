<script setup>

import { ref } from "vue";
let id = 0;
const attraction_list = ref([
  { id: id++, name: "勤美誠品綠園道", map_link: "https://maps.app.goo.gl/UJc9pFUMuFoBZi479", img: "https://cc.tvbs.com.tw/img/program/upload/2024/07/25/20240725221747-decb832e.jpg", desc: "勤美誠品綠園道，是一間位於臺灣臺中市西區的中型購物中心，商場樓板面積約為5,500坪，曾為閒置多年的大廣三百貨量販公益店舊址，後由勤美集團接手整修，並與誠品集團共同招商，於2008年5月開業。商場主力核心店為誠品書店、UNIQLO、UFC GYM、各式主題餐廳", web: "https://travel.taichung.gov.tw/zh-tw/attractions/intro/83" },
  { id: id++, name: "路思義教堂", map_link: "https://maps.app.goo.gl/NhjLL37bmKoMyAyB8", img: "https://travel.taichung.gov.tw/image/154/1024x768", desc: "路思義教堂是位於台灣台中市東海大學的基督新教禮拜堂，為著名台灣建築師陳其寬與美國華裔建築師貝聿銘之作。始建於1962年11月1日，並於1963年11月2日落成。被視為東海大學學校象徵與台灣最著名之現代建築之一", web: "https://travel.taichung.gov.tw/zh-tw/attractions/intro/74" },
  { id: id++, name: "逢甲夜市", map_link: "https://maps.app.goo.gl/9pf3ZU9twLCauePa8", img: "https://travel.taichung.gov.tw/Image/31585/?r=1675152421040", desc: "逢甲觀光夜市是位於臺灣臺中市西屯區逢甲大學周圍的知名大型商圈夜市", web: "https://travel.taichung.gov.tw/zh-tw/Attractions/Intro/39"},
  { id: id++, name: "宮原眼科", map_link: "https://maps.app.goo.gl/NhjLL37bmKoMyAyB8", img: "https://travel.taichung.gov.tw/Image/3028/?r=1662079676658", desc: "位於典雅歷史建築內的高人氣冰淇淋店，提供各種特色風味的冰淇淋，並附設餐廳", web: "https://travel.taichung.gov.tw/zh-tw/attractions/intro/74" },
  { id: id++, name: "臺中國家歌劇院", map_link: "https://maps.app.goo.gl/WNTFRzu7qbSBmhys8", img: "https://travel.taichung.gov.tw/content/images/content/attractions/top-ten-pic-01.jpg", desc: "臺中國家歌劇院是位於臺灣臺中市西屯區七期重劃區裡的大型公有展演空間，為日本建築師伊東豊雄設計，佔地57,685平方公尺。歌劇院內擁有大劇院、中劇院、小劇場以及一個小型戶外劇場，另有餐飲空間與空中花園", web: "https://travel.taichung.gov.tw/zh-tw/attractions/intro/942" },
  { id: id++, name: "草悟道", map_link: "https://maps.app.goo.gl/wnKbwQwywG7gPfyk7", img: "https://travel.taichung.gov.tw/Image/24364?r=637837893160746680", desc: "草悟道是臺灣臺中市中心一整段大範圍的綠園道景觀計畫的統稱。範圍包含經國園道到美術園道之間綠帶，全長3.6公里。景觀設計者為景觀建築事務所環藝工程顧問有限公司。", web: "https://travel.taichung.gov.tw/zh-tw/attractions/intro/786" },
  { id: id++, name: "高美濕地", map_link: "https://maps.app.goo.gl/sN8DMox5aMiD7Qiy8", img: "https://travel.taichung.gov.tw/Image/12578?r=637837893158126667", desc: "路思義教堂是位於台灣台中市東海大學的基督新教禮拜堂，為著名台灣建築師陳其寬與美國華裔建築師貝聿銘之作。始建於1962年11月1日，並於1963年11月2日落成。被視為東海大學學校象徵與台灣最著名之現代建築之一。", web: "https://travel.taichung.gov.tw/zh-tw/attractions/intro/54" },
  { id: id++, name: "臺中公園", map_link: "https://maps.app.goo.gl/aopkULe4UVvC1M8A7", img: "https://travel.taichung.gov.tw/Image/50424?r=637837893157956680", desc: "臺中公園是一座位於臺灣臺中市北區的公園，位於自由路、雙十路、精武路交接路口，該公園於日治時期所創立，是臺中市歷史最悠久的公園，園區佔地約32,889坪。 當前，該公園內的湖心亭為臺中市的重要象徵。自創設之初，即陸續移入或設置歷史主題的紀念物，使公園成為代表臺中歷史的展示空間，園區多個設施已具有文化資產身份", web: "https://travel.taichung.gov.tw/zh-tw/attractions/intro/28" },
]);

</script>

<template>

  <div>
    <div>
      <h2>景點</h2>
    </div>
    <div>
      <ul class="attractions" >
        <li v-for="attr in attraction_list" :key="attr.id">
          <div class="attr_head">
            <h3 class="attr_title">{{ attr.name }}</h3>
            <img class="attr_img" :src="attr.img">
          </div>
          <p class="attr_desc">{{ attr.desc }}</p>
          <div class="link_group">
            <a class="link" :href="attr.map_link" target="_blank">網頁</a>
            <a class="link" :href="attr.map_link" target="_blank">地圖</a>
          </div>
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
  color: white;
  font-weight: bold;
  font-family: monospace;
  font-size: 1.5rem;
}

.attr_head {
  display: inline;
  padding: 12px
}

.attr_title {
  display: inline;
  float: inline-start;
  padding: 12px;
}

.attr_img {
  display: inline;
  height: 64px;
  width: 64px;
  float: right;
  border-radius: 12px;
}

.attr_desc {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: normal;
  transition: max-height 0.3s ease;
  max-height: 3rem;
}

ul {
  list-style-type: none;
}

li {
  display: grid;
  grid-template-rows: 1fr;
  padding: 8px;
  border-radius: 12px;
}

.link_group {
  display: inline;
  padding: 4px
}

.link {
  float: right;
  padding: 4px;
  margin-inline: 4px;
  text-align: center;
  color: black;
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 4px;
}
.padding {
  padding: 2px;
}

@media (hover:hover){
  li:hover {
    background-color: rgba(255, 255, 255, 0.25);
  }
  .attr_map:hover {
    background-color: rgb(255, 255, 255);
  }

  li:hover .attr_desc {
    -webkit-line-clamp: unset;
    max-height: 100%;
    overflow: visible;
  }
}

@media (min-width: 1024px){
  .attractions {
    display: grid;
    grid-template-columns: 2fr 2fr;
  }
}
</style>
