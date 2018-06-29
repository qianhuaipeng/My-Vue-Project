
<view class="container">
  <swiper class="splash" indicator-dots>
    <swiper-item wx:for="{{ movies }}" wx:for-index="index" wx:key="id">
      <image src="{{ item.images.large }}" class="slide-image" mode="aspectFill"/>
      <button class="start" bindtap="handleStart" v-if="{{ index == movies.length - 1 }}">立即体验</button>
    </swiper-item>
  </swiper>
</view>

<script>
  export default {
    data () {
        return {
          movies: [],
          loading: true
        }
    },
    methods : {

    }
  }
</script>


<style>
  page {
    height: 100%;
  }
  .container {
    height: 100%;
  }

  .splash {
    height: 100%;
  }

  .splash swiper-item {
    flex: 1;
  }

  .splash swiper-item image {
    position: absolute;
    height: 100%;
    width: 100%;
    opacity: .9;
  }

  .start {
    position: absolute;
    bottom: 200rpx;
    left: 50%;
    width: 300rpx;
    margin-left: -150rpx;
    background-color: rgba(64, 88, 109, .4);
    color: #fff;
    border: 1rpx solid rgba(64, 88, 109, .8);
    border-radius: 200rpx;
    font-size: 40rpx;
  }

</style>
