<script>
  import Header from "../components/Header.svelte";
  export let location;
</script>

<Header navLoc="search"/>
<div class="search">
  <h1>내 문서 {location.href}</h1>
</div>

<style>
  .search {
  position: absolute;
  width: 100%;
  height: 900px;
  top: 120px;
  /* test border */
  border: 1px solid;
}
</style>
