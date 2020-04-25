<script>
  import ServerStatus from "./ServerStatus.svelte";
</script>

<style>
  h1 {
    color: lightskyblue;
  }
  .server-info {
    text-align: center;
  }
</style>

<div class="server-info">
  <h1>서버 관련 정보</h1>
  <ServerStatus />
</div>
