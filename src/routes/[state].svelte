<script context="module">
  // Run on the server and on the client as well
  // preload function takes two params (page, session)
  export async function preload(page, session) {
    // We get the param "state" because of the filename [state].svelte
    return {
      state: page.params["state"]
    };
  }
</script>

<script>
  import CovidStat from "../components/CovidStat.svelte";
  import CovidChart from "../components/CovidChart.svelte";
  import TableContainer from "../components/TableContainer.svelte";

  export let state;
</script>

<svelte:head>
  <title>Covid 19 Tracker - {state}</title>
</svelte:head>

<div class="section header">
  <div class="container">
    <h1 class="title">Covid 19 - {state}</h1>
  </div>
</div>

<CovidStat />
<CovidChart />
