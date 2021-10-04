<script>
  import LinkBtn from './linkBtn.svelte'
	import { location } from 'svelte-spa-router';
</script>

<div>
  <div class="frame"></div>
  <div id="decoLeftTop">
    <div class="one"></div>
    <div class="two"></div>
    <div class="two"></div>
    <div class="two"></div>
  </div>
  <div id="linkHeader">
    <LinkBtn>Home</LinkBtn>
    <LinkBtn></LinkBtn>
    <LinkBtn></LinkBtn>
  </div>
  <div id="decoRightTop">
    <div class="path_name">{$location}</div>
    <div class="long_bar beside">
      <div class="short_bar top"></div>
      <div class="short_bar bottom"></div>
    </div>
    <div class="long_bar vertical"></div>
  </div>
</div>

<style>
.frame {
  z-index: 0;
  position: fixed;
  width: calc(100vw - 96px);
  height: calc(100vh - 96px);
  border: solid 48px #68B9D2;
}

#decoLeftTop {
  position: absolute;
  margin-top: 48px;
  margin-left: 8px;
  width: 16px;
  height: 112px;
}

#decoLeftTop .one {
  width: 100%;
  height: 48px;
  background-color: #FEFEFE;
}

#decoLeftTop .two {
  width: 100%;
  height: 8px;
  margin-top: 8px;
  background-color: #FEFEFE;
}

#linkHeader {
  display: grid;
  position: absolute;
  height: 24px;
  left: 152px;
  top: 12px;
  display: inline-block;
}

#decoRightTop {
  position: absolute;
  top: 24px;
  right: 24px;
}

#decoRightTop .long_bar {
  position: absolute;
  width: 128px;
  height: 2px;
  background-color: #FEFEFE;
}

#decoRightTop .long_bar.beside {
  right: 0px;
  top: 0px;
}

#decoRightTop .long_bar.vertical {
  right: -64px;
  top: 64px;
  transform: rotate(-90deg);
}

#decoRightTop .short_bar {
  position: relative;
  width: 16px;
  height: 2px;
  background-color: #FEFEFE;
}

#decoRightTop .short_bar.top {
  right: 0px;
  top: -8px;
}

#decoRightTop .short_bar.bottom {
  right: 0px;
  top: 6px;
}

.path_name {
  position: relative;
  width: fit-content;
  top: 50%;
  right: 152px;
  line-height: 24px;
  transform: translateY(-50%);
  font-size: 24px;
  color: #FEFEFE;
}

</style>
