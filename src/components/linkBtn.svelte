<script lang="ts">
	import { link, push } from 'svelte-spa-router';

  export let linkPath = $$props['link-path']
</script>

<div
  class='linkHeaderBtn'
  on:click={() => push(linkPath)}
>
  <span class="text">
    <slot />
  </span>
</div>

<style>
.linkHeaderBtn {
  float: left;
  min-width: 24px;
  min-height: 24px;
  margin-right: 16px;
  text-decoration: none;
  background-color: #101010;
  cursor: pointer;
}

/*.linkHeaderBtn_select {
  width: 24px;
  height: 24px;
  margin-right: 16px;
  text-decoration: none;
  background-color: #FEFEFE;
}*/

.text {
  font-size: 16px;
  line-height: 16px;
  padding: 4px;

  font-weight: bold;
  color: #0084AD;
}
</style>