<script>
	import '@toast-ui/chart/dist/toastui-chart.css';
	import { onMount } from 'svelte';

	let chart;
	let container;

	export let data;

	const options = {
		chart: { width: 700, height: 400 }
	};

	onMount(async () => {
		const el = document.getElementById('chart-area');
		const ChartImport = await import('@toast-ui/chart');
		console.log(ChartImport);
		const Chart = ChartImport.default;
		console.log(Chart.barChart);
		chart = Chart.barChart({
			el,
			data,
			options
		});
	});
</script>

<div id="chart-area" />
