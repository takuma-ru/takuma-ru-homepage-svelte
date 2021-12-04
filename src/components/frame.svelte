<script>
  import LinkBtn from './linkBtn.svelte'
	import { location } from 'svelte-spa-router';
</script>

<div id="main_frame">
  <div class="frame">
    <div class="top" />
    <div class="bottom" />
    <div class="left" />
    <div class="right" />
  </div>
  <div id="deco_left_top">
    <div class="one" />
    <div class="two" />
    <div class="two" />
    <div class="two" />
  </div>
  <div id="deco_left_bottom">
    <div class="one" />
    <div class="one" />
    <div class="one" />
    <div class="one" />
    <div class="one" />
    <div class="one" />
    <div class="one" />
    <div class="one" />
  </div>
  <div id="deco_right_top">
    <div class="path_name">{$location}</div>
    <div class="long_bar beside">
      <div class="short_bar top"></div>
      <div class="short_bar bottom"></div>
    </div>
    <div class="long_bar vertical"></div>
  </div>
  <div id="deco_right_center">
    <div class="one" />
    <div class="one" />
    <div class="two" />
    <div class="one" />
    <div class="one" />
  </div>
  <div id="deco_right_bottom">
    <div class="bottom_contents"></div>
    <div class="long_bar beside">
      <div class="short_bar top"></div>
      <div class="short_bar bottom"></div>
    </div>
    <div class="long_bar vertical"></div>
  </div>
  <div id="deco_contents_left_top">
    <div class="one"></div>
  </div>
  <div id="deco_contents_right_bottom">
    <div class="one"></div>
  </div>
  <div id="link_header">
    <LinkBtn link-path="/">Home</LinkBtn>
    <LinkBtn link-path="/about">About</LinkBtn>
    <LinkBtn link-path="/app">APP</LinkBtn>
    <LinkBtn link-path="/contact">CONTACT</LinkBtn>
  </div>
</div>

<style>
.frame {
  position: fixed;
  z-index: 1;
}

.frame .top {
  position: fixed;
  width: 100vw;
  height: 48px;
  top: 0px;

  background-color: #0084AD;
}

.frame .bottom {
  position: fixed;
  width: 100vw;
  height: 48px;
  bottom: 0px;

  background-color: #0084AD;
}

.frame .left {
  position: fixed;
  width: 48px;
  height: 100vh;
  top: 0px;
  left: 0px;

  background-color: #0084AD;
}

.frame .right {
  position: fixed;
  width: 48px;
  height: 100vh;
  top: 0px;

  right: 0px;

  background-color: #0084AD;
}

/* deco_left_top */
#deco_left_top {
  position: fixed;
  z-index: 2;
  top: 48px;
  left: 16px;
  width: 16px;
  height: 112px;
}

#deco_left_top .one {
  width: 100%;
  height: 48px;
  background-color: #101010;
}

#deco_left_top .two {
  width: 100%;
  height: 8px;
  margin-top: 8px;
  background-color: #101010;
}

/* deco_left_bottom */
#deco_left_bottom {
  position: fixed;
  z-index: 2;
  bottom: 0px;
  left: 48px;
  height: 16px;
}

#deco_left_bottom .one {
  float: left;
  width: 4px;
  height: 100%;
  margin-right: 8px;
  margin-left: 0px;
  background: #101010;
}

/* link_header */
#link_header {
  position: fixed;
  z-index: 2;
  height: 24px;
  left: 152px;
  top: 12px;
}

/* deco_right_top */
#deco_right_top {
  position: fixed;
  z-index: 2;
  top: 24px;
  right: 24px;
}

#deco_right_top .long_bar {
  position: absolute;
  width: 128px;
  height: 2px;
  background-color: #101010;
}

#deco_right_top .long_bar.beside {
  right: 0px;
  top: 0px;
}

#deco_right_top .long_bar.vertical {
  right: -64px;
  top: 64px;
  transform: rotate(-90deg);
}

#deco_right_top .short_bar {
  position: relative;
  width: 16px;
  height: 2px;
  background-color: #101010;
}

#deco_right_top .short_bar.top {
  right: 0px;
  top: -8px;
}

#deco_right_top .short_bar.bottom {
  right: 0px;
  top: 6px;
}

/* path_name */
.path_name {
  position: relative;
  width: fit-content;
  top: 50%;
  right: 152px;
  line-height: 24px;
  transform: translateY(-50%);
  font-size: 24px;
  color: #101010;
}

/* deco_right_center */
#deco_right_center {
  position: fixed;
  z-index: 2;
  right: 16px;
  top: 50%;

  transform: translateY(-50%);

  width: 16px;
}

#deco_right_center .one {
  position: relative;
  width: 16px;
  height: 16px;
  margin-bottom: 8px;
}

#deco_right_center .one::before {
  position: absolute;
  content: "";
  width: 4px;
  height: 16px;
  left: 0px;

  background-color: #101010;
}

#deco_right_center .one::after {
  position:absolute;
  content: "";
  width: 4px;
  height: 16px;
  right: 0px;

  background-color: #101010;
}

#deco_right_center .two {
  position: relative;
  width: 16px;
  height: 16px;
  margin-bottom: 8px;

  background-color: #101010;
}

/* deco_right_bottom */
#deco_right_bottom {
  position: fixed;
  z-index: 2;
  bottom: 24px;
  right: 24px;
}
#deco_right_bottom .long_bar {
  position: absolute;
  width: 128px;
  height: 2px;
  background-color: #101010;
}

#deco_right_bottom .long_bar.beside {
  right: 0px;
  top: 0px;
}

#deco_right_bottom .long_bar.vertical {
  right: -64px;
  bottom: 61px;
  transform: rotate(-90deg);
}

#deco_right_bottom .short_bar {
  position: relative;
  width: 16px;
  height: 2px;
  background-color: #101010;
}

#deco_right_bottom .short_bar.top {
  right: 0px;
  top: -8px;
}

#deco_right_bottom .short_bar.bottom {
  right: 0px;
  top: 6px;
}

/* deco_contents_left_top */
#deco_contents_left_top {
  position: fixed;
  z-index: 2;
  width: 36px;
  height: 36px;
  left: 56px;
  top: 56px;
}

#deco_contents_left_top::before {
  position: absolute;
  content: "";
  width: 2px;
  height: 100%;

  background-color: #101010;
}

#deco_contents_left_top::after {
  position: absolute;
  content: "";
  width: 100%;
  height: 2px;

  background-color: #101010;
}

#deco_contents_left_top .one {
  position: absolute;
  width: 8px;
  height: 8px;
  margin: 4px;

  background-color: #101010;
}

/* deco_contents_right_bottom */
#deco_contents_right_bottom {
  position: fixed;
  z-index: 2;
  width: 36px;
  height: 36px;
  right: 56px;
  bottom: 56px;
}

#deco_contents_right_bottom::before {
  position: absolute;
  content: "";
  width: 2px;
  height: 100%;
  right: 0px;

  background-color: #101010;
}

#deco_contents_right_bottom::after {
  position: absolute;
  content: "";
  width: 100%;
  height: 2px;
  bottom: 0px;

  background-color: #101010;
}

#deco_contents_right_bottom .one {
  position: absolute;
  width: 8px;
  height: 8px;
  right: 4px;
  bottom: 4px;

  background-color: #101010;
}
</style>
