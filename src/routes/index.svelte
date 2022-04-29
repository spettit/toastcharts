<script>
	import ToastBarChart from '$lib/ToastBarChart.svelte';
	import ToastAreaChart from '../lib/ToastAreaChart.svelte';

	import areaChartData from '../data/areaChartData';
	import barChartData from '../data/barChartData';
</script>

<h1>Toast Chart</h1>

<ToastBarChart data={barChartData} />
<ToastAreaChart data={areaChartData} />
