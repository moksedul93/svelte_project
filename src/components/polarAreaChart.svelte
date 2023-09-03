<script>
  import { onMount } from 'svelte';
  import { countryDataStore } from '../store';
  import { Chart } from 'chart.js/auto';


  let chart;

  let chartData = {
    labels: [],
    datasets: [
      {
        data: [],
        backgroundColor: [], 
        label: 'Population',
      },
    ],
  };

  function updateChartData(data) {
    const sortedData = data
      .sort((a, b) => b.population - a.population)
      .slice(0, 10);

    chartData.labels = sortedData.map((country) => country.name.common);
    chartData.datasets[0].data = sortedData.map((country) => country.population);
  }

  // Use onMount to ensure the fetch and chart creation happen after component is mounted
  onMount(async () => {
    const canvas = document.getElementById('polarAreaChart');
    const ctx = canvas.getContext('2d');

    try {
      const response = await fetch('https://restcountries.com/v3.1/all');
      const data = await response.json();

      updateChartData(data);

      chart = new Chart(ctx, {
        type: 'polarArea',
        data: chartData,
        options: {
          responsive: true,
          maintainAspectRatio: false,
          title: {
            display: true,
            text: 'Top 10 Most Populated Countries',
          },
        },
      });
    } catch (error) {
      console.error('Error fetching data:', error);
    }
  });

  // Observe changes in countryDataStore and update the chart accordingly
  $: {
    if (chart) {
      updateChartData($countryDataStore);
      chart.update();
    }
  }
</script>

<canvas id="polarAreaChart"></canvas>
