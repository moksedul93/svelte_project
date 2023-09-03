<!-- src/App.svelte -->
<!-- <script>
  import { onMount } from "svelte";
  import { countryDataStore } from "./store";
  import Table from "./components/Table.svelte";
  import PolarAreaChart from "./components/PolarAreaChart.svelte";

  let countries = [];

  onMount(async () => {
    const response = await fetch("https://restcountries.com/v3.1/all");
    const data = await response.json();
    countryDataStore.set(data);
  });

  $: {
    countries = $countryDataStore;
  }
</script>

<main>
  <h1>Country Data</h1>
  <Table {countries} />
  <PolarAreaChart {countries} />
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
  }

  table {
    width: 100%;
    border-collapse: collapse;
    margin-bottom: 20px;
  }

  th,
  td {
    padding: 10px;
    text-align: left;
    border-bottom: 1px solid #ccc;
  }

  th {
    background-color: #f2f2f2;
  }

  canvas {
    max-width: 400px;
  }
</style> -->
