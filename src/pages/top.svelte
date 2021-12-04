<script lang="ts">
	import { push } from 'svelte-spa-router';

  let contents_right_items = [
    { name: 'ABOUT', link: '/about' },
    { name: 'APP', link: '/app' },
    { name: 'CONTACT', link: '/contact' },
  ]
</script>

<div id="container">
  <div id="grid">
    <div id="contents_left">
      <span class="intro">
        Hi! I'm takuma-ru
      </span>
    </div>
    <div id="contents_right">
      {#each contents_right_items as item, index}
        <button
          on:click={() => push(item.link)}
          style="grid-row: {index + 2};"
        >
          {item.name}
        </button>
      {/each}
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
  display: grid;
  grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
  align-items: center;
  justify-items: center;
}

#contents_right button {
  position: relative;
  width: 50%;
  font-size: 3vw;
  border: none;
  background-color: transparent;
  cursor: pointer;
}

#contents_right button::before {
  position: absolute;
  content: '';
  width: 100%;
  height: 4px;
  top: 0%;
  left: 0%;
  background-color: #101010;
  transform: scale(0, 1);
  transition: transform .4s;
  transform-origin: left;
}

#contents_right button:hover::before {
  transform: scale(1);
}

#contents_right button::after {
  position: absolute;
  content: '';
  width: 100%;
  height: 4px;
  bottom: 0%;
  right: 0%;
  background-color: #101010;
  transform: scale(0, 1);
  transition: transform .5s;
  transform-origin: right;
}

#contents_right button:hover::after {
  transform: scale(1);
}
</style>