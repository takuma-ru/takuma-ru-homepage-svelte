<script>
  import LinkBtn from './linkBtn.svelte'
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
    <LinkBtn></LinkBtn>
    <LinkBtn></LinkBtn>
    <LinkBtn></LinkBtn>
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
  position: absolute;
  width: 144px;
  height: 24px;
  left: 152px;
  top: 12px;
  display: inline-block;
}

</style>
