<script lang="ts">
	import { link, push } from 'svelte-spa-router';
</script>

<div class='linkHeaderBtn' on:click={() => push('/')}>
  <span class="text">
    <slot />
  </span>
</div>

<style>
.linkHeaderBtn {
  width: 24px;
  min-height: 24px;
  margin-right: 16px;
  text-decoration: none;
  background-color: #FEFEFE;
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
}
</style>