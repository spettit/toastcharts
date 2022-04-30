<script>
	import BarChart from '$lib/BarChart.svelte';
	import AreaChart from '../lib/AreaChart.svelte';

	import areaChartData from '../data/areaChartData';
	import barChartData from '../data/barChartData';
</script>

<h1>Toast Chart</h1>

<BarChart data={barChartData} />
<AreaChart data={areaChartData} />
