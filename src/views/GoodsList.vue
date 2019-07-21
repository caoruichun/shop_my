<template>
  <div>
    <nav-header></nav-header>
    <nav-bread>
      <span>good</span>
    </nav-bread>
    <div class="accessory-result-page accessory-page">
      <div class="container">
        <div class="filter-nav">
          <span class="sortby">Sort by:</span>
          <a href="javascript:void(0)" class="default cur">Default</a>
          <a href="javascript:void(0)" class="price">
            Price
            <svg class="icon icon-arrow-short">
              <use xlink:href="#icon-arrow-short" />
            </svg>
          </a>
          <a href="javascript:void(0)" class="filterby stopPop">Filter by</a>
        </div>
        <div class="accessory-result">
          <!-- filter -->
          <div class="filter stopPop" id="filter">
            <dl class="filter-price">
              <dt>Price:</dt>
              <dd>
                <a href="javascript:void(0)">All</a>
              </dd>
              <dd>
                <a href="javascript:void(0)">0 - 100</a>
              </dd>
              <dd>
                <a href="javascript:void(0)">100 - 500</a>
              </dd>
              <dd>
                <a href="javascript:void(0)">500 - 1000</a>
              </dd>
              <dd>
                <a href="javascript:void(0)">1000 - 2000</a>
              </dd>
            </dl>
          </div>

          <!-- search result accessories list -->
          <div class="accessory-list-wrap">
            <div class="accessory-list col-4">
              <ul>
                <li v-for="(item,index) in goodsList" :key="item.productId">
                  <div class="pic">
                    <a href="#">
                      <img :src="item.productImg" alt />
                    </a>
                  </div>
                  <div class="main">
                    <div class="name">{{item.productName}}</div>
                    <div class="price">{{item.productPrice}}</div>
                    <div class="btn-area">
                      <a href="javascript:;" class="btn btn--m" :data-id="item.productId">加入购物车</a>
                    </div>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <navFooter></navFooter>
  </div>
</template>
<script>
import '../assets/css/base.css'
import '../assets/css/product.css'
import navHeader from '@/components/header'
import navFooter from '@/components/footer'
import navBread from '@/components/navBread'
export default {
  data () {
    return {
      goodsList: [
        { 'productId': 0,
          'productName': 0,
          'productPrice': 0,
          'productImg': 0 }
      ]
    }
  },
  components: {
    navHeader,
    navFooter,
    navBread
  },
  created () {
    let { result } = {
      'status': '0',
      'msg': '',
      'result': [{
        'productId': '100001',
        'productName': '小米1',
        'productPrice': 2493,
        'productImg': require('../assets/1.jpg')
      }, {
        'productId': '100002',
        'productName': '小米2',
        'productPrice': 2492,
        'productImg': require('../assets/2.jpg')
      }, {
        'productId': '100003',
        'productName': '小米3',
        'productPrice': 2491,
        'productImg': require('../assets/3.jpg')
      }, {
        'productId': '100004',
        'productName': '小米4',
        'productPrice': 2466,
        'productImg': require('../assets/4.jpg')
      }, {
        'productId': '100005',
        'productName': '小米5',
        'productPrice': 24125,
        'productImg': require('../assets/5.jpg')
      }, {
        'productId': '100006',
        'productName': '小米6',
        'productPrice': 2423,
        'productImg': require('../assets/6.jpg')
      }, {
        'productId': '100007',
        'productName': '小米7',
        'productPrice': 2453,
        'productImg': require('../assets/7.jpg')
      }, {
        'productId': '100008',
        'productName': '小米8',
        'productPrice': 2465,
        'productImg': require('../assets/8.jpg')
      }, {
        'productId': '100009',
        'productName': '小米9',
        'productPrice': 241,
        'productImg': require('../assets/9.jpg')
      }, {
        'productId': '1000010',
        'productName': '小米10',
        'productPrice': 2451,
        'productImg': require('../assets/10.jpg')
      }, {
        'productId': '1000011',
        'productName': '小米11',
        'productPrice': 24124,
        'productImg': require('../assets/11.jpg')
      }, {
        'productId': '1000012',
        'productName': '小米12',
        'productPrice': 2444,
        'productImg': require('../assets/12.jpg')
      }, {
        'productId': '1000013',
        'productName': '小米13',
        'productPrice': 24123,
        'productImg': require('../assets/13.jpg')
      }, {
        'productId': '1000014',
        'productName': '小米14',
        'productPrice': 2432,
        'productImg': require('../assets/14.jpg')
      }, {
        'productId': '1000015',
        'productName': '小米15',
        'productPrice': 24112,
        'productImg': require('../assets/15.jpg')
      }, {
        'productId': '1000016',
        'productName': '小米16',
        'productPrice': 2411,
        'productImg': require('../assets/16.jpg')
      }]
    }
    this.goodsList = result
  }

}
</script>
<style lang="less" scoped>
.navbar-menu-container {
  display: flex;
  justify-content: space-between;
}
.navbar-cart-logo {
  width: 100px;
  height: 50px;
}
</style>
