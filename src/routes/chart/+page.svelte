<script>
	import ChartDev from "../../components/chart.svelte";
	import PolarAreaChart from '../../components/polarAreaChart.svelte';
  </script>
<svelte:head>
	<title>Chat</title>
	<meta name="description" content="chart this app" />
</svelte:head>
<div>
	<h1 class="mb-4 text-3xl text-[#980000]">Chart Page:</h1>
	<div class="flex flex-col md:flex-row md:h-[500px]">
		<div class="w-full md:w-9/12">
			<ChartDev/>
		</div>
		<div class="w-full md:w-3/12">
			<PolarAreaChart />
		</div>
	</div>
</div>