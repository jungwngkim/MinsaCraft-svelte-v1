<script>
  // 마인크래프트 서버 상태를 가져온다.
  let getStatus = fetch(
    "https://api.mcsrvstat.us/2/build.minsacraft.kro.kr:8633"
  )
    .then(res => {
      if (!res.ok) {
        throw new Error("오류 발생");
      }
      return res.json();
    })
    .then(data => {
      console.log(data);

      return data;
    })
    .catch(err => {
      console.log(err);
    });
</script>

<style>

</style>

<h2>서버 현황</h2>
<div class="status">
  {#await getStatus}
    <p>Loading...</p>
  {:then statusData}
    {#if statusData.online}
      <p>민사크래프트는 현재 온라인입니다!</p>
      {#if statusData.players.online > 0}
        <p>현재 접속자 수: {statusData.players.online}</p>
        {#each statusData.players.list as player}
          <p class="player">{player}</p>
        {/each}
      {:else}
        <p>아무도 서버에 접속하지 않았습니다</p>
      {/if}
    {:else}
      <p>민사크래프트는 현재 오프라인입니다!</p>
    {/if}
  {:catch error}
    {error.message}
  {/await}
</div>
