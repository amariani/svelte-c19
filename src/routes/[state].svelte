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

<h1>{state}</h1>
<CovidStat />
<CovidChart />
