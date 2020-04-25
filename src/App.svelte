<script>
  import Header from "./components/Header.svelte";
  import Footer from "./components/Footer.svelte";
  import HowToConnect from "./components/HowToConnect.svelte";
  import Home from "./components/Home.svelte";
  import ServerInfo from "./components/ServerInfo.svelte";
  import Tabs from "./shared/Tabs.svelte";

  // server info
  let version = "1.15.2";
  let url = "build.minsacraft.kro.kr";
  let port = 8633;

  // tabs
  let items = ["Home", "Server Status", "How to connect"];
  let activeItem = "Home";
  const tabChangeHandler = event => (activeItem = event.detail);
</script>

<style>
  main {
    max-width: 960px;
    margin: 40px auto;
  }
</style>

<Header />
<main>
  <Tabs {items} {activeItem} on:tabChange={tabChangeHandler} />
  {#if activeItem === 'Home'}
    <Home />
  {:else if activeItem === 'How to connect'}
    <HowToConnect {version} {url} {port} />
  {:else if activeItem === 'Server Status'}
    <ServerInfo />
  {/if}
</main>
<Footer />
