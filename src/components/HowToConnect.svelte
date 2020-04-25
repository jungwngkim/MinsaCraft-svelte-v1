<script>
  export let version;
  export let url;
  export let port;
</script>

<style>
  h1 {
    color: #ff9900;
  }
  img {
    width: 100%;
    margin-bottom: 18px;
  }
  .how-to-connect {
    text-align: center;
  }
</style>

<div class="how-to-connect">
  <h1>민사크래프트에 접속하는 법</h1>

  <p>1. 마인크래프트 런처를 실행한다.</p>
  <p>2. 버전을 {version}로 세팅 후 게임에 접속한다.</p>
  <img
    src="img/how-to-connect/1.png"
    alt="Open Minecraft Launcher and set version" />
  <p>
    3. 멀티 플레이 (Multiplayer)를 클릭한후, 서버추가(Add Server)를 클릭한다.
  </p>
  <img src="img/how-to-connect/2.png" alt="Start Game" />
  <p>4. 서버 주소(Server Address)에 {url}:{port} 를 입력한다</p>
  <img src="img/how-to-connect/3.png" alt="Select Multiplayer" />
  <img src="img/how-to-connect/4.png" alt="Add server" />
  <p>5. 서버에 접속한다.</p>
  <img src="img/how-to-connect/5.png" alt="Connect to server" />
</div>
