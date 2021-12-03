<div id="container">
  <div id="grid">
    <div id="contents_left">
      <span class="intro">
        Hi! I'm takuma-ru
      </span>
    </div>
    <div id="contents_right">
      right
    </div>
  </div>
</div>

<style>
#container {
	padding: 16px;
}

#grid {
  display: grid;
  grid-template-rows: calc(100vh - 96px - 32px);
  grid-template-columns: 1fr 1fr;
  align-items: center;
}

#contents_left {
  grid-row: 1;
  grid-column: 1;
}

.intro {
  position: relative;
  font-size: 3.9vw;
  vertical-align: text-bottom;
}

.intro::before {
  position: absolute;
  content: '';
  width: 100%;
  height: 4px;

  bottom: 0px;

  background-color: #101010;
}

.intro::after {
  position: absolute;
  content: '';
  width: 16px;
  height: 8px;
  bottom: 0vw;

  background-color: #101010;
}

#contents_right {
  grid-row: 1;
  grid-column: 2;
}
</style>